# Como instalar o método no Claude Code

Cinco comandos, uma etapa cada: **`/research` → `/plan` → `/break` → `/implement` → `/review`**. Você aprova entre uma etapa e outra.

Há dois jeitos de instalar:

- **Opção A — O Claude instala para você** (mais fácil): você cola um pedido no Claude Code, ele baixa o kit, instala as skills e monta o seu `CLAUDE.md` fazendo perguntas no chat.
- **Opção B — Manual:** você copia os arquivos para as pastas certas. Siga os passos 1 a 3 mais abaixo.

## O que você precisa
- **Claude Code** instalado (aplicativo de desktop, extensão do VS Code ou terminal) e uma conta Claude com acesso a ele.
- Para a opção B: esta pasta `construtor/` baixada. No GitHub: botão verde **Code › Download ZIP**, depois extraia.

---

## Opção A — Deixe o Claude instalar e configurar

1. Abra o Claude Code numa pasta qualquer (pode ser uma pasta vazia, por exemplo `Documentos\metodo-ia`).
2. Copie o pedido abaixo inteiro e cole no chat.
3. Responda as perguntas que ele fizer. Ele **mostra o que vai fazer e pede sua confirmação** antes de gravar qualquer arquivo.

```
Quero instalar no meu Claude Code o método "IA como processo" (versão 2.0), do kit público em
https://github.com/samuelsilva-sp/ia-como-processo

Faça assim, me mostrando cada passo:

1. Baixe o kit (git clone, ou o ZIP de https://github.com/samuelsilva-sp/ia-como-processo/archive/refs/heads/main.zip)
   para uma pasta temporária. Leia os arquivos antes de instalar e me diga, em poucas linhas, o que cada skill faz.
   Não execute nenhum script do kit: são só arquivos de texto para copiar.

2. Me pergunte, uma pergunta por vez (com opções quando fizer sentido):
   - se quero instalar para TODOS os meus projetos (pasta de usuário ~/.claude) ou só para ESTE projeto (.claude/ desta pasta);
   - meu nome, meu papel e o nome do escritório/empresa (cidade/UF);
   - a área (contábil, fiscal, DP, societário, outra) e os sistemas que usamos;
   - se programo ou não, e qual a stack preferida (ou "não sei", se for o caso);
   - quem aprova o quê no escritório (ex.: quem aprova transmissão de obrigação).

3. Instale as 5 skills (research, plan, break, implement, review) copiando as pastas de construtor/skills/
   para a pasta de skills escolhida. Se já existir uma skill com o mesmo nome, me avise e pergunte antes de substituir.

4. Monte o CLAUDE.md a partir de construtor/CLAUDE.md-modelo.md, preenchendo com as minhas respostas
   e apagando o que não se aplica. Mostre o texto final e peça minha aprovação antes de salvar.
   Se já existir um CLAUDE.md no destino, faça uma cópia de backup antes e me pergunte se quero juntar ou substituir.

5. Confira a instalação (os 5 arquivos SKILL.md e o CLAUDE.md no lugar certo) e me diga:
   - o que foi instalado e onde;
   - que preciso reiniciar o Claude Code para os comandos aparecerem;
   - um exemplo de primeiro /research para um processo do meu escritório.

Regras: não peça nem grave senhas, chaves ou dados de clientes; não mexa em nada fora das pastas de skills
e do CLAUDE.md; em caso de dúvida, pergunte.
```

> Depois de instalado, **reinicie o Claude Code** e digite `/` para ver os comandos.

---

## Opção B — Instalação manual

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
