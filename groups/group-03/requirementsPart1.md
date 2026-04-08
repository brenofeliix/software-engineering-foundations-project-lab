# Requirements Specification

Este documento descreve de forma estruturada os requisitos do sistema a ser desenvolvido. Ele deve ser claro, objetivo e completo, servindo como base para desenvolvimento, testes e validação do software.

## System Overview

O projeto consiste no desenvolvimento de um sistema educacional baseado em gamificação dos estudos, com o objetivo de tornar o aprendizado mais dinâmico, interativo e motivador para alunos do ensino fundamental.

A plataforma será voltada para estudantes do 6º ao 9º ano, que, após realizarem um cadastro simples, terão acesso a um login individual. Durante o cadastro, o aluno informará sua idade e o ano escolar em que está, permitindo que o sistema personalize automaticamente sua experiência de aprendizagem.

Com base nessas informações, o aplicativo será responsável por organizar e direcionar as atividades, disponibilizando jogos educativos adequados ao nível do aluno. Os jogos serão divididos por matérias como Português, Matemática, História, entre outras mas também haverá a opção de atividades no modo sortido, trazendo variedade e estimulando diferentes áreas do conhecimento.

Além disso, o sistema contará com elementos típicos de gamificação para aumentar o engajamento, como o controle de sequência de estudos "streak", que registra quantos dias seguidos o aluno utilizou a plataforma, incentivando a constância nos estudos.

Outro recurso importante será o sistema de grupos, permitindo que professores ou escolas criem turmas dentro da plataforma. Dessa forma, será possível acompanhar o desempenho dos alunos, promover interação e integrar o uso do aplicativo ao ambiente escolar.

No geral, o projeto busca unir tecnologia e educação de forma acessível, tornando o processo de aprendizagem mais leve, divertido e eficiente.

## Functional Requirements

* RF01: Permitir o cadastro de alunos.
* RF02: Gerar um login para o aluno após o cadastro.
* RF03: Permitir que o aluno informe idade e ano escolar (6º ao 9º ano).
* RF04: Permitir login e autenticação do usuário.
* RF05: Classificar o aluno em uma categoria com base na idade e ano escolar.
* RF06: Disponibilizar atividades compatíveis com a categoria do aluno.
* RF07: Oferecer jogos por disciplina (Português, Matemática, História, Geografia, Ciências, Arte e Inglês).
* RF08: Permitir ao aluno escolher a disciplina desejada.
* RF09: Oferecer a opção de jogos no modo “sortido”.
* RF10: Registrar o desempenho do aluno nos jogos.
* RF11: Registrar a sequência de dias em que o aluno estudou (streak).
* RF12: Atualizar automaticamente o streak a cada acesso diário.
* RF13: Reiniciar o streak caso o aluno não acesse no dia.
* RF14: Permitir que professores criem grupos.
* RF15: Permitir que alunos entrem em grupos.
* RF16: Permitir que professores visualizem o desempenho dos alunos no grupo.
* RF17: Armazenar o histórico de atividades do aluno.
* RF18: Permitir ao aluno visualizar seu progresso.
* RF19: Permitir que professores acompanhem o progresso dos alunos.
* FR20: Trilhas das principais matérias do ensino fundamental: Lingua Portuguesa; Matemática; História; Geografia; Ciências; Arte; Inglês.
* FR21: Sistema de ofensiva individual, responsável por gravar quantos dias seguidos um aluno estudou usando o serviço.
* FR22: Sistema de "grupos", onde professores/escolas podem criar um grupo para suas salas de aula.

## Non-Functional Requirements

### Performance

* RNF01: Responder às ações do usuário em até 3 segundos.
* RNF02: Suportar múltiplos usuários simultaneamente.

### Security

* RNF03: Proteger os dados dos usuários (login e informações pessoais).
* RNF04: Garantir autenticação segura.
* RNF05: Impedir acesso não autorizado aos dados.
  
### Usability

* RNF06: Possuir interface simples e intuitiva, adequada para crianças e adolescentes.
* RNF07: Ser fácil de navegar, com linguagem acessível.
* RNF08: Responsivo (funcionar em celular, tablet, computadore etc).
