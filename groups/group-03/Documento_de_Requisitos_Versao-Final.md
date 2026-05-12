#  Documento de Requisitos e Projeto de Software

---

## 1. Introdução

### 1.1 Objetivo
Este documento tem como objetivo descrever de forma clara e organizada os requisitos do sistema educacional baseado em gamificação. Ele serve como base para o desenvolvimento, validação e manutenção do sistema, alinhando as expectativas entre desenvolvedores, usuários e demais stakeholders.

### 1.2 Escopo
O sistema tem como finalidade oferecer uma plataforma educacional interativa voltada para alunos do 6º ao 9º ano do ensino fundamental, utilizando jogos educativos como ferramenta de apoio ao aprendizado.

A aplicação permitirá o cadastro e autenticação de usuários, personalização do conteúdo com base na idade e ano escolar, disponibilização de atividades por disciplina e em modo sortido, além de recursos de gamificação, como sistema de streak (sequência de estudos).

Também será possível a criação de grupos por professores ou instituições, permitindo o acompanhamento do desempenho dos alunos e promovendo interação no ambiente educacional.

Fora do escopo do sistema estão funcionalidades como substituição do ensino formal, emissão de certificados oficiais e integração com sistemas educacionais governamentais.

### 1.3 Definições, Acrônimos e Abreviações

- **Gamificação:** Uso de elementos de jogos (pontuação, desafios, recompensas) em contextos não relacionados a jogos, com o objetivo de aumentar o engajamento.
- **Streak (Ofensiva):** Contagem de dias consecutivos em que o usuário utiliza o sistema.
- **Usuário:** Qualquer pessoa que utiliza o sistema (aluno, professor ou administrador).
- **Aluno:** Usuário principal do sistema, responsável por realizar atividades e jogos educativos.
- **Professor:** Usuário responsável por acompanhar alunos e gerenciar grupos.
- **Grupo:** Conjunto de alunos organizados por um professor ou instituição dentro da plataforma.
- **Sistema:** Plataforma educacional desenvolvida neste projeto.

---

## 2. Product Vision

### 2.1 Problema
Cada vez torna-se mais comum a evasão escolar e o alto nível de desinteresse nas escolas, isso se deve, em partes, a forma de lecionar antiquada que ainda vem sendo muito utilizada adolescentes sentados em uma cadeira durante horas ao longo de uma semana realizando atividades cansativas que geralmente não gera bons resultados.

### 2.2 Solução
Nosso projeto vem com a proposta de levar o estudo de forma intuitiva e estimulante, querendo auxiliar na vida acadêmica dos adoslescentes. A proposta são jogos interativos que vão auxiliar no entendimento e fixação, vem como um auxilio para apresentação de trabalho e provas. A partir dessa forma de ensinar, mostrar aos alunos que estudar pode sim ser divertido.

### 2.3 Público-Alvo
Serão crianças/pré adolescentes que cursam entre o 6° ao 9° ano.

### 2.4 Proposta de Valor
Para tornar mais acessível o conteúdo do ensino básico. Auxiliando aqueles que ainda estão na escola à aprender de forma mais efetiva e divertida. Mas também pode auxiliar pessoas que já terminaram a escola, ou que não terminaram o ensino básico, a aprender/relembrar as partes mais fundamentais do ensino.

### 2.5 Diferencial
Nosso sistema tem como principal diferencial a oferta de diversas matérias da grade curricular do ensino fundamental. Diferentemente da concorrência, não será um produto que oferece apenas aprendizado de uma área, como linguagens, mas sim todo o escopo do ensino fundamental, como matemática, história, geografia, artes, e muitos outros. Além de promover a interação entre usuários da plataforma para ensinar uns aos outros por meio de grupos.

### 2.6 Funcionalidades principais (alto nível)
- Trilhas das matérias da grade curricular do MEC e BNCC.
- Grupos entre usuários comuns(grupos de estudo), com intuito de impulsionar o aprendizado por meio da interação social.
- Grupos entre alunos e professores de uma escola em comum(salas de aula), onde o professor pode passar atividades("missões") com recompensas para seus alunos, assim como fazer avisos.
- Sistema de ofensiva, que grava quantos dias seguidos o usuário tem utilizado o aplicativo.
- Sistema de "Loja", onde usuários podem comprar meios para impulsionar o ganho de "XP/experiência" na plataforma.

---

## 3. Visão Geral do Sistema

### 3.1 Descrição Geral
O projeto consiste no desenvolvimento de um sistema educacional baseado em gamificação dos estudos, com o objetivo de tornar o aprendizado mais dinâmico, interativo e motivador para alunos do ensino fundamental.

A plataforma será voltada para estudantes do 6º ao 9º ano, que, após realizarem um cadastro simples, terão acesso a um login individual. Durante o cadastro, o aluno informará sua idade e o ano escolar em que está, permitindo que o sistema personalize automaticamente sua experiência de aprendizagem.

Com base nessas informações, o aplicativo será responsável por organizar e direcionar as atividades, disponibilizando jogos educativos adequados ao nível do aluno. Os jogos serão divididos por matérias como Português, Matemática, História, entre outras mas também haverá a opção de atividades no modo sortido, trazendo variedade e estimulando diferentes áreas do conhecimento.

Além disso, o sistema contará com elementos típicos de gamificação para aumentar o engajamento, como o controle de sequência de estudos "streak", que registra quantos dias seguidos o aluno utilizou a plataforma, incentivando a constância nos estudos.

Outro recurso importante será o sistema de grupos, permitindo que professores ou escolas criem turmas dentro da plataforma. Dessa forma, será possível acompanhar o desempenho dos alunos, promover interação e integrar o uso do aplicativo ao ambiente escolar.

No geral, o projeto busca unir tecnologia e educação de forma acessível, tornando o processo de aprendizagem mais leve, divertido e eficiente.


### 3.2 Stakeholders
- Alunos (usuários finais): utilizam a plataforma para estudar por meio de jogos educativos.
- Professores: acompanham o desempenho dos alunos, criam ou gerenciam turmas e utilizam a plataforma como apoio pedagógico.
- Escolas/Instituições de Ensino: adotam o sistema para uso educacional e acompanham resultados gerais.
- Pais ou Responsáveis: acompanham o progresso e engajamento dos alunos.
- Desenvolvedores: responsáveis pela criação, manutenção e evolução do sistema.
- Equipe de suporte: presta auxílio técnico aos usuários e resolve problemas.
- Administradores do sistema: gerenciam usuários, conteúdos e funcionamento geral da plataforma.
- Equipe pedagógica: define conteúdos e valida os jogos educativos.
- Gestores escolares: analisam relatórios e resultados.

---

## 4. Requisitos Funcionais

### RF01 - Cadastro de aluno
**Descrição:**  
O sistema deve permitir que o aluno realize seu cadastro informando dados básicos.

**Prioridade:** Alta  
**Entradas:** Nome, idade, ano escolar, e-mail, senha  
**Saídas:** Cadastro realizado  

---

### RF02 - Geração de login
**Descrição:**  
O sistema deve gerar automaticamente um login após o cadastro do aluno.

**Prioridade:** Alta  
**Entradas:** Dados do cadastro  
**Saídas:** Conta criada  

---

### RF03 - Informar idade e ano escolar
**Descrição:**  
O sistema deve permitir que o aluno informe sua idade e ano escolar.

**Prioridade:** Alta  
**Entradas:** Idade, ano escolar  
**Saídas:** Dados armazenados  

---

### RF04 - Login e autenticação
**Descrição:**  
O sistema deve permitir que o usuário realize login utilizando suas credenciais.

**Prioridade:** Alta  
**Entradas:** E-mail, senha  
**Saídas:** Acesso ao sistema  

---

### RF05 - Classificação do aluno
**Descrição:**  
O sistema deve classificar o aluno com base na idade e no ano escolar.

**Prioridade:** Média  
**Entradas:** Idade, ano escolar  
**Saídas:** Categoria do aluno  

---

### RF06 - Disponibilizar atividades
**Descrição:**  
O sistema deve disponibilizar atividades compatíveis com a categoria do aluno.

**Prioridade:** Alta  
**Entradas:** Categoria do aluno  
**Saídas:** Lista de atividades  

---

### RF07 - Jogos por disciplina
**Descrição:**  
O sistema deve oferecer jogos organizados por disciplina.

**Prioridade:** Alta  
**Entradas:** Seleção de disciplina  
**Saídas:** Jogos disponíveis  

---

### RF08 - Escolha de disciplina
**Descrição:**  
O sistema deve permitir que o aluno escolha a disciplina desejada.

**Prioridade:** Alta  
**Entradas:** Disciplina escolhida  
**Saídas:** Conteúdo da disciplina  

---

### RF09 - Modo sortido
**Descrição:**  
O sistema deve oferecer atividades aleatórias de diferentes disciplinas.

**Prioridade:** Média  
**Entradas:** Seleção do modo sortido  
**Saídas:** Jogos variados  

---

### RF10 - Registro de desempenho
**Descrição:**  
O sistema deve registrar o desempenho do aluno nos jogos.

**Prioridade:** Alta  
**Entradas:** Resultados das atividades  
**Saídas:** Desempenho armazenado  

---

### RF11 - Sistema de streak (ofensiva)
**Descrição:**  
O sistema deve registrar e gerenciar a sequência de dias consecutivos de uso da plataforma.

**Prioridade:** Média  
**Entradas:** Acessos do aluno  
**Saídas:** Contagem de dias consecutivos  

---

### RF12 - Criação de grupos
**Descrição:**  
O sistema deve permitir que professores ou instituições criem grupos.

**Prioridade:** Alta  
**Entradas:** Nome do grupo  
**Saídas:** Grupo criado  

---

### RF13 - Entrada em grupos
**Descrição:**  
O sistema deve permitir que alunos entrem em grupos.

**Prioridade:** Alta  
**Entradas:** Código ou convite  
**Saídas:** Aluno adicionado ao grupo  

---

### RF14 - Visualização de desempenho (professor)
**Descrição:**  
O sistema deve permitir que professores visualizem o desempenho dos alunos.

**Prioridade:** Alta  
**Entradas:** Seleção de grupo ou aluno  
**Saídas:** Relatórios de desempenho  

---

### RF15 - Histórico de atividades
**Descrição:**  
O sistema deve armazenar o histórico de atividades do aluno.

**Prioridade:** Média  
**Entradas:** Resultados das atividades  
**Saídas:** Histórico armazenado  

---

### RF16 - Visualização de progresso (aluno)
**Descrição:**  
O sistema deve permitir que o aluno visualize seu progresso.

**Prioridade:** Média  
**Entradas:** Dados de desempenho  
**Saídas:** Relatório de progresso  

---

### RF17 - Acompanhamento de progresso (professor)
**Descrição:**  
O sistema deve permitir que professores acompanhem o progresso dos alunos.

**Prioridade:** Alta  
**Entradas:** Dados dos alunos  
**Saídas:** Relatórios  

---

### RF18 - Trilhas de aprendizagem
**Descrição:**  
O sistema deve disponibilizar trilhas de aprendizagem das matérias do ensino fundamental.

**Prioridade:** Alta  
**Entradas:** Seleção de matéria  
**Saídas:** Conteúdo organizado  

---

## 5. Requisitos Não Funcionais

### 5.1 Usabilidade
- O sistema deve possuir interface intuitiva e de fácil navegação, mesmo para novos usuários.
- O sistema deve ser fácil de navegar, com linguagem acessível, adequada para crianças e adolescentes.
- O sistema deve ser responsivo (adaptável a celular e desktop).
- O usuário deve conseguir realizar ações principais em até 3 cliques.
- O sistema deve fornecer mensagens de erro claras e orientativas.

### 5.2 Eficiência
- O sistema deve otimizar o carregamento de conteúdos, como vídeos e atividades interativas.
- O sistema deve suportar múltiplos usuários simultaneamente sem queda de desempenho.
- O sistema deve reduzir etapas desnecessárias, tornando o uso rápido e prático.
- O sistema deve garantir fluidez na navegação, evitando travamentos.  

### 5.3 Desempenho
- O sistema deve responder às ações do usuário em até 3 segundos em condições normais.
- O sistema deve suportar múltiplos usuários simultaneamente sem degradação significativa (ex: 10.000+ usuários online).
- O sistema deve ser escalável para suportar crescimento no número de usuários e dados.
- O sistema deve implementar atualizações de pontuação, rankings e conquistas devem ocorrer em tempo quase real.
  
### 5.4 Espaço
- O sistema deve otimizar o uso de memória durante a execução.
- O sistema deve permitir acesso sem necessidade de instalação (via navegador).
- O sistema deve minimizar o uso de dados móveis (internet).
- O sistema deve ocupar pouco espaço de armazenamento nos dispositivos.

### 5.5 Confiabilidade
- O sistema deve ter disponibilidade contínua do sistema.
- O sistema deve ter recuperação rápida em caso de falhas.
- O sistema deve possuir armazenamento seguro das informações.
- O sistema deve conter consistência dos dados acadêmicos. 

### 5.6 Segurança
- O sistema deve proteger os dados dos usuários (login e informações pessoais).
- O sistema deve implementar autenticação de usuários segura (ex: login com criptografia de senha).
- O sistema deve implementar níveis de acesso por perfil de usuário (ex: aluno, professor e administrador), limitando o acesso às funcionalidades.
- O sistema deve validar todas as entradas do usuário no cliente e no servidor, garantindo proteção contra ataques como SQL Injection e XSS.
- O sistema deve conter recuperação de senha segura (via e-mail).

---

## 6. Requisitos Organizacionais

### 6.1 Ambientais
- Infraestrutura tecnológica adequada (internet estável, computadores, tablets).
- Acesso a plataformas digitais educacionais.
- Conectividade para alunos e professores dentro da instituição.
- Disponibilidade de equipamentos para uso em sala.

### 6.2 Operacionais
- Definição de políticas de uso do sistema em ambiente escolar.  
- Disponibilidade de suporte técnico para usuários.  
- Realização de treinamento para professores e alunos.  
- Monitoramento do uso do sistema pela instituição.

### 6.3 Desenvolvimento
- O sistema deve ser desenvolvido seguindo boas práticas de engenharia de software.  
- O sistema deve utilizar ferramentas de controle de versão.  
- O sistema deve permitir manutenção e evolução contínua.  
- O sistema deve seguir padrões de qualidade e documentação de software.

---

##  7. Requisitos Externos

### 7.1 Reguladores
- LGPD (Lei Geral de Proteção de Dados): O sistema deve cumprir rigorosamente os artigos 14 e 15 da LGPD, que tratam do tratamento de dados de crianças e adolescentes. Isso implica a necessidade de consentimento específico e em destaque dado por pelo menos um dos pais ou pelo responsável legal para o tratamento de dados pessoais de menores.

- BNCC e MEC: Os conteúdos pedagógicos inseridos nas trilhas de aprendizagem devem estar estritamente alinhados às competências e habilidades definidas pela Base Nacional Comum Curricular (BNCC) para o Ensino Fundamental II.

- Acessibilidade (LBI): O software deve seguir a Lei Brasileira de Inclusão (Lei 13.146) e as diretrizes do WCAG 2.1, garantindo que alunos com deficiência visual ou motora possam utilizar o app de forma equivalente aos demais.

### 7.2 Éticos
- Não discriminação  
- Transparência
- Inclusão educacional 

### 7.3 Legais
- Leis aplicáveis
- Direitos autorais  

### 7.4 Segurança Externa
- Proteção contra ataques  
- Auditorias
- Criptografia

### 7.5 Contábeis
- Registro de transações  
- Relatórios  

---
