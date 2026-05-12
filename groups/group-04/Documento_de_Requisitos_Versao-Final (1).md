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

# 5. Requisitos Não Funcionais

---

## 5.1 Usabilidade

* *RNF01* — A interface do sistema deve ser intuitiva e de fácil navegação, permitindo que estudantes e servidores realizem suas ações principais sem necessidade de treinamento prévio.
* *RNF02* — O sistema deve ser compatível com dispositivos móveis, adaptando-se responsivamente a diferentes tamanhos de tela (smartphones e tablets).
* *RNF03* — O sistema deve oferecer recursos de acessibilidade, incluindo alto contraste e alternância entre tema claro e escuro, configuráveis pelo próprio usuário.
* *RNF04* — O sistema deve possuir um modo para pessoas com deficiência visual, com suporte a leitores de tela e leitura de textos presentes na interface, garantindo a inclusão a todos os membros da comunidade acadêmica.

---

## 5.2 Eficiência

* *RNF05* — O sistema deve responder às requisições em até 2 segundos em condições normais de uso, garantindo uma experiência ágil para os usuários.
* *RNF06* — O sistema deve suportar múltiplos acessos simultâneos com perda mínima de desempenho, mantendo a estabilidade especialmente nos horários de pico do RU.

---

## 5.3 Desempenho

* *RNF07* — O sistema deve responder às requisições em até 2 segundos em condições normais de uso.
* *RNF08* — O sistema deve suportar múltiplos acessos simultâneos — estimados em até 1.000 usuários — com perda mínima de desempenho, garantindo estabilidade em horários de pico.
* *RNF09* — O sistema deve estar disponível 99% do tempo, desconsiderando janelas de manutenção programadas previamente comunicadas aos usuários.
* *RNF10* — O sistema deve apresentar tempo de recuperação rápido em caso de falhas, minimizando interrupções ao usuário e retomando a operação normal em até 15 minutos.

---

## 5.4 Espaço

* *RNF11* — O sistema deve utilizar armazenamento de forma eficiente, priorizando a especificação de dados históricos com baixa frequência de acesso (ex.: relatórios e registros antigos).
* *RNF12* — O uso de memória em servidor deve ser monitorado continuamente, com alertas automáticos ao atingir 80% da capacidade alocada.
* *RNF13* — Dados de cardápio, saldo e histórico de transações devem ser dimensionados para suportar o crescimento da base de usuários da UFR sem manipulação de desempenho.

---

## 5.5 Confiabilidade

* *RNF14* — O sistema deve estar disponível pelo menos 99% do tempo, desconsiderando as manutenções programadas.
* *RNF15* — O sistema deve possuir mecanismos de backup automático de dados, com cópias realizadas diariamente e armazenadas em local seguro e geograficamente separado.
* *RNF16* — O sistema deve possuir mecanismos de recuperação de falhas que permitam o restabelecimento da operação em tempo hábil, com perda mínima ou nula de dados.
* *RNF17* — O sistema deve garantir a integridade dos dados durante operações de recarga e pagamento, utilizando transações atômicas para evitar inconsistências em caso de falha parcial.

---

## 5.6 Segurança (Proteção)

* *RNF18* — O acesso ao sistema deve ser limitado à autenticação via SUAP, não sendo permitidas formas alternativas de login ou criação de senhas locais.
* *RNF19* — O sistema deve garantir a integridade e o sigilo das informações durante todas as operações financeiras, em conformidade com os padrões de segurança aplicáveis (ex.: PCI-DSS para transações com cartão).
* *RNF20* — O sistema deve implementar controle de acesso baseado em perfis (RBAC), garantindo que cada usuário acesse apenas os recursos e dados compatíveis com seu nível de permissão (estudante, servidor ou administrador).

---

# 6. Requisitos Organizacionais

---

## 6.1 Ambientes

### Sistema Operacional

O sistema deverá ser compatível com ambientes Linux para hospedagem em servidores, devido à sua estabilidade, segurança e ampla utilização em aplicações web modernas. A aplicação cliente deverá operar os principais sistemas operacionais utilizados pela comunidade acadêmica, incluindo Windows, Linux e Android, por meio de navegadores atualizados compatíveis com os padrões web modernos.

### Infraestrutura

A infraestrutura do sistema deverá ser baseada em arquitetura web desacoplada, separando Front-end, Back-end e banco de dados, permitindo maior escalabilidade e facilidade de manutenção. O sistema deverá ser hospedado em servidores com suporte a:

* APIs REST;
* Banco de dados relationl;
* Comunicação segura via HTTPS/TLS;
* Rotinas automáticas de backup;
* Monitoramento de disponibilidade e desempenho.

A infraestrutura também deve suportar integração com serviços externos, como:

* SUAP, para autenticação institucional;
* Gateways de pagamento, para processamento de recargas via Pix e cartão de crédito.

---

## 6.2 Operacionais

### Registros

O sistema deverá registrar os logs das principais operações realizadas pelos usuários e administradores, garantindo rastreabilidade e auditoria das ações realizadas.

Os registros devem incluir:

* Autenticações realizadas;
* Tentativas de acesso inválidas;
* Recargas de saldo;
* Alterações administrativas;
* Publicação e edição de cardápios;
* Operações relacionadas ao consumo de créditos.

Os registros devem ser armazenados:

* Data e hora da operação;
* Usuário responsável;
* Tipo da prática;
* Resultado da operação (sucesso ou falha).

Os registros administrativos deverão ter acesso restrito apenas a usuários autorizados.

### Monitoramento

O sistema deverá possuir mecanismos de monitoramento contínuo da aplicação e da infraestrutura, permitindo identificar falhas, lentidão ou indisponibilidade do serviço.

O monitoramento deverá monitorar:

* Uso de CPU, memória e armazenamento;
* Tempo médio de resposta das requisições;
* Taxa de erros da aplicação;
* Disponibilidade do sistema;
* Consumo de recursos do banco de dados.

O sistema deverá emitir alertas automáticos em caso de:

* Indisponibilidade dos serviços;
* Alto consumo de recursos;
* Falhas em integrações externas;
* Erros críticos em operações financeiras.

---

## 6.3 Desenvolvimento

### Versionamento (Git)

O desenvolvimento do sistema deverá utilizar o Git como ferramenta oficial de controle de versão, permitindo rastreamento de alterações no código-fonte e colaboração entre os desenvolvedores.

O repositório deverá manter:

* Histórico completo de alterações;
* Controle de filiais para desenvolvimento, testes e produção;
* Registro de autoria das modificações;
* Padronização de mensagens de commit.

As alterações no sistema deverão ser revisadas antes da integração com a filial principal.

### Padrões de Código

O projeto deverá seguir padrões de desenvolvimento que garantam legibilidade, organização e facilidade de manutenção do código.

Assim também:

* Padronização de nomenclatura de variáveis, cargos e classes;
* Separação de responsabilidades entre módulos;
* Documentação básica das APIs e componentes principais;
* Utilização de boas práticas de segurança e desenvolvimento web;
* Estrutura modular compatível com a arquitetura desacoplada definida no projeto.

O código deve priorizar claramente e manutenção futura, além de cobertura superficial entre componentes.

### Testes Automatizados

O sistema deverá possuir testes automatizados para validar o funcionamento das principais funcionalidades da aplicação.

Os testes abragar:

* Testes unitários;
* Testes de integração;
* Testes de APIs;
* Validação das regras de negócio críticas, especialmente operações financeiras e autenticação.

As rotinas de teste devem ser realizadas antes da publicação de novas versões do sistema, reduzindo riscos de falhas na produção.

---

#  7. Requisitos Externos

### 7.1 Reguladores

### Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)
O sistema PODE PAPAR deverá estar em conformidade com a Lei Geral de Proteção de Dados Pessoais (LGPD), que regula o tratamento de dados pessoais no Brasil. Por tratar dados de estudantes e servidores públicos, incluindo informações de vínculo institucional, histórico financeiro e padrões de consumo, a plataforma se enquadra diretamente no escopo da lei.

Embora o sistema atue de forma integrada ao ecossistema de dados da UFR via API do SUAP, a plataforma assegura a conformidade com a LGPD ao adotar o modelo de privacidade por design (privacy by design). O sistema não replicará a base de dados integral do SUAP, limitando-se ao consumo e exibição dos dados necessários para a operação do RU, garantindo que o trânsito de informações entre as plataformas ocorra sob protocolos de criptografia e autenticação segura.

As obrigações aplicáveis ao sistema incluem:

- **Base legal para tratamento de dados:** O tratamento dos dados pessoais dos usuários deverá ser fundamentado em base legal prevista no Art. 7º da LGPD, especialmente no cumprimento de obrigação legal (prestação de serviço público) e no legítimo interesse institucional da UFR.
- **Princípio da finalidade:** Os dados coletados deverão ser utilizados exclusivamente para as finalidades declaradas no sistema — autenticação, gestão de créditos, controle de acesso ao RU e comunicação institucional —, sendo vedado o uso para finalidades incompatíveis.
- **Princípio da minimização:** O sistema deverá coletar apenas os dados estritamente necessários para a execução de suas funcionalidades, evitando a coleta excessiva de informações pessoais.
- **Relatório de Impacto à Proteção de Dados (RIPD):** Deverá ser elaborado um RIPD antes da entrada em produção do sistema, avaliando os riscos do tratamento de dados pessoais e as medidas adotadas para mitigá-los, conforme Art. 38 da LGPD.
- **Incidentes de segurança:** Em caso de vazamento ou acesso não autorizado a dados pessoais, a UFR deverá comunicar o incidente à ANPD e aos titulares afetados em prazo razoável, conforme Art. 48 da LGPD.

### Normas Específicas Aplicáveis
- **Resolução CFM / Normas do Banco Central (Bacen):** As operações de pagamento via Pix deverão estar em conformidade com o Regulamento do Pix instituído pelo Banco Central do Brasil, respeitando os requisitos de segurança, autenticação e rastreabilidade das transações instantâneas.
- **PCI-DSS (Payment Card Industry Data Security Standard):** O processamento de pagamentos via cartão de crédito deverá obedecer ao padrão PCI-DSS, conforme já previsto nos requisitos não funcionais de segurança (RNF03 e RNF08). Isso implica que dados sensíveis de cartão jamais deverão ser armazenados diretamente no sistema, sendo delegados integralmente ao gateway de pagamento contratado.
- **Decreto nº 8.777/2016 — Política de Dados Abertos do Poder Executivo Federal:** Como sistema de uma instituição federal, relatórios e dados estatísticos agregados e anonimizados poderão estar sujeitos a demandas de transparência ativa, devendo o sistema viabilizar a exportação de dados em formatos abertos quando solicitado.
- **Lei de Acesso à Informação (LAI — Lei nº 12.527/2011):** Informações de caráter público relativas ao funcionamento do RU — como cardápios, comunicados e indicadores gerais de uso — deverão estar acessíveis em conformidade com os princípios de transparência da LAI, sem que isso implique exposição de dados pessoais dos usuários.

---

## 7.2 Éticos

### Não Discriminação
O sistema deverá ser desenvolvido e operado de forma a garantir igualdade de acesso e tratamento a todos os membros da comunidade acadêmica da UFR, independentemente de condição socioeconômica, raça, gênero, deficiência ou qualquer outro fator que possa ensejar discriminação.

- **Acessibilidade universal:** Conforme previsto nos requisitos RNF11 e RNF12, o sistema deverá oferecer recursos de acessibilidade, como alto contraste, alternância entre temas e suporte a leitores de tela, de modo a não excluir usuários com deficiência visual ou outras necessidades específicas.
- **Inclusão digital:** Reconhecendo que nem todos os usuários possuem familiaridade com plataformas digitais, o sistema deverá manter a coexistência com os guichês físicos de atendimento durante o período de transição, não forçando a exclusividade digital como condição de acesso ao serviço de alimentação.

### Transparência
- **Clareza nas operações financeiras:** O sistema deverá exibir de forma clara e compreensível todas as informações relacionadas a saldo, recargas, débitos por refeição e histórico de transações, sem ambiguidades que possam prejudicar o usuário.
- **Comunicação de alterações:** Qualquer modificação relevante nas regras de uso, preços das refeições ou funcionamento do sistema deverá ser comunicada aos usuários com antecedência adequada, por meio das notificações previstas no RF06.
- **Uso de dados:** O sistema deverá informar aos usuários, de forma acessível, quais dados são coletados, com qual finalidade e por quanto tempo são armazenados, em conformidade com o princípio da transparência da LGPD.
- **Feedbacks e avaliações:** O mecanismo de feedback sobre refeições (RF08) deverá ser conduzido de forma que o usuário compreenda o caráter anônimo de suas avaliações perante outros usuários e saiba que os dados agregados serão utilizados para fins de melhoria do serviço.
- **Auditorias administrativas:** Todas as operações realizadas por administradores (especialmente ajustes manuais de crédito (RF11)) deverão ser registradas com identificação do responsável e justificativa, garantindo rastreabilidade e inibindo práticas arbitrárias ou abusivas.

---

## 7.3 Legais

- **Constituição Federal de 1988, Art. 6º:** O acesso à alimentação é direito social fundamental. O sistema, como instrumento de viabilização do RU, deverá ser desenvolvido de modo a não criar barreiras adicionais ao acesso à alimentação por parte dos estudantes, especialmente aqueles em situação de vulnerabilidade.
- **Lei nº 9.784/1999 — Lei do Processo Administrativo Federal:** Como sistema de uma autarquia federal, os procedimentos administrativos realizados por meio da plataforma, tais quais como cadastro de usuários e ajustes de crédito, deverão observar os princípios da legalidade, impessoalidade, moralidade, publicidade e eficiência previstos nesta lei.
- **Lei nº 8.078/1990 — Código de Defesa do Consumidor (CDC):** Embora o RU não seja uma relação de consumo típica, as operações de recarga financeira realizadas no sistema envolvem transação econômica e deverão respeitar princípios de proteção ao consumidor, incluindo clareza nas condições de uso, direito à informação e ausência de práticas abusivas.
- **Lei nº 12.527/2011 — Lei de Acesso à Informação:** Dados públicos relativos ao funcionamento do RU e ao uso dos recursos institucionais deverão estar disponíveis para acesso mediante solicitação formal, respeitados os limites de proteção de dados pessoais.
- **Decreto-Lei nº 200/1967 e legislação aplicável às IFES:** A UFR, como Instituição Federal de Ensino Superior, está sujeita ao controle da administração pública federal. O sistema deverá viabilizar a geração de informações compatíveis com as obrigações de prestação de contas aos órgãos de controle, como TCU e CGU.
- **Marco Civil da Internet (Lei nº 12.965/2014):** O sistema deverá observar os princípios do Marco Civil da Internet no que se refere à proteção dos dados dos usuários, neutralidade de rede, responsabilidade dos provedores e guarda de registros de acesso, em conformidade com os Arts. 10 a 17 da referida lei.

---

## 7.4 Segurança Externa

### Proteção contra Ataques

O sistema deverá adotar medidas técnicas e procedimentais para prevenção, detecção e resposta a ameaças de segurança cibernética, em conformidade com as boas práticas do mercado e as diretrizes do Centro de Estudos, Resposta e Tratamento de Incidentes de Segurança no Brasil (CERT.br).

As proteções mínimas exigidas incluem:

- **Prevenção a Injeção de Código (SQL Injection e XSS):** Todas as entradas de dados fornecidas pelos usuários deverão ser validadas, sanitizadas e tratadas de forma a impedir ataques de injeção de SQL, Cross-Site Scripting (XSS) e outras vulnerabilidades.
- **Proteção contra CSRF (Cross-Site Request Forgery):** O sistema deverá implementar tokens de verificação em requisições que alterem estado, como recargas, edições de perfil e operações administrativas, para impedir que ações sejam executadas de forma não intencional por terceiros.
- **Limitação de tentativas de acesso (Rate Limiting e Brute Force Protection):** O sistema deverá bloquear ou limitar requisições excessivas a endpoints críticos, especialmente o de autenticação, para mitigar ataques de força bruta e negação de serviço (DoS).
- **Proteção contra ataques DDoS:** A infraestrutura de hospedagem deverá contar com mecanismos de mitigação de ataques de negação de serviço distribuída (DDoS), seja por meio de serviços de CDN, firewalls de aplicação web (WAF) ou recursos oferecidos pelo provedor de hospedagem.
- **Gerenciamento seguro de sessões:** Tokens de sessão deverão ser gerados com entropia suficiente, ter prazo de expiração definido e ser invalidados imediatamente após o logout ou detecção de comportamento suspeito.
- **Segurança na comunicação com APIs externas:** Toda comunicação com o SUAP e com os gateways de pagamento deverá ocorrer por meio de canais criptografados (HTTPS/TLS 1.2 ou superior), com validação de certificados e uso de credenciais seguras gerenciadas por variáveis de ambiente, jamais expostas no código-fonte.
- **Gestão de vulnerabilidades:** O sistema deverá manter suas dependências e bibliotecas atualizadas, com monitoramento de CVEs (Common Vulnerabilities and Exposures) conhecidas que possam afetar os componentes utilizados.

### Auditorias de Segurança

- **Revisão de código com foco em segurança (Code Review):** O processo de desenvolvimento deverá incluir revisões de código orientadas à identificação de vulnerabilidades antes da integração à branch principal, conforme previsto nos requisitos organizacionais de desenvolvimento.
- **Testes de penetração (Pentest):** Recomenda-se a realização de testes de penetração periódicos (ao menos antes da entrada em produção e após mudanças significativas na arquitetura) para identificar vulnerabilidades não detectadas na fase de desenvolvimento.
- **Auditoria de logs de segurança:** Os logs de acesso, tentativas de autenticação inválidas e operações administrativas deverão ser revisados periodicamente pela equipe de TI da UFR para identificação de padrões anômalos ou tentativas de uso indevido do sistema.
- **Conformidade com o padrão PCI-DSS:** As operações com cartão de crédito deverão ser submetidas a avaliações periódicas de conformidade com o PCI-DSS, garantindo que os requisitos de segurança para dados de pagamento sejam mantidos ao longo do ciclo de vida do sistema.
- **Política de divulgação responsável de vulnerabilidades:** A UFR deverá estabelecer um canal formal para recebimento de relatos de vulnerabilidades identificadas por terceiros (responsible disclosure), permitindo que falhas sejam comunicadas e corrigidas antes de sua eventual exploração.

---

## 7.5 Contábeis

### Registro de Transações

Todas as movimentações financeiras realizadas no sistema deverão ser registradas de forma íntegra, rastreável e imutável, em conformidade com os princípios contábeis de confiabilidade e oportunidade.

- **Registro atômico e auditável:** Cada operação de recarga ou débito de crédito deverá ser registrada como uma transação única e indivisível, contendo: identificação do usuário, valor da operação, método de pagamento utilizado, data e hora, status da transação e identificador único da operação junto ao gateway de pagamento ou ao sistema interno.
- **Imutabilidade dos registros:** Registros de transações concluídas não deverão ser passíveis de edição ou exclusão por nenhum perfil de usuário, incluindo administradores. Eventuais correções deverão ser realizadas por meio de lançamentos de estorno ou ajuste devidamente justificados, preservando o histórico completo.
- **Conciliação financeira:** O sistema deverá permitir a conciliação entre os registros internos de recargas e os extratos fornecidos pelos gateways de pagamento (Pix e cartão de crédito), viabilizando a identificação de eventuais divergências.
- **Rastreabilidade de ajustes manuais:** Toda operação de ajuste manual de crédito realizada por administradores (RF11) deverá gerar um registro contábil específico, distinguindo-se das recargas automáticas e contendo a justificativa da operação, conforme exigido pelas regras de negócio do requisito funcional correspondente.

### Relatórios Contábeis e de Prestação de Contas

- **Relatórios financeiros periódicos:** O sistema deverá permitir a geração de relatórios consolidados de arrecadação (total de recargas por período), consumo (total de débitos por refeição) e ajustes manuais, com granularidade diária, semanal, mensal e por período personalizado, conforme previsto no RF13.
- **Compatibilidade com auditorias institucionais:** Os dados financeiros gerados pelo sistema deverão ser exportáveis em formatos estruturados (CSV ou PDF) para subsidiar auditorias internas da UFR e eventuais fiscalizações dos órgãos de controle externo, como o Tribunal de Contas da União (TCU) e a Controladoria-Geral da União (CGU).
- **Retenção de dados financeiros:** Os registros de transações financeiras deverão ser armazenados por prazo mínimo compatível com as exigências legais aplicáveis à administração pública federal, observando ao menos o prazo de 5 (cinco) anos previsto para guarda de documentos fiscais, sem prejuízo de prazos mais longos definidos pela política de arquivamento da UFR.

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
