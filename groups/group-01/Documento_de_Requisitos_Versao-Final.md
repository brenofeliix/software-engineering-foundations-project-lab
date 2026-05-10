# Documento de Requisitos e Projeto de Software

---

# 1. Introdução

## 1.1 Objetivo
Descrever o desenvolvimento de um minimercado autônomo instalado no campus universitário, oferecendo itens essenciais, higiene pessoal, primeiros socorros e alimentação rápida para a comunidade acadêmica.

## 1.2 Escopo
O sistema permitirá que usuários realizem compras de forma independente através de um terminal digital de autoatendimento, utilizando leitura de código de barras e pagamentos digitais.

O sistema contempla:
- Cadastro de usuários
- Leitura de produtos
- Pagamentos digitais
- Controle de estoque
- Emissão de comprovantes digitais

Fora do escopo:
- Atendimento presencial contínuo
- Pagamentos em dinheiro
- Entregas externas

## 1.3 Definições, Acrônimos e Abreviações
- PIX: Sistema de pagamento instantâneo
- LGPD: Lei Geral de Proteção de Dados
- Self-checkout: Sistema de autoatendimento
- Totem: Terminal de autoatendimento

---

# 2. Product Vision

## 2.1 Problema
Dificuldade de acesso a itens de higiene, alimentação e primeiros socorros durante o horário de aula, principalmente no período noturno, além dos riscos de sair do campus à noite.

## 2.2 Solução
Um minimercado autônomo onde o usuário escolhe os produtos e realiza o pagamento digital sem necessidade de atendente.

## 2.3 Público-Alvo
- Estudantes universitários
- Professores
- Funcionários da instituição

## 2.4 Proposta de Valor
Oferecer praticidade, rapidez e segurança para a comunidade acadêmica dentro do campus universitário.

## 2.5 Diferencial
- Funcionamento 24 horas
- Autoatendimento
- Pagamento rápido via PIX e cartão
- Segurança para alunos do turno noturno

## 2.6 Funcionalidades principais (alto nível)
- Cadastro de usuários
- Leitura de código de barras
- Pagamento digital
- Controle de estoque
- Emissão de comprovantes

---

# 3. Visão Geral do Sistema

## 3.1 Descrição Geral
O sistema consiste em um mercadinho autônomo instalado dentro da universidade, permitindo compras rápidas de produtos essenciais através de um terminal touch screen.

## 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Administração da universidade
- Desenvolvedores
- Repositores de estoque

---

# 4. Requisitos Funcionais

## RF01 - Cadastro de usuários

**Descrição:**
Permitir o cadastro de usuários utilizando e-mail institucional.

**Prioridade:** Alta

**Entradas:**
- Nome
- E-mail institucional
- Senha

**Saídas:**
- Cadastro realizado com sucesso

**Regras de negócio:**
- Apenas e-mails institucionais válidos serão aceitos

---

## RF02 - Leitura de produtos

**Descrição:**
Permitir leitura de produtos por código de barras.

**Prioridade:** Alta

**Entradas:**
- Código de barras

**Saídas:**
- Nome do produto
- Valor
- Quantidade disponível

**Regras de negócio:**
- A leitura deve ocorrer em até 2 segundos

---

## RF03 - Exibição do valor total

**Descrição:**
Exibir o valor total da compra antes da finalização.

**Prioridade:** Alta

**Entradas:**
- Produtos adicionados ao carrinho

**Saídas:**
- Valor total atualizado

**Regras de negócio:**
- O valor deve atualizar automaticamente

---

## RF04 - Pagamento digital

**Descrição:**
Processar pagamentos via PIX e cartão.

**Prioridade:** Alta

**Entradas:**
- Dados da transação
- Método de pagamento

**Saídas:**
- Confirmação do pagamento

**Regras de negócio:**
- Os dados financeiros devem ser criptografados

---

## RF05 - Envio de comprovante digital

**Descrição:**
Enviar comprovante digital após a compra.

**Prioridade:** Média

**Entradas:**
- Dados da compra
- E-mail do usuário

**Saídas:**
- Comprovante enviado

**Regras de negócio:**
- O comprovante deve conter itens, data e valor total

---

# 5. Requisitos Não Funcionais

## 5.1 Usabilidade
- Interface intuitiva
- Compatibilidade com touch screen
- Botões grandes e legíveis
- Compra finalizada em até 3 etapas
- Usuário deve concluir compras rapidamente

## 5.2 Eficiência
- Leitura de produtos em menos de 2 segundos
- Consulta ao banco em até 1,5 segundos
- Suporte à sincronização automática de estoque

## 5.3 Desempenho
- Funcionamento 24 horas por dia
- Estabilidade sob carga
- Suporte a múltiplos usuários simultâneos

## 5.4 Espaço
- Uso eficiente de memória
- Sistema leve para hardware limitado
- Estoque limitado ao espaço físico disponível

## 5.5 Confiabilidade
- Disponibilidade contínua
- Recuperação de falhas
- Integridade dos dados das compras

## 5.6 Segurança (Proteção)
- Autenticação de usuários
- Criptografia de ponta a ponta
- Controle de acesso
- Conformidade com LGPD

---
## 6. Requisitos Organizacionais 

### 6.1 Ambientais 
- Sistema Operacional: O programa de rodar de forma leve, considerando que o hardware do tablet de autoatendimento possui recursos de processamento limitados. A interface deve ser compatível com operações via touch, eliminando a necessidade de teclados e mouse. O ideal seria um sistema operacional Android, visando baixo custo e fácil manutenção, além de alta compatibilidade com outros sistemas.
- Infraestrutura: A instalação física no campus da faculdade depende obrigatoriamente de um ponto de energia e de uma rede Wi-Fi estável para garantir a conectividade do tablet.
  
### 6.2 Operacionais
- Logs: O sistema deve registrar transações financeiras de forma segura, garantindo que os dados sejam criptografados e não fiquem armazenados localmente no totem para evitar vulnerabilidades físicas. Além de gerar registros digitais de todas as compras para permitir o envio automático de comprovantes aos usuários. Todas as interações com o sistema devem respeitar as normas da LGPD, garantindo a privacidade dos logs de dados cadastrais dos alunos.
- Monitoramento: É essencial o acompanhamento em tempo real do estoque. O sistema deve permitir que o repositor visualize produtos com baixo nível de unidades para garantir a eficiência do abastecimento. O sistema deve exigir autenticação para que apenas usuários registrados como RGA realizem compras, criando responsabilidade em quem acessa o minimercado.
  
### 6.3 Desenvolvimento
- Versionamento (Git): O desenvolvimento do sistema utilizará Git para controle de versão, permitindo controle das alterações no código, organização das funcionalidades e colaboração entre os desenvolvedores.
- Padrões de Código: O desenvolvimento deve priorizar a leveza do software para se adaptar a limitação de processamento no tablet. O código deve ter integrações com sistemas como o da SEFAZ para emissão de cupons fiscais, além de integração com o banco de dados da universidade.
- Testes Automatizados: Serão implementados testes automatizados para validar funcionalidades como autenticação de usuários, registro de compras, pagamentos digitais e atualização de estoque, garantindo maior confiabilidade ao sistema e identificando “Bugs” para as devidas correções

## 7. Requisitos Externos

### 7.1 Reguladores
- LGPD: O sistema deve seguir integralmente as diretrizes da Lei Geral de Proteção de Dados (LGPD),
garantindo a segurança e privacidade das informações pessoais dos alunos cadastrados. Os dados devem ser
armazenados de forma segura, com acesso restrito apenas a usuários autorizados.
- Normas Específicas: O sistema deve respeitar normas institucionais da universidade e requisitos relacionados
a sistemas de pagamento digital, emissão de comprovantes e integração com serviços externos, garantindo
conformidade operacional e legal.

### 7.2 Éticos
- Não Discriminação: O sistema deve garantir igualdade de acesso a todos os usuários, sem qualquer tipo de
discriminação relacionada a curso, gênero, condição social ou necessidades especiais, promovendo
acessibilidade e inclusão digital.
- Transparência: Todas as operações realizadas no minimercado devem ser claras ao usuário, exibindo
informações corretas sobre preços, estoque, pagamentos e registros de compras, assegurando confiança e
credibilidade no sistema.

### 7.3 Legais
- Leis: O sistema deve atender às legislações brasileiras aplicáveis ao comércio digital e armazenamento de
dados, incluindo normas fiscais para emissão de comprovantes e regulamentações relacionadas ao tratamento
de informações pessoais e financeiras.

### 7.4 Segurança Externa
- Proteção contra Ataques: O sistema deve possuir mecanismos de proteção contra invasões, vazamento de
dados e acessos não autorizados, utilizando autenticação segura, criptografia e monitoramento de atividades
suspeitas.
- Auditorias: Devem ser realizados processos de auditoria e verificação periódica no sistema para garantir
integridade das informações, confiabilidade das transações financeiras e conformidade com padrões de
segurança.

### 7.5 Contábeis
- Registro de Transações: O sistema deve manter registros detalhados de todas as compras e pagamentos
realizados no minimercado, permitindo rastreamento completo das movimentações financeiras.
- Relatórios: O sistema deve gerar relatórios financeiros e operacionais para auxiliar o controle administrativo do
estoque, faturamento e fluxo de vendas, facilitando análises e tomadas de decisão pela gestão do minimercado.
