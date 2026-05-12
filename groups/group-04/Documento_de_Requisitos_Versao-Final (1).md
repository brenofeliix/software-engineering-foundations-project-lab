#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
Este documento tem como objetivo descrever de forma estruturada os requisitos do sistema de plataforma digital para o Restaurante Universitário (RU) da Universidade Federal de Rondonópolis (UFR), o PODE PAPAR. Ele serve como base para o desenvolvimento, testes e validação do software, garantindo alinhamento entre a equipe técnica, os usuários finais e os gestores do RU.
O sistema visa digitalizar e modernizar o processo de gestão e uso do RU, eliminando os gargalos logísticos do modelo presencial atual por meio de uma plataforma modular, desacoplada e escalável.


### 1.2 Escopo

O sistema contempla:

- Autenticação de usuários institucionais via SUAP  
- Consulta de saldo e histórico de recargas em tempo real  
- Recarga de créditos via Pix  
- Visualização do cardápio semanal  
- Registro e consulta de check-ins  
- Envio de notificações e comunicados  
- Feedback sobre refeições  
- Painel administrativo para gestão operacional do RU  
- Geração de relatórios visuais com gráficos e indicadores  
- Integração com APIs externas  

#### Fora do escopo:

- Controle físico de acesso (catracas e reconhecimento facial) — responsabilidade do sistema existente do RU  
- Manutenção técnica da infraestrutura — responsabilidade exclusiva da equipe desenvolvedora  
- Integração com sistemas de folha de pagamento ou ERP institucional  


### 1.3 Definições, Acrônimos e Abreviações
### Glossário

| Termo | Definição |
|------|----------|
| UFR | Universidade Federal de Rondonópolis |
| RU | Restaurante Universitário |
| API | Application Programming Interface — conjunto de normas que permite a comunicação entre o sistema e outras aplicações |
| Arquitetura Desacoplada | Modelo em que o front-end (interface) e o back-end (servidor) funcionam de forma independente |
| Pix | Sistema de pagamentos instantâneos criado pelo Banco Central do Brasil |
| PROAE | Pró-Reitoria de Assistência Estudantil |
| Stakeholders | Partes interessadas ou entidades afetadas pelo projeto |
| UX | User Experience — foco em tornar a navegação simples, intuitiva e eficiente |
---

##  2. Product Vision

### 2.1 Problema
A Universidade Federal de Rondonópolis (UFR) disponibiliza à comunidade acadêmica o Restaurante Universitário (RU), responsável por atender estudantes e servidores em suas refeições diárias. Trata-se de um serviço essencial para a permanência estudantil, oferecendo refeições a preços acessíveis por meio de um sistema de créditos pré-pagos realizado de forma presencial.

Entretanto, o modelo atual apresenta limitações significativas, como:
- Cadastro realizado exclusivamente de forma presencial
- Dificuldade de acesso ao cardápio atualizado
- Ausência de uma interface para consulta de saldo e recarga remota

Esses fatores geram filas, lentidão no atendimento e perda de tempo produtivo, evidenciando a necessidade de uma solução digital que otimize esse processo.

---

### 2.2 Solução
Propõe-se o desenvolvimento de um sistema digital integrado ao SUAP, que permitirá:
- Cadastro online de usuários  
- Consulta de saldo em tempo real  
- Recarga de créditos via Pix ou cartão de crédito  
- Acesso ao cardápio semanal atualizado  

O sistema busca melhorar a experiência dos usuários ao eliminar a necessidade de deslocamento para tarefas administrativas, reduzindo filas e proporcionando maior controle financeiro sobre o uso do RU.

---

### 2.3 Público-Alvo
- Estudantes matriculados na UFR com acesso ao SUAP  
- Servidores públicos da UFR

---

### 2.4 Proposta de Valor
A proposta de valor está centrada na otimização do tempo e na digitalização dos serviços do Restaurante Universitário.
O sistema elimina a necessidade de processos presenciais para atividades administrativas, tornando o acesso ao RU mais ágil e eficiente.

O projeto se fundamenta em três pilares:
- *Permanência Estudantil:* Redução de filas e melhor aproveitamento do tempo acadêmico  
- *Eficiência Operacional:* Diminuição da carga de trabalho manual no atendimento físico  
- *Modernização Institucional:* Uso de tecnologia para aprimorar serviços e processos internos

---

### 2.5 Diferencial
- *Arquitetura Desacoplada (API-First):* Permite integração e evolução do sistema sem necessidade de reestruturação completa
- *Foco na Experiência do Usuário (UX):* Interface simples, intuitiva e adaptada às necessidades da comunidade acadêmica
- *Centralização de Informações:* Reúne saldo, cardápio e comunicados em um único ambiente digital

---

### 2.6 Funcionalidades principais (alto nível)
- *Gestão de Carteira Digital:* Consulta de saldo em tempo real  
- *Recarga Remota:* Compra de créditos via Pix ou cartão de crédito  
- *Consulta de Cardápio e Avisos:* Visualização de refeições e recebimento de notificações  
- *Autenticação e Cadastro Digital:* Login integrado e pré-cadastro online  
- *API de Gerenciamento:* Painel administrativo com relatórios e controle operacional

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
