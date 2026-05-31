# Documento de Requisitos e Projeto de Software

---

## 1. Introdução

### 1.1 Objetivo
Este documento tem como objetivo especificar os requisitos funcionais, não funcionais e de projeto do sistema **Fireseeker**, servindo como guia técnico para o desenvolvimento, validação e implantação da solução. O sistema visa monitorar, prever e alertar sobre focos de incêndio em propriedades rurais de forma proativa.

### 1.2 Escopo
O Fireseeker é uma plataforma inteligente focada na detecção precoce e previsão de princípios de incêndio em áreas rurais. 

**O sistema contempla:**
* Coleta e processamento automatizado de dados geográficos e imagens das constelações de nanosatélites da AEB, INPE (BDQueimadas) e NASA (FIRMS).
* Modelagem preditiva via Inteligência Artificial para classificação de níveis de risco por perímetro de propriedade.
* Dashboard interativo com mapas de satélite, polígonos de risco e indicadores gráficos em tempo real.
* Sistema de alertas sonoros e notificações críticas push/SMS direcionadas para produtores rurais e órgãos competentes.
* Cadastro de propriedades rurais integrável com bases públicas (ex: CAR — Cadastro Ambiental Rural).

**Fora do escopo:**
* Aquisição ou processamento de imagens de satélite comerciais privadas pagas.
* Acionamento automatizado de sistemas físicos de irrigação ou infraestruturas físicas de combate ao fogo em campo.
* Monitoramento de incêndios urbanos, industriais ou residenciais.

### 1.3 Definições, Acrônimos e Abreviações
* **RF / FR:** Requisito Funcional.
* **RNF:** Requisito Não Funcional.
* **INPE:** Instituto Nacional de Pesquisas Espaciais.
* **AEB:** Agência Espacial Brasileira.
* **NASA:** *National Aeronautics and Space Administration*.
* **FIRMS:** *Fire Information for Resource Management System*.
* **CAR:** Cadastro Ambiental Rural.
* **LGPD:** Lei Geral de Proteção de Dados (Lei nº 13.709/2018).
* **WCAG AA:** *Web Content Accessibility Guidelines* (Nível AA de contraste e acessibilidade).
* **RBAC:** *Role-Based Access Control* (Controle de Acesso Baseado em Funções).
* **MVP:** *Minimum Viable Product* (Produto Mínimo Viável).

---

## 2. Product Vision

### 2.1 Problema
Incêndios no agronegócio e em reservas ambientais causam prejuízos financeiros devastadores, destruição de infraestruturas rurais e severos impactos ecológicos. Atualmente, a detecção de queimadas ocorre de forma essencialmente reativa e tardia (quando o fogo já se espalhou), em virtude do atraso no processamento de imagens convencionais e da falta de análise preditiva local.

### 2.2 Solução
O Fireseeker introduz um sistema proativo inteligente que cruza dados históricos de focos de calor com dados climáticos e imagens de nanosatélites capturadas em tempo próximo ao real. Utilizando Inteligência Artificial, a plataforma gera um mapa dinâmico de risco (semelhante a uma previsão do tempo para incêndios) e envia alertas imediatos para que o produtor rural monte aceiros ou acione brigadas antes da propagação do fogo.

### 2.3 Público-Alvo
* Produtores rurais, fazendeiros, sitiantes e pequenos agricultores.
* Grandes empresas, agroindústrias e cooperativas do agronegócio.
* Órgãos ambientais governamentais e brigadas de monitoramento/Defesa Civil.

### 2.4 Proposta de Valor
Mitigar riscos operacionais e prejuízos financeiros crônicos no agronegócio através da antecipação temporal. Oferecer proteção patrimonial e ambiental na palma da mão, fornecendo informações complexas de sensoriamento remoto de maneira simplificada, acionável e de alta usabilidade para o trabalhador do campo.

### 2.5 Diferencial
Enquanto as ferramentas tradicionais exibem apenas o histórico de focos ativos com atraso (*delay*), o Fireseeker foca na **proatividade**. Ele utiliza algoritmos de Machine Learning para prever vulnerabilidades territoriais futuras e possui uma interface projetada especificamente para o campo, operando sem necessidade de download (*Zero-Installation*), em ambiente de alta luminosidade solar e com fluxo de interação de no máximo 3 cliques.

### 2.6 Funcionalidades principais (alto nível)
* Captura e processamento automático de APIs geoespaciais públicas.
* Motor de IA para classificação e previsão de áreas de risco.
* Mapa interativo com polígonos de propriedades e níveis de criticidade.
* Dashboard analítico com gráficos e relatórios históricos de focos de calor.
* Disparador automático de alertas críticos e notificações push.

---

## 3. Visão Geral do Sistema

### 3.1 Descrição Geral
O sistema funciona como uma aplicação web responsiva que atua em barramento contínuo. Ele ingere imagens geoespaciais, atualiza camadas cartográficas dinamicamente via WebSockets e cruza as coordenadas das propriedades cadastradas com os polígonos de ameaça. O usuário visualiza indicadores semafóricos de risco através de seu smartphone e recebe alarmes instantâneos caso sua fazenda entre em perímetro crítico.

### 3.2 Stakeholders
* **Produtores e Proprietários Rurais:** Usuários finais que cadastram suas terras e monitoram os riscos locais.
* **Gestores de Cooperativas Agrícolas:** Administradores que gerenciam mapas consolidados de múltiplas fazendas associadas.
* **Analistas Ambientais e Órgãos Públicos:** Técnicos que emitem relatórios macro e planejam respostas a desastres.
* **Equipe de Desenvolvimento:** Engenheiros de software, cientistas de dados e arquitetos responsáveis pelo sistema.

---

## 4. Requisitos Funcionais

### RF01 (FR01) - Coleta de Dados de Satélite
**Descrição:** O sistema deve coletar e processar dados e imagens de satélites das bases da AEB, INPE e NASA para fins de monitoramento ambiental.  
**Prioridade:** Alta  
**Entradas:** Requisições automatizadas a endpoints públicos e APIs (ex: programa BDQueimadas e FIRMS).  
**Saídas:** Dados geoespaciais estruturados, focos de calor e imagens de sensores (MODIS/VIIRS) ingeridos pelo sistema.  
**Regras de negócio:** A coleta deve ocorrer continuamente respeitando a taxa de disponibilização das fontes, garantindo a resolução espacial mínima para identificar áreas a partir de 1 hectare (Premissa-06).

---

### RF02 (FR02) - Análise de Dados Históricos
**Descrição:** O sistema deve analisar dados históricos de ocorrências de queimadas e variáveis climáticas para identificar padrões de comportamento e vulnerabilidade do terreno.  
**Prioridade:** Alta  
**Entradas:** Históricos temporais de queimas territoriais e dados de mapeamentos anteriores.  
**Saídas:** Matriz de padrões estruturada e bases validadas para alimentação do modelo.  
**Regras de negócio:** O sistema deve cruzar as informações com coordenadas geográficas exatas obtidas de bases públicas ou informadas.

---

### RF03 (FR03) - Previsão de Áreas Propensas via IA
**Descrição:** Prever áreas com maior risco e propensão a incêndios rurais utilizando algoritmos de Inteligência Artificial e Machine Learning.  
**Prioridade:** Alta  
**Entradas:** Dados correntes de satélite cruzados com a matriz de padrões históricos (RF02).  
**Saídas:** Classificação de áreas geográficas por níveis dinâmicos de criticidade de incêndio.  
**Regras de negócio:** O processamento deve classificar os polígonos territoriais de forma semelhante a previsões meteorológicas, gerando previsões antes do surgimento físico do fogo.

---

### RF04 (FR04) - Mapa Interativo de Risco
**Descrição:** Exibir um mapa geográfico interativo contendo camadas de satélite com polígonos das regiões rurais classificados por nível de risco de queimadas.  
**Prioridade:** Alta  
**Entradas:** Coordenadas e mapas de satélite integrados aos dados preditivos da IA (RF03).  
**Saídas:** Interface visual cartográfica atualizada com sobreposição de polígonos coloridos por criticidade.  
**Regras de negócio:** O mapa deve utilizar o padrão semafórico de cores (Verde para risco baixo, Amarelo para risco médio, Vermelho para risco alto) (RF-USA-02).

---

### RF05 (FR05) - Dashboard de Indicadores
**Descrição:** Disponibilizar um painel de controle (dashboard) contendo relatórios, gráficos analíticos e indicadores quantitativos de riscos e focos de calor.  
**Prioridade:** Média  
**Entradas:** Dados analíticos armazenados no banco e filtros temporais selecionados pelo usuário.  
**Saídas:** Gráficos de linha/barra e relatórios históricos exportáveis ou visualizáveis de focos por período.  
**Regras de negócio:** Analistas ambientais devem conseguir extrair relatórios para fins de planejamento de aceiros preventivos.

---

### RF06 (FR06) - Cadastro de Usuários e Propriedades
**Descrição:** Permitir o cadastro de usuários de perfis distintos (fazendeiros, cooperativas e órgãos governamentais) vinculando suas respectivas propriedades rurais.  
**Prioridade:** Alta  
**Entradas:** Formulário de dados cadastrais (nome, e-mail, senha, perfil) e delimitação geográfica das terras (via CAR ou inserção manual).  
**Saídas:** Conta de usuário ativa e perímetros de monitoramento registrados.  
**Regras de negócio:** O sistema deve aplicar controle de acesso baseado em funções (RBAC), assegurando que produtores privados visualizem estritamente as suas próprias áreas (RF-SEC-01).

---

### RF07 (FR07) - Envio de Alertas Críticos
**Descrição:** Enviar notificações automáticas imediatas aos usuários quando um foco de calor ou nível de risco alto/severo for detectado em seu perímetro de interesse.  
**Prioridade:** Alta  
**Entradas:** Detecção positiva de foco de calor pela IA dentro do polígono monitorado de uma conta cadastrada.  
**Saídas:** Disparo de notificações push, SMS ou alertas sonoros críticos nos smartphones cadastrados.  
**Regras de negócio:** O envio do alerta deve ocorrer de forma imediata após a confirmação do evento, servindo para o acionamento célere de brigadas particulares de incêndio.

---

## 5. Requisitos Não Funcionais

### 5.1 Usabilidade
* **Navegação Eficiente (RNF07):** Um usuário leigo deve ser perfeitamente capaz de localizar sua propriedade rural e visualizar o risco de incêndio associado com no máximo 3 cliques a partir da tela inicial da aplicação.
* **Responsividade Mobile-First (RNF08 / RF-USA-01):** A interface da plataforma deve ser adaptável e responsiva, operando com total usabilidade em smartphones (Android/iOS) e desktops a partir de telas com largura de 360px.
* **Acessibilidade Visual (RNF09 / RF-USA-02):** O esquema de cores do dashboard deve manter um contraste mínimo de 4.5:1 (padrão WCAG AA) utilizando obrigatoriamente a paleta semafórica (Verde/Amarelo/Vermelho) para viabilizar a leitura sob luz solar direta em ambiente de campo.
* **Acesso Simplificado:** O fluxo para visualização de detalhes de um alerta crítico emitido não deve exceder 2 cliques a partir da tela inicial do dispositivo móvel (RF-USA-03).

### 5.2 Eficiência
* **Sincronização Cartográfica (RNF01):** O sistema deve carregar e renderizar as camadas cartográficas e polígonos de risco na tela do usuário em no máximo 2 segundos após a solicitação.
* **Sincronização de Tela (RF-USA-03):** A interface do mapa de monitoramento deve ser atualizada em tempo real por meio de conexões WebSockets ou polling curto, eliminando qualquer necessidade de refresh ou recarga manual de página.

### 5.3 Desempenho
* **Processamento de Imagens (RF-PERF-01):** O backend deve processar novas imagens de satélite recebidas e identificar focos de calor correspondentes em até 5 minutos após a disponibilização dos arquivos pela fonte primária (NASA/INPE).
* **Latência de Alerta (RF-PERF-02):** As notificações de detecção de incêndio devem ser transmitidas e recebidas nos celulares dos usuários em menos de 30 segundos após a confirmação analítica pela Inteligência Artificial.
* **Escalabilidade sob Carga (RNF02):** A infraestrutura tecnológica da plataforma deve ser dimensionada para suportar até 10.000 usuários conectados de forma simultânea, assegurando que a latência de requisições permaneça abaixo de 500ms.

### 5.4 Espaço
* **Armazenamento de Imagens:** O banco de dados e a camada de arquivos do sistema devem compactar imagens vetoriais geoespaciais para não onerar o armazenamento e garantir leveza em servidores com limitações físicas.

### 5.5 Confiabilidade
* **Disponibilidade Mínima (RNF03):** O serviço deve apresentar um índice de uptime garantido de 99,9%, operando em regime de funcionamento contínuo 24 horas por dia, 7 dias por semana (24/7).

### 5.6 Segurança (Proteção)
* **Criptografia de Dados em Repouso (RNF04):** Todos os registros sensíveis de identificação de usuários e perímetros geográficos das propriedades devem ser criptografados no banco de dados utilizando o algoritmo AES-256.
* **Criptografia de Dados em Trânsito (RF-SEC-03 / CONSTRAINT-04):** Toda comunicação efetuada entre cliente e servidor deve trafegar obrigatoriamente através do protocolo seguro HTTPS empregando criptografia TLS 1.2 ou superior, sendo vedado texto plano.
* **Segurança de Credenciais (RF-SEC-02 / CONSTRAINT-05):** O armazenamento de senhas de usuários deve utilizar de forma exclusiva algoritmos de hash seguros, especificamente o BCrypt com fator de custo mínimo igual a 12.
* **Autenticação Avançada (RNF06):** Exigência de implementação de Autenticação de Dois Fatores (2FA) para acessos efetuados por contas de órgãos governamentais e administradores de grandes extensões de terra.
* **Trilhas de Auditoria (RF-SEC-04):** Geração e manutenção de logs de auditoria imutáveis para ações críticas do sistema, tais como alterações cadastrais de propriedades monitoradas e modificações em diretrizes de alertas.

---

## 6. Requisitos Organizacionais

### 6.1 Ambientais
* **Compatibilidade de Software:** O frontend do sistema deve possuir compatibilidade estrita com as duas últimas versões estáveis dos navegadores Google Chrome, Mozilla Firefox e Apple Safari (CONSTRAINT-03).
* **Hardware Mobile Alvo:** A aplicação deve funcionar perfeitamente em dispositivos móveis modernos que executem sistemas operacionais Android 10+ ou iOS 14+ através de navegadores compatíveis com tecnologias assíncronas e geolocalização (Premissa-04).

### 6.2 Operacionais
* **Interpretação Técnica:** O sistema assume que órgãos governamentais e cooperativas mantêm equipes técnicas mínimas capazes de interpretar mapas cartográficos de risco e aplicar os protocolos operacionais de resposta a incêndios (Premissa-08).

### 6.3 Desenvolvimento
* **Versionamento de Código:** Uso obrigatório de repositórios baseados em Git para controle, ramificação e histórico de versões do código fonte do projeto.
* **Padrões de Ferramental (CONSTRAINT-09):** Os modelos e arquiteturas de Inteligência Artificial devem ser desenvolvidos exclusivamente utilizando frameworks de código aberto (open-source), tais como TensorFlow, PyTorch ou Scikit-learn, evitando dependência de fornecedor (*vendor lock-in*).

---

## 7. Requisitos Externos

### 7.1 Reguladores
* **Conformidade Legal com a LGPD (RNF05 / CONSTRAINT-01):** O sistema deve estar em total conformidade com as diretrizes da Lei Geral de Proteção de Dados (Lei nº 13.709/2018), exigindo consentimento explícito para coleta e garantindo a exclusão definitiva de dados pessoais em até 48 horas após solicitação formal do titular.

### 7.2 Éticos
* **Transparência Cartográfica:** Os critérios de definição e pesagem das variáveis de Machine Learning para cálculo do risco de fogo devem ser claros para auditorias, evitando alarmes falsos excessivos que induzam pânico ou desvalorização injustificada de áreas agrícolas.

### 7.3 Legais
* **Soberania de Dados Geográficos (CONSTRAINT-06):** O sistema deve ser integralmente hospedado em servidores de nuvem cujos data centers estejam localizados fisicamente em território brasileiro, cumprindo as exigências nacionais sobre dados geoespaciais estratégicos.

### 7.4 Segurança Externa
* **Proteção de Perímetro:** Aplicação de firewalls e mecanismos de proteção contra ataques de negação de serviço (DDoS) nas portas lógicas do provedor de nuvem para resguardar a entrega contínua dos alertas em tempo real.

### 7.5 Contábeis
* **Financiamento Gratuito (CONSTRAINT-08):** O desenvolvimento do projeto está estritamente limitado ao orçamento de recursos gratuitos ou camadas de nível gratuito (*free-tier*) de serviços em nuvem, não existindo verbas comerciais para aquisição de infraestruturas pagas adicionais no período.

---