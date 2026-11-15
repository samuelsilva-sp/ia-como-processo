---
name: implement
description: Etapa 4 do método (Implement). Implementa UMA tarefa do TAREFAS.md aprovado, só nos arquivos permitidos, e entrega para o Review. Use depois do Break aprovado ou quando o usuário digitar /implement.
argument-hint: "[ID da tarefa, ex.: T03 — vazio = próxima não concluída]"
disable-model-invocation: true
---

# ⚙️ Etapa 4 — Implement (uma tarefa por vez)

## Pré-requisito
`TAREFAS.md` existe e foi aprovado. Se não, pare e sugira o `/break`.

## Regras de ouro
1. **Uma tarefa por vez.** A tarefa pedida, ou a primeira não concluída cujas dependências estão marcadas `[x]` (revisadas) **e validadas pelo humano**.
2. **Só nos arquivos permitidos** ("Pode alterar"). Precisa mexer em outro? **Pare e pergunte.**
3. **Reaproveite antes de criar.** Confira o que a tarefa manda reaproveitar e procure algo parecido no projeto.
4. **Siga o plano.** Ideia nova ou melhoria não prevista vai para o `BACKLOG.md` (crie o arquivo se não existir), não para o código.
5. **Explique o não óbvio** em comentários curtos, principalmente integrações com sistemas externos.
6. **Erros visíveis:** nada falha em silêncio; mensagens ao usuário em português.
7. **Sem dados sensíveis em logs** (CPF, CNPJ, dados bancários) e **sem segredos no código**.
8. **Sem surpresas:** se algo muda o escopo ou bloqueia, pare e use o formato de bloqueio.

## Passo a passo
1. Leia a tarefa inteira no `TAREFAS.md` (objetivo, arquivos, cenários, aceite, como testar).
2. Faça a implementação cobrindo os cenários (feliz, exceção, erro). Em código, escreva **testes automatizados** para o critério de aceite e os cenários, nos arquivos de teste previstos na tarefa.
3. Rode o que der para rodar (testes, lint, build, execução de teste da automação).
4. **Não marque a tarefa como concluída.** Entregue para revisão:

```
🔧 Tarefa T__ implementada — pronta para o /review
Arquivos alterados: ...
O que foi feito: ...
Como testar: 1. ... 2. ...
Fora do escopo (foi para o BACKLOG): ...
```

## Em caso de bloqueio
```
🚨 BLOQUEIO
Tarefa: T__
Problema: ...
Opções: A) ... (prós/contras) · B) ... (prós/contras)
Recomendação: ...
Decisão necessária: ...
```

## Tarefa pedida
$ARGUMENTS
