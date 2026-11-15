# Como analisar qualquer processo em 5 perguntas

Um guia de uma página para olhar **qualquer** processo do escritório (contábil, fiscal, DP, atendimento) e descobrir o que vira automação, o que é trabalho da IA e o que fica com a equipe. **Não precisa saber programar nem dominar a regra fiscal de cabeça:** a regra a equipe já conhece; aqui você descobre como ela vira processo.

## As 5 perguntas

| # | Pergunta | O que a resposta indica | Quem cuida no futuro |
|---|---|---|---|
| 1 | **De onde vem o dado?** XML, OFX, PDF, foto, planilha, e-mail, WhatsApp, portal | Dado estruturado (XML, OFX) se lê sem IA. Dado bagunçado (PDF, foto, texto livre) é onde a IA mais ajuda | Automação ou IA |
| 2 | **O que é regra fixa?** Alíquota, tabela, prazo, cálculo, de-para | Regra fixa vira **código**: sempre igual e auditável. Ela fica escrita num lugar só, com um dono | Código |
| 3 | **O que é leitura ou interpretação?** Entender um documento, classificar, resumir | É o trabalho da IA | IA |
| 4 | **O que é decisão ou exceção?** Dúvida de enquadramento, divergência, caso novo | Vai para uma **fila do analista**. Na dúvida, a IA não decide sozinha | Analista |
| 5 | **Onde termina?** Sistema contábil, obrigação, guia, cliente | Ação irreversível (transmitir, enviar, pagar, apagar) sempre com **aprovação humana** | Analista |

## Exemplo rápido (fictício): conciliação bancária

1. **Dado:** extrato em OFX (se vier em PDF, peça o OFX ao cliente).
2. **Regra:** transferência entre contas próprias, tarifa, imposto recorrente: cada cliente tem as suas regras.
3. **Leitura:** quase nada aqui precisa de IA. Ela entra para sugerir a conta de um lançamento novo.
4. **Exceção:** o que nenhuma regra explica vai para a fila do analista, e cada decisão vira regra nova.
5. **Fim:** arquivo de importação para o sistema contábil, conferido pelo analista.

## Depois das 5 perguntas
- Passe as respostas para o [mapa de processo](mapa-de-processo.md): ele vira o insumo do **Research**.
- Use o pedido de Research pronto da sua área em [ideias por área](prompts-por-area.md).
- Defina o indicador e o dono (passos 2 e 5 do [comece aqui](../comece-aqui.md)).

> Regra de ouro: **processo para a IA, decisão para o analista.**
