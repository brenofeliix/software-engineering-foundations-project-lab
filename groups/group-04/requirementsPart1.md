# Requirements Specification

Este documento descreve de forma estruturada os requisitos do sistema a ser desenvolvido. Ele deve ser claro, objetivo e completo, servindo como base para desenvolvimento, testes e validação do software.

---

## 1. System Overview (Visão Geral do Sistema)
A Universidade Federal de Rondonópolis (UFR) disponibiliza à comunidade acadêmica o Restaurante Universitário (RU) que atende estudantes e servidores em suas refeições diárias, sendo essa uma unidade estratégica para a permanência estudantil que oferece refeições a preços acessíveis mediante um sistema de créditos pré-pagos realizado de forma presencial. Tendo em vista sua importância social, é relevante mitigar qualquer gargalo logístico que afete a eficiência desse processo.

Destacam-se como principais problemas nesse modelo, a burocracia do cadastro exclusivamente presencial, dificuldade no acesso ao cardápio e, principalmente, a falta de uma interface que permita consulta de saldo e recarga remotamente. Esse cenário promove um fluxo lento e filas longas, resultando na perda de tempo produtivo dos estudantes e servidores, reforçando a necessidade de um sistema digital que entre como facilitador desse serviço.

O sistema proposto visa solucionar esse problema por meio de uma plataforma digital para o RU, baseada em uma arquitetura modular e desacoplada. Essa arquitetura é dividida em dois módulos principais: a interface amigável e o sistema gerenciador que são capazes de atuar independentemente entre si, garantindo maior flexibilidade e facilidade de manutenção, permitindo uma maior facilidade de evolução futura. Dessa forma, a aplicação pode atender tanto cenários em que é necessário um sistema completo quanto situações em que apenas a integração via API com sistemas já existentes é suficiente. A interface permite ao usuário realizar ações como login, consulta do saldo, visualização do cardápio, recarga via Pix e acesso à comunicados do RU. Já o sistema gerenciador é responsável pelo processamento das informações, controle de dados, regras de negócio e integração com sistemas externos, recomendada para RUs que não possuem um sistema de gestão próprio ou que utilizam sistemas considerados obsoletos.

---

## 2. Functional Requirements (Requisitos Funcionais)

- RF01: O sistema deve permitir autenticação do usuário utilizando credenciais institucionais.
- RF02: O sistema deve permitir a consulta de saldo do usuário em tempo real.
- RF03: O sistema deve permitir a realização de recargas de saldo.
- RF04: O sistema deve exibir o cardápio semanal atualizado.
- RF05: O sistema deve exibir o histórico de recargas do usuário.
- RF06: O sistema deve enviar notificações ao usuário
- RF07: O sistema deve exibir o registro de check-in.
- RF08: O sistema deve permitir feedback sobre as refeições do dia. 
- RF09: O sistema deve permitir integração com APIs.
- RF10: O sistema deve permitir que o administrador realize o cadastro de usuários.
- RF11: O sistema deve permitir que o administrador gerencie os créditos dos usuários.
- RF12: O sistema deve permitir que o administrador gerencie o cardápio.
- RF13: O sistema deve permitir que o administrador gere relatórios de uso do sistema.


## 3. Non-Functional Requirements (Requisitos Não Funcionais)

- RNF01: O sistema, em um cenário ideal, deve responder às requisições em até 2 segundos.
- RNF02: O sistema deve suportar múltiplos acessos simultâneos com uma perda minima de desempenho.
- RNF03: Os dados dos usuários devem ser armazenados de forma segura, utilizando criptografia
- RNF04: O sistema deve ser compatível com dispositivos móveis.
- RNF05: A interface do sistema deve ser intuitiva e de fácil navegação.
- RNF06: O sistema deve ser limitado a login por SUAP.
- RNF07: O sistema deve estar disponível durante 99% do tempo, desconsiderando possíveis manutenções.
- RNF08: O sistema deve garantir integridade dos dados durante as operações de recarga e pagamento.
- RNF09: O sistema deve possuir mecanismos de backup e recuperação de dados.
- RNF10: O sistema deve apresentar tempo de recuperação rápido em caso de falhas.
- RNF11: O sistema deve possuir funções de acessibilidade, tais como alto contraste e tema claro ou escuro.
- RNF12: O sistema deve possuir um modo para pessoas com deficiência visual.


---


