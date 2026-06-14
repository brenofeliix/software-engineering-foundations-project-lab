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
- Interface intuitiva  
- Tempo de aprendizado < X minutos  
- Acessibilidade  

### 5.2 Eficiência
- Tempo de resposta < X segundos  
- Suporte a múltiplos usuários  

### 5.3 Desempenho
- Suporte a X usuários simultâneos  
- Estabilidade sob carga  

### 5.4 Espaço
- Limite de armazenamento  
- Uso eficiente de memória  

### 5.5 Confiabilidade
- Disponibilidade mínima (ex: 99,9%)  
- Recuperação de falhas  

### 5.6 Segurança (Proteção)
- Autenticação  
- Criptografia  
- Controle de acesso  

---

##  6. Requisitos Organizacionais

### 6.1 Ambientais
- Sistema operacional  
- Infraestrutura  

### 6.2 Operacionais
- Logs  
- Monitoramento  

### 6.3 Desenvolvimento
- Versionamento (Git)  
- Padrões de código  
- Testes automatizados  

---

##  7. Requisitos Externos

### 7.1 Reguladores
- LGPD  
- Normas específicas  

### 7.2 Éticos
- Não discriminação  
- Transparência  

### 7.3 Legais
- Leis aplicáveis  

### 7.4 Segurança Externa
- Proteção contra ataques  
- Auditorias  

### 7.5 Contábeis
- Registro de transações  
- Relatórios  

---

##  8. Arquitetura do Sistema

### 8.1 Visão Geral
Descreva a arquitetura (ex: monolito, microserviços).

### 8.2 Componentes
- Frontend  
- Backend  
- Banco de dados  
- APIs externas  

### 8.3 Tecnologias
- Linguagem  
- Framework  
- Banco de dados  

### 8.4 Decisões Arquiteturais
Explique como a arquitetura atende aos requisitos não funcionais:
- Desempenho  
- Segurança  
- Escalabilidade  

---

##  9. Casos de Uso

### UC01 - Nome do caso de uso
**Ator:**  
**Descrição:**  
**Fluxo principal:**  
**Fluxo alternativo:**  

---

##  10. Plano de Testes

### 10.1 Estratégia de Teste
O sistema será testado em diferentes níveis para garantir o correto funcionamento das funcionalidades do minimercado. Inicialmente serão realizados testes unitários nos módulos individuais, como cadastro de usuários, leitura de produtos, cálculo do valor total e processamento de pagamento. Em seguida, serão realizados testes de integração para verificar a comunicação entre o sistema de self-checkout e o sistema administrador. Posteriormente, serão executados testes de sistema para validar o funcionamento completo da aplicação e, por fim, testes de aceitação com usuários finais para confirmar se o sistema atende às necessidades estabelecidas nos requisitos.

### 10.2 Tipos de Teste
- Unitário: Testa individualmente cada funcionalidade do sistema, como validação de e-mail institucional, leitura de código de barras, cálculo do valor total e envio de comprovante.
- Integração: Verifica a comunicação entre os módulos do sistema, como a sincronização dos produtos entre o self-checkout e o sistema administrador, atualização do estoque e confirmação de pagamentos.
- Sistema: Avalia o sistema completo em ambiente de testes, garantindo que todas as funcionalidades funcionem em conjunto conforme os requisitos definidos.  
- Aceitação: Realizado com usuários finais para validar a usabilidade do sistema e confirmar se o processo de compra ocorre corretamente, desde o cadastro até o recebimento do comprovante digital. 

### 10.3 Casos de Teste
#### CT01 – Cadastro de usuário com e-mail institucional válido  
**Requisito relacionado:** RF01  
**Descrição:** Verificar se o sistema realiza o cadastro de usuários utilizando um e-mail institucional válido.  
**Entrada:**  
Nome: João Silva  
E-mail: joao@instituicao.edu.br  
Senha: 123456  
**Resultado esperado:** O sistema deve cadastrar o usuário com sucesso e exibir uma mensagem de confirmação.  

#### CT02 – Leitura de produto por código de barras  
**Requisito relacionado:** RF02  
**Descrição:** Verificar se o sistema identifica corretamente um produto por meio do código de barras dentro do tempo máximo permitido.  
**Entrada:**  
Código de barras do produto cadastrado.  
**Resultado esperado:** O sistema deve exibir o nome do produto, valor e quantidade disponível em até 2 segundos.  

#### CT03 – Atualização automática do valor total da compra  
**Requisito relacionado:** RF03  
**Descrição:** Verificar se o valor total da compra é atualizado automaticamente conforme novos produtos são adicionados ao carrinho.  
**Entrada:**  
Adição de produtos ao carrinho de compras.  
**Resultado esperado:** O sistema deve recalcular e exibir automaticamente o novo valor total da compra.  

#### CT04 – Processamento de pagamento digital  
**Requisito relacionado:** RF04  
**Descrição:** Verificar se o sistema processa corretamente pagamentos via PIX ou cartão garantindo a segurança dos dados.  
**Entrada:**  
Dados da transação.  
Método de pagamento selecionado (PIX ou cartão).  
**Resultado esperado:** O pagamento deve ser processado com sucesso, retornando uma confirmação da transação e mantendo os dados financeiros protegidos por criptografia.  

#### CT05 – Envio de comprovante digital  
**Requisito relacionado:** RF05  
**Descrição:** Verificar se o sistema envia corretamente o comprovante digital após a conclusão da compra.  
**Entrada:**  
Dados da compra realizada.  
E-mail do usuário.  
**Resultado esperado:** O usuário deve receber um comprovante digital contendo os produtos comprados, data da transação e valor total da compra.  

---

### 10.4 Testes de Requisitos Não Funcionais
- Usabilidade: Avaliar a facilidade de utilização da interface do self-checkout e do sistema administrador, verificando clareza dos comandos, tempo de aprendizado e recursos de acessibilidade.
- Eficiência: Verificar se o sistema mantém um bom tempo de resposta e suporta diversos usuários realizando compras ao mesmo tempo.
- Desempenho: Testar o funcionamento do sistema sob carga elevada, garantindo que não ocorram falhas ou travamentos durante períodos de maior utilização.
- Espaço: Validar se o sistema utiliza os recursos de armazenamento e memória de forma eficiente, evitando consumo excessivo e garantindo o armazenamento adequado dos dados de usuários, produtos e transações.
- Confiabilidade: Verificar a disponibilidade do sistema, a recuperação em caso de falhas e a integridade dos dados após interrupções ou erros inesperados.
- Segurança (Proteção): Testar os mecanismos de autenticação de usuários, criptografia de dados financeiros, validação de acessos e permissões entre usuários e administradores do sistema.

---

##  11. Critérios de Aceitação

Defina como validar os requisitos:
- Métricas  
- Testes  
- Condições de sucesso  

---

##  12. Restrições

- Tecnológicas  
- Legais  
- De prazo  

---

##  13. Premissas

- Usuário terá acesso à internet  
- Sistema será usado em dispositivos móveis  

---

##  14. Observações Finais

Informações adicionais relevantes.

---

#  Orientações importantes

- Requisitos devem ser claros, específicos e mensuráveis  
- Evite termos vagos como “rápido” ou “bom”  
- Requisitos não funcionais são obrigatórios  
- A arquitetura deve responder aos requisitos  
- Todo requisito deve ser testável  

---

# Regra de ouro

> Se não pode ser testado, não é um bom requisito.
