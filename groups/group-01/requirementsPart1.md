# Requirements Specification

Este documento descreve de forma estruturada os requisitos do sistema a ser desenvolvido. Ele deve ser claro, objetivo e completo, servindo como base para desenvolvimento, testes e validação do software.

---

## 1. System Overview (Visão Geral do Sistema)

### O que é:
Este sistema consiste em um minimercado autônomo instalado dentro do campus universitário, focado na venda de itens essenciais e de higiene para a comunidade acadêmica. O propósito é oferecer conveniência e segurança, especialmente para alunos do turno da noite.
1-	Problema a ser resolvido: A dificuldade de acesso a itens de higiene básica e primeiros socorros durante o horário de aula, além dos riscos de segurança ao sair do campus à noite para buscar farmácias ou mercados distantes.
2-	Solução: Um ponto de venda autônomo, onde o próprio aluno escolhe o produto e realiza o pagamento via terminal digital, sem necessidade de atendente físico no local.
3-	Público-alvo: Estudantes universitários (principalmente do turno noturno), professores e funcionários da instituição.
Resumo: O sistema de mercadinho é uma solução de varejo autônomo que permite a compra de itens de higiene, saúde e alimentação rápida dentro da universidade. O público-alvo inclui alunos e colaboradores que buscam praticidade e segurança em horários de emergência.

---

## 2. Functional Requirements (Requisitos Funcionais)

-	FR01: Permitir o cadastro de usuários com e-mail institucional.
-	FR02: Realizar a leitura de produtos via código de barras.
-	FR03: Exibir o valor total da compra antes da finalização.
-	FR04: Processar pagamentos via PIX ou cartão.
-	FR05: Enviar comprovante de compra digital para o usuário.

---

## 3. Non-Functional Requirements (Requisitos Não Funcionais)

-	NFR01 (Disponibilidade): O sistema deve estar disponível para uso 24 horas por dia, 7 dias por semana.
-	NFR02 (Segurança): Todos os dados de pagamento devem ser protegidos por criptografia de ponta a ponta.
-	NFR03 (Desempenho): O sistema deve processar a leitura do código de barras em menos de 2 segundos.
-	NFR04 (Usabilidade): A interface deve ser simples o suficiente para que uma compra seja concluída em no máximo 3 etapas.

---

