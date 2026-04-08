# Requirements Specification

Este documento descreve de forma estruturada os requisitos do sistema a ser desenvolvido. Ele deve ser claro, objetivo e completo, servindo como base para desenvolvimento, testes e validação do software.

## System Overview

O projeto consiste no desenvolvimento de um sistema educacional baseado em gamificação dos estudos, com o objetivo de tornar o aprendizado mais dinâmico, interativo e motivador para alunos do ensino fundamental.

A plataforma será voltada para estudantes do 6º ao 9º ano, que, após realizarem um cadastro simples, terão acesso a um login individual. Durante o cadastro, o aluno informará sua idade e o ano escolar em que está, permitindo que o sistema personalize automaticamente sua experiência de aprendizagem.

Com base nessas informações, o aplicativo será responsável por organizar e direcionar as atividades, disponibilizando jogos educativos adequados ao nível do aluno. Os jogos serão divididos por matérias — como Português, Matemática, História, entre outras — mas também haverá a opção de atividades no modo sortido, trazendo variedade e estimulando diferentes áreas do conhecimento.

Além disso, o sistema contará com elementos típicos de gamificação para aumentar o engajamento, como o controle de sequência de estudos (streak), que registra quantos dias seguidos o aluno utilizou a plataforma, incentivando a constância nos estudos.

Outro recurso importante será o sistema de grupos, permitindo que professores ou escolas criem turmas dentro da plataforma. Dessa forma, será possível acompanhar o desempenho dos alunos, promover interação e integrar o uso do aplicativo ao ambiente escolar.

No geral, o projeto busca unir tecnologia e educação de forma acessível, tornando o processo de aprendizagem mais leve, divertido e eficiente.

## Functional Requirements

* RF01: O sistema deve permitir o cadastro de alunos.
* RF02: O sistema deve gerar um login para o aluno após o cadastro.
* RF03: O sistema deve permitir que o aluno informe idade e ano escolar (6º ao 9º ano).
* RF04: O sistema deve permitir login e autenticação do usuário.
* RF05: O sistema deve classificar o aluno em uma categoria com base na idade e ano escolar.
* RF06: O sistema deve disponibilizar atividades compatíveis com a categoria do aluno.
* RF07: O sistema deve oferecer jogos por disciplina (Português, Matemática, História, Geografia, Ciências, Arte e Inglês).
* RF08: O sistema deve permitir ao aluno escolher a disciplina desejada.
* RF09: O sistema deve oferecer a opção de jogos no modo “sortido”.
* RF10: O sistema deve registrar o desempenho do aluno nos jogos.
* RF11: O sistema deve registrar a sequência de dias em que o aluno estudou (streak).
* RF12: O sistema deve atualizar automaticamente o streak a cada acesso diário.
* RF13: O sistema deve reiniciar o streak caso o aluno não acesse no dia.
* RF14: O sistema deve permitir que professores criem grupos.
* RF15: O sistema deve permitir que alunos entrem em grupos.
* RF16: O sistema deve permitir que professores visualizem o desempenho dos alunos no grupo.
* RF17: O sistema deve armazenar o histórico de atividades do aluno.
* RF18: O sistema deve permitir ao aluno visualizar seu progresso.
* RF19: O sistema deve permitir que professores acompanhem o progresso dos alunos.
* FR20 : Trilhas das principais matérias do ensino fundamental: Lingua Portuguesa; Matemática; História; Geografia; Ciências; Arte; Inglês.
* FR21: Sistema de ofensiva individual, responsável por gravar quantos dias seguidos um aluno estudou usando o serviço.
* FR22: Sistema de "grupos", onde professores/escolas podem criar um grupo para suas salas de aula.

## Non-Functional Requirements

* Performance:
* Security:
* Usability:
