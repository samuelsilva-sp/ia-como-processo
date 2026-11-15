---
name: research
description: Etapa 1 do método (Research). Entende o processo e o problema antes de qualquer solução e gera o RESEARCH.md com as Decisões Necessárias para o humano. Use no início de todo projeto novo (aplicativo, automação, agente, integração) ou quando o usuário digitar /research.
argument-hint: "[descreva o processo em linguagem de negócio]"
disable-model-invocation: true
---

# 🔎 Etapa 1 — Research (entender antes de resolver)

Você está na **Etapa 1**. Seu único objetivo é **entender**. Não planeje, não implemente, não escolha tecnologia.

## O que fazer

1. **Ler o que já existe** (se for continuação): pastas, arquivos, documentação, `CLAUDE.md`, sistemas e integrações em uso.
2. **Entender o processo como ele roda hoje**: etapas, quem faz cada uma, de onde vêm os dados, para onde vão, quanto tempo leva, onde dá erro.
3. **Definir o resultado e como medir** (obrigatório):
   - **Processo:** qual processo será apoiado ou transformado?
   - **Resultado:** o que muda para o negócio quando estiver pronto?
   - **Indicador:** qual número mostra que melhorou (ex.: horas por mês, % de documentos que vão para conferência, prazo cumprido)? Qual é o valor hoje, se souber?
4. **Separar o que é da IA e o que é do humano**:
   - o que a IA/automação pode executar sozinha;
   - o que ela **não pode** fazer (decidir em caso de dúvida, transmitir, pagar, apagar, falar com cliente…);
   - onde o humano decide.
5. **Mapear dados sensíveis e riscos**: CPF, CNPJ, dados bancários, LGPD, sistemas de terceiros, limites de API, o que acontece quando algo cai.
6. **Registrar restrições já impostas pelo usuário** (ex.: "tem que ser em Python", "roda no N8N") sem avaliá-las.
7. **Listar o que não está claro**: tudo o que você precisaria supor vira pergunta.
8. **Criar ou atualizar o `CLAUDE.md` do projeto** com nome, objetivo, etapa atual (Research) e próximo passo.

## O que NÃO fazer
- ❌ Propor solução ou arquitetura
- ❌ Escrever código ou montar automação
- ❌ Assumir qualquer coisa que não foi dita

## Saída: crie `RESEARCH.md` na raiz do projeto

```markdown
# Research: [nome do projeto]

## Resumo do problema
[O problema raiz, não o sintoma. 3 a 5 linhas.]

## Processo hoje
[Etapas em ordem, quem faz cada uma, de onde vêm e para onde vão os dados.]

## Resultado e indicador
- Processo: ...
- Resultado esperado: ...
- Indicador: ... (valor hoje: ... | meta: ...)
- Dono da solução depois de pronta: ...

## O que é da IA e o que é do humano
| Etapa | IA executa | Humano decide |
|---|---|---|

**A IA não pode:** ...

## Usuários e stakeholders
## Integrações e dependências
## Dados sensíveis e riscos (inclui LGPD)
## Casos principais e exceções

## Decisões Necessárias (perguntas para o humano)
1. ...
2. ...

## Fora do escopo

## Decisões respondidas (preenchido depois da resposta do humano)
- Data: ... · Status: aprovado | pendente
- 1. ... → resposta
```

## Ao terminar
Mostre um resumo curto e **liste as Decisões Necessárias**. Diga: "Responda as decisões e aprove o Research para seguirmos para o `/plan`."

Quando o humano responder, registre as respostas em **Decisões respondidas**. Decisão que ficou sem resposta **não é suposta**: fica marcada como pendente e vira dúvida explícita no Plan.

> ⚠️ Não avance para o Plan sem as decisões respondidas e o Research aprovado.

## Contexto passado pelo usuário
$ARGUMENTS
