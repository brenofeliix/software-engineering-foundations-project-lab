# Software Architecture

## Overview

O projeto consiste no desenvolvimento de um sistema educacional baseado em gamificação dos estudos, com o objetivo de tornar o aprendizado mais dinâmico, interativo e motivador para alunos do ensino fundamental.

A plataforma será voltada para estudantes do 6º ao 9º ano, que, após realizarem um cadastro simples, terão acesso a um login individual. Durante o cadastro, o aluno informará sua idade e o ano escolar em que está, permitindo que o sistema personalize automaticamente sua experiência de aprendizagem.

Com base nessas informações, o aplicativo será responsável por organizar e direcionar as atividades, disponibilizando jogos educativos adequados ao nível do aluno. Os jogos serão divididos por matérias como Português, Matemática, História, entre outras mas também haverá a opção de atividades no modo sortido, trazendo variedade e estimulando diferentes áreas do conhecimento.

Além disso, o sistema contará com elementos típicos de gamificação para aumentar o engajamento, como o controle de sequência de estudos "streak", que registra quantos dias seguidos o aluno utilizou a plataforma, incentivando a constância nos estudos.

Outro recurso importante será o sistema de grupos, permitindo que professores ou escolas criem turmas dentro da plataforma. Dessa forma, será possível acompanhar o desempenho dos alunos, promover interação e integrar o uso do aplicativo ao ambiente escolar.

No geral, o projeto busca unir tecnologia e educação de forma acessível, tornando o processo de aprendizagem mais leve, divertido e eficiente.



## Architectural Style

O sistema adota um estilo arquitetural híbrido, combinando o padrão Cliente-Servidor com uma abordagem Baseada em Eventos (Event-Driven) e comunicação em tempo real.

Justificativa:
A escolha desse estilo justifica-se pelas duas dinâmicas principais da plataforma:

Salas Interativas em Tempo Real: Para atender à necessidade dos professores de criarem salas e ensinarem de forma dinâmica, a arquitetura utiliza comunicação bidirecional (via WebSockets). Isso garante que as ações do professor e as respostas dos alunos sejam sincronizadas instantaneamente para todos os participantes da sala.

Estudo Independente: Para os alunos que acessam a plataforma de forma autônoma para fixar a matéria, o sistema funciona de maneira assíncrona e isolada. Essa separação de contextos garante que picos de acessos em salas de aula grandes não impactem a experiência e a performance dos usuários que estão estudando sozinhos.

A arquitetura foi desenhada para priorizar a baixa latência na gamificação e a escalabilidade independente de seus módulos principais.Explain chosen style.

## Components

* Component A
* Component B

## Diagram

Insert diagram.

## Data Flow

Describe flow.

## Technologies

List technologies.

## Risks

Describe risks.
