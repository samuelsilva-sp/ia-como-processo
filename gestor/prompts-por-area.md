# Por onde começar, área por área

Ideias de processos para colocar a IA para executar, com o que fica com a equipe. Cada uma tem um pedido de **Research** pronto para colar (no Claude Code com `/research`, ou em qualquer IA com o prompt de [prompts-qualquer-ia.md](prompts-qualquer-ia.md)).

> Use sempre **dados fictícios** nos testes e confira se a ferramenta é aprovada pela empresa antes de usar dados reais.

---

## Fiscal

| Processo | A IA executa | A equipe decide |
|---|---|---|
| Conferência das notas de entrada com a escrituração | Cruza as notas do período com o que foi escriturado e lista as diferenças | O que é erro, o que é ajuste, o que lançar |
| Retenções em notas de serviço tomado | Lê as notas e aponta as que deveriam ter retenção (IR, CSLL, PIS, Cofins, INSS) | Enquadramento duvidoso e correção com o cliente |
| Distribuição de lucros (IRRF) | Coleta e lê os comprovantes, liga ao sócio, apura e gera o arquivo | Casos ambíguos e a aprovação antes de transmitir |

```
/research Todo mês conferimos as notas de serviço tomadas pelos clientes para ver se as retenções foram feitas.
Hoje um analista abre nota por nota. Quero que a IA aponte só as notas com retenção faltando ou duvidosa,
e que o analista decida o que fazer com cada uma.
```

## Contábil

| Processo | A IA executa | A equipe decide |
|---|---|---|
| Conciliação bancária | Importa o extrato (OFX), casa com os lançamentos e aplica as regras de cada cliente | As exceções; cada decisão vira regra para o próximo mês |
| Pendências de documentos no fechamento | Lista o que falta de cada cliente e envia a cobrança | Quando escalar e o que fazer sem o documento |
| Classificação de lançamentos recorrentes | Sugere a conta com base no histórico do cliente | Lançamentos novos ou fora do padrão |

```
/research No fechamento mensal, a equipe concilia o extrato bancário de cada cliente na mão.
Quero que a IA concilie o que é óbvio (transferências, tarifas, impostos recorrentes) e deixe para o analista
só o que é diferente, aprendendo com cada decisão dele.
```

## Departamento Pessoal

| Processo | A IA executa | A equipe decide |
|---|---|---|
| Variáveis da folha enviadas pelo cliente | Lê a planilha ou o e-mail do cliente e organiza no formato do sistema | Valores fora do padrão e dúvidas de enquadramento |
| Admissão | Confere se todos os documentos chegaram e se os dados batem | Pendências e exceções com o cliente |
| Férias a vencer | Monitora os prazos e avisa com antecedência | Programação com o cliente |

```
/research Todo mês os clientes mandam as variáveis da folha (horas extras, faltas, comissões) em formatos diferentes.
Quero que a IA organize tudo no padrão do nosso sistema e aponte o que está fora do normal para o analista conferir.
```

## Societário e legalização

| Processo | A IA executa | A equipe decide |
|---|---|---|
| Certidões negativas | Monitora as datas de validade e avisa antes de vencer | A ação com o cliente quando há pendência |
| Alteração contratual | Monta o checklist de documentos e confere o que chegou | O conteúdo da alteração e a orientação ao cliente |

```
/research Precisamos acompanhar a validade das certidões negativas dos clientes.
Hoje isso é feito numa planilha que ninguém atualiza. Quero aviso automático antes de vencer
e uma lista do que exige ação do analista.
```

## Atendimento

| Processo | A IA executa | A equipe decide |
|---|---|---|
| Triagem de WhatsApp e e-mail | Identifica o assunto e encaminha para o setor certo, com um resumo | Respostas que envolvem orientação técnica ou cobrança |
| Dúvidas frequentes | Responde o que está no material aprovado e diz quando não sabe | Tudo que não está no material; o bot encaminha |

```
/research Recebemos muitas mensagens de clientes no WhatsApp sobre guias e prazos.
Quero que a IA responda só o que está no nosso material aprovado, diga quando não sabe
e encaminhe o resto para o setor certo com um resumo. Para agentes, quero começar definindo o que ele NÃO pode fazer.
```
