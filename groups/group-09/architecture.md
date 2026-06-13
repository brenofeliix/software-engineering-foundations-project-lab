# Software Architecture

## Overview

O sistema é uma aplicação gráfica multiplataforma (desktop e mobile) desenvolvida com OpenGL, que tem como objetivo fornecer um mapa interativo do campus da Universidade Federal de Rondonópolis (UFR), integrando serviços acadêmicos como cardápio do RU, horários de ônibus, grade horária do aluno e mural de avisos geolocalizados.

A arquitetura foi projetada para ser leve, modular e offline-first, garantindo que as funcionalidades principais (renderização do mapa, navegação, busca e seleção de locais) funcionem sem conexão com a internet. Os dados complementares (RU, ônibus, avisos) são atualizados via requisições HTTP quando há conectividade.

## Architectural Style

O estilo arquitetural adotado é o **MVC (Model-View-Controller)** adaptado para aplicações gráficas com OpenGL.

- **Model:** Gerencia os dados do sistema (mapa, pontos de interesse, grade horária, cardápio, horários de ônibus, avisos), além das regras de negócio (filtros, busca, geolocalização simulada).
- **View:** Responsável pela renderização gráfica do mapa e interface do usuário (botões, menus, painéis informativos). Utiliza OpenGL para desenho 2D/3D e uma camada de UI nativa (ou ImGui para prototipação).
- **Controller:** Trata as entradas do usuário (mouse, teclado, toque), coordena a interação entre Model e View e atualiza o estado da aplicação.

Essa separação permite manutenção independente de cada camada, facilita testes e possibilita reutilização de componentes.

## Components

A arquitetura é composta pelos seguintes módulos principais:

1. **Renderizador OpenGL**  
   Responsável por carregar o mapa e desenhar pontos de interesse, textos e destaques. Mantém a câmera e o viewport.

2. **Gerenciador de Navegação**  
   Controla movimentação, zoom, reset de câmera e centralização em locais buscados.

3. **Gerenciador de Seleção e Busca**  
   Implementa a detecção de cliques/toques sobre os elementos do mapa, realiza busca textual e coordena o destaque do item selecionado.

4. **Gerenciador de Categorias**  
   Armazena as categorias de locais e aplica filtros de visibilidade.

5. **Módulo de Localização**  
   Obtém a posição real do usuário via GPS (mobile) ou permite seleção manual (simulada). Fornece o marcador de posição atual.

6. **Central de Serviços**  
   Gerencia requisições HTTP para atualizar cardápio do RU, horários de ônibus e avisos. Armazena dados em cache local (JSON/XML).

7. **Gerenciador de Grade Horária**  
   Permite login seguro, armazena localmente a grade do aluno e calcula o roteiro entre salas de acordo com os horários.

8. **Módulo de Logs e Monitoramento**  
   Registra eventos (erros, buscas, falhas de renderização) em arquivos locais e oferece opção de envio anônimo de relatórios.

9. **Camada de Persistência**  
   Responsável por salvar/recuperar configurações (última posição do mapa, filtros, dados em cache) e dados sensíveis (credenciais, grade) com criptografia básica.

## Diagram

| Camada / Componente | Responsabilidades | Interage com |
|---------------------|-------------------|---------------|
| **VIEW** | Renderização OpenGL, interface de usuário (botões, menus, painéis), destaque visual de locais | Controller |
| **CONTROLLER** | Tratamento de entradas (mouse, teclado, toque), coordenação entre View e Model, eventos de navegação e busca | View, Model |
| **MODEL** | Dados do mapa e POIs, grade horária do aluno, cache de RU/ônibus/avisos, regras de negócio | Controller, Persistência |

### Componentes Internos

| Componente | Função | Dependências |
|------------|--------|----------------|
| **Renderizador OpenGL** | Gerencia câmera, viewport, picking (detecção de clique em POIs) e desenho de geometria/textos | OpenGL, GLFW/SDL |
| **Gerenciador de Navegação** | Movimento (arrasto), zoom, reset de câmera, centralização em locais | Controller, Renderizador |
| **Gerenciador de Busca e Seleção** | Busca textual (case-insensitive, parcial), destaque do item selecionado, exibição de informações | Model, Renderizador |
| **Gerenciador de Categorias** | Filtros de visibilidade por tipo de local (salas, laboratórios, secretarias etc.) | Model, View |
| **Central de Serviços (HTTP)** | Requisições para atualizar cardápio do RU, horários de ônibus e avisos; cache local | Model, Rede |
| **Módulo de Localização** | Obtém GPS real ou posição simulada; fornece marcador de localização atual | Controller, View |
| **Persistência e Logs** | Salva configurações, cache, grade horária criptografada; registra eventos de erro/depuração | Model, Sistema de Arquivos |

### Fluxo de Dados (Tabela de Interações)

| Ação | Origem | Caminho | Destino |
|------|--------|---------|---------|
| Clique em um ponto do mapa | Usuário (mouse/toque) | Controller → Gerenciador de Seleção → Model → Renderizador | View (destaque + painel informativo) |
| Busca por nome de local | Usuário (teclado) | Controller → Gerenciador de Busca → Model → Renderizador | View (centralização + zoom no local) |
| Atualização do cardápio do RU | Sistema (timer ou botão) | Central de Serviços → Model (cache) → View | Interface da Central de Serviços |
| Navegação (arrasto/zoom) | Usuário (mouse/teclado/touch) | Controller → Gerenciador de Navegação → Renderizador | View (nova posição/escala do mapa) |
| Inicialização do sistema | Sistema | Persistência → Model → Renderizador | View (mapa carregado na posição padrão) |

## Data Flow

1. **Inicialização**  
   - O sistema carrega o modelo do mapa e configurações salvas.  
   - Inicializa a câmera com posição padrão.

2. **Interação do usuário (exemplo: clique em um laboratório)**  
   - O Controller captura a posição do clique.  
   - Chama o Gerenciador de Seleção para identificar qual POI foi atingido.  
   - Solicita ao Model os detalhes daquele local.  
   - Atualiza a View: destaca o local e exibe um painel com informações (nome, tipo, horário de funcionamento).  

3. **Busca por nome**  
   - O usuário digita um texto no campo de busca.  
   - Controller repassa ao Gerenciador de Busca, que consulta o Model.  
   - Os resultados são exibidos em uma lista.  
   - Ao selecionar um resultado, o Controller calcula a nova posição da câmera para centralizar o local e aplica zoom adequado.  

4. **Atualização de dados externos (RU, ônibus)**  
   - Em segundo plano (se houver internet), a Central de Serviços faz requisições periódicas para endpoints predefinidos.  
   - Os dados recebidos são armazenados em cache (Model) e exibidos na interface quando o usuário acessa a Central.  

5. **Persistência de configurações**  
   - Ao fechar o aplicativo, a Camada de Persistência salva o último estado da câmera, filtros ativos e dados de login.

## Technologies

| Tecnologia | Finalidade |
|------------|------------|
| **OpenGL (3.3+)** | Renderização do mapa (geometria, texturas, textos) |
| **C++ (ou Python com PyOpenGL)** | Linguagem principal da aplicação (performance e compatibilidade) |
| **GLFW / SDL** | Criação de janela e gerenciamento de entrada (mouse/teclado) |
| **Dear ImGui (ou GUI nativa)** | Interface de botões, menus, painéis de informação |
| **JSON (nlohmann/json ou similar)** | Armazenamento de dados do mapa, POIs e cache |
| **SQLite (opcional)** | Persistência local para grade horária e histórico de buscas |
| **libcurl / HTTP requests** | Atualização de cardápio do RU, horários de ônibus e avisos |
| **OpenSSL / Crypto++** | Criptografia básica para dados sensíveis |
| **Git** | Versionamento |
| **CMake** | Gerenciamento de build multiplataforma |

## Risks

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|------------|
| **Desempenho de renderização em dispositivos móveis antigos** | Média | Alto | Utilizar níveis de detalhe e simplificar a geometria do mapa; testar em hardware limitado. |
| **Dependência de APIs externas para RU/ônibus** | Média | Médio | Implementar cache local e mecanismo de fallback (exibir último dado válido); permitir atualização manual. |
| **Dificuldade na detecção de toque/clique em alta densidade de POIs** | Baixa | Médio | Adotar bounding boxes e técnicas de quad-tree para consulta espacial eficiente. |
| **Falhas de integração com sistemas acadêmicos da UFR** | Alta | Alto | Priorizar entrada manual de grade horária em vez de integração automática; negociar com a TI da UFR. |
| **Segurança dos dados locais** | Baixa | Alto | Utilizar criptografia simétrica forte para armazenar login e grade; nunca salvar senha em texto puro. |
| **Atraso no desenvolvimento devido à complexidade do OpenGL** | Média | Médio | Reutilizar bibliotecas auxiliares (ex: glad, glm) e desenvolver protótipos iterativos. |
