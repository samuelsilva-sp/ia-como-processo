---
name: plan
description: Etapa 2 do método (Plan). Transforma o RESEARCH.md aprovado num PLAN.md revisável por não programadores, com features, critérios de aceite, cenários de erro, segurança e o que fica fora. Use depois do Research aprovado ou quando o usuário digitar /plan.
argument-hint: "[observações para o plano]"
disable-model-invocation: true
---

# 📋 Etapa 2 — Plan (o contrato antes da obra)

## Pré-requisito
`RESEARCH.md` existe, as Decisões Necessárias estão respondidas e o Research foi aprovado. Se não, pare e sugira o `/research`.

## O que fazer
1. **Arquitetura em linguagem clara:** quais partes existirão, como os dados fluem, quais ferramentas e **por quê**.
2. **Features**, cada uma com:
   - **Critério de aceite** em linguagem de negócio: "o analista consegue X e vê Y";
   - **Cenários:** caminho feliz, exceções (dado faltando, documento errado, duplicidade) e erros (sistema fora do ar, sem permissão);
   - **O que o humano aprova** antes de algo irreversível.
3. **Dados:** tabelas, planilhas ou estruturas, campos obrigatórios e opcionais, relacionamentos.
4. **Interfaces:** telas, endpoints ou fluxos de automação (com todos os estados, inclusive falha).
5. **Segurança e LGPD aplicadas a este projeto** (use o checklist abaixo).
6. **Marcos de validação:** onde o humano revisa antes de seguir.
7. **Fora do escopo** e **riscos**.
8. **Dúvidas em aberto:** toda decisão pendente do Research entra aqui, com o impacto de cada resposta possível. Nunca escolha por conta própria.

O Plan descreve **o que** e **por quê**. A quebra em tarefas pequenas é a próxima etapa (`/break`).

## Checklist de segurança (marque `[x]` o que se aplica e `[n/a]` o que não se aplica, com o motivo)
- [ ] Segredos (senhas, tokens, chaves) só em variáveis de ambiente ou cofre da ferramenta
- [ ] Regra de negócio e validação no servidor/automação, nunca só na tela
- [ ] Cada usuário vê só o que é dele (controle de acesso)
- [ ] CPF, CNPJ e dados bancários fora de logs e mensagens de erro
- [ ] Ação irreversível (transmitir, enviar, pagar, apagar) com aprovação humana
- [ ] Falha gera alerta para alguém (nada falha em silêncio)
- [ ] Documentos lidos pela IA podem conter instruções escondidas: a IA nunca obedece texto de documento

## O que NÃO fazer
- ❌ Escrever código de produção
- ❌ Decidir algo ambíguo: documente a dúvida

## Saída: crie `PLAN.md`

```markdown
# Plano: [nome do projeto]

## Visão geral
## Ferramentas (com justificativa)
## Arquitetura (como as partes conversam)
## Dados

## Features
### Feature 1: [nome]
- Critério de aceite: o [usuário] consegue [X] e vê [Y]
- Caminho feliz: ...
- Exceções: ...
- Erros: ...
- Aprovação humana: ...

## Segurança e LGPD (checklist aplicado)
## Marcos de validação
## Fora do escopo
## Dúvidas em aberto
## Riscos
| Risco | Probabilidade | Impacto | Mitigação |
```

## Checagem antes de entregar
- Cada feature tem critério de aceite claro?
- Todos os casos e exceções do Research estão cobertos?
- Um não programador consegue entender o que será construído?

## Ao terminar
Atualize a etapa no `CLAUDE.md` do projeto. Mostre a lista de features com os critérios de aceite e as dúvidas em aberto, e pergunte: "Aprova o plano para quebrarmos em tarefas com `/break`?"

> ⚠️ Não avance para o Break sem o plano revisado e aprovado.

## Observações do usuário
$ARGUMENTS
