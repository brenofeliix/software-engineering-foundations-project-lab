#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo

Este documento tem como objetivo apresentar a visão geral do produto CromStudy, descrevendo o problema identificado, os usuários-alvo, a solução proposta e as funcionalidades planejadas. Ele serve como referência para a equipe de desenvolvimento, garantindo o alinhamento entre os membros ao longo de todas as etapas do projeto.

O CromStudy tem como objetivo auxiliar estudantes do Ensino Médio e vestibulandos na organização de sua rotina de estudos, promovendo foco, constância e eficiência no aprendizado por meio de ferramentas integradas de planejamento, revisão e gamificação.

### 1.2 Escopo

O CromStudy é um aplicativo voltado para estudantes do Ensino Médio e vestibulandos que necessitam de estrutura e organização em sua rotina acadêmica, disponível nas versões mobile e web (notebooks e desktops). O sistema oferece as seguintes funcionalidades:

### Dentro do escopo do sistema:

- Agenda e Cronograma - Planejamento de tarefas diárias, semanais e mensais com visualização em checklist.

- Método Pomodoro - Temporizador de estudo com ciclos de 25 minutos de foco e 5 minutos de intervalo.

- Flashcards - Criação de cartões de memorização com registro de acertos e erros.

- Métricas de Estudo - Relatórios de desempenho com base no tempo estudado e no aproveitamento nos flashcards.

- Sistema de Alertas - Notificações e alertas sonoros para revisões, tarefas e ciclos do Pomodoro.

- Minijogo - Quiz baseado nos flashcards do usuário com recompensas para construção de um mundo virtual.

### Fora do escopo do sistema:

- Integração com plataformas educacionais externas (ex: Google Classroom, Moodle).

- Comunicação ou colaboração em tempo real entre usuários.

- Geração automática de conteúdo de estudo ou questões por inteligência artificial.

- Funcionalidades de pagamento ou assinatura premium.

- Suporte a usuários do Ensino Fundamental ou Ensino Superior..

### 1.3 Definições, Acrônimos e Abreviações

- **CromStudy** - Nome do aplicativo mobile de organização de estudos desenvolvido pelo Grupo 06.

- **Pomodoro** - Técnica de gestão de tempo que alterna ciclos de foco (25 min) e intervalos curtos (5 min).

- **Flashcard** - Cartão de memorização com uma pergunta na frente e a resposta no verso, usado para revisão ativa de conteúdo.

- **Checklist** - Lista de tarefas com caixas de seleção que podem ser marcadas conforme concluídas.

- **Minijogo** - Funcionalidade de gamificação do Fostudy baseada em quiz com recompensas virtuais.

- **Quiz** -  Conjunto de perguntas e respostas geradas a partir dos flashcards criados pelo usuário.

- **Avatar** - Personagem virtual personalizável pelo usuário dentro do minijogo do Fostudy.

- **Métrica** - Indicador de desempenho calculado com base no tempo de estudo e resultados dos flashcards.

- **Alerta** - Notificação sonora ou visual enviada ao usuário pelo sistema em momentos definidos.

- **Feedback** - Retorno de resposta ou avaliação ao usuário relacionado com os conteúdos com mais erros no quiz, indicando quais conteúdos devem ser priorizados e estudados com mais frequência. 

- **Escalabilidade** - Capacidade do aplicativo manter bom desempenho à medida que haja acréscimo de novas funções e aumento de usuários.

- **Backend** - Área não acessada e visível para o usuário, como: códigos, documentação sobre o aplicativo, sistema de segurança, banco de dados.

- **30 FPS (Frames Per Second ou Quadros Por Segundo)** - Quantidade de imagens exibidas por segundo para criar ilusão de movimento. 

- **Android 8+ e iOS 13+** - Versões mínimas dos sistemas operacionais Android e iOS com capacidade de suportar aplicativos e funções mais exigentes, não suportadas por versões inferiores.

- **APK** (Android Package Kit ou Pacote de Aplicativo Android) - Formato de aplicativo (app) usado para instalação de app em dispositivos Android.

- **IPA** (iPhone Application ou Aplicativo para iPhone) -  Formato de aplicativo usado para a instalação de app em dispositivos iOS.

- **WCAG** (Web Content Accessibility Guidelines ou Diretrizes de Acessibilidade para Conteúdo Web) - Diretrizes para tornar conteúdos digitais acessíveis para pessoas com deficiência.

- **Criptografia** - Prática de transformar informações legíveis em formato ilegível a fim de proteger dados e informações contra roubos, alteração e acesso não autorizado. 

- **Hash** - Um dos métodos usados para criptografar dados, transformando-os em um código de tamanho fixo.

- **LGPD** (Lei Geral de Proteção de Dados) - Lei brasileira que obriga órgãos e empresas a protegerem os dados e informações de seus usuários contra vazamento e roubo.

---

##  2. Product Vision

### 2.1 Problema
Muitos estudantes enfrentam dificuldades na organização de suas rotinas de estudos, como definir horários, manter a constância e revisar conteúdos de forma eficiente. Essa falta de organização pode levar a perda de foco, desorganização e baixo rendimento nos estudos.

### 2.2 Solução
O CromStudy é um aplicativo que visa ajudar principalmente na organização e foco dos estudantes durante o processo de estudos. Para isso, é disponibilizado algumas funções: agenda, cronograma, Flashcards, Método Pomodoro, métrica de estudos, sistema de alerta e mini game. 

### 2.3 Público-Alvo
O público-alvo é composto por estudantes do ensino médio e vestibulandos do ENEM que necessitam de estrutura e organização no ambiente acadêmico para atingir metas escolares de maneira eficiente e prática.

### 2.4 Proposta de Valor
O sistema é importante porque auxilia estudantes a organizarem melhor seu tempo e manterem uma rotina de estudos mais eficiente e produtiva. Dessa forma, o aplicativo busca centralizar ferramentas essenciais de planejamento, controle e motivação em uma única plataforma, facilitando o gerenciamento dos estudos.

### 2.5 Diferencial
O principal diferencial está na integração de múltiplas funcionalidades em uma única aplicação, combinando agenda, cronograma, métricas de desempenho, flashcards, sistemas de alertas e elementos de gamificação por meio de um mini game educativo. Essa abordagem proporciona uma experiência mais dinâmica e motivadora, incentivando a criação de hábitos de estudos consistentes e melhorando o egajamento de usuário durante o processo de aprendizagem.

### 2.6 Funcionalidades principais (alto nível)
**01 - Agenda**

Estará disponível uma agenda para a verificação de datas, a fim de ajudar o usuário no momento de criação de seu cronograma e melhor visualização de datas e tarefas de maneira micro e macro. Com isso, será possível verificar dias, semanas, meses e ano. 

**02 - Cronograma**

Em cada dia da semana, a pessoa incluirá as tarefas a serem executadas e concluídas ao longo da semana e dia. Após a inclusão, as atividades diárias serão organizadas em formato de cheklist, que poderão ser marcadas, por causa das caixas de seleção, assim que as tarefas forem concluídas. 

**03 - Método Pomodoro**

O Método Pomodoro visa a definição de tempo para o processo de estudo e intervalo. Para auxiliar o estudante, o software indicará um tempo corrido de 25min para o estudo de um conteúdo e, após a finalização desse tempo, um tempo de 5mim de intervalo é iniciado. Com a finalização do intervalo, é ativado novamente o tempo de 25min, assim sucessivamente até que o conteúdo seja completamente estudado ou seu tempo total diário seja atingido. Por exemplo, a pessoa estabecele um total de 2h para estudar um conteúdo específico, ou seja, uma das tarefas inseridas no cronograma. Esse tempo de 2h será fracionado em 25min, sem contar o tempo de intervalo. Além disso, ao clicar na atividade a ser realizada no momento, o Método Pomodoro enviará uma mensagem sugerindo um tempo de estudo, com a intenção de não haver demora, o que contribui para a procrastinação e desistência.

**04 - Flashcards**

Para ajudar na revisão e aprendizagem dos conteúdos, será possível a criação de flashcards, um método de estudo que consiste na formação de uma pergunta em um card e a reposta no verso desse card. O estudante deverá responder a pergunta antes de verificar a resposta no verso no card. Após responder e verificar, o usuário deverá marcar uma das opções que aparecer "Acertei" ou "Errei". 

**05 - Métrica de estudo**

Baseado no tempo de estudo e quantidade de erros e acertos dos flashcards, um relatório será criado, com o objetivo de mostrar a evolução do usuário ao longo dos estudos. Referente a quantidade de acertos e erros dos Flashcards, o software indicará ao usuário quais conteúdos devem ser revisados com mais frequência ( conteúdos com mais erros) e  quais podem ter revisões espaçadas (conteúdos com mais acertos).

**06 - Sistema de alerta**

O sistema de alerta será incluído com o objetivo de enviar notificações relacionadas às revisões aos estudantes e às atividades inseridas no cronograma a serem estudadas no dia determinado. Isto é, quando o usuário criar seu cronograma, ele definirá um horário para que seja lembrado sobre seus afazeres do dia, além de receber um lembrete para as revisões agendadas. Também, ao término do tempo de estudo (aplicação do Método Pomodoro), o usuário receberá alertas sonoros  sobre a finalização do tempo de estudo e intervalo e, início do tempo de intervalo. 

**07 - Game**

Será incluído um mini game ao aplicativo CromStudy. Esse jogo tem relação com um mundo vazio com avatares a ser construído desde o início pelo próprio usuário. Para isso, o estudante deverá jogar um quiz baseado nos conteúdos dos flashcards criados. Ao término do jogo, a pessoa receberá pontuações, que acumularão e serão utilizadas para desbloquear cada item para construir o mini mundo de seu avatar: casa, roupas, alimentos, pets, avatares, etc.

### 2.7 Concorrentes
Os três principais concorrentes do CromStudy são:
- Aprovado - Controle de Estudos (Sand Robot)
- Forest: Mantenha o foco (Seektech)
- Notion: notas, tarefas e IA (Notion Labs, Inc.)

---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
O CromStudy é um aplicativo voltado para estudantes que enfrentam dificuldades na organização dos estudos, foco e baixa constância ao longo do tempo. Muitos usuários apresentam desafios no gerenciamento de tarefas, na realização de revisões eficientes e na manutenção da disciplina, o que impacta diretamente seu desempenho acadêmico.

Com o objetivo de mitigar esses problemas, o CromStudy oferece uma plataforma integrada que reúne funcionalidades como agenda, cronograma de estudos, método Pomodoro, flashcards, métricas de desempenho, sistema de alertas e elementos de gamificação. Essas ferramentas atuam de forma complementar, auxiliando o estudante no planejamento, execução e acompanhamento de seus estudos de maneira estruturada e contínua.

O público-alvo do sistema é composto por estudantes do ensino médio e vestibulandos que estão se preparando para o ENEM, e que buscam aprimorar sua organização, produtividade e desempenho acadêmico.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Estudantes do Ensino Médio 
- Vestibulandos do ENEM
- Equipe de Desenvolvimento
  
---

##  4. Requisitos Funcionais

## RF01 - Cadastro de Usuário

**Descrição:**
O sistema deve permitir que o usuário crie uma conta utilizando e-mail e senha para acesso à plataforma.

**Prioridade:** Alta

**Entradas:**

* Nome do usuário
* E-mail
* Senha

**Saídas:**

* Conta cadastrada com sucesso
* Mensagem de erro em caso de dados inválidos

**Regras de negócio:**

* O e-mail deve ser único no sistema.
* A senha deve possuir no mínimo 8 caracteres.
* O sistema deve validar o formato do e-mail.

---

## RF02 - Gerenciamento de Cronograma Semanal

**Descrição:**
O sistema deve permitir ao usuário criar, editar e excluir cronogramas semanais de estudos.

**Prioridade:** Alta

**Entradas:**

* Matéria
* Horário
* Dias da semana

**Saídas:**

* Cronograma salvo e exibido ao usuário

**Regras de negócio:**

* O usuário pode possuir múltiplos cronogramas.
* O sistema deve impedir conflitos de horários.

---

## RF03 - Execução do Método Pomodoro

**Descrição:**
O sistema deve permitir a execução do método Pomodoro com temporizador automático e intervalos programados.

**Prioridade:** Alta

**Entradas:**

* Quantidade de ciclos

**Saídas:**

* Contagem regressiva do tempo
* Alertas de início e fim dos ciclos

**Regras de negócio:**

* O sistema deve iniciar automaticamente o intervalo após o término do foco.
* O usuário pode pausar ou encerrar o cronômetro.

---

## RF04 - Gerenciamento de Flashcards

**Descrição:**
O sistema deve permitir criar, editar, excluir e revisar flashcards com registro de desempenho.

**Prioridade:** Alta

**Entradas:**

* Pergunta
* Resposta
* Categoria/Tema

**Saídas:**

* Flashcard salvo
* Histórico de desempenho do usuário

**Regras de negócio:**

* O sistema deve registrar acertos e erros.
* O usuário pode revisar flashcards ilimitadamente.

---

## RF05 - Geração de Relatórios de Desempenho

**Descrição:**
O sistema deve gerar relatórios com base no tempo de estudo e resultados obtidos nos flashcards.

**Prioridade:** Média

**Entradas:**

* Dados de sessões de estudo
* Resultados dos flashcards

**Saídas:**

* Relatórios estatísticos
* Gráficos de desempenho

**Regras de negócio:**

* O sistema deve atualizar os relatórios automaticamente.
* Os relatórios devem considerar apenas dados do usuário autenticado.

---

## RF06 - Controle de Alertas

**Descrição:**
O sistema deve permitir ativar ou desativar notificações e alertas.

**Prioridade:** Média

**Entradas:**

* Preferência do usuário

**Saídas:**

* Confirmação da alteração de configuração

**Regras de negócio:**

* O usuário pode alterar as notificações a qualquer momento.
* As alterações devem ser salvas automaticamente.

---

## RF07 - Gerenciamento de Tarefas

**Descrição:**
O sistema deve permitir a criação, edição e exclusão de tarefas.

**Prioridade:** Alta

**Entradas:**

* Nome da tarefa
* Data
* Horário
* Descrição

**Saídas:**

* Tarefa cadastrada ou atualizada

**Regras de negócio:**

* O usuário pode marcar tarefas como concluídas.
* O sistema deve organizar tarefas por data.

---

## RF08 - Desbloqueio de Itens do Minigame

**Descrição:**
O sistema deve permitir o desbloqueio de itens dentro do minigame.

**Prioridade:** Média

**Entradas:**

* Pontuação do usuário
* Solicitação de desbloqueio

**Saídas:**

* Item desbloqueado

**Regras de negócio:**

* Apenas usuários com pontuação suficiente podem desbloquear itens.
* Itens desbloqueados devem permanecer vinculados à conta do usuário.

---

## RF09 - Visualização da Agenda Online e Offline

**Descrição:**
O sistema deve permitir a visualização da agenda mesmo sem conexão com a internet.

**Prioridade:** Alta

**Entradas:**

* Dados da agenda

**Saídas:**

* Agenda exibida ao usuário

**Regras de negócio:**

* O sistema deve sincronizar os dados quando houver conexão.
* Dados offline devem permanecer armazenados localmente.

---

## RF10 - Acúmulo de Pontuações em Quizzes

**Descrição:**
O sistema deve acumular pontuações obtidas nos quizzes e permitir sua utilização para desbloquear itens do mini mundo.

**Prioridade:** Média

**Entradas:**

* Resultado dos quizzes

**Saídas:**

* Atualização da pontuação do usuário

**Regras de negócio:**

* As pontuações devem ser acumulativas.
* O sistema deve impedir saldo negativo de pontos.

---

## RF11 - Identificação de Conteúdos com Maior Índice de Erros

**Descrição:**
O sistema deve identificar conteúdos com maior índice de erros nos quizzes e sugerir revisões prioritárias.

**Prioridade:** Média

**Entradas:**

* Histórico de respostas dos quizzes

**Saídas:**

* Lista de conteúdos prioritários para revisão

**Regras de negócio:**

* O sistema deve calcular o percentual de erros por tema.
* As recomendações devem ser atualizadas automaticamente.

---

## RF12 - Geração Automática de Quizzes

**Descrição:**
O sistema deve gerar quizzes automaticamente com base nos flashcards criados pelo usuário.

**Prioridade:** Alta

**Entradas:**

* Flashcards cadastrados

**Saídas:**

* Quiz gerado automaticamente

**Regras de negócio:**

* O sistema deve selecionar perguntas aleatoriamente.
* O quiz deve respeitar a matéria ou tema escolhido.

---

## RF13 - Personalização de Avatar

**Descrição:**
O sistema deve permitir a personalização do avatar utilizando itens desbloqueados.

**Prioridade:** Baixa

**Entradas:**

* Seleção de itens pelo usuário

**Saídas:**

* Avatar atualizado

**Regras de negócio:**

* Apenas itens desbloqueados podem ser utilizados.
* As alterações devem ser salvas automaticamente.

---

## RF14 - Organização de Flashcards

**Descrição:**
O sistema deve organizar os flashcards por matéria ou tema.

**Prioridade:** Alta

**Entradas:**

* Categoria definida pelo usuário

**Saídas:**

* Flashcards agrupados por tema

**Regras de negócio:**

* Um flashcard deve pertencer a pelo menos uma categoria.
* O usuário pode alterar a categoria posteriormente.

---

## RF15 - Edição de Perfil do Usuário

**Descrição:**
O sistema deve permitir que o usuário edite seus dados de perfil.

**Prioridade:** Média

**Entradas:**

* Nome
* Foto de perfil
* Senha
* Informações pessoais

**Saídas:**

* Perfil atualizado

**Regras de negócio:**

* O sistema deve solicitar autenticação para alteração de senha.
* As alterações devem ser refletidas imediatamente no perfil do usuário.

---

##  5. Requisitos Não Funcionais

### 5.1 Usabilidade
- O sistema deve apresentar uma interface intuitiva e de fácil navegação, adequada ao público estudantil. 

- As principais funcionalidades devem ser acessadas em até 5 interações do usuário. 

- O sistema deve fornecer feedback visual imediato após ações realizadas. 

- O sistema deve possuir design simples e organizado, reduzindo distrações durante o uso.

- O sistema deverá possuir um botão de acessibilidade localizado na lateral direita da interface, permitindo ativar recursos de leitura por voz para usuários com deficiência visual e suporte em Libras para usuários com deficiência auditiva ou de fala.

### 5.2 Eficiência  
- Suporte a múltiplos usuários  
- O aplicativo deve responder rapidamente às ações do usuário para evitar atrasos durante o uso
- O aplicativo deve minimizar o consumo de bateria durante o uso contínuo
  
### 5.3 Desempenho
- O sistema deve garantir uma experiência fluida, respondendo a requisições de carregamento de tela em até 2 segundos em conexões 4G ou Wi-Fi.

- O timer do Método Pomodoro deve iniciar ou pausar em no máximo 300ms após o comando do usuário, garantindo precisão imediata nas sessões de foco.

- Para manter o fluxo de aprendizado sem interrupções, os Flashcards devem carregar e exibir seu conteúdo em até 1 segundo.

- O relatório de métricas de estudo deve ser gerado e exibido em até 1,5 segundos se os dados estiverem em cache local, ou até 3 segundos mediante o uso de uma animação de carregamento para otimizar a percepção de espera.

- Em termos de escalabilidade, a infraestrutura do backend deve suportar 10.000 usuários simultâneos sem qualquer degradação de performance.

- O sistema deve ser capaz de absorver picos de até 15.000 usuários simultâneos por períodos de até 10 minutos, garantindo a estabilidade em momentos de alta demanda.

- O sistema de alertas deve ser altamente confiável, disparando notificações com uma tolerância máxima de atraso de apenas 5 segundos em relação ao horário configurado pelo estudante.

- No que diz respeito ao Mini Game, o desempenho gráfico deve ser estável, mantendo uma taxa de atualização mínima de 30 FPS em dispositivos Android 8+ ou iOS 13+.

- O aplicativo deve permitir o funcionamento pleno em modo offline para as funções de cronograma, flashcards e Pomodoro, garantindo a continuidade dos estudos sem internet.

- O tamanho total do pacote de instalação (APK/IPA) deve ser mantido em até 80MB, utilizando técnicas de compressão de assets, especialmente para os elementos do mini game.

- O sistema deve garantir a acessibilidade, sendo totalmente compatível com leitores de tela e seguindo padrões de contraste WCAG 2.1 para assegurar a inclusão de todos os usuários  

### 5.4 Espaço
- Limite de armazenamento  
- Uso eficiente de memória
- Recursos não utilizados devem ser liberados automaticamente
- O minigame não deve comprometer funções principais do app

### 5.5 Confiabilidade  
- O sistema deve realizar salvamento automático
- O sistema deve registrar corretamente pontos, experiência e conquistas do usuário

### 5.6 Segurança (Proteção)
- O sistema deve exigir autenticação
segura por meio de login e senha,
podendo incluir biometria. 
- As senhas dos usuários devem ser
armazenadas utilizando criptografia com
hash seguro. 
- O sistema deve bloquear
temporariamente o acesso após
múltiplas tentativas inválidas.
- Os dados do usuário devem ser
protegidos contra acessos não
autorizados. 
- O aplicativo deve seguir a LGPD.  

---

##  6. Requisitos Organizacionais

### 6.1 Ambientais
- O sistema deverá ser compatível com dispositivos Android e IOS.
- O aplicativo deverá funcionar em diferentes resoluções de tela.
- O sistema deverá utilizar banco de dados para armazenamento das informações dos usuários.
- A infraestrutura deverá suportar múltiplos acessos simultâneos.
  
### 6.2 Operacionais
- O sistema deverá registrar erros e falhas de execução. 
- Os logs deverão auxiliar na identificação e correção de problemas do sistema.
- O sistema deverá identificar falhas de disponibilidade dos serviços.

### 6.3 Desenvolvimento
- O projeto deverá utilizar o Git para controle de versões.
- O sistema deverá manter histórico de alterações no código-fonte.
- O sistema deverá utilizar boas práticas de programação.
- O código-fonte deverá ser organizado e documentado.
- Os testes automatizados deverão auxiliar na redução de falhas e erros do sistema.

---

##  7. Requisitos Externos

### 7.1 Reguladores
- O sistema deverá estar em conformidade com a Lei Geral de Proteção de Dados (LGPD), garantindo proteção dos dados pessoais cadastrados pelos estudantes, como nome, e-mail e histórico de estudos.
- O aplicativo deverá solicitar autorização do usuário antes de enviar notificações e alertas relacionados ao cronograma e sessões de estudo.
- O sistema deverá garantir armazenamento seguro das métricas de desempenho, flashcards e informações da agenda do usuário.
  
### 7.2 Éticos
- O sistema não deverá utilizar métricas de desempenho para expor, constranger ou comparar usuários de forma negativa.
- O aplicativo deverá apresentar de forma transparente como os dados de estudo e produtividade são utilizados pelo sistema.
- O mini game integrado deverá incentivar hábitos saudáveis de estudo, evitando estímulos excessivos ou comportamentos prejudiciais ao usuário.

### 7.3 Legais
- O sistema deverá disponibilizar termos de uso e política de privacidade durante o cadastro do usuário.
- O aplicativo deverá respeitar direitos autorais relacionados aos conteúdos adicionados nos flashcards e materiais cadastrados pelos usuários.
- O sistema deverá cumprir legislações brasileiras relacionadas ao armazenamento de dados digitais e privacidade dos usuários.

### 7.4 Segurança Externa
- O sistema deverá proteger contas de usuários contra acessos não autorizados por meio de autenticação segura.
- O aplicativo deverá criptografar dados sensíveis, como senhas e informações pessoais dos estudantes.

### 7.5 Contábeis
- O sistema deverá registrar transações caso haja monetização.
- O sistema deve permitir a exportação de dados financeiros para softwares contábeis.
- O sistema deve seguir as normas fiscais e tributárias brasileiras.
---
