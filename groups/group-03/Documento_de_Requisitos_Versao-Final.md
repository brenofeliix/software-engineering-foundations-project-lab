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
- Pais ou Responsáveis: acompanham o progresso e engajamento dos alunos.
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

- Acessibilidade e inclusão: O sistema deve assegurar que todos os usuários possam utilizar a plataforma em condições equivalentes de acesso e usabilidade.
  
- Transparência: O sistema deve assegurar clareza na coleta, armazenamento e utilização de dados acadêmicos e pessoais dos usuários.

- Inclusão educacional: O sistema deve promover acessibilidade e usabilidade compatíveis com diferentes perfis de estudantes, incluindo usuários com deficiência.

---

### 7.3 Legais

- LGPD (Lei Geral de Proteção de Dados): O sistema deve estar em conformidade com a Lei nº 13.709/2018, garantindo privacidade, segurança e tratamento adequado das informações pessoais.

- Direitos autorais: O sistema deve respeitar a legislação de direitos autorais aplicada a conteúdos pedagógicos, documentos e materiais disponibilizados na plataforma.

- Normas educacionais: O sistema deve atender às regulamentações definidas pelos órgãos competentes, como MEC e BNCC.

---

### 7.4 Segurança Externa

- Proteção contra ataques: O sistema deve implementar mecanismos de segurança contra ataques cibernéticos, incluindo autenticação segura e controle de acesso.

- Auditorias: O sistema deve manter registros de auditoria para rastreamento das operações realizadas por usuários e administradores.

- Criptografia: O sistema deve utilizar protocolos de criptografia para proteção de dados sensíveis durante armazenamento e transmissão.

- Backup e recuperação: O sistema deve possuir políticas de backup e recuperação de dados para garantir continuidade operacional em casos de falha.

---

### 7.5 Contábeis

- Registro de transações: O sistema deve registrar transações financeiras e operacionais de forma íntegra, consistente e auditável.

- Relatórios: O sistema deve gerar relatórios contábeis e financeiros para apoio à gestão administrativa e prestação de contas.

- Histórico financeiro: O sistema deve manter histórico de movimentações financeiras para rastreabilidade e conferência de informações.

- Conformidade fiscal: O sistema deve garantir conformidade com normas contábeis e fiscais aplicáveis à instituição.
  
---

##  8. Arquitetura do Sistema

### 8.1 Visão Geral
A arquitetura escolhida para o sistema será em microserviços, permitindo que cada funcionalidade da plataforma funcione de maneira independente e organizada. A escolha dessa arquitetura garante maior escalabilidade, facilidade de manutenção e melhor desempenho do sistema, tornando possível criar uma plataforma educacional moderna, dinâmica e mais atrativa para reduzir a evasão escolar e aumentar o desempenho dos estudantes.

### 8.2 Componentes
- Frontend: Interface visual do sistema, onde alunos e professores poderão acessar aulas, atividades interativas, desafios, rankings e acompanhar o progresso de aprendizagem.   
- Backend: Responsável pelo processamento das informações, gerenciamento das funcionalidades do sistema, autenticação de usuários, regras de negócio e controle das atividades educacionais. . 
- Banco de dados: Armazena informações dos usuários, conteúdos das aulas, desempenho dos alunos, frequência, histórico de atividades e dados necessários para o funcionamento da plataforma.   
- APIs externas: Utilizadas para integração com serviços complementares, como envio de notificações, autenticação, recursos multimídia e ferramentas que auxiliem na experiência interativa do aprendizado. 

### 8.3 Tecnologias
- Linguagem: JavaScript será utilizada no desenvolvimento do sistema, por ser uma linguagem versátil e amplamente utilizada tanto no frontend quanto no backend.
- Framework: React será utilizado no frontend para criar uma interface interativa e dinâmica, enquanto Node.js será utilizado no backend para processar dados e gerenciar as funcionalidades do sistema.
- Banco de dados: MySQL será utilizado para armazenar informações como cadastro de usuários, desempenho escolar, atividades realizadas, frequência e demais dados necessários para o funcionamento da plataforma.  

### 8.4 Decisões Arquiteturais
A arquitetura foi planejada para atender aos principais requisitos não funcionais do sistema, garantindo qualidade, estabilidade e capacidade de crescimento da plataforma.

- Desempenho: A utilização de microserviços permite que diferentes funções do sistema operem de forma independente, reduzindo sobrecarga e melhorando o tempo de resposta durante o acesso simultâneo de vários usuários  
- Segurança: O sistema contará com autenticação de usuários, controle de acesso por níveis (aluno e professor), criptografia de dados sensíveis e proteção das informações armazenadas no banco de dados. 
- Escalabilidade: A arquitetura escolhida permite expandir o sistema de maneira gradual, adicionando novos serviços e funcionalidades sem comprometer o funcionamento geral da plataforma, suportando o aumento de usuários ao longo do tempo.

---

## 9. Casos de Uso e Diagramas UML


# 9.1 Casos de Uso

### UC01 - Autenticação e Gerenciamento de Conta
Ator: Usuário (Aluno, Professor ou Administrador)

Descrição: Permite que o usuário realize o cadastro inicial no sistema, acesse a plataforma por meio de credenciais validadas, solicite a recuperação de senhas e gerencie os dados informados em seu perfil.



Fluxo principal
Usuário acessa a interface inicial e escolhe realizar o cadastro ou autenticação.

Usuário insere as informações e credenciais requeridas.

Sistema criptografa a senha de forma automática e realiza a validação do login.

Sistema autentica o usuário e libera o acesso às funções mapeadas ao seu respectivo perfil.



Fluxo alternativo
Credenciais inválidas ou falha na validação de permissões pelo sistema.

Usuário executa a rotina para recuperar senha por esquecimento.

Usuário edita informações ou realiza a visualização do perfil após o login.

Usuário realiza o encerramento da sessão ativa utilizando a opção Sair.



### UC02 - Execução de Atividades Pedagógicas e Jogos
Ator: Aluno

Descrição: Permite ao aluno acessar as trilhas de aprendizado da plataforma, selecionar a disciplina desejada e responder a questões e atividades práticas utilizando os jogos educativos.



Fluxo principal
Aluno acessa o ambiente de trilhas de aprendizagem da plataforma.

Sistema classifica de forma automática o aluno por idade e ano escolar para personalizar o conteúdo exposto.

Aluno seleciona a matéria e escolhe a disciplina específica que planeja estudar.

Aluno inicia o jogo didático e responde às atividades integradas.

Sistema registra o desempenho do aluno e armazena os dados no histórico de maneira automática.



Fluxo alternativo
Aluno decide praticar ativando o Modo Sortido para responder atividades aleatórias.


### UC03 - Evolução e Recompensas (Gamificação)
Ator: Aluno

Descrição: Mapeia os recursos internos de engajamento do aluno baseados no acúmulo de experiência (XP), recebimento de conquistas por metas batidas, controle de sequência de estudos (streak) e compras na loja virtual.



Fluxo principal
Aluno interage no sistema e conclui as tarefas pedagógicas propostas.

Sistema atualiza de forma automática os indicadores de XP, nível, ranking e o streak de acessos seguidos.

Aluno é condecorado e recebe conquistas associadas à evolução demonstrada.

Aluno realiza a consulta ao ranking geral para verificar seu posicionamento.



Fluxo alternativo
Aluno acessa a loja interna da plataforma para comprar recompensas utilizando os pontos coletados.

### UC04 - Participação e Cooperação em Grupos
Ator: Aluno

Descrição: Permite que o estudante faça parte de turmas escolares ou grupos de estudo virtuais, acompanhe os comunicados enviados e cumpra missões designadas.



Fluxo principal
Aluno insere o código ou convite recebido para entrar no grupo.

Aluno participa das atividades integradas do grupo e visualiza as missões pedagógicas disponibilizadas.

Aluno realiza e conclui as missões que foram publicadas para a sua turma.

Sistema envia notificações automáticas e expõe avisos emitidos para o aluno.



Fluxo alternativo
Aluno realiza apenas a leitura de notificações e avisos sem iniciar missões pendentes.



### UC05 - Organização de Grupos e Avisos (Professor)
Ator: Professor

Descrição: Engloba as funções concedidas ao professor para coordenar suas turmas de alunos na plataforma, engajando a criação de novas salas, controle de membros e emissão de avisos informativos.



Fluxo principal
Professor solicita a criação de um novo grupo no sistema.

Sistema gera automaticamente o código de convite exclusivo para compartilhamento.

Professor gerencia o grupo realizando a adição ou a remoção manual de alunos.

Professor digita e realiza o envio de avisos gerais direcionados aos estudantes vinculados.



Fluxo alternativo
Professor seleciona e executa a exclusão permanente de um grupo ou turma existente.



### UC06 - Controle e Gestão de Missões (Professor)
Ator: Professor

Descrição: Responsável pela manutenção pedagógica e publicação de tarefas e missões voltadas aos grupos moderados pelo educador.



Fluxo principal
Professor acessa a área operacional da turma e aciona a opção para criar uma nova missão.

Professor preenche os requisitos e publica a missão oficial para que fique visível ao grupo de alunos.



Fluxo alternativo
Professor localiza uma missão em aberto para realizar edições ou excluí-la de circulação.



### UC07 - Monitoramento de Evolução Acadêmica
Ator: Professor ou Aluno

Descrição: Provê relatórios visuais e históricos do progresso, permitindo ao aluno monitorar seu avanço e ao professor obter indicadores pedagógicos unificados das turmas.



Fluxo principal
Usuário acessa o painel de monitoramento (o Aluno visualiza seu progresso pessoal; o Professor seleciona a opção de visualizar seus alunos).

Sistema recupera as informações do banco e realiza a montagem do histórico e evolução.

Professor acompanha o rendimento da turma e emite relatórios consolidados sobre o desempenho dos estudantes.



Fluxo alternativo
Professor ou aluno executa uma consulta rápida nos rankings da disciplina para verificação do progresso contextual.



## UC08 - Administração Geral e Infraestrutura do Sistema
Ator: Administrador

Descrição: Concede total autoridade técnica ao administrador para operar e manter a integridade operacional e pedagógica do sistema educacional.



Fluxo principal
Administrador realiza o login e o sistema executa a validação automática das permissões administrativas.

Administrador acessa os painéis operacionais para gerenciar usuários cadastrados (professores e alunos).

Administrador gerencia conteúdos pedagógicos e disciplinas, podendo cadastrar, editar, excluir ou publicar matérias e gerenciar o funcionamento dos jogos.

Administrador gerencia as regras e itens da loja, parâmetros de rankings e a entrega de recompensas.

Sistema gera de forma contínua o registro de logs de auditoria e executa rotinas de backup automático para preservação dos dados.



Fluxo alternativo
Administrador acessa a aba gerencial para visualizar estatísticas de uso gerais da plataforma.

Administrador dispara comandos manuais pontuais para forçar a realização de um backup do sistema.

---



# Casos de Uso do Sistema

## Usuário

```text
[Usuário]
│
├── (Cadastrar Conta)
├── (Realizar Login)
├── (Recuperar Senha)
├── (Gerenciar Perfil)
└── (Encerrar Sessão)
```

---

## Aluno

```text
[Aluno]
│
├── (Acessar Trilhas de Aprendizagem)
├── (Selecionar Disciplina)
├── (Responder Atividades)
├── (Jogar Jogos Educativos)
├── (Utilizar Modo Sortido)
├── (Ganhar XP)
├── (Receber Conquistas)
├── (Visualizar Streak)
├── (Consultar Ranking)
├── (Comprar Recompensas na Loja)
├── (Entrar em Grupo)
├── (Visualizar Missões)
├── (Realizar Missões)
├── (Visualizar Avisos)
└── (Receber Notificações)
```

---

## Professor

```text
[Professor]
│
├── (Criar Grupo)
├── (Gerenciar Grupo)
│   ├── (Adicionar Alunos)
│   └── (Remover Alunos)
├── (Enviar Avisos)
├── (Excluir Grupo)
├── (Criar Missão)
├── (Publicar Missão)
├── (Editar Missão)
├── (Excluir Missão)
├── (Visualizar Progresso dos Alunos)
├── (Emitir Relatórios)
└── (Consultar Ranking)
```

---

## Administrador

```text
[Administrador]
│
├── (Realizar Login)
├── (Gerenciar Usuários)
├── (Gerenciar Conteúdos)
├── (Gerenciar Disciplinas)
├── (Gerenciar Jogos)
├── (Gerenciar Loja)
├── (Gerenciar Recompensas)
├── (Gerenciar Rankings)
├── (Visualizar Estatísticas)
├── (Visualizar Logs)
└── (Executar Backup)
```

---

# Visão Geral

```text
                              [Usuário]
                                  │
          ┌───────────────────────┼────────────────────────┐
          │                       │                        │
  (Cadastrar Conta)      (Realizar Login)      (Recuperar Senha)
          │
  (Gerenciar Perfil)
          │
  (Encerrar Sessão)


                              [Aluno]
                                  │
 ┌──────────────┬─────────────────┬────────────────┬─────────────────┐
 │              │                 │                │                 │
(Acessar) (Selecionar) (Responder Atividades) (Jogar) (Modo Sortido)
                                                │
                                                ▼
                                         (Ganhar XP)
                                                │
                                         (Receber Conquistas)
                                                │
                                        (Visualizar Streak)
                                                │
                                        (Consultar Ranking)
                                                │
                                   (Comprar Recompensas)
                                                │
                                         (Entrar em Grupo)
                                                │
                        ┌───────────────────────┼─────────────────────┐
                        │                       │                     │
               (Visualizar Missões)   (Realizar Missões)   (Visualizar Avisos)
                                                │
                                       (Receber Notificações)


                            [Professor]
                                 │
 ┌───────────────┬─────────────────────┬────────────────────┐
 │               │                     │                    │
(Criar Grupo) (Gerenciar Grupo) (Criar Missão) (Visualizar Progresso)
      │               │                    │                    │
      │         ┌─────┴─────┐        ┌─────┴─────┐              │
      │         │           │        │           │              │
(Enviar Avisos) (Adicionar) (Remover) (Editar) (Excluir) (Emitir Relatórios)
                                                   │
                                          (Consultar Ranking)


                          [Administrador]
                                │
 ┌───────────────┬────────────────┬────────────────┬────────────────┐
 │               │                │                │                │
(Gerenciar   (Gerenciar      (Gerenciar      (Gerenciar      (Gerenciar
 Usuários)    Conteúdos)        Jogos)           Loja)         Rankings)
        │
(Visualizar Estatísticas)
        │
(Visualizar Logs)
        │
(Executar Backup)
```

## 9.2 Diagrama de Classes (UML)

## Classe: Usuário

```text
+---------------------------+
|          Usuário          |
+---------------------------+
| - id                      |
| - nome                    |
| - email                   |
| - senha                   |
| - tipo                    |
+---------------------------+
| + login()                 |
| + logout()                |
| + cadastrar()             |
| + recuperarSenha()        |
| + editarPerfil()          |
+---------------------------+
```



## Classe: Aluno

```text
+---------------------------+
|          Aluno            |
+---------------------------+
| - idade                   |
| - anoEscolar              |
| - xp                      |
| - nivel                   |
| - streak                  |
+---------------------------+
| + responderAtividade()    |
| + ganharXP()              |
| + visualizarProgresso()   |
| + entrarGrupo()           |
| + comprarItem()           |
+---------------------------+
```



## Classe: Professor

```text
+---------------------------+
|        Professor          |
+---------------------------+
| - instituicao             |
+---------------------------+
| + criarGrupo()            |
| + removerAluno()          |
| + criarMissao()           |
| + editarMissao()          |
| + enviarAviso()           |
| + visualizarRelatorio()   |
+---------------------------+
```



## Classe: Administrador

```text
+---------------------------+
|      Administrador        |
+---------------------------+
| - permissao               |
+---------------------------+
| + gerenciarUsuarios()     |
| + gerenciarConteudos()    |
| + gerenciarJogos()        |
| + executarBackup()        |
| + visualizarLogs()        |
+---------------------------+
```



## Classe: Grupo

```text
+---------------------------+
|          Grupo            |
+---------------------------+
| - id                      |
| - nome                    |
| - codigo                  |
| - descricao               |
+---------------------------+
| + adicionarAluno()        |
| + removerAluno()          |
| + gerarCodigo()           |
+---------------------------+
```



## Classe: Missão

```text
+---------------------------+
|         Missão            |
+---------------------------+
| - id                      |
| - titulo                  |
| - descricao               |
| - recompensaXP            |
| - dataLimite              |
+---------------------------+
| + publicar()              |
| + editar()                |
| + excluir()               |
+---------------------------+
```



## Classe: Disciplina

```text
+---------------------------+
|        Disciplina         |
+---------------------------+
| - id                      |
| - nome                    |
+---------------------------+
| + listarAtividades()      |
+---------------------------+
```


## Classe: Atividade

```text
+---------------------------+
|        Atividade          |
+---------------------------+
| - id                      |
| - titulo                  |
| - dificuldade             |
| - pontuacao               |
+---------------------------+
| + iniciar()               |
| + finalizar()             |
+---------------------------+
```



## Classe: Jogo

```text
+---------------------------+
|          Jogo             |
+---------------------------+
| - id                      |
| - nome                    |
| - tipo                    |
+---------------------------+
| + iniciarJogo()           |
| + registrarResultado()    |
+---------------------------+
```


## Classe: Histórico

```text
+---------------------------+
|        Histórico          |
+---------------------------+
| - id                      |
| - data                    |
| - pontuacao               |
+---------------------------+
| + registrar()             |
| + consultar()             |
+---------------------------+
```



## Classe: Conquista

```text
+---------------------------+
|        Conquista          |
+---------------------------+
| - id                      |
| - nome                    |
| - descricao               |
+---------------------------+
| + desbloquear()           |
+---------------------------+
```



## Classe: Ranking

```text
+---------------------------+
|         Ranking           |
+---------------------------+
| - id                      |
| - posicao                 |
| - pontuacao               |
+---------------------------+
| + atualizar()             |
+---------------------------+
```



## Classe: Loja

```text
+---------------------------+
|           Loja            |
+---------------------------+
| - id                      |
| - nome                    |
+---------------------------+
| + listarItens()           |
| + venderItem()            |
+---------------------------+
```


## Classe: ItemLoja

```text
+---------------------------+
|        ItemLoja           |
+---------------------------+
| - id                      |
| - nome                    |
| - precoXP                 |
+---------------------------+
| + aplicarBonus()          |
+---------------------------+
```

# Relacionamento

```text
Usuário 1 -------- 1 Aluno

Usuário 1 -------- 1 Professor

Usuário 1 -------- 1 Administrador

Professor 1 -------- * Grupo

Aluno * -------- * Grupo

Grupo 1 -------- * Missão

Disciplina 1 -------- * Atividade

Jogo 1 -------- * Atividade

Aluno 1 -------- * Histórico

Aluno * -------- * Conquista

Aluno 1 -------- 1 Ranking

Loja 1 -------- * ItemLoja
```
    

## 9.3 Diagrama de Atividades (UML)

Representa o fluxo de execução de processos no sistema.

---

<img width="669" height="2074" alt="diagrama-atividades drawio" src="https://github.com/user-attachments/assets/a20935cf-df53-4a23-8a12-3d86392bcb6e" />

---

## 9.4 Diagrama de Sequência (UML)

Representa a comunicação entre objetos ao longo do tempo.

---

<img width="1440" height="900" alt="diagrama-sequencia drawio" src="https://github.com/user-attachments/assets/74b1d436-715d-4194-bafe-d4b6bb32e639" />

---

## 9.5 Diagrama de Componentes

Representa os módulos e componentes principais do sistema.

---

### Exemplo

<img width="1384" height="733" alt="diagrama-componentes drawio" src="https://github.com/user-attachments/assets/9e7524ee-b413-49ef-9e8b-aaff4a82c513" />

---

## 9.6 Diagrama de Implantação (Deployment)

Representa onde o sistema será executado.

---

### Exemplo

<img width="1158" height="804" alt="diagrama-implantacao drawio" src="https://github.com/user-attachments/assets/df39b044-f11f-4a62-86d4-ff36b7f06f75" />

---

## 10. Plano de Testes

### 10.1 Estratégia de Teste

A validação do sistema será realizada de forma incremental ao longo do ciclo de desenvolvimento, visando garantir a conformidade com os requisitos funcionais e não funcionais especificados. Serão aplicadas diferentes técnicas de teste, abrangendo desde a verificação individual dos componentes até a validação do sistema em ambiente integrado. Os testes de aceitação serão conduzidos com usuários representativos do público-alvo, a fim de avaliar a aderência da solução às necessidades identificadas.

### 10.2 Tipos de Teste

- **Teste Unitário: Verificação individual de métodos, funções e componentes do sistema.
- **Teste de Integração: Validação da comunicação e interoperabilidade entre módulos.
- **Teste de Sistema: Avaliação do comportamento do sistema como um todo em ambiente controlado.
- **Teste de Aceitação: Validação dos requisitos junto aos usuários e demais partes interessadas.

### 10.3 Casos de Teste

#### CT01 – Cadastro de Aluno

**Requisito Relacionado: RF01

**Descrição:** Verificar a capacidade do sistema de realizar o cadastro de novos alunos.

**Dados de Entrada:
- Nome completo;
- E-mail válido;
- Senha válida;
- Idade;
- Ano escolar.

**Resultado Esperado:  
O sistema deve registrar os dados informados e criar a conta do usuário com sucesso.

---

#### CT02 – Autenticação de Usuário

**Requisito Relacionado: RF04

**Descrição:** Verificar a autenticação de usuários previamente cadastrados.

**Dados de Entrada:
- E-mail válido;
- Senha correspondente.

**Resultado Esperado: 
O sistema deve permitir o acesso do usuário às funcionalidades autorizadas.

---

#### CT03 – Registro de Sequência de Estudos (Streak)

**Requisito Relacionado: RF11

**Descrição: Verificar o registro e a atualização da sequência diária de estudos.

**Dados de Entrada:
- Acessos consecutivos realizados em dias subsequentes.

**Resultado Esperado: 
O sistema deve atualizar corretamente o contador de sequência de estudos.

### 10.4 Testes de Requisitos Não Funcionais

#### Desempenho

- Avaliar o tempo de resposta das funcionalidades críticas.
- Verificar a capacidade do sistema sob condições de carga previstas.
- Validar a escalabilidade da solução.

#### Segurança

- Verificar mecanismos de autenticação e autorização.
- Avaliar a proteção de dados dos usuários.
- Testar a resistência a vulnerabilidades comuns, como SQL Injection e XSS.

#### Usabilidade

- Avaliar a facilidade de utilização da interface.
- Verificar a navegabilidade do sistema.
- Validar a adequação da solução ao público-alvo.

---

## 11. Critérios de Aceitação

Os requisitos serão considerados aceitos quando atenderem aos seguintes critérios:

- Todos os casos de teste previstos forem executados com sucesso;
- Os requisitos funcionais forem implementados conforme especificado;
- O tempo de resposta permanecer dentro dos limites estabelecidos;
- Não forem identificadas falhas críticas que comprometam a utilização do sistema;
- Os mecanismos de segurança estiverem operando conforme os requisitos definidos;
- Os usuários participantes dos testes de aceitação validarem o funcionamento adequado da solução.

---

## 12. Restrições

### Restrições Tecnológicas

- O sistema deverá operar por meio de conexão com a internet.
- A solução deverá ser compatível com dispositivos móveis e computadores.
- A infraestrutura utilizada deverá suportar múltiplos acessos simultâneos.
- O sistema deverá manter tempo de resposta inferior a três segundos em condições normais de operação.

### Restrições Legais

- O sistema deverá realizar o tratamento dos dados pessoais dos usuários em conformidade com a Lei Geral de Proteção de Dados Pessoais (LGPD – Lei nº 13.709/2018).
- O armazenamento e processamento das informações dos usuários deverão respeitar os princípios de privacidade, finalidade, necessidade e segurança previstos na legislação vigente.
- O conteúdo educacional disponibilizado na plataforma deverá respeitar a legislação relacionada à propriedade intelectual e aos direitos autorais.

### Restrições de Prazo

- O desenvolvimento do sistema deverá ser concluído dentro do período estabelecido pelo cronograma do projeto.
- As atividades de análise, implementação, testes e validação deverão ser realizadas dentro dos prazos definidos para cada etapa do desenvolvimento.
- A versão final do sistema deverá estar disponível para avaliação e entrega até a data prevista pela instituição ou disciplina responsável pelo projeto.
- Eventuais alterações de escopo após a aprovação dos requisitos poderão impactar os prazos inicialmente estabelecidos..

---

## 13. Premissas

- Os usuários possuirão acesso à internet para utilização da plataforma.
- Os dispositivos utilizados atenderão aos requisitos mínimos para execução do sistema.
- Os alunos fornecerão informações corretas durante o processo de cadastro.
- Os professores utilizarão a plataforma para gerenciamento de grupos e acompanhamento do desempenho dos alunos.
- A infraestrutura tecnológica necessária para hospedagem e operação do sistema estará disponível durante todo o período de utilização.

---

## 14. Observações Finais

Este documento estabelece os requisitos e critérios necessários para o desenvolvimento do sistema educacional gamificado proposto. As especificações apresentadas servirão como referência para as atividades de análise, desenvolvimento, testes e validação, contribuindo para a construção de uma solução alinhada aos objetivos pedagógicos e tecnológicos definidos para o projeto.