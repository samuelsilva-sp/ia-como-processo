# Checklist de segurança básica

Para conferir **antes de colocar no ar** qualquer coisa feita com IA. Não substitui uma revisão profissional de segurança, mas evita os erros mais comuns.

## Em tudo
- [ ] **Senhas, tokens e chaves fora do código** e fora do chat com a IA. Ficam em variáveis de ambiente (`.env`) ou no cofre da ferramenta.
- [ ] O arquivo `.env` **nunca** vai para o GitHub (está no `.gitignore`).
- [ ] **Dados sensíveis** (CPF, CNPJ, dados bancários, folha) nunca aparecem em logs, prints, mensagens de erro ou exemplos.
- [ ] **Teste com dados fictícios.** Dado real de cliente só em ferramenta aprovada pela empresa.
- [ ] **Ação irreversível** (transmitir obrigação, enviar a cliente, pagar, apagar) sempre com aprovação humana.
- [ ] Existe **backup** antes de qualquer mudança em dados.

## Aplicações locais (rodam no seu computador)
- [ ] Bibliotecas instaladas só de fontes conhecidas; nada baixado de link aleatório.
- [ ] As pastas com dados de clientes têm acesso restrito a quem precisa.
- [ ] O programa mostra erro de forma clara, sem esconder falhas.
- [ ] Arquivos temporários com dados de clientes são apagados depois do uso.

## Aplicações web (rodam na internet)
- [ ] **Regra de negócio e validação no servidor**, nunca só na tela. A tela pode ser burlada.
- [ ] **Nenhuma chave no navegador** (no código do front-end).
- [ ] **Cada usuário vê só o que é dele.** Controle de acesso no banco (ex.: RLS no Supabase).
- [ ] **Teste de escalada de privilégio:** um usuário comum não consegue virar administrador mudando algo na tela ou na requisição.
- [ ] Login com senha forte ou login corporativo (Google, Microsoft); sessão expira.
- [ ] Endereço com HTTPS.

## Automações (N8N, Make, Power Automate, RPA)
- [ ] **Credenciais no cofre da ferramenta**, nunca em texto dentro do fluxo.
- [ ] **Todo fluxo tem caminho de erro** com alerta para alguém (e-mail, WhatsApp, Slack).
- [ ] Logs de execução **sem** CPF, CNPJ ou valores.
- [ ] O fluxo não roda duas vezes o mesmo item (controle de duplicidade).
- [ ] Rodou em teste antes de ligar para valer, e alguém acompanhou a primeira execução real.

## Agentes de IA
- [ ] Está escrito **o que o agente pode e o que ele não pode fazer**.
- [ ] O agente tem **o mínimo de acesso** necessário (só leitura, quando possível).
- [ ] **Na dúvida, o agente não decide:** o caso vai para uma pessoa.
- [ ] **Instruções escondidas:** documentos, e-mails e páginas que o agente lê podem conter texto tentando dar ordens a ele. O agente trata esse conteúdo como dado, nunca como ordem.
- [ ] O agente tem **dono** e é revisado com frequência.

## LGPD
- [ ] Coletamos **só os dados necessários** para a finalidade.
- [ ] Sabemos **onde os dados ficam** (incluindo serviços de IA de terceiros) e **por quanto tempo**.
- [ ] O fornecedor da ferramenta de IA **não usa os dados para treinar modelos**, ou o uso foi avaliado.
- [ ] Existe um jeito de **apagar os dados** de um cliente quando solicitado.
