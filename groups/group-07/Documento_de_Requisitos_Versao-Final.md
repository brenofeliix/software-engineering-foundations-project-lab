# Especificação de Requisitos e Projeto de Arquitetura — Fireseeker
## 1. Introdução
### 1.1 Objetivo do Documento
Este documento estabelece a especificação formal de requisitos e a arquitetura de software para o **Fireseeker**, uma plataforma inteligente de sensoriamento remoto focada na detecção preditiva e monitoramento de incêndios em zonas rurais. O sistema integra Inteligência Artificial (Machine Learning/Deep Learning) e telemetria de satélites para fornecer análises de risco de alta precisão. Este artefato servirá como linha de base (baseline) para o ciclo de desenvolvimento, validação arquitetural, execução de testes e rastreabilidade do projeto ao longo do seu ciclo de vida.
### 1.2 Escopo do Sistema
O escopo de atuação do Fireseeker compreende a ingestão contínua de dados geoespaciais, processamento analítico de risco, execução de modelos preditivos baseados em IA, renderização de dashboards interativos e orquestração de alertas em tempo real.
**Exclusões do Escopo:**
 * Acionamento ou gestão direta de brigadas de incêndio físico.
 * Integração com constelações de satélites comerciais de acesso pago.
 * Operação do cliente web em ambientes estritamente offline (air-gapped).
### 1.3 Glossário e Acrônimos
| Termo | Definição |
|---|---|
| **AEB / INPE** | Agência Espacial Brasileira / Instituto Nacional de Pesquisas Espaciais. |
| **NASA FIRMS** | *Fire Information for Resource Management System* (Sistema de dados de focos de calor). |
| **MVP** | *Minimum Viable Product* (Produto Mínimo Viável focado no ciclo acadêmico atual). |
| **RBAC** | *Role-Based Access Control* (Controle de acesso baseado em papéis). |
| **PostGIS** | Extensão espacial para o banco de dados PostgreSQL. |
| **Telemetria** | Processo de medição e transmissão de dados de fontes remotas (satélites) para o sistema. |
## 2. Visão do Produto e Contexto de Negócio
### 2.1 Declaração do Problema
A detecção tardia de incêndios rurais resulta em degradação severa de biomas, prejuízos expressivos no agronegócio e riscos à infraestrutura local. Soluções convencionais baseiam-se na observação reativa, notificando focos de calor apenas após a ignição e propagação inicial, o que reduz drasticamente a janela de resposta operacional.
### 2.2 Proposta de Solução (Fireseeker)
O Fireseeker atua na **camada preventiva**. Consumindo bases históricas (BDQueimadas) e cruzando-as com imagens de satélite atualizadas, a plataforma utiliza modelos preditivos para mapear assinaturas de risco no terreno antes que a ignição ocorra, permitindo ações de mitigação proativas.
### 2.3 Perfil dos Stakeholders
| Stakeholder | Interesse / Valor Agregado |
|---|---|
| **Produtores Rurais** | Proteção de ativos, lavouras e infraestrutura privada. |
| **Órgãos Ambientais** | Mapeamento de risco para alocação eficiente de recursos de fiscalização. |
| **Banca Avaliadora/Academia** | Validação da aplicação prática de Engenharia de Software e IA em problemas reais. |
| **Equipe de Engenharia** | Construção de arquitetura escalável, otimizada e de alta disponibilidade. |
## 3. Especificação de Requisitos Funcionais (RF)
| ID | Nomenclatura | Descrição Técnica | Prioridade |
|---|---|---|---|
| **RF01** | Ingestão de Telemetria Satelital | Consumir, tratar e padronizar dados das APIs da AEB, INPE e NASA FIRMS com rotinas de polling em intervalos máximos de 5 minutos. | Alta |
| **RF02** | Processamento de Dados Históricos | Ingerir a base BDQueimadas e aplicar filtros de sazonalidade e clima regional para modelagem estatística. | Alta |
| **RF03** | Motor de Inferência de Risco (IA) | Executar pipeline de Machine Learning cruzando telemetria atual e dados históricos para classificar zonas em risco: Baixo, Médio, Alto e Crítico. | Alta |
| **RF04** | Renderização Geoespacial (Dashboard) | Projetar camadas topográficas e mapas de calor interativos no frontend, com suporte a zoom granular e atualização de estado via WebSockets. | Alta |
| **RF05** | Gestão de Identidade (IAM) | Prover fluxos completos de autenticação e autorização (cadastro, login, recuperação de senha) com unicidade de e-mail e regras de complexidade criptográfica. | Alta |
| **RF06** | Motor de Notificações em Tempo Real | Orquestrar e despachar alertas (Push/SMS/E-mail) para usuários monitorando zonas que atinjam o threshold de "Risco Crítico" em até 30 segundos após a inferência. | Alta |
| **RF07** | Exportação de Relatórios Analíticos | Gerar artefatos estáticos (PDF) contendo compilações de dados históricos e gráficos de tendências com base em recortes temporais definidos pelo usuário. | Média |
## 4. Especificação de Requisitos Não Funcionais (RNF)
Esta seção segue as diretrizes de qualidade de software da norma **ISO/IEC 25010**.
### 4.1 Desempenho e Eficiência (Performance)
 * **RNF01:** A latência máxima da API de consumo de dados pelo frontend não deve exceder 500ms (p95).
 * **RNF02:** A renderização inicial (First Contentful Paint) do mapa principal deve ocorrer em menos de 2 segundos.
 * **RNF03:** A arquitetura deve suportar picos de 10.000 conexões simultâneas via WebSocket sem degradação do serviço.
### 4.2 Segurança (Security)
 * **RNF04:** Todas as transações de dados devem ocorrer sob protocolo HTTPS (TLS 1.2 ou superior).
 * **RNF05:** Credenciais no banco de dados devem ser hasheadas utilizando o algoritmo BCrypt (cost factor 12).
 * **RNF06:** O sistema deve implementar controle de acesso estrito (RBAC) e proteção contra ataques de negação de serviço (DDoS).
### 4.3 Confiabilidade e Disponibilidade (Reliability)
 * **RNF07:** O sistema deve garantir um uptime (disponibilidade) de 99,9% (Service Level Objective).
 * **RNF08:** Rotinas de backup do banco de dados relacional e espacial devem ser executadas a cada 24 horas.
### 4.4 Manutenibilidade e Restrições de Projeto
 * **RNF09:** O projeto é restrito ao escopo de um MVP acadêmico, limitando a infraestrutura ao *free-tier* dos provedores de nuvem.
 * **RNF10:** É obrigatória a utilização de tecnologias e frameworks de código aberto (Open Source).
## 5. Arquitetura do Sistema
### 5.1 Estilo Arquitetural
A solução adotará uma arquitetura de **Microsserviços** ou **Monólito Modular** (dependendo das restrições do free-tier), orientada a eventos para o fluxo de alertas, visando alta coesão no processamento de dados pesados e baixo acoplamento na entrega ao cliente.
### 5.2 Stack Tecnológica
| Camada | Tecnologia Principal | Justificativa de Engenharia |
|---|---|---|
| **Frontend (Cliente)** | React.js | Reatividade fluida para manipulação de componentes geoespaciais e mapas. |
| **Backend (API Geral)** | Node.js (Express/NestJS) | Excelente I/O não bloqueante para lidar com milhares de conexões WebSocket. |
| **Backend (Motor IA/Dados)** | Python (FastAPI + TensorFlow) | Ecossistema nativo e superior para manipulação de matrizes de dados e Machine Learning. |
| **Persistência de Dados** | PostgreSQL + PostGIS | Solução robusta padrão da indústria para queries de dados vetoriais e geográficos. |
| **Infraestrutura** | Docker + Cloud Provider | Containerização para garantir paridade entre ambientes de desenvolvimento e produção. |
## 6. Casos de Uso Críticos
### UC01 — Avaliação Preditiva de Perímetro
**Ator Primário:** Produtor Rural / Analista Ambiental
**Fluxo de Eventos:**
 1. O usuário autenticado acessa a interface de monitoramento.
 2. O sistema estabelece uma conexão WebSocket.
 3. O sistema requisita ao banco espacial (PostGIS) a matriz de risco atualizada.
 4. O frontend renderiza polígonos de calor sobre o mapa topográfico.
 5. O usuário inspeciona visualmente as áreas demarcadas como "Risco Crítico".
### UC02 — Disparo Automático de Alerta Preventivo
**Ator Primário:** Motor de Inferência (Sistema)
**Fluxo de Eventos:**
 1. O worker de IA finaliza a análise de um lote de imagens de satélite.
 2. O modelo identifica a transição de um perímetro para "Risco Crítico" (threshold ultrapassado).
 3. O serviço de notificação identifica os usuários inscritos nas coordenadas geográficas afetadas.
 4. O sistema despacha a notificação push/e-mail imediatamente, concluindo a transação em menos de 30 segundos.
## 7. Estratégia de Qualidade e Testes
A validação do MVP seguirá a abordagem de "Testes Contínuos" integrada à esteira de CI/CD (Integração e Entrega Contínuas).
### 7.1 Escopo de Validação
 * **Testes Unitários:** Foco em funções puras, especialmente nos algoritmos de cálculo de coordenadas e conversão de dados satelitais.
 * **Testes de Integração:** Validação dos contratos de API entre o Node.js e o serviço Python de IA, e entre o backend e as APIs públicas (INPE/NASA).
 * **Testes de Carga (Stress):** Simulação de ingestão massiva de falsos positivos de telemetria para estressar o worker de processamento do mapa.
 * **Avaliação do Modelo (IA):** Acurácia preditiva do modelo de Machine Learning deve atingir um limite (threshold) mínimo aceitável de 85% contra o dataset de validação.
## 8. Considerações Finais e Premissas Tecnológicas
O **Fireseeker** é desenhado sob fortes premissas de conformidade com a Lei Geral de Proteção de Dados (LGPD) no tratamento dos cadastros de propriedades. Adicionalmente, assume-se que as APIs governamentais e internacionais (INPE, AEB, NASA) manterão suas rotinas de disponibilidade pública durante a avaliação do protótipo.
**Fim do Documento**
