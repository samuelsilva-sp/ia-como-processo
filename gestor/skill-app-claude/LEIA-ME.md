# O método como skill no app do Claude

Para quem usa o **Claude no navegador ou no aplicativo** (claude.ai), sem Claude Code. A skill conduz as 5 etapas do método (Research → Plan → Break → Implement → Review) em conversa, com a sua aprovação entre elas, e entrega os documentos de cada etapa.

## Antes de começar
- A **execução de código** precisa estar ligada na sua conta. Sem ela, a opção de skills não aparece.
- Em conta de empresa (Team ou Enterprise), o administrador pode ter bloqueado skills personalizadas. Se não achar a opção, fale com ele.

## Instalar (2 minutos)
1. Baixe o arquivo **[metodo-ia-como-processo.zip](metodo-ia-como-processo.zip)**. **Não descompacte.**
2. No Claude, vá em **Customize › Skills** (ou abra direto `claude.ai/customize/skills`).
3. Clique em **+**, depois **Create skill** › **Upload a skill**, e envie o arquivo `.zip`.
4. Confira se a skill **metodo-ia-como-processo** aparece na lista e está ligada.

> Os nomes dos menus podem mudar com atualizações do Claude. Se não encontrar, procure por "Skills" nas configurações.

## Usar
Abra uma conversa nova e peça, por exemplo:

```
Vamos usar o método IA como processo.
Quero melhorar este processo do escritório: [descreva como explicaria a um funcionário novo].
```

A skill começa pelo **Research**: faz perguntas, organiza o processo e devolve as decisões que só você pode tomar. Responda, aprove, e ela segue para a próxima etapa.

**Dicas**
- Se ela não entrar sozinha, peça de forma explícita: "use a skill metodo-ia-como-processo".
- Use **exemplos fictícios**: nada de CPF, CNPJ ou dados reais de clientes.
- A skill organiza o processo, mas **a regra fiscal é do especialista do seu escritório**: ela marca o que precisa ser confirmado.

## Não usa o app do Claude?
O mesmo método funciona no ChatGPT e no Gemini colando as instruções num Projeto ou Gem: veja [prompts para qualquer IA](../prompts-qualquer-ia.md).
