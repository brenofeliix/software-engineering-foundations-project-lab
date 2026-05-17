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
Muitas empresas e pequenos negócios enfrentam dificuldades no controle de estoque interno, como falta de organização, erros manuais, perda de produtos, dificuldade em acompanhar entradas e saídas e ausência de dados em tempo real. Esses problemas podem gerar prejuízos financeiros, desperdício de recursos e baixa eficiência operacional.

### 2.2 Solução
Esse software permite que as empresas moonitorem o fluxo de extoque em tempo real, acompanhando as entradas e saídas de produtos. Além disso, pode gerar relatorios personalizados simples com base nesses dados, como listas de saldos atuais e resumo de movimentações, além de oferecer alertas altomaticos para estoque baixo do normal ou excessivo.


### 2.3 Público-Alvo
Os principais usuários do aplicativo serão:
-	Pequenos comerciantes com lojas físicas e/ou virtuais (e-commerce)
-	Empreendedores do varejo que precisam controlar produtos, entradas e saídas.
-	Equipes de almoxarifado
-	Gestores de microempresas que desejam substituir controles manuais ou planilhas
-	Equipes de estoque com múltiplos operadores e necessidade de controle de acesso

### 2.4 Proposta de Valor
É uma forma de pequenas empresas usarem sistemas mais avançados para acompanhar as entradas e saidas de produtos de forma mais pratica e visivel.

Por que esse sistema é importante?

### 2.5 Diferencial
Um sistema mais simples de se ultilizar, sem a necessidade de treinamento para se usar o sistema.

O que torna esse sistema melhor que outros?

### 2.6 Funcionalidades principais (alto nível)
- Funcionalidade 1
- Funcionalidade 2

---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
O StockFácil é um aplicativo web e mobile para gestão de estoque de pequenas empresas e e-commerces varejistas. A plataforma permite registrar e monitorar movimentações de produtos em tempo real, com alertas de reposição e relatórios, substituindo planilhas manuais e processos desorganizados.
Explique o sistema de forma resumida.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais
- FR01 - Permitir o cadastro de usuários com diferentes perfis de acesso (administrador, operador, visualizador).
- FR02 - Permitir o login com autenticação por e-mail e senha.
- FR03 - Permitir o cadastro, edição e exclusão de produtos com nome, código SKU, categoria, unidade de medida e descrição.
- FR04 - Registrar entradas e saídas de estoque com data, quantidade e responsável.
- FR05 - Exibir o saldo atual de cada produto em tempo real.
- FR06 - Emitir alertas automáticos quando o estoque de um produto atingir o nível mínimo configurado.
- FR07 - Permitir a geração de relatórios de movimentação por período, produto ou categoria.
- FR08 - Permitir o cadastro de fornecedores com nome, CNPJ, contato e produtos associados.
- FR09 - Registrar o histórico completo de todas as movimentações de estoque.
- FR10 - Permitir a importação e exportação de dados em formato CSV/Excel.
- FR11 - Exibir um dashboard com indicadores gerais: total de itens, produtos em falta, últimas movimentações.
- FR12 - Permitir a busca e filtragem de produtos por nome, categoria ou código.
- FR13 - Permitir o controle de múltiplos locais de armazenamento (filiais, depósitos).
- FR14 - Registrar o custo de compra dos produtos para cálculo de valor total do estoque .
- FR15 - Permitir a recuperação de senha via e-mail.


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
- NFR02 - O sistema deve suportar até 500 usuários simultâneos sem degradação de desempenho.
- NFR03 - Todas as senhas devem ser armazenadas com criptografia (bcrypt ou equivalente).
- NFR04 - As comunicações entre cliente e servidor devem ser feitas via HTTPS (TLS 1.2 ou superior).
- NFR05 - O sistema deve registrar logs de acesso e ações críticas para auditoria.
- NFR06 - A interface deve ser intuitiva e responsiva, adaptando-se a dispositivos móveis e desktop.
- NFR07 - O sistema deve seguir padrões de acessibilidade WCAG 2.1 nível AA.
- NFR08 - O sistema deve ter disponibilidade mínima de 99,5% ao mês (exceto manutenções programadas).
- NFR09 - O código-fonte deve seguir padrões de clean code e ser documentado para facilitar manutenção.
- NFR10 - A arquitetura deve permitir escalabilidade horizontal para aumento de usuários e volume de dados.
- 
### 5.1 Usabilidade
- O sistema deve ser totalmente responsivo, adaptando-se a dispositivos móveis, tablets e desktops.
- O usuário deve conseguir registrar uma entrada ou saída de estoque em no máximo 3 cliques a partir do menu principal.
- O sistema deve exibir mensagens de erro claras e orientações de correção sempre que uma ação falhar.
- O dashboard principal deve apresentar os indicadores mais importantes de forma visual e de fácil interpretação.

---

### 5.2 Eficiência
- Tempo de resposta < X segundos  
- Suporte a múltiplos usuários  

### 5.3 Desempenho
-	O sistema deve responder a qualquer requisição do usuário em até 2 segundos em condições normais de uso.
- O sistema deve suportar até 500 usuários simultâneos sem degradação perceptível de desempenho.
- O carregamento inicial do dashboard não deve ultrapassar 3 segundos em conexões de banda larga.
- Operações de busca e filtro de produtos devem retornar resultados em menos de 1 segundo.
- A geração de relatórios de até 12 meses de histórico deve ser concluída em no máximo 5 segundos.

### 5.4 Espaço
- Limite de armazenamento  
- Uso eficiente de memória  

### 5.5 Confiabilidade
- Disponibilidade mínima (ex: 99,9%)  
- Recuperação de falhas  

### 5.6 Segurança (Proteção)
- O sistema deve criptografar senhas utilizando algoritmo de hash seguro (bcrypt com salt).
- O sistema deve implementar autenticação com bloqueio após 5 tentativas incorretas consecutivas.
- O sistema deve restringir o acesso às funcionalidades conforme o perfil do usuário (administrador, operador, visualizador).
- Todas as comunicações devem ser realizadas via HTTPS (TLS 1.2 ou superior).
- Tokens de sessão devem expirar após 8 horas de inatividade, exigindo novo login.
- O sistema deve registrar logs de auditoria para ações críticas como exclusão de produtos e alterações de estoque.

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
