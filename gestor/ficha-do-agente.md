# Ficha do agente (o "organograma da IA")

Se o agente faz parte da equipe, ele precisa ser gerido como alguém da equipe: missão, dono, limites e um plano de evolução (um "PDI da IA"). Uma ficha por agente ou automação.

| Campo | Preencha |
|---|---|
| **Nome do agente** | |
| **Missão** (uma frase: o que ele entrega) | |
| **Área / processo** | |
| **Dono** (quem responde por ele) | |
| **Quem usa o resultado** | |
| **Entradas** (de onde vêm os dados) | |
| **Sistemas que acessa** (e com qual permissão: ler / escrever) | |
| **Dados sensíveis que toca** | |
| **Pode fazer sozinho** | |
| **Nunca faz sozinho** | |
| **Quando chama um humano** (as exceções) | |
| **Indicadores** (valor de hoje e meta) | |
| **Como saber que ele falhou** (alerta, para quem) | |
| **Revisão** (cadência: semanal, mensal) | |
| **Plano de evolução** (próximas melhorias, em ordem) | |

---

## Exemplo preenchido (fictício)

| Campo | Exemplo |
|---|---|
| **Nome** | Leitor de comprovantes |
| **Missão** | Ler os comprovantes de distribuição de lucros do mês e entregar os dados prontos para a apuração |
| **Área / processo** | Fiscal · IRRF sobre distribuição de lucros |
| **Dono** | Coordenador fiscal |
| **Quem usa** | Analistas fiscais (fila "Conferir") |
| **Entradas** | Anexos baixados das tarefas do mês |
| **Sistemas** | Pasta do cliente (ler), banco do sistema interno (escrever) |
| **Dados sensíveis** | CPF de sócios, valores (nunca em log) |
| **Pode fazer sozinho** | Extrair pagador, recebedor, banco e valor; ligar ao sócio quando é inequívoco |
| **Nunca faz sozinho** | Decidir em caso de dúvida; transmitir a Reinf |
| **Quando chama um humano** | Documento ilegível, extrato no lugar de comprovante, recebedor sem sócio, empate entre sócios |
| **Indicadores** | % de documentos que vão para conferência (meta: cair mês a mês) |
| **Falha** | Erro de leitura ou falta de cota da IA gera alerta para o dono |
| **Revisão** | Mensal, depois do fechamento |
| **Plano de evolução** | 1) Aprender com cada decisão do analista; 2) Ler planilhas enviadas pelo cliente; 3) Painel de acompanhamento |

> "O departamento de TI de toda empresa vai ser o RH dos agentes de IA." — Jensen Huang, CEO da NVIDIA (CES, 2025)
