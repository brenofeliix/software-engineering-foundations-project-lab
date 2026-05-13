# Registro de Inovação

## Nome da Solução
Deal Connection.

---

## Problema
O atendimento presencial em estabelecimentos gastronômicos compromete a experiência do cliente e a eficiência de negócio, entre os quais:

- Ineficiência no Fluxo de Atendimento devido a dependência de interação humana, gerando tempo de espera e insatisfação do cliente.
- Falhas de Comunicação Operacional, como erros no preenchimento da comanda física.
- Inflexibilidade de Custos, consequência direta dos recursos humanos empregados independentemente do horário de atendimento, o que compromete a escalabilidade dos lucros nos períodos de baixa demanda.

---

## Solução Proposta
A solução consiste em uma Plataforma Web que acompanhe o processo de compra e gestão de negócio, proporcionando:

- Redução drástica do tempo de espera no que diz respeito ao atendimento imediato;
- Confiabilidade dos pedidos entregues ao mitigar erros na comanda;
- Eficiência operacional ao atender diferentes níveis de demanda a custos mais estabilizados, isso porque o sistema permite o atendimento simultâneo de clientes.
---

## Diferencial Inovador
Considerando que a ultilização de sistemas semelhantes, o que propomos oferece vatagens que são aproveitadas pelo cliente final, tais como:  
- Não precisa baixar o sistema no aparalho do cliente;  
- O cliente faz o seu pedido diretamente no sistema, não precisando de outro para ter uma experiência completa;
- Por ser mais interativo, também se torna um diferencial aos olhos do cliente final;  

Sendo assim, as vantagens que o sistema proposto tem, é justamente focado em melhor experiência dos clientes. Sendo uma experiência que foca na satisfação do cliente.

---

## Potencial de Aplicação
Em empreendimentos gastronômicos.

---

## Tecnologias Utilizadas

- Linguagem JavaScript com sua variante TypeScript.
- NestJS Framework.
- APIs RESTful: Para a comunicação entre o seu servidor e os provedores de pagamento (PSPs).
- WebSockets: Tecnologia usada para a comunicação em tempo real (bidirecional), permitindo que o servidor "avise" instantaneamente a maquininha sobre um novo pagamento.
- Tecnologias Web (HTML5/CSS3/JavaScript): O sistema é disponibilizado via navegador (Web), permitindo o acesso através da leitura de QR Codes nas mesas sem a necessidade de o cliente instalar um aplicativo.
- Protocolos de Pagamento: Integração com PSPs (Payment Service Providers) para processar Pix e Cartões.
- TEF (Transferência Eletrônica de Fundos) ou SDKs: Softwares específicos para conversar com o hardware das maquininhas.
- Smart POS (Android): Os terminais físicos que rodam as aplicações de pagamento e interagem com o seu sistema.
- HTTPS / TLS ($\ge$ 1.2): Protocolos de segurança para criptografia de dados em trânsito na internet.
- Tokenização: Tecnologia para substituir dados sensíveis de cartões por chaves aleatórias (tokens).
- Webhooks: Para o recebimento de notificações automáticas de confirmação de pagamento.
- Criptografia de Ponta a Ponta: Garantindo a privacidade desde o celular do cliente até o banco de dados.
- NoSQL para cache de cardápio e um banco de dados relacional para as demais interações, como o (PostgreSQL).

---

## Possível contribuição científica ou tecnológica
Este projeto representa uma solução de vanguarda para a automação do food service, unificando a agilidade do autoatendimento via QR Code com a robustez da automação financeira em terminais Smart POS. Ao implementar uma arquitetura agnóstica e segura, baseada em tokenização e comunicação em tempo real, a aplicação elimina erros humanos, protege dados sensíveis e otimiza a logística de pagamentos. O resultado é um ecossistema tecnológico de alta performance que oferece conformidade rigorosa com normas internacionais, reduz custos operacionais e entrega uma experiência de consumo fluida, posicionando-se como uma infraestrutura digital escalável e competitiva para o mercado global.

---

## Data de Registro
12/05/2026

---

## Autores
- Thiago Rafael Caixeta Tavares da Silva
- Flávio Eduardo Mendes Peixoto
- Rafael Elim Oliveira
- Joaber Moreira da Silva
- Walky Antoine

---
