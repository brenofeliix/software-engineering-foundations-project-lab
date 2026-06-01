# Software Architecture

## Overview

O **Fireseeker** será desenvolvido utilizando uma arquitetura baseada em microsserviços leves e orientada a eventos, permitindo alta escalabilidade, processamento em tempo real e integração contínua com fontes externas de dados de satélite (INPE, NASA e AEB).

A solução será composta por:
- Frontend web responsivo para visualização dos mapas e alertas.
- Backend de APIs REST para autenticação, gestão de usuários e integração de dados.
- Módulo de Inteligência Artificial para análise preditiva de queimadas.
- Pipeline de ingestão de dados geoespaciais.
- Sistema de notificações em tempo real.

---

## Architectural Style

### Arquitetura em Camadas + Event-Driven Architecture

#### Motivos da escolha:
- Separação clara entre frontend, backend, IA e processamento geoespacial.
- Facilidade de manutenção e evolução do sistema.
- Melhor escalabilidade para processamento de imagens de satélite.
- Permite atualização em tempo real via eventos e WebSockets.

### Camadas:
1. Presentation Layer
2. Application Layer
3. Processing Layer
4. Data Layer

---

## Components

### Component A — Frontend Dashboard
- Exibição do mapa interativo.
- Visualização de alertas.
- Gráficos e indicadores.

### Component B — API Gateway
- Centralização de requisições.
- Autenticação JWT.
- Controle RBAC.

### Component C — Serviço de IA
- Predição de áreas de risco.
- Classificação de focos de calor.

### Component D — Serviço de Ingestão
- Coleta de dados do INPE/NASA.
- Processamento geoespacial.

### Component E — Serviço de Notificações
- Alertas push.
- Eventos em tempo real.

### Component F — Banco de Dados
- Persistência geográfica.
- Histórico de queimadas.

---

## Diagram

```text
                    +-------------------+
                    |   Usuário Web     |
                    +---------+---------+
                              |
                              v
                    +-------------------+
                    | Frontend React    |
                    +---------+---------+
                              |
                              v
                    +-------------------+
                    |   API Gateway     |
                    +----+----+----+----+
                         |    |    |
          +--------------+    |    +----------------+
          |                   |                     |
          v                   v                     v
+----------------+   +----------------+   +----------------+
| Serviço IA     |   | Notificações   |   | Ingestão Dados |
+--------+-------+   +--------+-------+   +--------+-------+
         |                        |                    |
         +------------------------+--------------------+
                                  |
                                  v
                      +----------------------+
                      | PostgreSQL + PostGIS |
                      +----------------------+
```

---

## Data Flow

1. Coleta de dados via APIs INPE/NASA.
2. Processamento geoespacial.
3. Análise preditiva por IA.
4. Classificação do risco.
5. Armazenamento no banco.
6. Atualização do dashboard.
7. Envio de alertas.

---

## Technologies

| Categoria | Tecnologia |
|---|---|
| Frontend | React + TypeScript |
| Backend | Node.js + NestJS |
| IA | Python + TensorFlow |
| Banco | PostgreSQL + PostGIS |
| Tempo Real | WebSockets |
| Infraestrutura | Docker |

---

## Risks

| Risco | Impacto |
|---|---|
| APIs indisponíveis | Falha no monitoramento |
| Sobrecarga de imagens | Lentidão |
| Falsos positivos | Alertas indevidos |
| Custos cloud | Limitação de escalabilidade |
