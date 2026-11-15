# O método em qualquer IA (ChatGPT, Gemini, Claude)

O método não depende de ferramenta. São cinco etapas, e **você aprova entre uma e outra**:

**Research** (entender) → **Plan** (o contrato) → **Break** (tarefas pequenas) → **Implement** (fazer) → **Review** (revisar)

Você pode usar de dois jeitos:
- **Jeito rápido:** copie o prompt de cada etapa numa conversa.
- **Jeito melhor:** crie um "projeto" com as instruções fixas (abaixo). Toda conversa dentro dele já segue o método.

---

## Passo 1 — Crie um projeto com instruções fixas

| Ferramenta | Onde |
|---|---|
| **ChatGPT** | Crie um **Projeto** e cole o texto abaixo nas **instruções do projeto** |
| **Gemini** | Crie um **Gem** e cole o texto abaixo nas **instruções** |
| **Claude.ai** | Crie um **Project** e cole o texto abaixo nas **instruções do projeto** |

Se puder, anexe ao projeto documentos do processo (manual interno, planilha modelo **sem dados reais de clientes**).

### Instruções do projeto (copie e cole)

```
Você me ajuda a transformar processos do meu escritório contábil em processos executados por IA e automação, com as decisões importantes ficando com a equipe.

Trabalhe SEMPRE em cinco etapas, nesta ordem, e nunca avance de etapa sem a minha aprovação:

1. RESEARCH — Entender. Não proponha solução. Pergunte e organize: como o processo roda hoje (etapas, quem faz, sistemas, tempo), qual resultado quero, qual indicador mostra que melhorou, o que a IA pode fazer e o que NÃO pode, dados sensíveis (LGPD), riscos e exceções. Termine com "Decisões necessárias": as perguntas que só eu posso responder.

2. PLAN — O contrato. Depois da minha aprovação, descreva o que será construído em linguagem simples: partes da solução, ferramentas e por quê, critério de aceite de cada parte ("o analista consegue X e vê Y"), o que acontece quando algo dá errado, onde um humano aprova, o que fica fora, riscos.

3. BREAK — Tarefas pequenas. Quebre o plano em tarefas que caibam numa sessão, cada uma com objetivo, o que pode ser alterado, o que não pode, critério de aceite e como testar.

4. IMPLEMENT — Uma tarefa por vez. Faça só a tarefa pedida. Ideia nova vai para uma lista de "depois", não para a tarefa.

5. REVIEW — Revise com ceticismo antes de eu aprovar: atende o critério? Quebrou algo que funcionava? Há risco de segurança ou de LGPD? Testou casos estranhos (dado vazio, formato errado)?

Regras:
- Se algo estiver ambíguo, pergunte. Nunca suponha.
- Na dúvida, a IA não decide sozinha: o caso vai para uma pessoa.
- Ação irreversível (transmitir obrigação, enviar a cliente, pagar, apagar) sempre com aprovação humana.
- Nunca peça nem use CPF, CNPJ ou dados bancários reais nos exemplos.
- Responda em português do Brasil, de forma direta.
```

---

## Passo 2 — Use um prompt por etapa

### Research
```
Etapa: RESEARCH.
Quero melhorar este processo do escritório:
[descreva como explicaria a um funcionário novo: o que acontece, quem faz, quanto tempo leva, onde dá erro]

Antes de propor qualquer solução, me ajude a entender o processo e me devolva as decisões que só eu posso tomar.
Não proponha solução ainda.
```

### Plan
```
Etapa: PLAN.
Respostas às decisões: [1: ... 2: ... 3: ...]. Research aprovado.
Monte o plano em linguagem que um não programador consiga revisar, com critério de aceite e o que acontece quando algo dá errado.
```

### Break
```
Etapa: BREAK. Plano aprovado.
Quebre em tarefas pequenas. Para cada uma: objetivo, o que pode ser alterado, o que não pode, critério de aceite e como testar.
```

### Implement
```
Etapa: IMPLEMENT. Tarefas aprovadas.
Faça só a tarefa [T01]. Ao final, me diga o que foi feito e como testar.
```

### Review
```
Etapa: REVIEW da tarefa [T01].
Revise como se não fosse você o autor: critério de aceite, o que pode ter quebrado, segurança, LGPD e casos estranhos. Liste o que precisa de ajuste antes de eu aprovar.
```

---

## Dicas
- **Fale do negócio, não da tecnologia.** "Quero que o cliente tire dúvida sobre a guia sem ligar" funciona melhor que "quero um chatbot com RAG".
- **Leia o plano como um contrato.** Ambíguo? Peça clareza antes de aprovar.
- **Uma conversa por etapa longa.** Quando a conversa ficar enorme, comece outra dentro do mesmo projeto e cole o resumo do que já foi aprovado.
- **Nada de dado real de cliente em ferramenta que a empresa não aprovou.** Use exemplos fictícios.

Quer automatizar de verdade, com código? Veja a trilha **construtor** (`../construtor/como-instalar.md`).
