# Mapa de processo: o que é da IA e o que é do analista

Preencha antes de pedir qualquer coisa à IA. Ele vira o insumo do **Research**.
Também existe em planilha: [`mapa-de-processo.xlsx`](mapa-de-processo.xlsx).

## 1. Cabeçalho

| Campo | Preencha |
|---|---|
| **Processo** | |
| **Resultado esperado** (o que muda para o negócio) | |
| **Indicador** (o número que mostra que melhorou) | |
| **Valor hoje** | |
| **Meta** | |
| **Dono da solução** (quem responde e melhora todo mês) | |
| **Dados sensíveis envolvidos** (CPF, CNPJ, bancários…) | |

## 2. Etapas

Para cada etapa, decida quem faz no futuro:
- **IA executa:** roda sozinha, sem conferência caso a caso;
- **IA apoia:** a IA prepara, uma pessoa confere;
- **Humano:** só uma pessoa decide (julgamento, risco, ação irreversível).

| # | Etapa | Quem faz hoje | Sistema / fonte | Tempo por mês | No futuro: IA executa / IA apoia / Humano | Decisão humana (quando?) | Exceções comuns |
|---|---|---|---|---|---|---|---|
| 1 | | | | | | | |
| 2 | | | | | | | |
| 3 | | | | | | | |
| 4 | | | | | | | |
| 5 | | | | | | | |

## 3. Exemplo preenchido (fictício)

**Processo:** apuração de IRRF sobre distribuição de lucros · **Resultado:** a equipe só confere o que é ambíguo · **Indicador:** % de documentos que vão para conferência · **Dono:** coordenador fiscal

| # | Etapa | Hoje | No futuro | Decisão humana |
|---|---|---|---|---|
| 1 | Cobrar comprovantes dos clientes | Analista, por e-mail | **IA executa** (automação cobra e baixa) | — |
| 2 | Ler cada comprovante | Analista, um por um | **IA executa** (extrai pagador, recebedor, valor) | Documento ilegível vai para conferência |
| 3 | Identificar o sócio | Analista | **IA apoia** (regras ligam e registram o motivo) | Recebedor sem sócio, empate entre sócios |
| 4 | Calcular o IRRF | Analista, em planilha | **IA executa** (código, regra da lei) | — |
| 5 | Gerar o arquivo para a Reinf | Analista | **IA executa** | **Humano aprova antes de transmitir** |

## 4. Perguntas de checagem
- Alguma etapa marcada "IA executa" envolve **ação irreversível**? Se sim, ela precisa de aprovação humana.
- Toda **exceção** tem para onde ir (uma fila, uma pessoa)?
- O **indicador** pode ser medido hoje, antes de mudar algo?
- O **dono** sabe que é o dono?
