#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
O objetivo deste documento é especificar detalhadamente os requisitos funcionais, não funcionais, organizacionais, externos e a arquitetura do sistema Conexão Comunitária.
O Conexão Comunitária é uma plataforma digital colaborativa que conecta vizinhos para trocar favores, compartilhar recursos, organizar ações solidárias e disseminar informações relevantes dentro de um mesmo bairro ou região. O objetivo é ser diferente de redes sociais genéricas ou aplicativos de serviços isolados e integrar em um único lugar, alertas de segurança, troca de habilidades, além de outros recursos ja ditos para fortalecer e unir a comunidade local.

### 1.2 Escopo
O Conexão Comunitária é uma plataforma colaborativa que centraliza o compartilhamento de recursos (doações de itens), alertas de segurança pública/infraestrutura, gerenciamento de eventos beneficentes e trocas de habilidades.

- Limites do Sistema: A plataforma atua de forma hiperlocal, segmentando as interações com base no CEP e bairro do usuário para garantir relevância geográfica.

- Fora de Escopo: O sistema não processa transações financeiras (doações em dinheiro), não fornece serviços de frete ou logística de entrega de mercadorias e não realiza moderação de conteúdo automatizada baseada em Inteligência Artificial nesta versão.

### 1.3 Definições, Acrônimos e Abreviações
- RF / FR: Requisito Funcional (Functional Requirement).

- RNF / NFR: Requisito Não Funcional (Non-Functional Requirement).

- LGPD: Lei Geral de Proteção de Dados (Lei nº 13.709/2018).

- MVP: Mínimo Produto Viável (Minimum Viable Product).

- API: Interface de Programação de Aplicação (Application Programming Interface).

- WAF: Firewall de Aplicação Web (Web Application Firewall).

- Rate Limiting: Bloqueio temporário de requisições baseado no volume por IP.

---

##  2. Product Vision

### 2.1 Problema
Atualmente, as redes de apoio de bairros (pedidos de doações, mutirões, alertas de alagamentos ou segurança) operam espalhadas em grupos caóticos de WhatsApp, Facebook ou Telegram. Nesses ambientes, as informações se perdem rapidamente no fluxo de conversas, gerando falta de engajamento, proliferação de notícias falsas e ineficiência na distribuição de ajuda a quem realmente precisa.

### 2.2 Solução
O Conexão Comunitária centraliza e organiza essas interações em uma plataforma estruturada e geolocalizada. Ele transforma mensagens soltas em um painel visual composto por um mapa interativo e listas filtráveis, permitindo que moradores saibam exatamente o que está acontecendo e como podem ajudar em seu próprio bairro.

### 2.3 Público-Alvo
- Moradores locais e vizinhanças voluntárias.

- Associações de moradores e líderes comunitários.

- Centros comunitários, coletivos locais e ONGs regionais.

### 2.4 Proposta de Valor
Para os moradores, o sistema oferece um canal direto, seguro e prático de exercer a solidariedade e se manter informado sobre a segurança local. Para as lideranças comunitárias, atua como uma ferramenta de gestão capaz de mensurar o impacto social, coordenar mutirões e validar a veracidade de incidentes.

### 2.5 Diferencial
Diferente de redes sociais genéricas ou classificados de doação puras, a plataforma une geolocalização estrita via CEP, um índice de reputação por estrelas construído por validações reais e um mecanismo descentralizado de checagem e contestação comunitária de alertas de urgência.

### 2.6 Funcionalidades principais (alto nível)
- Mapa da Solidariedade: Interface interativa para localizar ofertas de ajuda, doações e necessidades ativas.

- Central de Alertas Críticos: Sistema de notificação instantânea de incidentes locais com moderação colaborativa.
  
---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
O sistema funciona como uma rede social de utilidade pública baseada no território do usuário. Ao se cadastrar com o CEP, o usuário passa a visualizar o feed de doações, o calendário de eventos locais e o mapa de incidentes restritos à sua região ou bairros vizinhos. Os usuários podem anunciar itens para doação, manifestar interesse em desapegos, confirmar presença em mutirões e reportar ocorrências emergenciais no bairro.

### 3.2 Stakeholders
- Usuários: Cidadãos comuns que utilizam a plataforma para doar, solicitar auxílio ou monitorar alertas locais.

- Clientes: Associações de moradores, prefeituras locais ou ONGs mantenedoras que patrocinam e gerenciam as regras da comunidade.

- Outros (Moderadores): Líderes comunitários responsáveis pela curadoria de alertas e auditoria de abusos reportados no sistema.

---

##  4. Requisitos Funcionais

### RF01 - Cadastro por E-mail e Senha
**Descrição:**  
Permitir que o usuário realize o seu cadastro inicial na plataforma informando suas credenciais de acesso de forma segura.

**Prioridade:** Alta  
**Entradas:** E-mail válido e criação de senha (mínimo de 8 caracteres).  
**Saídas:** Conta de usuário criada na base de dados e mensagem de confirmação de cadastro enviado por e-mail.  
**Regras de negócio:** Não deve ser permitida a criação de mais de uma conta utilizando o mesmo endereço de e-mail.

---

### RF02 - Associação Territorial via CEP
**Descrição:**  
Solicitar, obrigatoriamente no momento do cadastro, o CEP e o nome do bairro do usuário para vinculá-lo ao seu território geográfico de atuação.

**Prioridade:** Alta  
**Entradas:** CEP (8 dígitos) e Nome do Bairro.  
**Saídas:** Vínculo geográfico registrado no perfil do usuário no banco de dados.  
**Regras de negócio:** O nome do bairro deve ser preenchido de forma automática e validada com base no CEP fornecido para evitar cadastros com inconsistências regionais.

---

### RF03 - Complementação de Perfil de Usuário
**Descrição:**  
Permitir que o usuário adicione informações adicionais e personalizadas ao seu perfil após o cadastro inicial.

**Prioridade:** Média  
**Entradas:** Foto de perfil, nome completo, número de telefone, lista de habilidades (tags) e interesses.  
**Saídas:** Perfil de usuário enriquecido e atualizado no banco de dados.  
**Regras de negócio:** A lista de habilidades pode conter opções predefinidas pela plataforma ou novas tags inseridas livremente pelo usuário.

---

### RF04 - Edição de Dados Cadastrais
**Descrição:**  
Permitir que o usuário altere suas informações pessoais, de contato e habilidades sempre que julgar necessário.

**Prioridade:** Alta  
**Entradas:** Modificação dos campos de dados pessoais, foto ou exclusão/adição de novas habilidades.  
**Saídas:** Alerta em tela de "Perfil atualizado com sucesso" e persistência dos dados.  
**Regras de negócio:** A alteração do e-mail principal exige uma revalidação de segurança através de token enviado para o endereço antigo e para o novo.

---

### RF05 - Exibição Pública de Perfil
**Descrição:**  
Disponibilizar uma visualização pública do perfil do usuário para que outros membros da comunidade identifiquem com quem estão interagindo.

**Prioridade:** Alta  
**Entradas:** Requisição de clique para visualização do perfil de um usuário por outro membro cadastrado.  
**Saídas:** Renderização em tela do Nome, foto, bairro, data de ingresso na plataforma e reputação média calculada.  
**Regras de negócio:** Dados estritamente privados como e-mail completo, número de telefone e endereço residencial exato (rua e número) nunca devem ser expostos publicamente.

---

### RF06 - Cálculo do Índice de Reputação
**Descrição:**  
Processar a média aritmética das avaliações recebidas pelo usuário e renderizar esse indicador no formato de pontuação visual.

**Prioridade:** Média  
**Entradas:** Notas coletadas no histórico de interações finalizadas do usuário.  
**Saídas:** Índice numérico e representação gráfica (ex: de 0 a 5 estrelas) atualizado no perfil público.  
**Regras de negócio:** Usuários novos que ainda não participaram de nenhuma transação finalizada exibirão o rótulo "Novo membro" em vez de nota zero.

---

### RF07 - Avaliação Pós-Interação
**Descrição:**  
Permitir que os usuários envolvidos atribuam uma nota e um comentário sobre a experiência ao fim de uma doação ou ajuda mútua.

**Prioridade:** Média  
**Entradas:** Nota de 1 a 5 e comentário opcional em formato de texto.  
**Saídas:** Gravação do registro de avaliação atrelado à contraparte da interação.  
**Regras de negócio:** O formulário de avaliação mútua só ficará disponível para preenchimento após o status da doação ser formalmente alterado para "concluído".

---

### RF08 - Mapa Interativo da Solidariedade
**Descrição:**  
Exibir um mapa dinâmico contendo marcadores visuais geolocalizados com as atividades do bairro.

**Prioridade:** Alta  
**Entradas:** Coordenadas de localização geográfica do bairro ou do dispositivo do usuário.  
**Saídas:** Mapa interativo renderizado em tela com ícones indicativos (pins) de doações, necessidades e eventos.  
**Regras de negócio:** O mapa deve ser atualizado dinamicamente sempre que o usuário arrastar a tela ou alterar o zoom de visualização.

---

### RF09 - Configuração de Raio de Visualização no Mapa
**Descrição:**  
Permitir que o usuário restrinja ou expanda o escopo geográfico dos marcadores exibidos no mapa.

**Prioridade:** Média  
**Entradas:** Seleção de filtro de alcance ("Apenas meu bairro" ou "Incluir bairros vizinhos").  
**Saídas:** Filtragem instantânea e atualização dos pins visíveis no mapa.  
**Regras de negócio:** Por padrão, a inicialização do mapa deve ocultar marcadores pertencentes a bairros distantes que não façam divisa com a região do usuário.

---

### RF10 - Publicação de Pontos de Ajuda no Mapa
**Descrição:**  
Permitir a inserção de um novo marcador fixo no mapa pelo usuário, sinalizando que há uma oferta ou pedido emergencial em andamento.

**Prioridade:** Alta  
**Entradas:** Título, categoria do pedido/oferta, endereço de referência e descrição textual livre.  
**Saídas:** Novo pin inserido no mapa interativo visível para a comunidade regional.  
**Regras de negócio:** Um ponto de ajuda expira e é removido automaticamente do mapa após 7 dias seguidos sem interações ou renovações do autor.

---

### RF11 - Detalhamento de Marcadores do Mapa
**Descrição:**  
Apresentar um pop-up ou modal informativo contendo o resumo da ação ao clicar sobre qualquer pin contido no mapa.

**Prioridade:** Alta  
**Entradas:** Clique/Toque do usuário sobre um marcador específico do mapa.  
**Saídas:** Janela sobreposta (modal) contendo descrição detalhada, foto e botão para "Entrar em contato".  
**Regras de negócio:** O acionamento do botão de contato deve abrir um canal de mensagens direto seguro (chat interno) com o usuário que criou o ponto.

---

### RF12 - Filtragem de Categorias do Mapa
**Descrição:**  
Permitir a filtragem rápida dos pins do mapa de acordo com os interesses específicos do usuário.

**Prioridade:** Alta  
**Entradas:** Seleção de caixas de checagem de categorias (ex: alimentos, pets, reparos domésticos, eventos).  
**Saídas:** Recarregamento dos marcadores em tela exibindo apenas as categorias ativas.  
**Regras de negócio:** O sistema deve suportar a seleção múltipla e simultânea de categorias nos filtros do mapa.

---

### RF13 - Cadastro de Itens para Doação
**Descrição:**  
Permitir a publicação de um item físico disponível para doação comunitária.

**Prioridade:** Alta  
**Entradas:** Foto do item (upload ou captura de câmera), título, descrição, quantidade e estado de conservação (novo, usado, necessita reparos).  
**Saídas:** Anúncio de doação inserido no banco de dados e adicionado ao feed e mapa da plataforma.  
**Regras de negócio:** É obrigatório o envio de pelo menos uma foto real do item para validar a publicação do anúncio.

---

### RF14 - Manifestação de Interesse em Doações
**Descrição:**  
Disponibilizar um mecanismo para que usuários interessados em uma doação notifiquem o doador diretamente pela publicação.

**Prioridade:** Alta  
**Entradas:** Clique no botão "Tenho Interesse" na página do anúncio de doação.  
**Saídas:** Vinculação do interesse do usuário à listagem interna daquele item e disparo de sinalização ao doador.  
**Regras de negócio:** Um usuário não pode clicar em "Tenho Interesse" mais de uma vez no mesmo anúncio.

---

### RF15 - Ciclo de Status de Doação
**Descrição:**  
Controlar o ciclo de vida e disponibilidade de uma doação por meio de estados lógicos bem definidos.

**Prioridade:** Alta  
**Entradas:** Modificação manual executada pelo doador do item.  
**Saídas:** Alteração visual imediata da tag indicativa do anúncio para: "Disponível", "Reservado" ou "Concluído".  
**Regras de negócio:** Quando o doador aceita um pretendente, o sistema deve mudar o status automaticamente para "Reservado" e congelar novos pedidos de interesse.

---

### RF16 - Remoção Automática de Doações Concluídas
**Descrição:**  
Limpar a listagem pública ativa do sistema retirando anúncios cujo ciclo de doação já foi finalizado.

**Prioridade:** Média  
**Entradas:** Alteração de status promovida pelo usuário para o estado "Concluído".  
**Saídas:** O anúncio é retirado de todos os feeds de busca públicos e do mapa.  
**Regras de negócio:** O anúncio deixa a visibilidade pública, mas os dados persistem na base histórica restrita dos envolvidos para viabilizar as avaliações (RF07).

---

### RF17 - Cancelamento de Doação Publicada
**Descrição:**  
Garantir ao doador a possibilidade de desistir ou retirar um anúncio de doação de circulação antes que a entrega física aconteça.

**Prioridade:** Alta  
**Entradas:** Comando de acionamento do botão "Cancelar Doação" na área gerencial do usuário.  
**Saídas:** Atualização do status lógico do item para "Cancelado" e arquivamento do anúncio.  
**Regras de negócio:** Um item cujo status final já tenha sido definido como "Concluído" não pode sofrer operações de cancelamento.

---

### RF18 - Notificação de Manifesto de Interesse
**Descrição:**  
Alertar o proprietário de uma doação assim que outro membro da plataforma demonstrar desejo em receber o item ofertado.

**Prioridade:** Média  
**Entradas:** Evento lógico gerado pelo manifesto de interesse de um terceiro (RF14).  
**Saídas:** Envio de mensagem push de notificação em tempo real na conta do doador.  
**Regras de negócio:** A notificação deve redirecionar o doador diretamente para o painel de gerenciamento de interessados daquela respectiva doação.

---

### RF19 - Notificação de Desfecho de Doação aos Interessados
**Descrição:**  
Comunicar de forma automatizada todos os usuários da fila de interesse caso o anúncio sofra alterações críticas de fechamento.

**Prioridade:** Baixa  
**Entradas:** Mudança no status do item para "Cancelado" ou para "Concluído" (fechado com outro usuário).  
**Saídas:** Mensagens automáticas disparadas para as centrais de notificação dos demais usuários da lista de espera.  
**Regras de negócio:** O conteúdo da mensagem de aviso deve ocultar dados pessoais do usuário escolhido para preservar a privacidade.

---

### RF20 - Criação de Eventos Comunitários
**Descrição:**  
Permitir a postagem e o agendamento de eventos voltados à integração ou apoio à vizinhança.

**Prioridade:** Média  
**Entradas:** Título do evento, descrição, data de realização, horário de início/fim, local físico de encontro e categoria (mutirão, bazar, palestra, feira).  
**Saídas:** Evento persistido no banco de dados e adicionado ao feed de eventos locais.  
**Regras de negócio:** A data e o horário estipulados para a realização do evento não podem ser inferiores ao horário atual do servidor.

---

### RF21 - Calendário Visceral Integrado
**Descrição:**  
Disponibilizar uma interface de agenda organizada cronologicamente para a visualização dos eventos do bairro.

**Prioridade:** Média  
**Entradas:** Clique de redirecionamento para a aba "Calendário Comunitário".  
**Saídas:** Interface de calendário renderizada em tela nos formatos de visualização por Mês, Semana ou Lista Cronológica de atividades.  
**Regras de negócio:** O calendário deve destacar visualmente e fixar no topo os eventos agendados para o dia vigente.

---

### RF22 - Confirmação de Presença em Eventos
**Descrição:**  
Permitir que os usuários sinalizem sua intenção de comparecer aos eventos criados por outros membros.

**Prioridade:** Média  
**Entradas:** Clique no botão "Confirmar Presença" contido no card de detalhes do evento.  
**Saídas:** Incremento do contador público de presentes no evento e adição do usuário à lista de presença.  
**Regras de negócio:** O usuário possui total autonomia para cancelar sua confirmação de presença a qualquer instante antes do início do evento.

---

### RF23 - Envio de Lembretes Automáticos de Eventos
**Descrição:**  
Disparar avisos preventivos para assegurar o comparecimento dos voluntários e participantes confirmados.

**Prioridade:** Baixa  
**Entradas:** Verificação por rotina de tarefas do servidor ($T - 24\text{ horas}$ em relação ao início cronológico do evento).  
**Saídas:** Envio de notificação eletrônica do tipo push aos usuários com presença confirmada (RF22).  
**Regras de negócio:** Caso o criador altere o evento para o status de "Cancelado", os disparos agendados de lembrete devem ser expurgados da fila de envio.

---

### RF24 - Edição e Cancelamento de Eventos
**Descrição:**  
Permitir ao criador/organizador do evento modificar seus parâmetros estruturais ou cancelá-lo em definitivo.

**Prioridade:** Média  
**Entradas:** Modificação manual dos campos informativos do evento ou acionamento do comando "Cancelar Evento".  
**Saídas:** Atualização da base de dados e emissão imediata de um alerta de alteração/cancelamento a todos os confirmados na lista de presença.  
**Regras de negócio:** O cancelamento de um evento com presença confirmada gera a obrigação de disparo de notificação imediata em lote para mitigar deslocamentos frustrados.

---

### RF25 - Publicação de Alertas Comunitários
**Descrição:**  
Permitir a postagem rápida de incidentes e acontecimentos críticos que afetam a rotina ou a segurança local imediata.

**Prioridade:** Alta  
**Entradas:** Descrição em texto do fato observado, localização do ocorrido e inserção opcional de imagem comprobatória.  
**Saídas:** Alerta inserido no banco de dados e projetado no mural de urgências do bairro em tempo real.  
**Regras de negócio:** O usuário deve possuir uma conta ativa com CEP validado na região para estar elegível a abrir um alerta público.

---

### RF26 - Categorização Estruturada de Alertas
**Descrição:**  
Obrigar a classificação do alerta em categorias previamente parametrizadas para fins de triagem e inteligência visual.

**Prioridade:** Alta  
**Entradas:** Escolha de uma categoria predefinida: Segurança, Emergência Climática, Serviços Públicos, Animal Perdido, Outros.  
**Saídas:** Registro do alerta tagueado com a categoria selecionada.  
**Regras de negócio:** A categoria selecionada define de forma estrita a cor de destaque e o ícone do pin do alerta que será renderizado nas telas de visualização.

---

### RF27 - Ordenação e Destaque Visual de Alertas
**Descrição:**  
Exibir a central de alertas priorizando critérios cronológicos e de impacto de gravidade.

**Prioridade:** Alta  
**Entradas:** Requisição de acesso ao feed de utilidade pública de alertas do bairro.  
**Saídas:** Lista de ocorrências ordenada a partir da data mais recente, com estilização visual realçada (ex: molduras vermelhas piscantes) para as categorias "Segurança" e "Emergência Climática".  
**Regras de negócio:** Alertas que ultrapassarem 48 horas de existência ativa são automaticamente arquivados na listagem de histórico para evitar saturação visual do feed.

---

### RF28 - Notificação Coletiva de Alertas em Massa
**Descrição:**  
Distribuir notificações instantâneas para salvaguardar a comunidade vizinha assim que uma ocorrência crítica é registrada.

**Prioridade:** Alta  
**Entradas:** Gatilho originado pela inserção de um alerta válido no sistema (RF25).  
**Saídas:** Envio massivo de notificações push em lote para as contas de todos os usuários registrados sob o mesmo bairro do incidente.  
**Regras de negócio:** Moradores de bairros limítrofes cadastrados também receberão o alerta se tiverem marcado a opção "Receber alertas de adjacências" em suas configurações.

---

### RF29 - Validação e Contestação Comunitária de Alertas
**Descrição:**  
Permitir o controle descentralizado de veracidade de informações através do engajamento dos próprios moradores.

**Prioridade:** Média  
**Entradas:** Cliques nos botões de engajamento "Confirmo Ocorrência" ou "É Falso / Fake News".  
**Saídas:** Atualização numérica dos contadores de votos anexados ao corpo descritivo do alerta.  
**Regras de negócio:** Alertas que acumularem uma taxa de contestação de falsidade superior a 70% em uma amostragem mínima de 10 votos serão suspensos temporariamente e ocultados até auditoria.

---

### RF30 - Moderação Avançada de Alertas por Líderes Comunitários
**Descrição:**  
Permitir que usuários com permissões administrativas elevadas intervenham na moderação de conteúdos abusivos ou incorretos.

**Prioridade:** Alta  
**Entradas:** Comando de ação administrativa "Remover Alerta" ou "Arquivar por Duplicidade".  
**Saídas:** Exclusão imediata do alerta do feed público e envio dos logs da ação para a base de auditoria da gerência.  
**Regras de negócio:** Apenas contas associadas a perfis especiais com privilégios de moderação (como líderes e diretores de associações de moradores pré-cadastrados) podem invocar este comando.

---

##  5. Requisitos Não Funcionais

### 5.1 Usabilidade

- Interface Intuitiva: A interface do usuário deve possuir navegação fluida, utilizando componentes visuais familiares (como botões iconográficos de mapa e abas inferiores de feed), permitindo que ações complexas como cadastro de doações sejam feitas em menos de 3 cliques.

- Tempo de Aprendizado: O tempo estimado para que um usuário leigo compreenda e execute as funções básicas da plataforma (como abrir um alerta ou buscar uma doação) deve ser menor que 5 minutos de navegação livre, sem necessidade de tutoriais extensos.

- Acessibilidade: A interface web e mobile deve respeitar as diretrizes de acessibilidade WCAG, fornecendo suporte completo para modo de alto contraste, redimensionamento de fontes tipográficas e descrições alternativas nas imagens (alt text) para leitura de tela por deficientes visuais. 

### 5.2 Eficiência

- Tempo de Resposta: As requisições de leitura de dados de API, renderização de feeds textuais e carregamento de informações básicas de perfil devem apresentar um tempo de resposta inferior a 2 segundos em condições normais de conectividade de rede (3G/4G/Wi-Fi).

- Suporte a Múltiplos Usuários: O back-end deve responder de forma eficiente e simultânea a requisições paralelas concorrentes, gerenciando conexões abertas sem degradação do tempo de processamento por meio de técnicas de concorrência e filas.  

### 5.3 Desempenho

- Suporte a Usuários Simultâneos: A infraestrutura de computação deve ser capaz de suportar um volume de até 1.000 usuários ativos navegando simultaneamente na plataforma sem oscilações ou quedas na taxa de transferência de dados (throughput).

- Estabilidade Sob Carga: O sistema deve demonstrar estabilidade operacional sob estresse de carga. Em situações de incidentes climáticos graves no bairro, quando o volume de requisições de leitura e inserção de alertas pode dobrar repentinamente, o sistema deve manter uma taxa de falhas inferior a 1% das requisições totais. 

### 5.4 Espaço

- Limite de Armazenamento: Para preservar a eficiência e controle de custos de infraestrutura, os uploads de imagens anexados a doações e alertas devem possuir um teto de armazenamento físico máximo restrito a 5 MB por arquivo de imagem enviado.

- Uso Eficiente de Memória: O aplicativo móvel e as requisições de front-end web devem processar a renderização do mapa de forma otimizada, destruindo da memória instâncias e marcadores geográficos que estejam localizados fora do quadrante de visualização visível da tela do dispositivo.

### 5.5 Confiabilidade

- Disponibilidade Mínima: A plataforma Conexão Comunitária deve apresentar uma taxa de disponibilidade mínima estipulada em 99,5% do tempo operacional mensal (Uptime), medida ao longo de períodos de 24 horas por dia, 7 dias por semana.

- Recuperação de Falhas: Em cenários de interrupção abrupta de serviços na nuvem ou queda de instâncias, o sistema deve possuir mecanismos automáticos de failover e reinicialização, com tempo estimado de recuperação completa (Recovery Time Objective - RTO) inferior a 5 minutos, restaurando o último estado consistente do banco de dados. 

### 5.6 Segurança (Proteção)

- Autenticação: O mecanismo de autenticação deve exigir validação rigorosa através do padrão de tokens seguros (JSON Web Tokens - JWT) com tempo de expiração determinado, bloqueando o acesso de chamadas de API não autorizadas a rotas privadas.

- Criptografia: Todas as comunicações em trânsito entre o cliente e os servidores devem ser obrigatoriamente criptografadas utilizando o protocolo criptográfico HTTPS/TLS 1.3. Adicionalmente, as senhas armazenadas na base de dados devem utilizar hash criptográfico forte com fator salt (ex: BCrypt).

- Controle de Acesso: O sistema deve operar sob controle de acesso baseado em funções (RBAC - Role-Based Access Control), garantindo distinção absoluta de permissões operacionais entre "Usuários Comuns", "Moderadores/Líderes Comunitários" e "Administradores Gerais".

---

##  6. Requisitos Organizacionais

### 6.1 Ambientais

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

---

## 9. Casos de Uso e Diagramas UML

Esta seção deve representar visualmente e descritivamente o funcionamento do sistema.

Os diagramas ajudam na:
- modelagem do sistema;
- comunicação entre equipe;
- entendimento da arquitetura e funcionalidades;
- documentação técnica do projeto.

---

# 9.1 Casos de Uso

Os casos de uso representam as interações entre usuários (atores) e o sistema.

---

### UC01 - Realizar Login

**Ator:** Usuário  

**Descrição:**  
Permite que o usuário acesse o sistema utilizando credenciais válidas.

---

### Fluxo principal
1. Usuário acessa a tela de login  
2. Usuário informa e-mail e senha  
3. Sistema valida credenciais  
4. Sistema libera acesso  

---

### Fluxo alternativo
- Credenciais inválidas  
- Usuário esqueceu senha  

---

## Exemplo de Diagrama de Caso de Uso

[Usuário]

    |
    
    | ---- (Realizar Login)
    
    | ---- (Cadastrar Conta)
    
    | ---- (Recuperar Senha) 

---

## 9.2 Diagrama de Classes (UML)

O diagrama de classes representa:

- estrutura do sistema;
- entidades;
- atributos;
- métodos;
- relacionamentos.

---

### Exemplo

```text
+------------------+
|     Usuário      |
+------------------+
| - id             |
| - nome           |
| - email          |
| - senha          |
+------------------+
| + login()        |
| + logout()       |
+------------------+
```

---

### Exemplo com relacionamento

```text
+------------------+        +------------------+
|     Usuário      | 1    * |      Pedido      |
+------------------+--------+------------------+
| id               |        | id               |
| nome             |        | valor            |
+------------------+        +------------------+
```

---

## 9.3 Diagrama de Atividades (UML)

Representa o fluxo de execução de processos no sistema.

---

### Exemplo

```text
[Início]
   |
[Acessar sistema]
   |
[Inserir login]
   |
{Credenciais válidas?}
   | Sim
[Acessa sistema]
   |
[Fim]

   | Não
[Mensagem de erro]
```

---

## 9.4 Diagrama de Sequência (UML)

Representa a comunicação entre objetos ao longo do tempo.

---

### Exemplo

```text
Usuário -> Sistema: realizar login
Sistema -> Banco: validar usuário
Banco -> Sistema: usuário válido
Sistema -> Usuário: acesso liberado
```

---

## 9.5 Diagrama de Componentes

Representa os módulos e componentes principais do sistema.

---

### Exemplo

```text
[Frontend]
     |
     v
[API Backend]
     |
     v
[Banco de Dados]
```

---

## 9.6 Diagrama de Implantação (Deployment)

Representa onde o sistema será executado.

---

### Exemplo

```text
[Usuário]
     |
Internet
     |
[Servidor Web]
     |
[Servidor Banco de Dados]
```

---

## 9.7 Ferramentas Recomendadas

Os diagramas podem ser feitos utilizando:

- Draw.io
- Lucidchart
- StarUML
- Visual Paradigm
- PlantUML
- Mermaid
- Figma

---

## 9.8 Observações Importantes

- Os diagramas devem representar o sistema REAL do grupo;
- Evitem diagramas genéricos;
- Mantenham consistência entre requisitos e diagramas;
- Diagramas devem possuir nomes claros;
- Atualizem os diagramas conforme o sistema evoluir.

---

# Regra importante

> “Diagramas não são apenas desenhos: eles representam decisões arquiteturais e técnicas do sistema.”

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
