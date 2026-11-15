# Como instalar o método no Claude Code

Cinco comandos, uma etapa cada: **`/research` → `/plan` → `/break` → `/implement` → `/review`**. Você aprova entre uma etapa e outra.

## O que você precisa
- **Claude Code** instalado (aplicativo de desktop, extensão do VS Code ou terminal) e uma conta Claude com acesso a ele.
- Esta pasta `construtor/` baixada. No GitHub: botão verde **Code › Download ZIP**, depois extraia.

## Passo 1 — As skills (os 5 comandos)

Escolha **uma** das opções:

**Para todos os seus projetos** (recomendado): copie as 5 pastas de `skills/` para a pasta de skills do seu usuário.

| Sistema | Pasta de destino |
|---|---|
| Windows | `C:\Users\SEU_USUARIO\.claude\skills\` |
| Mac / Linux | `~/.claude/skills/` |

Depois de copiar, deve existir, por exemplo, `...\.claude\skills\research\SKILL.md`.

**Só para um projeto:** copie as 5 pastas para `.claude/skills/` dentro da pasta do projeto.

> A pasta `.claude` fica oculta. No Windows: Explorador de Arquivos › Exibir › Mostrar › Itens ocultos. No Mac: `Cmd + Shift + .` no Finder.

## Passo 2 — O CLAUDE.md (as regras de trabalho)

1. Abra `CLAUDE.md-modelo.md` e preencha o que está entre `[colchetes]`: seu nome, empresa, sistemas, stack.
2. Salve como:
   - `C:\Users\SEU_USUARIO\.claude\CLAUDE.md` (Windows) ou `~/.claude/CLAUDE.md` (Mac/Linux) para valer em todos os projetos; **ou**
   - `CLAUDE.md` na raiz de um projeto para valer só nele.

## Passo 3 — Primeiro uso

1. Crie uma pasta para o projeto e abra o Claude Code nela.
2. Reinicie o Claude Code se ele já estava aberto (ele carrega as skills ao iniciar).
3. Digite `/` e confira se aparecem `research`, `plan`, `break`, `implement` e `review`.
4. Comece descrevendo o processo **em linguagem de negócio**, como explicaria para um funcionário novo:

```
/research Todo mês recebemos comprovantes de distribuição de lucros dos clientes por e-mail.
Alguém baixa um por um, identifica o sócio, calcula o IRRF e monta a planilha para a Reinf.
Quero que isso rode sozinho e que a equipe só confira o que for duvidoso.
```

5. Responda as **Decisões Necessárias**, aprove, e siga: `/plan` → aprove → `/break` → aprove → `/implement` → `/review` → valide → próxima tarefa.

## Dicas
- **Linguagem de negócio, não técnica.** "Quero que o cliente tire dúvida sobre guia sem ligar" funciona melhor que "quero um chatbot com RAG".
- **Leia o plano como um contrato.** Se estiver ambíguo, peça clareza antes de aprovar.
- **Ideia nova no meio do caminho vai para o `BACKLOG.md`.** Termine o que foi planejado primeiro.
- **Ao voltar outro dia**, diga: "continue de onde paramos no TAREFAS.md".

## Não usa o Claude Code?
O método funciona em qualquer IA. Veja a trilha **gestor** (`../gestor/prompts-qualquer-ia.md`), com as versões para Projetos do ChatGPT, Gems do Gemini e Projects do Claude.ai.
