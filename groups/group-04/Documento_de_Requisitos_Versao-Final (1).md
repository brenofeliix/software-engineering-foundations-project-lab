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
O PODE PAPAR é uma plataforma digital modular e desacoplada desenvolvida para modernizar os serviços do Restaurante Universitário da UFR. O sistema é estruturado em dois módulos independentes que se comunicam via API REST:

#### Módulo de Interface (Frontend PWA)

O Módulo de Interface (Frontend PWA) é a camada voltada ao usuário final, acessível via navegador ou instalável como aplicativo em dispositivos móveis. Por meio dele, estudantes e servidores podem realizar login via SUAP, consultar saldo, visualizar o cardápio semanal, recarregar créditos via Pix ou cartão de crédito, acessar histórico de recargas e check-ins, e receber notificações do RU.

#### Módulo Gerenciador (Backend + Painel Administrativo)

O Módulo Gerenciador (Backend + Painel Administrativo) é a camada de gestão operacional, destinada aos administradores e operadores do RU. Permite o gerenciamento de usuários, créditos, cardápio e a geração de relatórios visuais, sem exigir conhecimento técnico do operador.

--

Essa separação garante flexibilidade de implantação: no caso da UFR, o frontend pode ser integrado via API ao sistema já existente do RU; em outras instituições sem sistema próprio, o pacote completo pode ser implantado.

### 3.2 Stakeholders
### Stakeholders

| Papel | Descrição |
|------|----------|
| Estudantes e Servidores da UFR | Usuários finais do sistema, beneficiados pela digitalização do processo |
| Gestão do RU da UFR | Responsável pela operação do restaurante; utilizará o painel administrativo |
| Equipe Desenvolvedora | Responsável pelo desenvolvimento, manutenção técnica e evolução do sistema |
| Instituições Parceiras | Outras universidades que poderão adotar a plataforma |
| Banco Central do Brasil | Regulador das transações via Pix |
| SUAP | Provedor da API de autenticação institucional |
---

##  4. Requisitos Funcionais

### RF01 - Autenticação Institucional
*Prioridade:* Alta
*Entradas:*
- Credenciais institucionais do usuário (login e senha do SUAP)
*Saídas:*
- Acesso autenticado ao sistema com sessão iniciada
- Mensagem de erro em caso de credenciais inválidas
*Regras de negócio:*
- O sistema deve autenticar o usuário exclusivamente via integração com o SUAP, não sendo permitido cadastro por e-mail ou outros provedores externos.
- Sessões inativas por tempo prolongado devem ser encerradas automaticamente.
- O acesso deve ser diferenciado por perfil: estudante, servidor ou administrador.

---

### RF02 - Consulta de Saldo
*Prioridade:* Alta
*Entradas:*
- Sessão autenticada do usuário
*Saídas:*
- Exibição do saldo disponível em créditos na conta do usuário, atualizado em tempo real
*Regras de negócio:*
- O saldo exibido deve refletir o estado mais recente da conta, considerando recargas e consumos já processados.
- A consulta de saldo deve estar disponível na tela inicial após o login.
- Não deve ser possível consultar o saldo de outro usuário.

---

### RF03 - Recarga de Saldo
*Prioridade:* Alta
*Entradas:*
- Valor desejado para recarga
- Método de pagamento selecionado (Pix ou cartão de crédito cadastrado)
*Saídas:*
- Confirmação de recarga bem-sucedida com atualização imediata do saldo
- Comprovante ou notificação da transação realizada
- Mensagem de erro em caso de falha no pagamento
*Regras de negócio:*
- O sistema deve suportar pagamento via Pix e cartão de crédito previamente cadastrado pelo usuário.
- O saldo só deve ser creditado após a confirmação do pagamento pela instituição financeira.
- Recargas com falha não devem alterar o saldo do usuário.
- Deve haver um valor mínimo de recarga definido pelo administrador.

---

### RF04 - Exibição do Cardápio Semanal
*Prioridade:* Alta
*Entradas:*
- Solicitação de visualização do cardápio pelo usuário autenticado
*Saídas:*
- Exibição do cardápio da semana vigente, organizado por dia e tipo de refeição
*Regras de negócio:*
- O cardápio deve ser atualizado semanalmente pelo administrador.
- Caso o cardápio da semana ainda não tenha sido publicado, o sistema deve exibir uma mensagem informativa ao usuário.
- O cardápio deve indicar claramente a data de vigência de cada refeição listada.

---

### RF05 - Histórico de Recargas
*Prioridade:* Média
*Entradas:*
- Sessão autenticada do usuário
- Filtros opcionais (período, método de pagamento)
*Saídas:*
- Lista paginada das recargas realizadas, contendo data, valor e método de pagamento
*Regras de negócio:*
- O histórico deve exibir apenas as recargas do próprio usuário autenticado.
- Os registros devem ser apresentados em ordem cronológica decrescente (mais recente primeiro).
- O sistema deve manter o histórico por, no mínimo, 12 meses.

---

### RF06 - Envio de Notificações
*Prioridade:* Média
*Entradas:*
- Eventos disparadores: saldo baixo, recarga confirmada, publicação de novo cardápio, manutenções programadas
*Saídas:*
- Notificação enviada ao usuário pelo canal configurado (push, e-mail institucional ou in-app)
*Regras de negócio:*
- O usuário deve poder configurar quais tipos de notificações deseja receber.
- Notificações de saldo baixo devem ser disparadas quando o saldo atingir um limite mínimo configurável.
- Notificações críticas do sistema (ex.: manutenção programada) não podem ser desabilitadas pelo usuário.

---

### RF07 - Registro de Check-in
*Prioridade:* Média
*Entradas:*
- Identificação do usuário no acesso ao RU (via QR Code, cartão ou biometria)
*Saídas:*
- Registro da entrada do usuário com data e hora
- Desconto automático do crédito correspondente à refeição no saldo do usuário
*Regras de negócio:*
- Cada check-in deve debitar automaticamente o valor da refeição do saldo do usuário.
- Não deve ser permitido o check-in caso o saldo seja insuficiente.
- O registro deve ser armazenado para consulta no histórico do usuário e nos relatórios administrativos.

---

### RF08 - Feedback sobre Refeições
*Prioridade:* Baixa
*Entradas:*
- Avaliação do usuário (nota e/ou comentário) referente à refeição do dia
*Saídas:*
- Confirmação de recebimento do feedback
- Dados agregados disponíveis para o administrador nos relatórios
*Regras de negócio:*
- O usuário só pode enviar feedback referente a refeições nas quais realizou check-in.
- Cada usuário pode enviar apenas um feedback por refeição por dia.
- Os feedbacks devem ser anônimos para outros usuários, sendo identificáveis apenas pelos administradores.

---

### RF09 - Integração com APIs Externas
*Prioridade:* Alta
*Entradas:*
- Dados de autenticação e transação encaminhados às APIs externas (SUAP, gateways de pagamento)
*Saídas:*
- Respostas das APIs processadas e refletidas no sistema (autenticação validada, pagamento confirmado, etc.)
*Regras de negócio:*
- A integração com o SUAP deve ser utilizada exclusivamente para autenticação e validação de vínculo institucional.
- A integração com o gateway de pagamento deve seguir os padrões de segurança PCI-DSS.
- Falhas na comunicação com APIs externas devem ser tratadas com mensagens de erro adequadas ao usuário, sem expor detalhes técnicos.

---

### RF10 - Cadastro de Usuários pelo Administrador
*Prioridade:* Alta
*Entradas:*
- Dados do usuário a ser cadastrado (nome, matrícula, vínculo institucional, perfil de acesso)
*Saídas:*
- Confirmação de cadastro realizado com sucesso
- Mensagem de erro em caso de dados inválidos ou usuário já existente
*Regras de negócio:*
- O administrador pode cadastrar usuários dos tipos: estudante, servidor e administrador.
- Não deve ser permitido cadastrar usuários com matrícula já existente no sistema.
- O cadastro deve verificar o vínculo ativo do usuário com a instituição via integração com o SUAP.

---

### RF11 - Gerenciamento de Créditos pelo Administrador
*Prioridade:* Alta
*Entradas:*
- Identificação do usuário e operação desejada (adição, remoção ou ajuste manual de créditos)
*Saídas:*
- Confirmação da operação realizada com atualização do saldo do usuário
- Registro da alteração no histórico administrativo
*Regras de negócio:*
- Toda alteração manual de crédito deve ser registrada com identificação do administrador responsável, data, hora e justificativa.
- Não deve ser possível definir saldo negativo a um usuário.
- Apenas administradores com permissão específica podem realizar ajustes manuais de crédito.

---

### RF12 - Gerenciamento do Cardápio pelo Administrador
*Prioridade:* Alta
*Entradas:*
- Dados do cardápio (data, tipo de refeição, itens do menu)
*Saídas:*
- Cardápio publicado e disponível para visualização pelos usuários
- Confirmação de atualização ou mensagem de erro em caso de dados inválidos
*Regras de negócio:*
- O cardápio deve ser cadastrado com antecedência mínima de 24 horas antes da refeição correspondente.
- Somente administradores podem criar, editar ou excluir entradas do cardápio.
- Alterações no cardápio já publicado devem gerar notificação automática aos usuários.

---

### RF13 - Geração de Relatórios pelo Administrador
*Prioridade:* Média
*Entradas:*
- Filtros selecionados pelo administrador (período, tipo de relatório, usuário ou grupo)
*Saídas:*
- Relatório gerado com dados de uso do sistema (recargas, check-ins, feedbacks, acessos) em formato exportável (PDF ou CSV)
*Regras de negócio:*
- Os relatórios devem estar disponíveis apenas para usuários com perfil de administrador.
- O sistema deve permitir a geração de relatórios por período (diário, semanal, mensal e personalizado).
- Os dados exibidos nos relatórios devem ser anonimizados quando exportados para fins estatísticos.
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
