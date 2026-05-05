#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
Descrever o objetivo deste documento e do sistema.

### 1.2 Escopo
Descrever o que o sistema faz, seus limites e o que está fora do escopo.

### 1.3 Definições, Acrônimos e Abreviações
Liste termos importantes utilizados no documento.

---

##  2. Product Vision

### 2.1 Problema
Qual problema o sistema resolve?

### 2.2 Solução
Descreva a solução proposta.

### 2.3 Público-Alvo
Quem utilizará o sistema?

### 2.4 Proposta de Valor
Por que esse sistema é importante?

### 2.5 Diferencial
O que torna esse sistema melhor que outros?

### 2.6 Funcionalidades principais (alto nível)
- Funcionalidade 1
- Funcionalidade 2

---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
Explique o sistema de forma resumida.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais

### RF01 - Nome do requisito
**Descrição:**  
Descreva a funcionalidade.

**Prioridade:** Alta / Média / Baixa  
**Entradas:**  
**Saídas:**  
**Regras de negócio:**  

---

### RF02 - Nome do requisito
(repita o padrão)

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

6. Requisitos Organizacionais

6.1 Ambientais

SISTEMA OPERACIONAL

- O sistema deve rodar em distribuição Linux (Ubuntu Server).
- O sistema deve implementar tecnologia Docker.
- O sistema deve suportar Android 8.0+ e iOS 14.0+ em dispositivos móveis.
- O sistema deve ter compatibilidade com versões atuais dos principais navegadores, como Chrome e o Safari.

INFRAESTRUTURA

- O sistema deve possuir conectividade via HTTPS com gateways de pagamento.
- O sistema deve garantir a escalabilidade durante os picos de atendimento através do uso de infraestrutura de nuvem.
- O sistema deve manter um banco de dados com base relacional para pedidos e NoSQL para cache de cardápio.


6.2 Operacionais

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

