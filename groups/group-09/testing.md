# Test Plan

## Strategy

A estratégia de testes do sistema  será baseada em uma abordagem **iterativa e incremental**, combinando testes manuais e automatizados sempre que possível. Serão realizados testes em diferentes níveis (unidade, integração e sistema) para garantir a qualidade, estabilidade e conformidade com os requisitos funcionais e não funcionais.

**Ferramentas sugeridas:**  
- **Google Test (C++)** ou **pytest (Python)** para testes de unidade  
- **Scripts manuais** para testes de integração e interface gráfica  
- **Testes de usabilidade** com usuários reais (calouros e veteranos)  

**Ambiente de teste:**  
- Windows 10/11, Linux Ubuntu 22.04, Android 12+, iOS 15+  
- Hardware: notebook básico (8GB RAM, GPU integrada) e smartphone intermediário  

## Test Levels

### Unit Tests (Testes de Unidade)
- **Objetivo:** Validar componentes individuais (funções, classes) isoladamente.
- **Exemplos:**
  - Cálculo de bounding box para detecção de clique (picking)
  - Lógica de busca textual (case-insensitive, parcial)
  - Funções de filtro por categoria
  - Rotinas de criptografia/descriptografia de dados sensíveis
- **Responsável:** Desenvolvedores

### Integration Tests (Testes de Integração)
- **Objetivo:** Verificar a comunicação entre módulos e camadas.
- **Exemplos:**
  - Interação Controller ↔ Model (ex: seleção de POI atualiza o painel de informações)
  - Atualização de cache da Central de Serviços e persistência local
  - Fluxo de busca → centralização → destaque no mapa
  - Inicialização do sistema: carregamento do mapa e configurações salvas
- **Responsável:** Desenvolvedores / Testador designado

### System Tests (Testes de Sistema)
- **Objetivo:** Validar o sistema como um todo em ambiente próximo ao real.
- **Tipos de teste:**
  - **Testes funcionais:** Execução de todos os requisitos funcionais (RF01 a RF13).
  - **Testes de usabilidade:** Com usuários representativos (calouros) – tempo de aprendizado < 5 min.
  - **Testes de desempenho:** Renderização sustentada a ≥30 FPS em dispositivos alvo.
  - **Testes de segurança:** Verificação de criptografia e sanitização de entradas.
  - **Testes de recuperação:** Falhas simuladas (ex: falta de arquivo de mapa) não interrompem o sistema.
  - **Testes de compatibilidade:** Execução nos SOs listados (Windows, Linux, Android, iOS, HyperOS).
- **Responsável:** Equipe de QA (ou time completo)


## Test Cases

| ID   | Description | Expected Result |
| ---- | ----------- | --------------- |
| TC01 | Abrir o aplicativo e verificar se o mapa é renderizado na posição inicial (visão geral do campus) | Mapa exibido sem erros, blocos e salas identificáveis, FPS ≥ 30 |
| TC02 | Navegar pelo mapa usando arrasto (mouse/toque) | O mapa se desloca suavemente; não há travamentos |
| TC03 | Aplicar zoom com scroll do mouse ou pinça touch | Zoom aproxima e afasta com limites; centro da operação é o cursor |
| TC04 | Clicar em um bloco/laboratório/sala | O local é destacado (borda/cor alterada) e um painel com informações detalhadas aparece |
| TC05 | Ativar filtro de categoria (ex: desmarcar "salas") | Apenas locais das categorias ativas permanecem visíveis no mapa |
| TC06 | Buscar por nome parcial (ex: "Lab" para Laboratório de Informática) | Lista de resultados mostra o laboratório; ao selecionar, mapa centraliza e aplica zoom adequado |
| TC07 | Simular localização atual (selecionar ponto de partida manual) | Marcador de posição atual é exibido no local escolhido |
| TC08 | Clicar no botão "Reset" | Mapa retorna à posição e zoom iniciais (mesmo da inicialização) |
| TC09 | Acessar a Central de Serviços (RU) com conexão de internet ativa | Cardápio do dia é carregado e exibido corretamente |
| TC10 | Acessar a Central de Serviços (RU) sem conexão de internet | Sistema exibe último cardápio em cache e uma mensagem "dados offline" |
| TC11 | Inserir busca com caracteres especiais (ex: "Sala 2-A") | Busca retorna resultados esperados sem erros de execução |
| TC12 | Realizar login com credenciais (simuladas) e carregar grade horária | Dados de grade são armazenados localmente com criptografia; roteiro entre salas é exibido |
| TC13 | Executar o sistema em dispositivos com hardware mínimo (Android 4GB RAM) | Mapa renderiza a ≥25 FPS (tolerado) sem crashes |
| TC14 | Manter o aplicativo aberto por 2 horas com navegação intermitente | Nenhuma falha ou degradação perceptível de desempenho |
| TC15 | Teste de usabilidade com calouro realizando tarefas: (1) encontrar bloco A, (2) buscar cantina, (3) resetar mapa | Usuário completa todas as tarefas em menos de 5 minutos sem ajuda externa |

## Acceptance Criteria

Os critérios de aceitação do sistema são baseados nos requisitos funcionais e não funcionais documentados. O sistema será considerado aceito quando:

1. **Todos os requisitos funcionais (RF01 a RF13) forem implementados e testados com sucesso** (conforme casos de teste acima).
2. **Desempenho e fluidez:** Renderização ≥ 30 FPS em hardware-alvo (computador com GPU integrada básica) e tempo de resposta ≤ 1 segundo para interações.
3. **Usabilidade:** Um grupo de pelo menos 10 usuários representativos (calouros) realiza as tarefas principais em menos de 5 minutos, com taxa de sucesso ≥ 90%.
4. **Confiabilidade:** O sistema não apresenta falhas (crashes) durante 2 horas de uso contínuo simulado (navegação, busca, filtros).
5. **Segurança:** Dados de login e grade horária armazenados localmente não estão em texto puro; entradas do usuário não causam injeção ou quebra do sistema.
6. **Compatibilidade:** O sistema é executado e funciona conforme esperado em pelo menos um ambiente de cada família de SO: Windows, Linux, Android, iOS (ou HyperOS).
7. **Documentação:** O código-fonte está documentado e o repositório Git contém histórico de commits e instruções básicas de compilação/execução.
8. **Entrega:** Todos os artefatos (requisitos, arquitetura, plano de testes, código-fonte) são entregues dentro do prazo estipulado.


## Risks

| Risco | Probabilidade | Impacto | Mitigação no Teste |
|-------|---------------|---------|--------------------|
| **Falhas de renderização em dispositivos com drivers OpenGL antigos** | Média | Alto | Incluir testes em hardware variado (notebooks de diferentes gerações); implementar fallback com software rendering (ex: Mesa) |
| **Mau desempenho em dispositivos móveis de baixa capacidade** | Média | Médio | Testar com perfis de carga (mapa com 200 POIs); usar ferramentas de profiling; aplicar LOD dinâmico |
| **Falhas na detecção de clique/toque em áreas de alta densidade de POIs** | Baixa | Médio | Testes de unidade extensivos para a lógica de bounding boxes; testes de sistema com cenários de POIs sobrepostos |
| **Corrupção de arquivos de cache/persistência** | Baixa | Médio | Testes de recuperação: simular arquivo corrompido e verificar se o sistema recria ou trata o erro sem crash |
| **Vazamento de memória durante uso prolongado** | Baixa | Alto | Executar testes de longa duração (2h+) com monitoramento de memória; usar valgrind (Linux) ou ferramentas similares |
| **Dependência de APIs externas (RU/ônibus) fora do ar** | Média | Médio | Testes de integração com simulação de indisponibilidade de rede; validar cache e mensagens amigáveis |
| **Problemas de usabilidade para usuários não experientes** | Média | Alto | Convidar calouros reais para testes de usabilidade; aplicar questionário SUS (System Usability Scale) |
