#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução
A busca por agilidade no atendimento tornou-se um dos principais critérios na hora de escolher uma experiência gastronômica. A fim de proporcionar aos clientes uma visita agradável e atender habilmente a demanda de pedidos, muitos restaurantes e lanchonetes automatizaram seus serviços através de cardápio e formas de pagamento digitais.

### 1.1 Objetivo 
Este documento tem como objetivo principal, conter informações primordiais de todas as etapas do desenvolvimento da engenharia de requisitos do projeto proposto. Este projeto tem como foco principal, reduzir o tempo de atendimento e dar mais flexibilidade para clientes em suas escolhas do menu, automatizando o atendimento ao cliente com uma aplicação web à disposição dos usuários. 



### 1.2 Escopo
O sistema incorpora a automação dos serviços prestados por restaurantes e lanchonetes, de forma que os clientes realizem seus próprios pedidos e efetuem os pagamentos de forma rápida e simples; auxilia também a equipe operacional no preparo e na entrega dos pedidos, assim como, os gerentes e proprietários na administração do negócio.


### 1.3 Definições, Acrônimos e Abreviações
RF - Requisitos Funcionais.  
RNF - Requisitos não funcionais.

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
Porque aumenta a produtividade do estabelecimento, pois os pedidos são feitos mais rápidos e sem erros de comunicação. Otimiza o tempo que o cliente leva para fazer seus pedidos e mantém um ambiente organizado e bem estruturado.


### 2.5 Diferencial
O que torna esse sistema melhor que outros?

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
**Descrição:** Fluxo de alteração de status: Cozinha muda para “Em andamento”/“Pronto para servir” e Garçom muda para “Servido”.
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
- Interface intuitiva: O design deve ser responsivo e compatível com os principais navegadores, garantindo adaptabilidade a diferentes dispositivos.
- Tempo de aprendizado: O fluxo de pedido deve ser otimizado para no máximo 4 ações principais: "Selecionar pedido", "Fechar pedido", "Confirmar pedido" e "Efetuar pagamento".
- Acessibilidade: Implementar padrões de interface que suportem a navegação fluida em diferentes tamanhos de tela.

### 5.2 Eficiência
- Tempo de resposta: Carregamento de página em menos de 2 segundos e retorno de busca por pratos em menos de 1 segundo.
- Suporte a múltiplos usuários: Capacidade de processar múltiplos pedidos simultâneos sem perda de fluidez.  

### 5.3 Desempenho
- Suporte a usuários simultâneos: Arquitetura capaz de escalar para atender centenas de clientes.
- Estabilidade sob carga: Suporte a um aumento de 50% no volume de acesso durante picos de demanda, mantendo a performance estável.

### 5.4 Espaço
- Limite de armazenamento: O sistema deve otimizar o armazenamento de logs e histórico de transações para não comprometer o banco de dados principal.
- Uso eficiente de memória: O sistema deve permitir atualizações de cardápio em tempo real sem a necessidade de reiniciar o serviço ou sobrecarregar a memória do servidor.

### 5.5 Confiabilidade
- Disponibilidade mínima: O sistema deve garantir uma disponibilidade de 99,9% do tempo.
- Recuperação de falhas: Implementar mecanismos de persistência que garantam a integridade dos dados mesmo em eventuais quedas de conexão ou falhas de sistema.

### 5.6 Segurança (Proteção)
- Autenticação e Controle de Acesso: Implementação de controle de acesso restrito a gestores e colaboradores.
- Criptografia: Criptografia de ponta a ponta em todas as transações  e conformidade com TLS 1.2 ou superior para APIs.
- Privacidade e Conformidade: Conformidade total com a LGPD e padrões de segurança financeira PCI DSS, com uso de tokenização para dados sensíveis.
- Interoperabilidade Segura: Integração com PSPs via webhooks e automação de terminais físicos (Smart POS) via camadas de abstração agnósticas, garantindo que nenhum dado sensível trafegue ou seja armazenado de forma insegura no servidor.
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
- LGPD (Lei Geral de Proteção de Dados – Lei nº 13.709/2018)
O sistema deve garantir a proteção dos dados pessoais dos usuários, assegurando princípios como privacidade, transparência, consentimento e segurança das informações coletadas e armazenadas.
- Normas específicas de segurança da informação
Devem ser consideradas práticas e normas relacionadas à segurança digital, como controle de acesso, criptografia de dados, autenticação de usuários e prevenção contra vazamento de informações.
- Regulamentações de uso de Inteligência Artificial
O sistema deve seguir diretrizes éticas para utilização de IA, evitando discriminação algorítmica.
- Políticas de conformidade organizacional
A solução deve respeitar as políticas internas da instituição ou empresa onde será implementada, incluindo regras de armazenamento, auditoria e monitoramento de dados.
- Normas técnicas de software e acessibilidade
Sempre que aplicável, o sistema deverá seguir padrões de qualidade de software e acessibilidade digital, garantindo melhor experiência e inclusão dos usuários.

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
- Diferenciar contabilmente receitas vindas de e-commerce (NFR06) de receitas de lojas físicas (NFR07). 
- Registro imutável de quem acessou os dados financeiros e quando as transações foram confirmadas via webhooks. 
- O sistema deve fornecer relatórios claros sobre cancelamentos para ajustes de dedução de receita bruta no fechamento contábil.
- Relatórios que prevejam as datas de recebimento (D+0 para Pix, D+30 para crédito, etc.), permitindo o controle de fluxo de caixa e provisionamento contábil.
