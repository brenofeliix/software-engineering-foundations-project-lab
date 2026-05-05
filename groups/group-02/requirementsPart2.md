### Performance (Desempenho)

* O sistema deve carregar a página web em menos de 2 segundos **(NRF01)**.
* O sistema deve retornar uma busca em menos de 1 segundo **(NRF02)**.
* O sistema deve processar pedidos simultâneos de até 1.000 usuários **(NRF03)**.
* O sistema deve suportar um aumento de até 50% no volume de acesso **(NRF11)**.


### Security (Segurança)

* O sistema deve criptografar a comunicação cliente-servidor via protocolo HTTPS **(NRF07)**.
* O sistema deve segregar o acesso por níveis de permissão.
* O sistema deve exigir autenticação dos usuários que se utilizam das funcionalidades descritas nos **RF13 - RF19**.
* O sistema deve informar claramente quais dados e para qual finalidade serão coletados dos usuários **(NRF08)**.
* O sistema deve permitir que o usuário solicite que seus dados sejam excluídos do banco de dados **(NRF08)**.
* O sistema deve solicitar a permissão do usuário para o envio de sugestões **(RF19 e NRF08)**.


### Usability (Usabilidade)

* O sistema deve adaptar-se a diferentes tamanhos de tela **(NFR09)**.
* O sistema deve garantir que o fluxo do pedido seja concluído no máximo em 4 clicks **(NFR10)**.
* O sistema deve operar nos quatro principais navegadores: Google Chrome, Apple Safari, Microsoft Edge e Mozilla Firefox **(NFR12)**.

## 4. User Stories (Histórias de Usuário)

**US01: Navegação por Menu e Categorias (Ref: FR01, FR02, FR10)**

- User Story: As a customer, I want to browse the menu by categories or search for specific dishes, so that I can quickly find what I want to eat.  
- Tradução: Como um cliente, eu quero navegar no cardápio por categorias ou buscar por pratos específicos, para que eu possa encontrar rapidamente o que desejo comer.

**US02: Detalhes e Personalização do Prato (Ref: FR03, FR04, FR05)**

- User Story: As a customer, I want to see photos, ingredients, and prices of a dish and customize my order, so that I can tailor the meal to my preferences and know exactly what I am buying.  
- Tradução: Como um cliente, eu quero ver fotos, ingredientes e preços de um prato e personalizar meu pedido, para que eu possa ajustar a refeição às minhas preferências e saber exatamente o que estou comprando.  

**US03: Rapidez e Sugestões (Ref: FR06, FR09)**

- User Story: As a customer, I want to receive curated suggestions (like "Dish of the Day") and be able to send my order as soon as I pick the first item, so that I can save time during the ordering process.  
- Tradução: Como um cliente, eu quero receber sugestões selecionadas (como "Prato do Dia") e poder enviar meu pedido assim que escolher o primeiro item, para que eu possa economizar tempo durante o processo de pedido.  

**US04: Checkout e Acompanhamento (Ref: FR07, FR08, FR11)**

- User Story: As a customer, I want to see a summary of my order with the estimated time and track its status, so that I can be informed about when my food will arrive.  
- Tradução: Como um cliente, eu quero ver um resumo do meu pedido com o tempo estimado e acompanhar seu status, para que eu possa ser informado sobre quando minha comida chegará.  

**US05: Pagamento Seguro e Versátil (Ref: FR12 / NFR05, NFR07)**

- User Story: As a customer, I want to pay using Pix, credit cards, or digital wallets securely, so that I can complete my purchase using my preferred payment method without worrying about data safety.  
- Tradução: Como um cliente, eu quero pagar usando Pix, cartões de crédito ou carteiras digitais de forma segura, para que eu possa concluir minha compra usando meu método de pagamento preferido sem me preocupar com a segurança dos dados.

**US06: Gestão de Cardápio em Tempo Real (Ref: FR15, FR16, FR17 / NFR13)**  

- User Story: As a manager, I want to update dish availability, prices, and descriptions instantly, so that the digital menu always reflects the current stock and pricing.
- Tradução: Como um gestor, eu quero atualizar a disponibilidade dos pratos, preços e descrições instantaneamente, para que o cardápio digital sempre reflita o estoque e os preços atuais.  

**US07: Monitoramento e Relatórios (Ref: FR13, FR19)**

- User Story: As a manager, I want to monitor active orders in real-time and access monthly performance reports, so that I can make data-driven decisions to improve the restaurant's profitability.  
- Tradução: Como um gestor, eu quero monitorar os pedidos ativos em tempo real e acessar relatórios de desempenho mensais, para que eu possa tomar decisões baseadas em dados para melhorar a lucratividade do restaurante.
  
**US08: Controle de Fluxo de Preparo (Ref: FR14, FR18)**

- User Story: As a kitchen staff member or waiter, I want to update the order status (In Progress, Ready, Served), so that the entire team and the customer stay synchronized on the progress.  
- Tradução: Como um membro da equipe de cozinha ou garçom, eu quero atualizar o status do pedido (Em Andamento, Pronto, Servido), para que toda a equipe e o cliente permaneçam sincronizados sobre o progresso.  

**US09: Experiência Fluida e Responsiva (Ref: NFR01, NFR09, NFR10)**

- User Story: As a user, I want the interface to load quickly and adapt to my device screen, so that I can place an order in 4 steps or less without technical frustrations.  
- Tradução: Como um usuário, eu quero que a interface carregue rapidamente e se adapte à tela do meu dispositivo, para que eu possa fazer um pedido em 4 etapas ou menos, sem frustrações técnicas.  
