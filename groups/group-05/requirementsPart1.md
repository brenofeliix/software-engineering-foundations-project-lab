# Requirements Specification

Este documento descreve de forma estruturada os requisitos do sistema a ser desenvolvido. Ele deve ser claro, objetivo e completo, servindo como base para desenvolvimento, testes e validação do software.

---

## 1. System Overview (Visão Geral do Sistema)

### O que é:
O StockFácil é um aplicativo web e mobile para gestão de estoque de pequenas empresas e e-commerces varejistas. A plataforma permite registrar e monitorar movimentações de produtos em tempo real, com alertas de reposição e relatórios, substituindo planilhas manuais e processos desorganizados.

### Público-alvo

Pequenos comerciantes com lojas físicas e/ou virtuais (e-commerce)

Empreendedores do varejo que precisam controlar produtos, entradas e saídas

Gestores de microempresas que desejam substituir controles manuais ou planilhas

Equipes de estoque com múltiplos operadores e necessidade de controle de acesso


### Problema resolvido

Ruptura de estoque por falta de monitoramento em tempo real

Excesso de mercadoria parada por ausência de análise de giro de produtos

Falta de rastreabilidade nas movimentações (quem fez, quando e quanto)

Dificuldade em integrar controle de estoque com operações de e-commerce

---

## 2. Functional Requirements (Requisitos Funcionais)

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


## 3. Non-Functional Requirements (Requisitos Não Funcionais)

- NFR01 - O sistema deve carregar qualquer tela em no máximo 3 segundos em condições normais de uso.
- NFR02 - O sistema deve suportar até 500 usuários simultâneos sem degradação de desempenho.
- NFR03 - Todas as senhas devem ser armazenadas com criptografia (bcrypt ou equivalente).
- NFR04 - As comunicações entre cliente e servidor devem ser feitas via HTTPS (TLS 1.2 ou superior).
- NFR05 - O sistema deve registrar logs de acesso e ações críticas para auditoria.
- NFR06 - A interface deve ser intuitiva e responsiva, adaptando-se a dispositivos móveis e desktop.
- NFR07 - O sistema deve seguir padrões de acessibilidade WCAG 2.1 nível AA.
- NFR08 - O sistema deve ter disponibilidade mínima de 99,5% ao mês (exceto manutenções programadas).
- NFR09 - O código-fonte deve seguir padrões de clean code e ser documentado para facilitar manutenção.
- NFR10 - A arquitetura deve permitir escalabilidade horizontal para aumento de usuários e volume de dados.


