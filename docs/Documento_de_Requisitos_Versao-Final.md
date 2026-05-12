#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
Este documento tem como objetivo definir os requisitos, a arquitetura e as diretrizes funcionais para o desenvolvimento do novo Sistema Digital do Restaurante Universitário (RU) da Universidade Federal de Rondonópolis (UFR), o PODE PAPAR. O sistema visa modernizar a gestão de créditos e o acesso à informação, substituindo processos manuais e presenciais por uma solução digital modular que garanta agilidade, transparência e eficiência no atendimento à comunidade acadêmica. 

### 1.2 Escopo
O que o sistema faz:
- Gestão de Créditos: Permite a compra de créditos via Pix e cartão de crédito, e consulta de saldo em tempo real por meio de dispositivos móveis ou web. (?)
- Informação ao Usuário: Disponibiliza o cardápio atualizado e comunicados oficiais da administração do RU.
- Módulo Gerenciador: Oferece uma interface administrativa para controle de vendas, geração de relatórios de consumo e gestão de perfis de usuários (estudantes, servidores e visitantes).
- Integração via API: Utiliza-se de outros sistemas para validar os acessos, como o SUAP, e os pagamentos realizados.

Limites e Fora de Escopo:
- Gestão de Estoque: O sistema não realizará o controle de insumos alimentícios (estoque de alimentos, fornecedores de carga seca, etc.).
- Hardware de Acesso: O projeto foca no software; a instalação física de catracas ou leitores biométricos é tratada como uma infraestrutura externa que apenas consome a API deste sistema.
- Pagamento em Espécie: O sistema não processará recebimento de dinheiro físico ou cartão de débito; essa função continuará restrita aos guichês humanos, que apenas lançarão o crédito no sistema após o recebimento.

### 1.3 Definições, Acrônimos e Abreviações
UFR: Universidade Federal de Rondonópolis.
RU: Restaurante Universitário.
API: Application Programming Interface (Interface de Programação de Aplicações); conjunto de normas que permite a comunicação entre o módulo gerenciador e a interface.
Arquitetura Desacoplada: Modelo de desenvolvimento onde o Front-end (interface) e o Back-end (servidor) funcionam de forma independente.
Pix: Sistema de pagamentos instantâneos criado pelo Banco Central do Brasil.
PROAE: Pró-Reitoria de Assistência Estudantil.
Stakeholders: Partes interessadas ou pessoas/entidades afetadas pelo projeto.
UX: User Experience (Experiência do Usuário); foco em tornar a navegação simples e intuitiva.

---

##  2. Product Vision

### 2.1 Problema
A Universidade Federal de Rondonópolis (UFR) disponibiliza à comunidade acadêmica o Restaurante Universitário (RU) que atende estudantes e servidores em suas refeições diárias, sendo essa uma unidade estratégica para a permanência estudantil que oferece refeições a preços acessíveis mediante um sistema de créditos pré-pagos realizado de forma presencial. Tendo em vista sua importância social, é relevante mitigar qualquer gargalo logístico que afete a eficiência desse processo.
Destacam-se como principais problemas nesse modelo, a burocracia do cadastro exclusivamente presencial, dificuldade no acesso ao cardápio e, principalmente, a falta de uma interface que permita consulta de saldo e recarga remotamente. Esse cenário promove um fluxo lento e filas longas, resultando na perda de tempo produtivo dos estudantes e servidores, reforçando a necessidade de um sistema digital que entre como facilitador desse serviço.
### 2.2 Solução
Temos como solução o desenvolvimento de um software que possibilitará a realização do cadastro online do RU, por meio das credenciais de acesso presentes no SUAP. O software terá o cardápio atualizado semanalmente, e será possível visualizar seu saldo disponível, permitindo a possibilidade de recargar o saldo via Pix, ou por meio de débitos descontados em um cartão de crédito cadastrado pelo usuário. O projeto visa melhorar a usabilidade do RU pelos universitários por meio da facilitação do processo de cadastro, identificação do cardápio e a agilidade no processo de recarga do saldo, evitando o enfrentamento de filas e organização financeira dos usuários do RU, uma vez que poderão conferir quanto de saldo possuem. 

### 2.3 Público-Alvo
Os Target Users (Usuários alvo) são estudantes matriculados na Universidade Federal de Rondonópolis (UFR) com acesso ao sistema SUAP e servidores públicos da UFR. 

### 2.4 Proposta de Valor
Por que esse sistema é importante?

### 2.5 Diferencial
O que torna esse sistema melhor que outros?

### 2.6 Funcionalidades principais (alto nível)
- Funcionalidade 1
- Funcionalidade 2

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
- Interface intuitiva  
- Tempo de aprendizado < X minutos  
- Acessibilidade  

### 5.2 Eficiência
- Tempo de resposta < X segundos  
- Suporte a múltiplos usuários  

### 5.3 Desempenho
- Suporte a X usuários simultâneos  
- Estabilidade sob carga  

### 5.4 Espaço
- Limite de armazenamento  
- Uso eficiente de memória  

### 5.5 Confiabilidade
- Disponibilidade mínima (ex: 99,9%)  
- Recuperação de falhas  

### 5.6 Segurança (Proteção)
- Autenticação  
- Criptografia  
- Controle de acesso  

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

##  9. Casos de Uso

### UC01 - Nome do caso de uso
**Ator:**  
**Descrição:**  
**Fluxo principal:**  
**Fluxo alternativo:**  

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
