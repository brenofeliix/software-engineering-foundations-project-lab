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

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
Explique o sistema de forma resumida.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais

### RF01 - Nome do requisito
**Descrição:**  
Descreva a funcionalidade.

**Prioridade:** Alta / Média / Baixa  
**Entradas:**  
**Saídas:**  
**Regras de negócio:**  

---

### RF02 - Nome do requisito
(repita o padrão)

---

##  5. Requisitos Não Funcionais

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
- Deve otimizar o uso de memória durante a execução.
- Deve permitir acesso sem necessidade de instalação (via navegador).
- Deve minimizar o uso de dados móveis (internet).
- O sistema deve ocupar pouco espaço de armazenamento nos dispositivos.

### 5.5 Confiabilidade
- O sistema deve ter disponibilidade contínua do sistema.
- O sistema deve ter recuperação rápida em caso de falhas.
- O sistema deve possuir armazenamento seguro das informações.
- O sistema deve conter consistência dos dados acadêmicos. 

### 5.6 Segurança (Proteção)
- O sistema deve proteger os dados dos usuários (login e informações pessoais).
- O sistema deve implementar autenticação de usuários segura (ex: login com criptografia de senha).
- O sistema deve implementar níveis de acesso por perfil de usuário (ex: aluno, professor e administrador), limitando o acesso às funcionalidades.
- O sistema deve validar todas as entradas do usuário no cliente e no servidor, garantindo proteção contra ataques como SQL Injection e XSS.
- O sistema deve conter recuperação de senha segura (via e-mail).

---

##  6. Requisitos Organizacionais

### 6.1 Ambientais
- Infraestrutura tecnológica adequada (internet estável, computadores, tablets) 
- Acesso a plataformas digitais educacionais
- Conectividade para alunos e professores dentro da instituição
- Disponibilidade de equipamentos para uso em sala

### 6.2 Operacionais
- Comunicação eficiente entre professores, alunos e coordenação  
- Registro e acompanhamento do desempenho acadêmico
- Monitoramento contínuo do engajamento e frequência dos alunos
- Definição de regras para uso de dispositivos em sala de aula  

### 6.3 Desenvolvimento
- Atualização constante dos conteúdos e métodos aplicados  
- Treinamentos para uso de ferramentas digitais
- Adoção de padrões pedagógicos atualizados
- Capacitação contínua de professores

---
