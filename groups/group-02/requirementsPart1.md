# Requirements Specification

Este documento descreve de forma estruturada os requisitos do sistema a ser desenvolvido. Ele deve ser claro, objetivo e completo, servindo como base para desenvolvimento, testes e validação do software.

---

## 1. System Overview (Visão Geral do Sistema)

O Sistema de Gestão de Pedidos é uma plataforma web que visa reduzir a ineficiência do fluxo de atendimento tradicional oferecendo os serviços de cardápio digital e interativo, gerenciamento de pedidos e pagamento integrado. Este produto destina-se aos proprietários e/ou gestores de negócios gastronômicos e, em último caso, aos seus próprios clientes.

## 2. Functional Requirements (Requisitos Funcionais)

FR01: O sistema deve permitir que o cliente inicie seu pedido através de um menu principal.  
FR02: O sistema deve permitir que o cliente realize o pedido por categoria de prato.  
FR03: O sistema deve permitir que o cliente tenha acesso aos detalhes dos pratos, como ingredientes, valores, tempo estimado e imagens dos mesmos.  
FR04: O sistema deve permitir que o cliente selecione a quantidade de itens por pedido.  
FR05: O sistema deve permitir que o cliente personalize o pedido adicionando ou excluindo acompanhamentos.  
FR06: O sistema deve permitir que o cliente envie seu pedido assim que selecionado o primeiro item.  
FR07: O sistema deve exibir a descrição do pedido, subtotal e tempo total estimado assim que o cliente fechar o pedido.  
FR08: O sistema deve exigir a confirmação de envio de pedido.  
FR09: O sistema deve sugerir pedidos por classes, como jantar romântico, prato do dia, pratos mais bem avaliados do estabelecimento, entre outros.  
FR10: O sistema deve permitir que o cliente faça busca por prato.  
FR11: O sistema deve permitir que o cliente faça novos pedidos e acompanhe o status de outros já enviados.  
FR12: O sistema deve permitir que os clientes efetuem o pagamento via Pix, cartões crédito/débito ou carteira digital.  
FR13: O sistema deve permitir que os gestores acompanhem os pedidos em tempo real.    
FR14: O sistema deve permitir que os responsáveis na cozinha modifiquem o status do pedido na seguinte sequência: “Em andamento”, “Pronto para servir” e os garçons para “Servido”.  
FR15: O sistema deve permitir que os gestores modifiquem a disponibilidade dos pratos em tempo real.  
FR16: O sistema deve permitir que os gestores alterem a descrição e os valores dos produtos.  
FR17: O sistema deve permitir que os gestores solicitem a inclusão ou exclusão de novos pratos.  
FR18: O sistema deve atualizar o status para “Finalizado” após a confirmação do pagamento.  
FR19: O sistema deve fazer um relatório mensal, contendo quantidade de pedidos feitos, porcentagem de pedidos de cada prato, avaliações de cada prato que foi pedido no mês, deve mostrar qual foi o prato que menos teve pedidos e avaliações e sugerir que mude o prato ou adicione um novo no lugar, e a receita bruta de todos os pagamentos do mês.


## 3. Non-Functional Requirements (Requisitos Não Funcionais)

**DESEMPENHO**:

NRF01: A página deve carregar em menos de 2 segundos.  
NRF02: O sistema deve retornar a busca por pratos em menos de 1 segundo.  
NRF03: O sistema deve processar pedidos simultâneos de centenas de clientes, sem comprometer sua fluidez.

**DISPONIBILIDADE**:

NFR04: O sistema deve funcionar em 99,9% do tempo.

**INTEROPERABILIDADE**:

NFR05: O sistema deve integrar-se a PSPs via APIs RESTful (HTTPS, TLS maior ou igual á  1.2), processando Pix (QR Code Dinâmico/Copia e Cola) com confirmação via webhooks, e pagamentos via cartões/carteiras digitais sob conformidade PCI DSS, utilizando obrigatoriamente tokenização para evitar o tráfego ou armazenamento de dados sensíveis no servidor.  
NFR06: O sistema deve realizar a automação de terminais físicos (Smart POS) via TEF ou SDKs, estabelecendo comunicação via HTTP Local ou WebSockets para envio de valores e recepção de status sem digitação manual, operando através de uma camada de abstração agnóstica que suporte diferentes adquirentes e modelos de hardware.

**SEGURANÇA E PRIVACIDADE**:

NFR07: O sistema deve criptografar de ponta a ponta todas as transações.  
NFR08: O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados.

**QUALIDADE**:

NFR09: A plataforma deve-se adaptar a diferentes tamanhos de tela.  
NFR10: O fluxo do pedido deve ser no máximo 4 ações (“Selecionar pedido”, “Fechar pedido”, “Confirmar pedido” e “Efetuar pagamento”).  
NFR11: O sistema deve suportar um aumento de 50% no volume de acesso durante alta demanda, sem interferir no desempenho.  
NFR12: A plataforma deve funcionar nos principais navegadores.  
NFR13: O sistema deve permitir atualizações no cardápio, sem interromper o serviço aos clientes.
