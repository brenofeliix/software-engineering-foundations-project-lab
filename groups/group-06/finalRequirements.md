#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
Descrever o objetivo deste documento e do sistema.

### 1.2 Escopo
Descrever o que o sistema faz, seus limites e o que está fora do escopo.

### 1.3 Definições, Acrônimos e Abreviações
Liste termos importantes utilizados no documento.

---

##  2. Product Vision

### 2.1 Problema
Muitos estudantes enfrentam dificuldades na organização de suas rotinas de estudos, como definir horários, manter a constância e revisar conteúdos de forma eficiente. Essa falta de organização pode levar a perda de foco, desorganização e baixo rendimento nos estudos.

### 2.2 Solução
O Fostudy é um aplicativo que visa ajudar principalmente na organização e foco dos estudantes durante o processo de estudos. Para isso, é disponibilizado algumas funções: agenda, cronograma, Flashcards, Método Pomodoro, métrica de estudos, sistema de alerta e mini game. 

01 - Agenda 

Estará disponível uma agenda para a verificação de datas, a fim de ajudar o usuário no momento de criação de seu cronograma e melhor visualização de datas e tarefas de maneira micro e macro. Com isso, será possível verificar dias, semanas, meses e ano. 

02 - Cronograma 

Em cada dia da semana, a pessoa incluirá as tarefas a serem executadas e concluídas ao longo da semana e dia. Após a inclusão, as atividades diárias serão organizadas em formato de cheklist, que poderão ser marcadas, por causa das caixas de seleção, assim que as tarefas forem concluídas. 

03 - Método Pomodoro 

O Método Pomodoro visa a definição de tempo para o processo de estudo e intervalo. Para auxiliar o estudante, o software indicará um tempo corrido de 25min para o estudo de um conteúdo e, após a finalização desse tempo, um tempo de 5mim de intervalo é iniciado. Com a finalização do intervalo, é ativado novamente o tempo de 25min, assim sucessivamente até que o conteúdo seja completamente estudado ou seu tempo total diário seja atingido. Por exemplo, a pessoa estabecele um total de 2h para estudar um conteúdo específico, ou seja, uma das tarefas inseridas no cronograma. Esse tempo de 2h será fracionado em 25min, sem contar o tempo de intervalo. Além disso, ao clicar na atividade a ser realizada no momento, o Método Pomodoro enviará uma mensagem sugerindo um tempo de estudo, com a intenção de não haver demora, o que contribui para a procrastinação e desistência.

04 - Flashcards 

Para ajudar na revisão e aprendizagem dos conteúdos, será possível a criação de flashcards, um método de estudo que consiste na formação de uma pergunta em um card e a reposta no verso desse card. O estudante deverá responder a pergunta antes de verificar a resposta no verso no card. Após responder e verificar, o usuário deverá marcar uma das opções que aparecer "Acertei" ou "Errei". 

05 - Métrica de estudo

Baseado no tempo de estudo e quantidade de erros e acertos dos flashcards, um relatório será criado, com o objetivo de mostrar a evolução do usuário ao longo dos estudos. Referente a quantidade de acertos e erros dos Flashcards, o software indicará ao usuário quais conteúdos devem ser revisados com mais frequência ( conteúdos com mais erros) e  quais podem ter revisões espaçadas (conteúdos com mais acertos).

06 - Sistema de alerta 

O sistema de alerta será incluído com o objetivo de enviar notificações relacionadas às revisões aos estudantes e às atividades inseridas no cronograma a serem estudadas no dia determinado. Isto é, quando o usuário criar seu cronograma, ele definirá um horário para que seja lembrado sobre seus afazeres do dia, além de receber um lembrete para as revisões agendadas. Também, ao término do tempo de estudo (aplicação do Método Pomodoro), o usuário receberá alertas sonoros  sobre a finalização do tempo de estudo e intervalo e, início do tempo de intervalo. 

07 - Game 

Será incluído um mini   game ao aplicativo Fostudy. Esse jogo tem relação com um mundo vazio com avatares a ser construído desde o início pelo próprio usuário. Para isso, o estudante deverá jogar um quiz baseado nos conteúdos dos flashcards criados. Ao término do jogo, a pessoa receberá pontuações, que acumularão e serão utilizadas para desbloquear cada item para construir o mini mundo de seu avatar: casa, roupas, alimentos, pets, avatares, etc.

### 2.3 Público-Alvo
O público-alvo é composto por estudantes do ensino médio e vestibulandos do ENEM que necessitam de estrutura e organização no ambiente acadêmico para atingir metas escolares de maneira eficiente e prática.

### 2.4 Proposta de Valor
Por que esse sistema é importante?

### 2.5 Diferencial
O que torna esse sistema melhor que outros?

### 2.6 Funcionalidades principais (alto nível)
- Funcionalidade 1
- Funcionalidade 2

### 2.7 Concorrentes
Os três principais concorrentes do Fostudy são:
- Aprovado - Controle de Estudos (Sand Robot)
- Forest: Mantenha o foco (Seektech)
- Notion: notas, tarefas e IA (Notion Labs, Inc.)

---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
O FoStudy é um aplicativo voltado para estudantes que enfrentam dificuldades na organização dos estudos, foco e baixa constância ao longo do tempo. Muitos usuários apresentam desafios no gerenciamento de tarefas, na realização de revisões eficientes e na manutenção da disciplina, o que impacta diretamente seu desempenho acadêmico.

Com o objetivo de mitigar esses problemas, o FoStudy oferece uma plataforma integrada que reúne funcionalidades como agenda, cronograma de estudos, método Pomodoro, flashcards, métricas de desempenho, sistema de alertas e elementos de gamificação. Essas ferramentas atuam de forma complementar, auxiliando o estudante no planejamento, execução e acompanhamento de seus estudos de maneira estruturada e contínua.

O público-alvo do sistema é composto por estudantes do ensino médio e vestibulandos que estão se preparando para o ENEM, e que buscam aprimorar sua organização, produtividade e desempenho acadêmico.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais

- FR1: O sistema deve permitir que o usuário crie uma conta com email e senha.

- FR2: O sistema deve permitir ao usuário criar e gerenciar um cronograma semanal de estudos.

- FR3: O sistema deve permitir a execução do método Pomodoro com contagem automática de tempo e intervalos.

- FR4: O sistema deve permitir a criação, edição e revisão de flashcards com registro de desempenho.

- FR5: O sistema deve gerar relatórios com base no tempo de estudo e nos resultados dos flashcards.

- FR6: O sistema deve permitir que o usuário ative ou desative o sistema de alerta.

- FR7: O sistema deve permitir a criação e modificação de uma nova tarefa.

- FR8: O sistema deve permitir o desbloqueio de itens no minigame.

- FR9: O sistema deve permitir a visualização da agenda online e offline.

- FR10: O sistema deve acumular as pontuações obtidas nos quizzes e permitir que sejam usadas para desbloquear itens do mini mundo.

- FR11: O sistema deve identificar e indicar os conteúdos com maior índice de erros nos quizzes, sugerindo revisão prioritária ao usuário. 

- FR12: O sistema deve gerar quizzes automaticamente com base nos flashcards criados pelo usuário. 

- FR13: O sistema deve permitir a personalização do avatar com itens desbloqueados

- FR14: O sistema deve organizar os flashcards por matéria ou tema

- FR15: O sistema deve permitir que o usuário edite seus dados de perfil.

---

##  5. Requisitos Não Funcionais

### 5.1 Usabilidade
- O sistema deve apresentar uma interface intuitiva e de fácil navegação, adequada ao público estudantil. 

- As principais funcionalidades devem ser acessadas em até 5 interações do usuário. 

- O sistema deve fornecer feedback visual imediato após ações realizadas. 

- O sistema deve possuir design simples e organizado, reduzindo distrações durante o uso. 

### 5.2 Eficiência
- Tempo de resposta < X segundos  
- Suporte a múltiplos usuários  

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

### 5.5 Confiabilidade
- Disponibilidade mínima (ex: 99,9%)  
- Recuperação de falhas  

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
