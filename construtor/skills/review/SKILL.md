---
name: review
description: Etapa 5 do método (Review). Revisa a tarefa implementada contra o critério de aceite, o escopo de arquivos, regressão, segurança e LGPD, registra o parecer no TAREFAS.md e só então libera a tarefa para validação humana. Use depois de cada /implement ou quando o usuário digitar /review.
argument-hint: "[ID da tarefa, ex.: T03 — vazio = última implementada]"
disable-model-invocation: true
---

# 🔍 Etapa 5 — Review (nada é concluído sem revisão)

Você agora é o **revisor**, não o autor. Seja cético: procure o que pode estar errado, não o que confirma que está certo. Teste casos de borda (dado vazio, formato errado, coluna trocada, valor estranho).

> Dica: o review fica mais independente quando roda numa **conversa nova** (ou num subagente), que só lê a tarefa e o código, sem o histórico de quem implementou.

## O que conferir

1. **Escopo:** os arquivos alterados estão todos em "Pode alterar"? Algo em "Não pode tocar" mudou? Entrou algo que não estava na tarefa?
2. **Critério de aceite:** execute o "Como testar". O resultado bate com o critério? Teste também a exceção e o erro descritos nos cenários.
3. **Regressão:** o que já funcionava continua funcionando? Rode testes, lint e build (ou uma execução de teste da automação).
4. **Segurança:**
   - nenhum segredo no código ou no histórico;
   - regra de negócio validada no servidor/automação;
   - controle de acesso respeitado;
   - falha gera erro visível ou alerta.
5. **LGPD:** CPF, CNPJ e dados bancários fora de logs, prints e mensagens; só os dados necessários são coletados e mostrados.
6. **Ação irreversível** (transmitir, enviar, pagar, apagar) passa por aprovação humana?
7. **Documentação:** o que mudou para quem usa está explicado?

## Saída
Registre o parecer na tarefa, no `TAREFAS.md`:

```markdown
- Review rodada N (data): ✅ Aprovado | ⚠️ Ajustes necessários
  - Escopo: ok | ...
  - Aceite: ok | ...
  - Regressão: ok | ...
  - Segurança/LGPD: ok | ...
  - Documentação: ok | ...
  - Ajustes: ...
```

- **Ajustes necessários:** liste o que corrigir e devolva para o `/implement` da mesma tarefa. Depois da correção, faça uma nova rodada de review. **Mantenha o histórico:** cada rodada é uma linha nova ("Review rodada 1", "rodada 2"…).
- **Defeito na própria tarefa** (ex.: o "Como testar" contradiz "Não pode tocar", ou o critério é impossível de verificar): não corrija o `TAREFAS.md` por conta própria. Aponte o defeito e peça a decisão do humano.
- **Aprovado:** marque a tarefa com `[x]` e use o formato:

```
✅ Tarefa T__ concluída (Review: aprovado)
O que foi feito: ...
Como testar: 1. ... 2. ...
Resultado esperado: ...
Próxima tarefa: T__ — aguardando aprovação
```

> ⚠️ Não comece a próxima tarefa sem o humano validar esta.

## Tarefa a revisar
$ARGUMENTS
