INSTRUÇÕES - GlowKing site (versão com checagem manual)
========================================

Arquivos incluídos:
- index.html  -> página pública (exibe PIX e pede comprovante)
- style.css   -> estilos
- admin.html  -> painel local para adicionar códigos de confirmação (armazena no navegador)
- README.txt  -> este arquivo

Como o site protege o acesso:
- O site NÃO libera automaticamente o link do Telegram.
- O visitante faz o PIX e usa o botão 'Já paguei' para enviar comprovante por e-mail ou WhatsApp.
- O administrador confere o comprovante manualmente.
- Após checar, o administrator gera um código (ex.: ABC123) e envia ao comprador.
- O comprador volta ao site, abre 'Já paguei', cola o código em 'Já recebeu o código?' e clica em validar.
- Se o código estiver presente no armazenamento local do navegador do visitante, o botão 'Entrar no grupo' será habilitado.

Observações importantes:
- Este método é MANUAL e funciona sem servidor. Ele depende que o administrador gere/compartilhe códigos.
- Para automação (liberar o acesso automaticamente após confirmação real do PIX) é necessário:
  1) Ter uma conta em um provedor de pagamento que suporte PIX (Gerencianet, Mercado Pago, Pagar.me).
  2) Criar uma 'cobrança' via API/checkout e usar webhook para receber notificação automática quando a cobrança for liquidada.
  3) Buildar um pequeno backend (pode ser serverless) que receba o webhook e envie ao cliente o código de liberação ou atualize um banco de dados que o site consulte.

Links úteis (começar aqui):
- Gerencianet (API PIX): https://gerencianet.com.br
- Mercado Pago (PIX): https://www.mercadopago.com.br
- Pagar.me: https://pagar.me
- Exemplo de tutorial sobre Pix + webhooks: procure por 'pix webhook gerencianet tutorial' no Google.

Como publicar:
- Faça upload dos arquivos em seu repositório GitHub (index.html, style.css, admin.html).
- Ative GitHub Pages na branch 'main' e pasta '/ (root)'.
- Abra admin.html no seu navegador (apenas você como administrador) e gere os códigos quando confirmar pagamentos.

Personalizações:
- Substitua 'admin@example.com' no index.html por seu e-mail real.
- Substitua o número de WhatsApp no index.html (formato internacional) pelo seu número.
- Se preferir automação completa, eu posso ajudar a integrar Mercado Pago ou Gerencianet com um pequeno backend (te mostro o passo a passo).

Se quiser, eu já gero um ZIP com tudo pronto para você baixar.
