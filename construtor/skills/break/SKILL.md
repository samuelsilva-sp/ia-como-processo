---
name: break
description: Etapa 3 do método (Break). Quebra o PLAN.md aprovado em tarefas pequenas e verificáveis no TAREFAS.md, cada uma com arquivos permitidos, cenários, critério de aceite e como testar. Use depois do Plan aprovado ou quando o usuário digitar /break.
argument-hint: "[feature específica, se quiser quebrar só uma]"
disable-model-invocation: true
---

# 🧩 Etapa 3 — Break (tarefas pequenas)

## Pré-requisito
`PLAN.md` existe e foi aprovado. Se não, pare e sugira o `/plan`.

## Por que esta etapa existe
Tarefa grande demais faz a IA perder o fio, misturar responsabilidades e mexer no que já funcionava. Tarefa pequena é mais fácil de conferir, de testar e de desfazer.

## O que fazer
1. **Pesquise antes de quebrar:** procure no projeto o que já existe e pode ser reaproveitado (componentes, funções, fluxos, tabelas). Anote em cada tarefa.
2. **Quebre cada feature em tarefas pequenas:** como referência, até ~3 arquivos alterados e **um** critério de aceite por tarefa.
3. **Ordene por dependência.** Para telas, comece pelo protótipo visual (sem lógica) e depois ligue aos dados.
4. **Para cada tarefa, escreva:**
   - **Objetivo** em uma frase;
   - **Pode alterar:** a lista exata de arquivos ou nós a criar ou modificar, **incluindo os arquivos de teste**;
   - **Não pode tocar:** o que deve continuar igual;
   - **Reaproveitar:** o que já existe e deve ser usado;
   - **Cenários:** caminho feliz, exceção, erro;
   - **Critério de aceite** (vindo do Plan);
   - **Como testar** em passos que o humano consegue seguir. O teste **nunca** pode exigir alterar algo de "Não pode tocar": use cópias ou arquivos temporários;
   - **Depende de:** tarefas anteriores.

## O que NÃO fazer
- ❌ Implementar
- ❌ Criar tarefa que não esteja ligada a uma feature do Plan (isso vai para o `BACKLOG.md`)

## Saída: crie `TAREFAS.md`

```markdown
# Tarefas: [nome do projeto]

## Feature 1: [nome]

### [ ] T01 — [objetivo em uma frase]
- Pode alterar: `...`, `...`
- Não pode tocar: `...`
- Reaproveitar: `...`
- Cenários: feliz: ... · exceção: ... · erro: ...
- Critério de aceite: ...
- Como testar: 1. ... 2. ...
- Depende de: —
- Review: (preenchido pelo /review)
```

## Ao terminar
Mostre a lista resumida (ID + objetivo) e pergunte: "Aprova as tarefas para começarmos pela T01 com `/implement`?"

> ⚠️ Não implemente sem a lista aprovada.

## Escopo pedido pelo usuário
$ARGUMENTS
