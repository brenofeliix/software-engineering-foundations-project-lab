# 02-requirements: Fireseeker

## 1. Performance (Desempenho)

* **RF-PERF-01:** O sistema deve processar novas imagens de satélite e identificar focos de calor em até 5 minutos após a disponibilização dos dados pela fonte (NASA/INPE).
* **RF-PERF-02:** As notificações de detecção de incêndio devem ser enviadas aos usuários em menos de 30 segundos após a confirmação pela IA.
* **RF-PERF-03:** A interface do mapa de monitoramento deve ser atualizada em tempo real via WebSockets ou polling curto, sem necessidade de refresh manual.

## 2. Security (Segurança)

* **RF-SEC-01:** O sistema deve implementar controle de acesso baseado em funções (RBAC), garantindo que produtores visualizem apenas suas próprias áreas.
* **RF-SEC-02:** Todas as senhas de usuários devem ser armazenadas utilizando algoritmos de hash seguros (ex: BCrypt).
* **RF-SEC-03:** O sistema deve utilizar o protocolo HTTPS para garantir a integridade e criptografia dos dados em trânsito.
* **RF-SEC-04:** Deve haver um log de auditoria para ações críticas, como alteração de áreas de monitoramento ou configurações de alertas.

## 3. Usability (Usabilidade)

* **RF-USA-01:** O sistema deve ser responsivo, garantindo usabilidade total em smartphones (Android/iOS) e desktops.
* **RF-USA-02:** O dashboard deve utilizar um esquema de cores de alto contraste (padrão semafórico: Verde/Amarelo/Vermelho) para facilitar a leitura sob luz solar.
* **RF-USA-03:** O fluxo para visualizar os detalhes de um alerta de incêndio não deve ultrapassar 2 cliques a partir da tela inicial.

## 4. User Stories (Histórias de Usuário)

* **Como um produtor rural,** eu quero receber um alerta sonoro crítico no meu celular assim que um foco de calor for detectado, para que eu possa acionar a brigada de incêndio imediatamente.
* **Como um gestor de cooperativa agrícola,** eu quero visualizar um mapa consolidado de todas as propriedades associadas, para organizar uma resposta conjunta em caso de grandes queimadas.
* **Como um analista ambiental,** eu quero acessar relatórios históricos de focos de calor por período, para identificar áreas de maior recorrência e planejar aceiros preventivos.

---
*Documento de Requisitos - Grupo 07*
