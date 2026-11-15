# CLAUDE.md — Instruções de trabalho

> **Como usar este modelo:** copie este arquivo para `~/.claude/CLAUDE.md` (vale para todos os seus projetos) ou para a raiz de um projeto com o nome `CLAUDE.md` (vale só para ele). Troque tudo que está entre `[colchetes]`. Apague o que não se aplica.
> O Claude Code lê este arquivo no começo de **toda** sessão. Pense nele como o onboarding que você daria a um funcionário novo.

---

## 👤 Quem sou eu
- **Nome:** [seu nome]
- **Papel:** [ex.: sócio-diretor, gestor de processos, analista de automação]
- **Empresa:** [nome do escritório] — [cidade/UF]
- **Área:** [ex.: contabilidade, fiscal, DP, societário]
- **Idioma:** português do Brasil, sempre
- **Como prefiro receber respostas:** diretas e objetivas; em dúvida técnica, opções com prós e contras e uma recomendação

## 🏢 Contexto do negócio
- **Sistemas que usamos:** [ex.: Domínio, Questor, eSocial, portal do Simples, Gestta, WhatsApp]
- **O que é sensível aqui:** CPF, CNPJ, dados bancários, folha de pagamento, dados de clientes em geral (LGPD)
- **Quem decide o quê:** [ex.: o analista aprova toda transmissão; o gestor aprova mudança de processo]

---

## 📋 Workflow obrigatório: Research → Plan → Break → Implement → Review

Todo projeto (tela, aplicativo, automação, agente, integração) segue estas etapas, nesta ordem. **A IA nunca avança de etapa sozinha: eu aprovo entre elas.**

| Etapa | Comando | O que sai | Para avançar |
|---|---|---|---|
| 1. Research | `/research` | `RESEARCH.md` | Respondi as "Decisões Necessárias" e aprovei |
| 2. Plan | `/plan` | `PLAN.md` | Revisei e aprovei o plano |
| 3. Break | `/break` | `TAREFAS.md` | Aprovei a lista de tarefas |
| 4. Implement | `/implement` | Uma tarefa feita | A tarefa passou no Review |
| 5. Review | `/review` | Parecer da tarefa | Validei o resultado; só então a próxima tarefa |

### Regras do workflow
- **Nunca pule etapas.** Antes de escrever código ou montar automação, verifique na raiz do projeto:
  - não existe `RESEARCH.md` aprovado → comece pelo Research;
  - não existe `PLAN.md` aprovado → faça o Plan;
  - não existe `TAREFAS.md` aprovado → faça o Break;
  - existe → implemente a primeira tarefa não concluída.
- Se eu pedir para implementar direto, **pergunte se as etapas anteriores já foram feitas**.
- **Research:** só entender. Não propor solução, não escrever código.
- **Plan:** não escrever código. Dúvida vira pergunta documentada, nunca suposição.
- **Break:** tarefas pequenas, cada uma com os arquivos que pode alterar e o critério de aceite.
- **Implement:** uma tarefa por vez, só nos arquivos permitidos.
- **Review:** nenhuma tarefa é dada como concluída sem revisão.
- **Fora do escopo:** o que não está no plano não é implementado. Vai para `BACKLOG.md`.
- **Ambiguidade:** pergunte antes de assumir. Uma pergunta agora vale horas de retrabalho.
- **Ao retomar uma sessão:** leia este arquivo, `PLAN.md`, `TAREFAS.md` e `BACKLOG.md`, e continue da primeira tarefa não concluída.

### Etapa crítica por tipo de projeto
- **Chatbots e agentes de IA** → Research: definir o que o agente pode e não pode fazer.
- **Automações (RPA, N8N, Make, Power Automate)** → Plan: mapear todos os estados do processo, inclusive falhas.
- **Aplicativos web** → todas pesam; atenção ao modelo de dados no Plan.
- **Integrações com sistemas e APIs** → Research: limites de uso, autenticação, o que acontece quando o sistema cai.

### Estrutura base de todo projeto
```
meu-projeto/
├── CLAUDE.md      ← contexto do projeto (estado atual, decisões)
├── RESEARCH.md    ← etapa 1
├── PLAN.md        ← etapa 2
├── TAREFAS.md     ← etapa 3 (com o parecer do Review de cada tarefa)
├── BACKLOG.md     ← o que ficou para depois
└── ...            ← código, automações, documentos
```

---

## 🧱 Padrões técnicos
> Preencha com a sua realidade. Exemplos:
- **Stack preferida:** [ex.: React + TypeScript + Supabase | N8N | Python | Power Automate]
- **Nomes:** [ex.: componentes em PascalCase, funções em camelCase, tabelas em snake_case]
- **Sempre:** tratamento de erro visível (nunca silencioso), mensagens ao usuário em português, variáveis de ambiente no `.env` (nunca no código) e documentadas
- **Automações:** sempre um caminho de erro com alerta; credenciais no cofre da ferramenta

## ⚠️ Restrições que nunca mudam
- **LGPD:** coletar e mostrar só o necessário; CPF, CNPJ e dados bancários **nunca** em logs, prints ou mensagens de erro.
- **Ação irreversível** (transmitir obrigação, enviar e-mail a cliente, pagar guia, apagar dado) **sempre** passa por aprovação humana.
- **Confirme antes de qualquer operação destrutiva** (apagar, sobrescrever, truncar).
- **Segredos** (senhas, tokens, chaves) nunca no código, nunca no chat.

---

## 💬 Formatos de comunicação

**Ao concluir uma tarefa:**
```
✅ Tarefa T__ concluída (Review: aprovado)
O que foi feito: ...
Como testar: 1. ... 2. ...
Resultado esperado: ...
Próxima tarefa: T__ — aguardando aprovação
```

**Em caso de bloqueio:**
```
🚨 BLOQUEIO
Tarefa: ...
Problema: ...
Opções: A) ... (prós/contras) · B) ... (prós/contras)
Recomendação: ...
Decisão necessária: ...
```

## ✅ Checklist de entrega
- [ ] Todas as tarefas do `TAREFAS.md` concluídas e revisadas
- [ ] Documentação de uso atualizada
- [ ] Variáveis de ambiente documentadas
- [ ] `BACKLOG.md` com o que ficou fora
- [ ] Indicador do Research medido pela primeira vez e um dono definido para a solução
