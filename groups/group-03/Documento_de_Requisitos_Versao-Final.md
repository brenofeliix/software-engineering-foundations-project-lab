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
A arquitetura escolhida para o sistema será em microserviços, permitindo que cada funcionalidade da plataforma funcione de maneira independente e organizada. A escolha dessa arquitetura garante maior escalabilidade, facilidade de manutenção e melhor desempenho do sistema, tornando possível criar uma plataforma educacional moderna, dinâmica e mais atrativa para reduzir a evasão escolar e aumentar o engajamento dos estudantes.

### 8.2 Componentes
- Frontend: Interface visual do sistema, onde alunos e professores poderão acessar aulas, atividades interativas, desafios, rankings e acompanhar o progresso de aprendizagem.   
- Backend: Interface visual do sistema, onde alunos e professores poderão acessar aulas, atividades interativas, desafios, rankings e acompanhar o progresso de aprendizagem. 
- Banco de dados: Interface visual do sistema, onde alunos e professores poderão acessar aulas, atividades interativas, desafios, rankings e acompanhar o progresso de aprendizagem.  
- APIs externas: Interface visual do sistema, onde alunos e professores poderão acessar aulas, atividades interativas, desafios, rankings e acompanhar o progresso de aprendizagem. 

### 8.3 Tecnologias
- Linguagem: JavaScript será utilizada no desenvolvimento do sistema, por ser uma linguagem versátil e amplamente utilizada tanto no frontend quanto no backend.
- Framework: React será utilizado no frontend para criar uma interface interativa e dinâmica, enquanto Node.js será utilizado no backend para processar dados e gerenciar as funcionalidades do sistema.
- Banco de dados: MySQL será utilizado para armazenar informações como cadastro de usuários, desempenho escolar, atividades realizadas, frequência e demais dados necessários para o funcionamento da plataforma.  

### 8.4 Decisões Arquiteturais
A arquitetura foi planejada para atender aos principais requisitos não funcionais do sistema, garantindo qualidade, estabilidade e capacidade de crescimento da plataforma.

- Desempenho: A utilização de microserviços permite que diferentes funções do sistema operem de forma independente, reduzindo sobrecarga e melhorando o tempo de resposta durante o acesso simultâneo de vários usuários  
- Segurança: A utilização de microserviços permite que diferentes funções do sistema operem de forma independente, reduzindo sobrecarga e melhorando o tempo de resposta durante o acesso simultâneo de vários usuários.
- Escalabilidade: A arquitetura escolhida permite expandir o sistema de maneira gradual, adicionando novos serviços e funcionalidades sem comprometer o funcionamento geral da plataforma, suportando o aumento de usuários ao longo do tempo.

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
