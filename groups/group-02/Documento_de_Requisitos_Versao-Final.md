<details>
  <summary><b>Clique para expandir o Sumário</b></summary>
  
  * [1. Introdução](#1-Introdução)
  * [2. Product Vision](#2-Product-Vision)
  * [3. Visão-Geral do Sistema](#3-Visão-Geral-do-Sistema)
  * [4. Requisitos Funcionais](#4-Requisitos-Funcionais)
  * [5. Requisitos Não Funcionais](#5-Requisitos-Não-Funcionais)
  * [6. Requisitos Organizacionais](#6-Requisitos-Organizacionais)
  * [7. Requisitos Externos](#7-Requisitos-Externos)
  * [8. Arquitetura do Sistema](#8-Arquitetura-do-Sistema)
  * [9. Casos de Uso e Diagramas UML](#9-Casos-de-Uso-e-Diagramas-UML)
  * [10. Plano de Testes](#10-Plano-de-Testes)
  * [11. Critérios de Aceitação](#11-Critérios-de-Aceitação)
  * [12. Restrições](#12-Restrições)
  * [13. Premissas](#13-Premissas)
  * [14. Observações Finais](#14-Observações-Finais)
</details>

#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução
A busca por agilidade no atendimento tornou-se um dos principais critérios na hora de escolher uma experiência gastronômica. A fim de proporcionar aos clientes uma visita agradável e atender habilmente a demanda de pedidos, muitos restaurantes e lanchonetes automatizaram seus serviços através de cardápio e formas de pagamento digitais.

### 1.1 Objetivo 
Este documento tem como objetivo principal, conter informações primordiais de todas as etapas do desenvolvimento da engenharia de requisitos do projeto proposto. Este projeto tem como foco principal, reduzir o tempo de atendimento e dar mais flexibilidade para clientes em suas escolhas do menu, automatizando o atendimento ao cliente com uma aplicação web à disposição dos usuários. 



### 1.2 Escopo
O sistema incorpora a automação dos serviços prestados por restaurantes e lanchonetes, de forma que os clientes realizem seus próprios pedidos e efetuem os pagamentos de forma rápida e simples; auxilia também a equipe operacional no preparo e na entrega dos pedidos, assim como, os gerentes e proprietários na administração do negócio.


### 1.3 Definições, Acrônimos e Abreviações
|Acrônimos e Abreviações|Definição| 
|---|---|
|RF|Requisitos Funcionais|    
|RN|Requisitos não funcionais|  
|LGPD|Lei Geral de Proteção de Dados|  
|Smart POS|Smart Point of Sale|  
|HTTP|Hypertext Transfer Protocol|  
|HTTPS|Hypertext Transfer Protocol Secure|  
|PSP|Payment Service Providers|  
|APIs|Application Programming Interface|
|REST|epresentational State Transfer| 
|PCI DSS|Payment Card Industry Data Security Standard| 
|TLS|Transport Layer Security|  
|TEF|Transferência Eletrônica de Fundos|  
|SDK|Software Development Kit| 

---

##  2. Product Vision

### 2.1 Problema
O atendimento presencial em estabelecimentos gastronômicos compromete a experiência do cliente e a eficiência de negócio, entre os quais:
- **Ineficiência no Fluxo de Atendimento** devido a dependência de interação humana, gerando tempo de espera e insatisfação do cliente.
- **Falhas de Comunicação Operacional**, como erros no preenchimento da comanda física.
- **Inflexibilidade de Custos**, consequência direta dos recursos humanos empregados independentemente do horário de atendimento, o que compromete a escalabilidade dos lucros nos períodos de baixa demanda.


### 2.2 Solução
A solução consiste em uma Plataforma Web que acompanhe o processo de compra e gestão de negócio, proporcionando:
- **Redução drástica do tempo de espera** no que diz respeito ao atendimento imediato;
- **Confiabilidade dos pedidos entregues** ao mitigar erros na comanda;
- **Eficiência operacional** ao atender diferentes níveis de demanda a custos mais estabilizados, isso porque o sistema permite o atendimento simultâneo de clientes.


### 2.3 Público-Alvo
- **Usuário Final**: o consumidor interessado pelo atendimento mais ágil e transparente.
- **Cliente (Stakeholder/Gestor)**: proprietários e gerentes de estabelecimentos gastronômicos que necessitam de maior controle de negócio.


### 2.4 Proposta de Valor
Aumenta a produtividade do estabelecimento, pois os pedidos são feitos mais rápidos e sem erros de comunicação. Otimiza o tempo que o cliente leva para fazer seus pedidos e mantém um ambiente organizado e bem estruturado.


### 2.5 Diferencial
Considerando que a ultilização de sistemas semelhantes, o que propomos oferece vatagens que são aproveitadas pelo cliente final, tais como:
- Não precisa baixar o sistema no aparalho do cliente;
- O cliente faz o seu pedido diretamente no sistema, não precisando de outro para ter uma experiência completa;
- Por ser mais interativo, também se torna um diferencial aos olhos do cliente final;  

Sendo assim, as vantagens que o sistema proposto tem, é justamente focado em melhor experiência dos clientes. Sendo uma experiência que foca na satisfação do cliente.

### 2.6 Funcionalidades principais (alto nível)
- Interface via QR Code;
- Cardápio dinâmico e interativo;
- Customização dos pedidos;
- Pagamento integrado;
- Dashboard Administrativo;

---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
O sistema é uma aplicação web disponibilizada por meio de um QR Code, a fim de reduzir o tempo de atendimento em empreendimentos gastronômicos.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais

## RF01 - Início de Pedido via Menu Principal  
**Descrição:** O sistema deve fornecer uma interface inicial (menu principal) onde o cliente pode iniciar o processo de compra.  
**Prioridade:** Alta.  
**Entradas:** Interação do usuário com o botão de início.  
**Saídas:** Exibição do catálogo ou categorias de produtos.  
**Regras de Negócio:** O menu deve estar disponível assim que o aplicativo/sistema for carregado.  

## RF02 - Navegação por Categoria  
**Descrição:** O sistema deve organizar os pratos em categorias (ex: Entradas, Bebidas, Sobremesas) para facilitar a navegação.  
**Prioridade:** Alta.  
**Entradas:** Seleção de uma categoria específica pelo cliente.  
**Saídas:** Lista de pratos pertencentes à categoria selecionada.  
**Regras de Negócio:** Um prato pode pertencer a mais de uma categoria se necessário.  

## RF03 - Detalhes do Prato  
**Descrição:** O sistema deve exibir informações detalhadas de cada item, incluindo ingredientes, preço, tempo de preparo e fotos.  
**Prioridade:** Alta.  
**Entradas:** Seleção de um prato específico.  
**Saídas:** Tela de detalhes com textos e imagens.  
**Regras de Negócio:** As imagens devem ser de alta resolução e os valores devem estar atualizados conforme o banco de dados.  

## RF04 - Seleção de Quantidade  
**Descrição:** O sistema deve permitir que o usuário defina quantas unidades de um mesmo item deseja adicionar ao carrinho.  
**Prioridade:** Alta.  
**Entradas:** Incremento ou decremento numérico (ex: + ou -).  
**Saídas:** Valor total do item atualizado.  
**Regras de Negócio:** A quantidade mínima é 1 e a máxima pode ser limitada pelo estoque ou política da casa.  

## RF05 - Personalização de Acompanhamentos
**Descrição:** Permite ao cliente adicionar (adicionais pagos ou não) ou remover ingredientes/acompanhamentos de um prato.  
**Prioridade:** Média.  
**Entradas:** Seleção de opcionais ou campos de "retirar item".  
**Saídas:** Resumo da personalização no item do pedido.  
**Regras de Negócio:** Adicionais podem alterar o valor final do prato.  

## RF06 - Envio de Pedido Parcial  
**Descrição:** O sistema deve permitir que o cliente envie o pedido para a cozinha assim que o primeiro item for selecionado, sem necessidade de fechar todo o carrinho primeiro.  
**Prioridade:** Média.  
**Entradas:** Comando de "Enviar para Cozinha" no item selecionado.  
**Saídas:** Notificação de item enviado.  
**Regras de Negócio:** Itens enviados não podem ser editados, apenas cancelados mediante regra específica.  

## RF07 - Resumo e Fechamento de Pedido  
**Descrição:** Ao finalizar, o sistema deve exibir a lista de itens, o subtotal financeiro e o tempo total estimado para entrega/serviço.  
**Prioridade:** Alta.  
**Entradas:** Ação de "Fechar Pedido" ou "Ir para o Carrinho".  
**Saídas:** Relatório visual do pedido antes do pagamento.  
**Regras de Negócio:** O tempo estimado deve ser a soma lógica ou o maior tempo entre os pratos selecionados.  

## RF08 - Confirmação de Envio  
**Descrição:** O sistema deve exigir que o cliente confirme explicitamente o envio do pedido para evitar pedidos acidentais.  
**Prioridade:** Alta.  
**Entradas:** Clique no botão de confirmação em pop-up ou tela dedicada.  
**Saídas:** Mensagem de sucesso e início do processamento.  
**Regras de Negócio:** O pedido só é registrado no banco de dados após esta confirmação.  

## RF09 - Sugestões por Contexto (Classes)  
**Descrição:** O sistema deve sugerir pratos baseados em categorias especiais como "Jantar Romântico", "Prato do Dia" ou "Mais Bem Avaliados".  
**Prioridade:** Baixa.  
**Entradas:** Dados de avaliação e tags de categorias especiais.  
**Saídas:** Carrossel ou seção de destaques na tela inicial.  
**Regras de Negócio:** As sugestões devem ser atualizadas dinamicamente conforme as avaliações dos clientes.  

## RF10 - Busca de Pratos  
**Descrição:** Disponibilizar uma barra de pesquisa para localização rápida de pratos por nome ou palavra-chave.  
**Prioridade:** Média.  
**Entradas:** Texto digitado pelo cliente.  
**Saídas:** Lista de resultados correspondentes.  
**Regras de Negócio:** A busca deve ser insensível a maiúsculas/minúsculas.  

## RF11 - Acompanhamento de Status e Novos Pedidos  
**Descrição:** O cliente deve poder visualizar o progresso de pedidos ativos e iniciar novos pedidos simultaneamente.  
**Prioridade:** Alta.  
**Entradas:** Acesso à aba "Meus Pedidos".  
**Saídas:** Status atualizado (ex: Recebido, Em Preparo, Pronto).  
**Regras de Negócio:** O status deve ser sincronizado com a atualização feita pela cozinha/garçom.  

## RF12 - Múltiplas Formas de Pagamento  
**Descrição:** O sistema deve processar pagamentos via Pix, cartões (crédito/débito) e carteiras digitais.  
**Prioridade:** Alta.  
**Entradas:** Maquininha ou geração de QR Code Pix.  
**Saídas:** Comprovante de pagamento e atualização de status.  
**Regras de Negócio:** A transação deve ser criptografada e seguir normas de segurança financeira.  

## RF13 - Monitoramento em Tempo Real (Gestores)  
**Descrição:** Painel para gestores visualizarem todos os pedidos que entram no sistema instantaneamente.  
**Prioridade:** Alta.  
**Entradas:** Fluxo de dados dos pedidos dos clientes.  
**Saídas:** Dashboard com lista de pedidos ativos e tempos de espera.  
**Regras de Negócio:** A atualização deve ter um delay mínimo (latência baixa).  

## RF14 - Alteração de Status Operacional  
**Descrição:** Cozinha muda para “Em andamento”/“Pronto para servir” e Garçom muda para “Servido”.  
**Prioridade:** Alta.  
**Entradas:** Seleção do novo status no painel operacional.  
**Saídas:** Notificação de atualização para o cliente e gestor.  
**Regras de Negócio:** A sequência de status deve ser respeitada cronologicamente.  

## RF15 - Gestão de Disponibilidade  
**Descrição:** Gestores podem ativar ou desativar a visibilidade de pratos conforme a disponibilidade de estoque.  
**Prioridade:** Média.  
**Entradas:** Botão de alternância (on/off) no painel administrativo.  
**Saídas:** Remoção/Inclusão imediata do item no menu do cliente.  
**Regras de Negócio:** Pratos desativados não devem aparecer na busca nem nas categorias.  

## RF16 - Edição de Descrição e Valores  
**Descrição:** Permite que o gestor altere textos descritivos e preços dos produtos.  
**Prioridade:** Média.  
**Entradas:** Novos dados inseridos no formulário de edição do prato.  
**Saídas:** Dados atualizados no banco de dados e interface do cliente.  
**Regras de Negócio:** Alterações de preço não afetam pedidos que já foram finalizados/pagos.  

## RF17 - Gestão de Cardápio (Inclusão/Exclusão)  
**Descrição:** Funcionalidade para cadastrar novos pratos ou excluir pratos existentes permanentemente.  
**Prioridade:** Média.  
**Entradas:** Formulário de cadastro (nome, foto, preço, ingredientes).  
**Saídas:** Atualização da estrutura do menu.  
**Regras de Negócio:** A exclusão deve ser lógica (arquivamento) para manter histórico de relatórios antigos.  

## RF18 - Finalização Automática por Pagamento  
**Descrição:** O status do pedido deve mudar automaticamente para “Finalizado” assim que a confirmação do pagamento for recebida.  
**Prioridade:** Alta.  
**Entradas:** Confirmação da API de pagamento ou baixa manual.  
**Saídas:** Status do pedido atualizado para Finalizado.  
**Regras de Negócio:** Somente pedidos com status "Servido" ou conforme regra de fluxo podem ser finalizados via pagamento.  

## RF19 - Relatório Gerencial Mensal  
**Descrição:** Geração de relatório consolidado com: volume de pedidos, popularidade de pratos, avaliações, identificação de pratos de baixa performance (com sugestão de substituição) e receita bruta.  
**Prioridade:** Baixa.  
**Entradas:** Histórico de vendas, avaliações e dados financeiros do mês.  
**Saídas:** Documento (PDF/Painel) com gráficos e dados analíticos.  
**Regras de Negócio:** O sistema deve calcular a porcentagem de cada prato em relação ao total de vendas do período.  

---

##  5. Requisitos Não Funcionais

### 5.1 Usabilidade
**RNF01** - O design deve ser responsivo e compatível com os principais navegadores, garantindo adaptabilidade a diferentes dispositivos.  
**RNF02** - O fluxo de pedido deve ser otimizado para no máximo 4 ações principais: "Selecionar pedido", "Fechar pedido", "Confirmar pedido" e "Efetuar pagamento".  
**RNF03** - Implementar padrões de interface que suportem a navegação fluida em diferentes tamanhos de tela.  

### 5.2 Eficiência
**RNF04** - Tempo de resposta: Carregamento de página em menos de 2 segundos e retorno de busca por pratos em menos de 1 segundo.  
**RNF05** - Suporte a múltiplos usuários: Capacidade de processar múltiplos pedidos simultâneos sem perda de fluidez.    

### 5.3 Desempenho
**RNF06** - Arquitetura capaz de escalar para atender centenas de clientes.  
**RNF07** - Suporte a um aumento de 50% no volume de acesso durante picos de demanda, mantendo a performance estável.  

### 5.4 Espaço
**RNF08** - O sistema deve otimizar o armazenamento de logs e histórico de transações para não comprometer o banco de dados principal.  
**RNF09** - O sistema deve permitir atualizações de cardápio em tempo real sem a necessidade de reiniciar o serviço ou sobrecarregar a memória do servidor.  

### 5.5 Confiabilidade
**RNF10** - O sistema deve garantir uma disponibilidade de 99,9% do tempo.
**RNF11** - Implementar mecanismos de persistência que garantam a integridade dos dados mesmo em eventuais quedas de conexão ou falhas de sistema.

### 5.6 Segurança (Proteção)
**RNF12** - Implementação de controle de acesso restrito a gestores e colaboradores.  
**RNF13** - Criptografia de ponta a ponta em todas as transações  e conformidade com TLS 1.2 ou superior para APIs.  
**RNF14** - Conformidade total com a LGPD e padrões de segurança financeira PCI DSS, com uso de tokenização para dados sensíveis.  
**RNF15** - O sistema deve garantir a segurança no fluxo de pagamento Web-to-Physical: a intenção de pagamento gerada via interface Web (QR Code) deve ser notificada ao terminal Smart POS de forma criptografada. A transação deve ser executada via camada agnóstica, populando o terminal automaticamente e utilizando tokenização para impedir o tráfego ou armazenamento de dados sensíveis no servidor, em conformidade com o PCI DSS.  

---

## 6. Requisitos Organizacionais

### 6.1 Ambientais

SISTEMA OPERACIONAL

- O sistema deve rodar em distribuição Linux (Ubuntu Server).
- O sistema deve implementar tecnologia Docker.
- O sistema deve suportar Android 8.0+ e iOS 14.0+ em dispositivos móveis.
- O sistema deve ter compatibilidade com versões atuais dos principais navegadores, como Chrome e o Safari.

INFRAESTRUTURA

- O sistema deve possuir conectividade via HTTPS com gateways de pagamento.
- O sistema deve garantir a escalabilidade durante os picos de atendimento através do uso de infraestrutura de nuvem.
- O sistema deve manter um banco de dados com base relacional para pedidos e NoSQL para cache de cardápio.


### 6.2 Operacionais

LOGS

- O sistema deve registrar cada etapa do pagamento. Restrição: nunca registrar CVV e senha de cartão.
- O sistema deve registrar quem acessou dados sensíveis ou alterou preços de cardápio no painel administrativo.
- O sistema deve registrar o status do pedido e estipular o tempo de entrega.
- O sistema deve armazenar logs financeiros por pelo menos 5 anos em conformidade fiscal e jurídica.

MONITORAMENTO

- O sistema deve monitorar se os dispositivos (monitor, impressora etc.) da cozinha estão online. Um alerta deve soar se o dispositivo não responder por mais de 30 segundos.
- O sistema deve emitir alertas se o tempo entre o pedido feito no celular do cliente e a aceitação no dispositivo da cozinha for alto demais.
- O sistema deve monitorar a consistência entre o que está no banco de dados e o que aparece no menu. Se um item "esgotado" for pedido, um log de erro crítico deve ser gerado para ajuste imediato.
- O sistema deve monitorar a latência da aplicação para garantir que o cardápio digital não demore a carregar em horários de pico no restaurante.
  
### 6.3 Desenvolvimento

VERSIONAMENTO (GIT)  

- A codificação do sistema deve seguir estrutura ramificada, separando o código principal em branches de incrementações futuras, temporárias e de emergências (em caso de falha na estrutura principal).
- A organização deve padronizar as mensagens utilizando-se de Conventional Commits.
- A organização deve incluir a identificação do requisito em todo commit para que fique claro que mudança de negócio aquele trecho de código representa.
- A organização deve criar tags para o lançamento de versões estáveis contendo o número da versão e a descrição do incremento (Git Tags).
- A organização deve garantir o retorno à versão anterior em segundos caso a versão mais recente apresente erro no cálculo da conta (Rollback rápido).
- A organização deve bloquear commits direto na main.
- A organização deve revisar os códigos através de Pull Requests (PRs).
- A organização deve impedir o commit caso o código esteja fora do padrão.

PADRÃO DE CÓDIGO

- A codificação deve utilizar-se de indentação e espaçamento quando necessário.
- Os nomes de variáveis, funções e comentários devem ser escritos em língua portuguesa.
- A nomenclatura para as variáveis e funções devem ser claras e descritivas.
- A função ou classe deve executar apenas uma tarefa.
- A função deve suceder o comentário que a descreve.

TESTES AUTOMATIZADOS

A organização deve verificar o comportamento do sistema adotando a estratégia da Pirâmide de Testes, o qual consiste em:

- realizar testes unitários para verificar o funcionamento de cada módulo;
- realizar testes de integração a fim de garantir que todos os módulos e serviços estejam funcionando bem em conjunto;
- simular o comportamento do usuário navegando por toda a aplicação (uso de robô).

---

## 7. Requisitos Externos

### 7.1 Reguladores
- LGPD (Lei Geral de Proteção de Dados – Lei nº 13.709/2018): O sistema deve garantir a proteção dos dados pessoais dos usuários, assegurando princípios como privacidade, transparência, consentimento e segurança das informações coletadas e armazenadas.
- Normas específicas de segurança da informação: Devem ser consideradas práticas e normas relacionadas à segurança digital, como controle de acesso, criptografia de dados, autenticação de usuários e prevenção contra vazamento de informações.
- Regulamentações de uso de Inteligência Artificial: O sistema deve seguir diretrizes éticas para utilização de IA, evitando discriminação algorítmica.
- Políticas de conformidade organizacional: A solução deve respeitar as políticas internas da instituição ou empresa onde será implementada, incluindo regras de armazenamento, auditoria e monitoramento de dados.
- Normas técnicas de software e acessibilidade: Sempre que aplicável, o sistema deverá seguir padrões de qualidade de software e acessibilidade digital, garantindo melhor experiência e inclusão dos usuários.

### 7.2 Éticos
-  O sistema deve garantir um atendimento a todo tipo de cliente.
-  O sistema deve coletar unicamente os dados necessários para prestar um bom atendimento ao cliente.
-  O sistema deve ser responsável por erros que não são de controle do cliente.
-  O sistema deve seguir a Lei Geral de Proteção de Dados(LGPD).
-  O sistema deve ter total transparência sobre como utiliza os dados coletados do cliente.

### 7.3 Legais
- A Nota Fiscal de Serviço Eletrônica (NFS-e) deve seguir o padrão nacional.
- Sistemas de emissão devem configurar automaticamente os novos campos para IBS e CBS.
- O pagamento da taxa de 10% (ou similar) deve ser configurado como opcional no checkout da aplicação.
- A plataforma digital deve detalhar de forma visível como o valor pago pelo consumidor é dividido entre o estabelecimento e a plataforma.
- Qualquer cartão de benefício (VA/VR) deve ser aceito em qualquer terminal ou sistema de pagamento devido à nova regra de interoperabilidade do Programa de Alimentação do Trabalhador (PAT). 


### 7.4 Segurança Externa
- O sistema deve possuir proteção contra ataques de força bruta e tentativas de invasão.
- O sistema deve utilizar criptografia para proteger os dados dos clientes e pagamentos.
- O sistema deve realizar autenticação segura para administradores e funcionários.
- O sistema deve possuir proteção contra ataques DDoS (Negação de Serviço Distribuída) e acessos maliciosos.
- O sistema deve monitorar atividades suspeitas em tempo real.
- O sistema deve realizar backups automáticos dos dados do sistema.
- O sistema deve registrar logs de acesso e alterações realizadas na plataforma.
- O sistema deve possuir auditorias periódicas para identificar vulnerabilidades.
- O sistema deve manter atualização constante de segurança contra novas ameaças digitais.
- O sistema deve limitar acessos administrativos apenas a usuários autorizados.
- O sistema deve garantir segurança nas integrações com gateways de pagamento e APIs externas.
- O sistema deve possuir mecanismos de recuperação rápida em caso de falhas ou ataques.

  
### 7.5 Contábeis
- O sistema deve registrar cada transação (Pix, Crédito, Débito) vinculando o ID da transação do Gateway/Adquirente ao pedido interno. Isso é essencial para bater o saldo bancário com as vendas realizadas.  
- Contabilmente, é necessário registrar o valor bruto da venda, a taxa de intermediação (cobrada pelo PSP/Adquirente) e o valor líquido a receber. 
- Diferenciar contabilmente receitas vindas de e-commerce de receitas de lojas físicas. 
- Registro imutável de quem acessou os dados financeiros e quando as transações foram confirmadas via webhooks. 
- O sistema deve fornecer relatórios claros sobre cancelamentos para ajustes de dedução de receita bruta no fechamento contábil.
- Relatórios que prevejam as datas de recebimento (D+0 para Pix, D+30 para crédito, etc.), permitindo o controle de fluxo de caixa e provisionamento contábil.

---

## 8. Arquitetura do Sistema

### 8.1 Visão Geral

A arquitetura desta aplicação prioriza alta velocidade, atualizações em tempo real e tolerância à falhas. Quanto à estrutura do código, recomenda-se organizá-lo em monólito modular para este etapa inicial de pequena escala.

### 8.2 Componentes

FRONTEND

- HTML5/CSS3/JavaScript.
- Linguagem JavaScript/TypeScript.

BACKEND

- NestJS Framework.
- Linguagem JavaScript/TypeScript.
- WebSockets.
- Tokenização.
- Webhooks.

BANCO DE DADOS

- Banco de dados relacional (PostgreSQL).
- NoSQL para cache de cardápio.

APIS EXTERNAS

- APIs RESTful.
- Protocolos de Pagamento.
- TEF ou SDKs.


### 8.3 Tecnologias

- Linguagem JavaScript com sua variante TypeScript.
- NestJS Framework.
- APIs RESTful: Para a comunicação entre o seu servidor e os provedores de pagamento (PSPs).
- WebSockets: Tecnologia usada para a comunicação em tempo real (bidirecional), permitindo que o servidor "avise" instantaneamente a maquininha sobre um novo pagamento.
- Tecnologias Web (HTML5/CSS3/JavaScript): O sistema é disponibilizado via navegador (Web), permitindo o acesso através da leitura de QR Codes nas mesas sem a necessidade de o cliente instalar um aplicativo.
- Protocolos de Pagamento: Integração com PSPs (Payment Service Providers) para processar Pix e Cartões.
- Smart POS (Android): Os terminais físicos que rodam as aplicações de pagamento e interagem com o seu sistema.
- HTTPS / TLS (≥ 1.2): Protocolos de segurança para criptografia de dados em trânsito na internet.
- Tokenização: Tecnologia para substituir dados sensíveis de cartões por chaves aleatórias (tokens).
- Webhooks: Para o recebimento de notificações automáticas de confirmação de pagamento.
- Criptografia de Ponta a Ponta: Garantindo a privacidade desde o celular do cliente até o banco de dados.
- NoSQL para cache de cardápio e um banco de dados relacional para as demais interações, como o (PostgreSQL).

### 8.4 Decisões Arquiteturais

DESEMPENHO

- A aplicação deve utilizar WebSockets para comunicação em tempo real entre clientes, cozinha e painel administrativo, reduzindo atrasos na atualização de pedidos e status.
- O sistema deve utilizar cache NoSQL para armazenar dados frequentes do cardápio, diminuindo o tempo de resposta e reduzindo consultas ao banco relacional.
- A arquitetura deve permitir escalabilidade horizontal e balanceamento de carga, suportando múltiplos acessos simultâneos em horários de pico sem perda de desempenho.
- O backend deve implementar processamento assíncrono para pagamentos, notificações e webhooks, evitando bloqueios no fluxo principal da aplicação.
- O sistema deve monitorar continuamente métricas de desempenho, como latência, uso de recursos e volume de requisições, permitindo ajustes preventivos na infraestrutura.

SEGURANÇA

ESCALABILIDADE

---

## 9. Casos de Uso e Diagramas UML

Esta seção deve representar visualmente e descritivamente o funcionamento do sistema.

Os diagramas ajudam na:
- modelagem do sistema;
- comunicação entre equipe;
- entendimento da arquitetura e funcionalidades;
- documentação técnica do projeto.

---

# 9.1 Casos de Uso

Os casos de uso representam as interações entre usuários (atores) e o sistema.

---

### UC01 - Consultar Cardápio e Buscar Pratos

**Ator:** Cliente.  

**Descrição:**  Permite ao cliente visualizar a tela inicial, navegar por categorias, buscar itens específicos e visualizar detalhes de cada prato.  

---

### Fluxo principal
1. O cliente acessa o menu principal do sistema.  
2. O sistema exibe o catálogo inicial com as sugestões contextuais (ex: "Prato do Dia", "Mais Bem Avaliados").  
3. O cliente seleciona uma categoria (ex: Bebidas, Sobremesas) ou digita um termo na barra de busca.  
4. O sistema exibe a lista filtrada de pratos ativos.  
5. O cliente clica em um prato específico.  
6. O sistema exibe os detalhes: foto em alta resolução, ingredientes, preço e tempo estimado de preparo.  

---

### Fluxo alternativo
- Nenhum resultado na busca: Se o termo digitado não corresponder a nenhum prato, o sistema exibe a mensagem "Nenhum prato encontrado" e sugere retornar ao menu principal.  

---

## Exemplo de Diagrama de Caso de Uso

    [Cliente]
        |
        | ---- (Consultar Cardápio)
        | ---- (Navegar por Categoria)
        | ---- (Visualizar Detalhes do Prato)
        | ---- (Buscar Pratos)

---

### UC02 - Gerenciar Carrinho e Personalizar Itens

**Ator:** Cliente.  

**Descrição:**  Permite ao cliente adicionar itens ao carrinho, ajustar quantidades e personalizar ingredientes.  

---

### Fluxo principal
1. Na tela de detalhes do prato, o cliente ajusta a quantidade desejada através dos botões (+ ou -).  
2. O cliente seleciona os acompanhamentos adicionais ou marca a remoção de ingredientes específicos.  
3. O sistema atualiza o valor total do item dinamicamente com base nas escolhas.  
4. O cliente confirma a adição ao carrinho.  

---

### Fluxo alternativo
- Limite de Estoque/Regra da Casa: Se o cliente tentar incrementar uma quantidade superior ao limite permitido, o sistema bloqueia o avanço e exibe um aviso em tela.  

---

## Exemplo de Diagrama de Caso de Uso

    [Cliente]
        |
        | ---- (Selecionar Quantidade)
        | ---- (Personalizar Acompanhamentos)
        | ---- (Adicionar Item ao Carrinho)

---

### UC03 - Enviar Pedido Parcial

**Ator:** Cliente.  

**Descrição:**  Permite enviar um item selecionado diretamente para a produção na cozinha sem necessidade de fechar a conta inteira.  

---

### Fluxo principal
1. No carrinho ou na tela do item, o cliente aciona a opção "Enviar para Cozinha".  
2. O sistema envia as especificações do prato para o painel da cozinha.  
3. O sistema exibe uma notificação confirmando o envio do item parcial.
4. O sistema inclui este pedido diretamente na comanda, para ser visualizado no pagamento.  

---

### Fluxo alternativo
- Tentativa de Edição: Se o cliente tentar editar um item que já foi enviado para a cozinha, o sistema impede a ação e informa que o item só poderá ser cancelado mediante regra interna da casa.  

---

## Exemplo de Diagrama de Caso de Uso

    [Cliente]
        |
        | ---- (Enviar Pedido Parcial para a Cozinha)
        | ---- (Adicionar pedido a comanda final)

---

### UC04 - Fechar e Confirmar Pedido

**Ator:** Cliente.  

**Descrição:** Apresenta o resumo financeiro e operacional antes de consolidar o pedido na base de dados.   

---

### Fluxo principal
1. O cliente clica em "Ir para o Carrinho" ou "Fechar Pedido".
2. O sistema exibe a lista de itens, o subtotal e o tempo total estimado de entrega (maior tempo entre os pratos selecionados).
3. O cliente clica em "Confirmar Envio".
4. O sistema exibe uma janela de confirmação (pop-up) para evitar cliques acidentais.
5. O cliente confirma a ação.
6. O sistema registra o pedido definitivamente no banco de dados e inicia o processamento. 

---

### Fluxo alternativo
- No passo 4 (exibição do pop-up de confirmação), o cliente decide não enviar o pedido e clica em "Cancelar".
- O sistema fecha a janela flutuante.  
- O sistema mantém o cliente na tela do carrinho, preservando todos os itens e configurações intocados para modificação posterior.  

---

## Exemplo de Diagrama de Caso de Uso

    [Cliente] 
        |
        | ---- (Visualizar Resumo do Pedido)
        | ---- (Fechar Pedido)
        | ---- (Confirmar Envio do Pedido)

---

### UC05 - Acompanhar Status do Pedido

**Ator:** Cliente.

**Descrição:** Permite monitorar o progresso dos pedidos em andamento enquanto mantém a liberdade de realizar novas compras. 

---

### Fluxo principal
1. O cliente acessa a aba "Meus Pedidos".  
2. O sistema exibe os pedidos ativos e seus respectivos status atualizados em tempo real (Recebido, Em Preparo, Pronto, etc.).  
3. O cliente pode alternar para a tela inicial a qualquer momento para abrir um novo pedido simultâneo.  

---

### Fluxo alternativo
- O sistema tenta atualizar o status do pedido em tempo real, mas detecta uma falha de conexão com o servidor.
- O sistema exibe um aviso discreto na tela: "Atualizando status... Verifique sua conexão".
- O sistema exibe a última informação de status salva em cache local.
- Assim que a conexão é restabelecida, o status é sincronizado automaticamente com a cozinha. 

---

## Exemplo de Diagrama de Caso de Uso

    [Cliente]
        |
        | ---- (Visualizar Progresso de Pedidos Ativos)
        | ---- (Iniciar Novo Pedido Simultâneo)

---

### UC06 - Realizar Pagamento

**Ator:** Cliente e Sistema de Pagamento (API).

**Descrição:** Processa a cobrança do pedido através da modalidade escolhida e finaliza o fluxo comercial.

---

### Fluxo principal
1. O cliente seleciona a forma de pagamento (Pix, Cartão de Crédito/Débito, Carteira Digital ou Vale Refeição).
2. O sistema gera as credenciais (como o QR Code Pix) ou faz a interface com a maquininha/integração de terminal POS.  
3. O Sistema de Pagamento processa a transação e envia o retorno de sucesso.  
4. O sistema valida se o status operacional do pedido é "Servido".  
5. O sistema altera automaticamente o status do pedido para “Finalizado” e emite o comprovante na tela.  

---

### Fluxo alternativo
- No passo 3, o Sistema de Pagamento (API) retorna um erro (ex: saldo insuficiente, cartão bloqueado ou timeout do Pix).  
- O sistema notifica o cliente sobre o motivo da recusa.  
- O sistema permite que o cliente selecione uma nova modalidade de pagamento (ex: trocar de cartão ou mudar para Pix) e reinicie o processo a partir do passo 1.
- No passo 4, o sistema valida que o pedido atual ainda não atingiu o status operacional "Servido" (conforme a regra de fluxo da casa).
- O sistema impede a finalização automática e exibe um alerta ao operador ou ao cliente: "Este pedido ainda está em preparação e não pode ser finalizado".

---

## Exemplo de Diagrama de Caso de Uso

    [Cliente]    
        |
        | ---- (Selecionar Forma de Pagamento)
        | ---- (Efetuar Pagamento)

    [Sistema de Pagamento (API)]
              |
              | ---- (Processar Transação Financeira)
              | ---- (Confirmar Pagamento)

---

### UC07 - Monitorar Pedidos em Tempo Real

**Ator:** Gestor.

**Descrição:** Disponibiliza uma tela de gerenciamento centralizado para visualização imediata do fluxo do estabelecimento.  

---

### Fluxo principal
1. O Gestor acessa o Dashboard Administrativo.
2. O sistema exibe, com baixa latência, todos os pedidos ativos, seus respectivos tempos de espera e status atuais.

---

### Fluxo alternativo
- O sistema detecta que o fluxo de dados em tempo real com a cozinha/mesas sofreu uma interrupção.
- O painel do Gestor exibe um alerta visual indicando que os dados podem estar desatualizados.
- O sistema disponibiliza um botão de "Forçar Atualização Manual" para tentar restabelecer o canal de baixa latência imediatamente. 

---

## Exemplo de Diagrama de Caso de Uso

    [Gestor]
        |
        | ---- (Acessar Dashboard)
        | ---- (Visualizar Pedidos Ativos e Tempos de Espera)

---

### UC08 - Alterar Status Operacional

**Ator:** Operador (Cozinha/Garçom) ou Gestor

**Descrição:** Permite atualizar a situação física do pedido na linha de produção e atendimento.  

---

### Fluxo principal
1. O operador visualiza o pedido no painel operacional.
2. A Cozinha altera o status para “Em andamento” e posteriormente para “Pronto para servir”.
3. O Garçom altera o status para “Servido” ao entregar o prato na mesa.
4. O sistema dispara notificações automáticas de atualização para o cliente e para o painel do gestor.

---

### Fluxo alternativo
- No passo 2 ou 3, o operador tenta mudar o status de um pedido pulando etapas (ex: tentar mudar de "Recebido" direto para "Servido", sem passar por "Em andamento" ou "Pronto").
- O sistema bloqueia a alteração.
- O sistema exibe uma mensagem de erro na tela operacional informando que a sequência cronológica dos status deve ser respeitada. 

---

## Exemplo de Diagrama de Caso de Uso

    [Operador (Cozinha/Garçom)]
              |
              | ---- (Alterar Status para "Em Andamento")
              | ---- (Alterar Status para "Pronto para Servir")
              | ---- (Alterar Status para "Servido")

    [Gestor]
        |
        | ---- (Monitorar Alterações de Status Operacional)

---

### UC09 - Gerenciar Disponibilidade de Itens

**Ator:** Gestor.

**Descrição:** Permite ocultar ou reexibir pratos no cardápio do cliente com base no estoque de insumos.

---

### Fluxo principal
1. O Gestor acessa a lista de produtos no painel administrativo.
2. O Gestor altera a chave de visibilidade (on/off) de um prato específico.
3. O sistema remove ou inclui imediatamente o item do cardápio visualizado pelo cliente, bloqueando-o também nas buscas.

---

### Fluxo alternativo
- No passo 2, o Gestor altera a chave para off (desativado) de um prato que possui unidades em preparação na cozinha naquele exato momento.  
- O sistema remove o item imediatamente para novas buscas e compras dos clientes.  
- O sistema emite um aviso ao Gestor: "O prato foi ocultado do cardápio. Nota: Existem [X] pedidos ativos deste item que continuarão em produção até a entrega."  

---

## Exemplo de Diagrama de Caso de Uso

    [Gestor]
        |
        | ---- (Ativar Visibilidade de Prato)
        | ---- (Desativar Visibilidade de Prato)

---

### UC10 - Manter Itens do Cardápio

**Ator:** Gestor.

**Descrição:** grupa as operações de cadastro, edição de valores/descrições e arquivamento de pratos. 

---

### Fluxo principal
1. O Gestor preenche o formulário com nome, foto, preço, ingredientes e submete.  
2. O sistema valida e inclui o novo item na estrutura do menu.  

---

### Fluxo alternativo
- O Gestor altera o valor de um prato existente.  
- O sistema atualiza o banco de dados. Os pedidos anteriores já finalizados mantêm seus valores históricos inalterados.  
- O Gestor solicita a exclusão de um prato.  
- O sistema realiza uma exclusão lógica (arquivamento), mantendo o prato oculto para o cliente, mas preservando seus dados para estatísticas de relatórios passados.  

---

## Exemplo de Diagrama de Caso de Uso

    [Gestor]
        |
        | ---- (Cadastrar Novo Prato)
        | ---- (Editar Descrição e Valores)
        | ---- (Excluir Prato Permanentemente)

---

### UC11 - Gerar Relatório Gerencial Mensal

**Ator:** Gestor.

**Descrição:** Consolida os dados financeiros e operacionais do mês para suporte à tomada de decisões.

---

### Fluxo principal
1. O Gestor solicita o fechamento do mês na aba de relatórios.
2. O sistema compila o histórico de vendas, avaliações e receitas.
3. O sistema calcula a porcentagem de saída de cada prato em relação ao volume total.
4. O sistema gera um documento analítico estruturado com gráficos, destacando pratos de alta performance e indicando sugestões de substituição para os de baixa performance.

---

### Fluxo alternativo
- No passo 1, o Gestor solicita o relatório de um mês específico em que o sistema ficou inativo ou não houve movimentação comercial registrada.
- O sistema interrompe o processamento do relatório.
- O sistema exibe a mensagem: "Não foram encontrados registros financeiros ou de vendas para o período selecionado".
- O sistema retorna o Gestor para a tela de seleção de datas.

---

## Exemplo de Diagrama de Caso de Uso

    [Gestor]
        |
        | ---- (Solicitar Relatório Consolidado)
        | ---- (Visualizar Gráficos e Dados Analíticos)

---

## 9.2 Diagrama de Classes (UML)

O diagrama de classes representa:

- estrutura do sistema;
- entidades;
- atributos;
- métodos;
- relacionamentos.

---

### Exemplo

```text
+------------------+
|     Usuário      |
+------------------+
| - id             |
| - nome           |
| - email          |
| - senha          |
+------------------+
| + login()        |
| + logout()       |
+------------------+
```

---

### Exemplo com relacionamento

```text
+------------------+        +------------------+
|     Usuário      | 1    * |      Pedido      |
+------------------+--------+------------------+
| id               |        | id               |
| nome             |        | valor            |
+------------------+        +------------------+
```

---

## 9.3 Diagrama de Atividades (UML)

Representa o fluxo de execução de processos no sistema.

---

## 1. Fluxo do Cliente

### 1.1 Navegação, Personalização e Montagem do Carrinho

![Diagrama](https://github.com/thiagocaixeta01/software-engineering-foundations-project-lab/blob/f5cc90efdeda1be6b862e142b61343b9648a2dfc/groups/group-02/Fluxo%20Do%20Cliente%20-%20Navega%C3%A7%C3%A3o%2C%20Personaliza%C3%A7%C3%A3o%20e%20Montagem%20do%20Carrinho%20(Com%20Fundo).png)

### 1.2 Envio e Fechamento de Pedido

![Diagrama](https://github.com/thiagocaixeta01/software-engineering-foundations-project-lab/blob/b2c4413e271b380fb2bad0f0bf75dacc3efcc8cd/groups/group-02/Fluxo%20Do%20Cliente%20-%20Envio%20e%20Fechamento%20de%20Pedido.png)

### 1.3 Acompanhamento e Pagamento 

![Diagrama](https://github.com/thiagocaixeta01/software-engineering-foundations-project-lab/blob/758450a0af683d6f51a7395592d34f8bd577977e/groups/group-02/Fluxo%20Do%20Cliente%20-%20Acompanhamento%20e%20Pagamento.png)

---

## 2. Fluxo Operacional

### 2.1 Ciclo de Vida do Pedido na Cozinha/Salão

![Diagrama](https://github.com/thiagocaixeta01/software-engineering-foundations-project-lab/blob/4ef46d59206acf66e1191a99438776d671614901/groups/group-02/Fluxo%20Operacional%20(Cozinha%20e%20Gar%C3%A7om).png)

---

## 3. Fluxos Administrativos (Gestor) 

### 3.1 Gestão de Cardápio e Disponibilidade de Estoque

![Diagrama]()


### 3.2 Geração de Relatório Gerencial Mensal

![Diagrama]()

---

## 9.4 Diagrama de Sequência (UML)

Representa a comunicação entre objetos ao longo do tempo.

---

### Exemplo

```text
Usuário -> Sistema: realizar login
Sistema -> Banco: validar usuário
Banco -> Sistema: usuário válido
Sistema -> Usuário: acesso liberado
```

---

## 9.5 Diagrama de Componentes

Representa os módulos e componentes principais do sistema.

---

### Exemplo

```text
[Frontend]
     |
     v
[API Backend]
     |
     v
[Banco de Dados]
```

---

## 9.6 Diagrama de Implantação (Deployment)

Representa onde o sistema será executado.

---

### Exemplo

```text
[Usuário]
     |
Internet
     |
[Servidor Web]
     |
[Servidor Banco de Dados]
```

---

## 9.7 Ferramentas Recomendadas

Os diagramas podem ser feitos utilizando:

- Draw.io
- Lucidchart
- StarUML
- Visual Paradigm
- PlantUML
- Mermaid
- Figma

---

## 9.8 Observações Importantes

- Os diagramas devem representar o sistema REAL do grupo;
- Evitem diagramas genéricos;
- Mantenham consistência entre requisitos e diagramas;
- Diagramas devem possuir nomes claros;
- Atualizem os diagramas conforme o sistema evoluir.

---

# Regra importante

> “Diagramas não são apenas desenhos: eles representam decisões arquiteturais e técnicas do sistema.”

---

##  10. Plano de Testes

### 10.1 Estratégia de Teste
Como o sistema será testado?

### 10.2 Tipos de Teste
- Unitário  
- Integração  
- Sistema  
- Aceitação  

### 10.3 Casos de Teste

#### CT01 - Nome
**Requisito relacionado:** RF01  
**Descrição:**  
**Entrada:**  
**Resultado esperado:**  

---

### 10.4 Testes de Requisitos Não Funcionais
- Performance (tempo de resposta)  
- Segurança  
- Usabilidade  

---

##  11. Critérios de Aceitação

Defina como validar os requisitos:
- Métricas  
- Testes  
- Condições de sucesso  

---

##  12. Restrições

- O sistema deve ser desenvolvido utilizando-se tecnologia web responsiva.  
- O sistema deve rodar nos principais navegadores (Chrome, Firefox, Safari, Edge).  
- O projeto deve ser entregue em até 6 meses.  
- O sistema deve realizar integrações com Payment Service Providers (PSPs) exclusivamente via APIs RESTful sobre HTTPS com TLS 1.2 ou superior.  
- O projeto deve implementar uma camada de abstração agnóstica para hardware, permitindo a comunicação com diferentes adquirentes e modelos de Smart POS via TEF ou SDKs.  
- O sistema deve utilizar obrigatoriamente comunicação via HTTP Local ou WebSockets para o envio de valores aos terminais, vedando a digitação manual.  
- O sistema deve processar pagamentos via Pix, cartões e carteiras digitais utilizando obrigatoriamente tokenização, sendo proibido o armazenamento de dados sensíveis de pagamento em servidores próprios.  
- O sistema deve garantir que o tempo de carregamento de qualquer página web seja inferior a 2 segundos.  
- O projeto deve assegurar que o motor de busca de pratos retorne resultados em menos de 1 segundo.  
- O sistema deve suportar a carga simultânea de até 1.000 usuários ativos sem perda de fluidez.
- O projeto deve manter uma disponibilidade mínima de 99,9% (Uptime).  
- O sistema deve criptografar toda a comunicação cliente-servidor através do protocolo HTTPS.  
- O projeto deve estar em conformidade estrita com a LGPD, informando a finalidade da coleta de dados e permitindo a exclusão dos mesmos mediante solicitação do usuário.    

---

##  13. Premissas

- Pressupõe-se que os usuários possuam seus smartphones.
- Pressupõe-se que os funcionários e gestores do estabelecimento tenham acesso ao sistema via smartphone, tablet, notebook ou desktop.
- Assume-se que funcionários e gestores possuam cadastro no banco de dados do sistema para realizar-se às autenticações.
- Exige-se que o estabelecimento tenha acesso a internet.
- Exige-se que os usuários tenham acesso à internet.
- Exige-se que todos os dispositivos eletrônicos/digitais do estabelecimento estejam conectados à internet.
- Assume-se que todas as mesas possuam QR Code do endereço da aplicação web e estejam devidamente sinalizadas.
- Assume-se que o estabelecimento possua maquininha de pagamentos.
- Assume-se que o usuário final possui um dispositivo com acesso estável à internet e um navegador moderno (Chrome, Safari, Edge ou Firefox) para garantir a performance de carregamento prevista.
- Pressupõe-se que os estabelecimentos utilizem terminais Smart POS ou hardware de rede compatíveis com os protocolos HTTP Local ou WebSockets para a automação física.
- Exige-se que o provedor de infraestrutura (Cloud/Servidor) suporte escalabilidade horizontal para absorver picos de 50% de demanda sem degradação de performance.
- Considera-se que o gateway de pagamento (PSP) escolhido ofereça suporte nativo a Webhooks e APIs baseadas em REST com certificação PCI DSS.  
- Assume-se que os gestores e a equipe da cozinha possuam treinamento básico para operar a interface administrativa e atualizar o status dos pedidos em tempo real.  
- Pressupõe-se que a base de dados de pratos e categorias já contenha imagens e descrições otimizadas para garantir o tempo de resposta nas buscas. 

---

# 14. Observações Finais


---
