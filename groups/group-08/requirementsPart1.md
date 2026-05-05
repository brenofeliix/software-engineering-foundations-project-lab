## System Overview

O sistema proposto, denominado Serpy, tem como objetivo auxiliar na educação, prevenção e resposta a acidentes envolvendo animais peçonhentos, com foco principal em serpentes.

O problema abordado é a dificuldade da população em identificar corretamente esses animais e saber como agir em situações de risco ou acidentes, o que pode resultar em decisões inadequadas e agravamento de casos. Além disso, há uma carência de ferramentas acessíveis que integrem informação, prevenção e monitoramento em um único ambiente.

A solução proposta consiste em um software (web e mobile) que permite ao usuário identificar animais peçonhentos, acessar informações confiáveis sobre suas características e nível de risco, receber orientações de primeiros socorros em situações de emergência e registrar ocorrências geolocalizadas.

O sistema também incorpora funcionalidades de monitoramento de áreas de risco por meio de um mapa de ocorrências, além de um módulo educacional com conteúdos e treinamentos. Para aumentar o engajamento, são utilizados elementos de gamificação, como pontuação, conquistas e desafios.

Os principais usuários do sistema são:
- Usuários comuns, que buscam identificar animais e obter orientações
- Profissionais da saúde, que utilizam o sistema como apoio informativo
- Administradores, responsáveis pelo gerenciamento de dados e monitoramento do sistema

Dessa forma, o sistema integra utilidade prática, educação e tecnologia, oferecendo suporte tanto para uso cotidiano quanto para situações de emergência, contribuindo para a redução de acidentes e aumento da conscientização da população.

## Functional Requirements

- FR01 - Permitir o cadastro de usuários no sistema.
- FR02 - Permitir autenticação de usuários por login e senha.
- FR03 - Permitir recuperação de senha.
- FR04 - Permitir edição de perfil do usuário.
- FR05 - Permitir diferenciação de perfis (usuário comum, profissional e administrador).
- FR06 - Permitir identificar animais peçonhentos por meio de seleção manual.
- FR07 - Permitir identificar animais por meio de imagem (upload ou câmera).
- FR08 - Exibir informações detalhadas sobre o animal identificado.
- FR09 - Exibir nível de risco do animal (baixo, médio, alto).
- FR10 - Exibir características físicas e comportamento do animal.
- FR11 - Exibir habitat e regiões onde o animal é encontrado.
- FR12 - Permitir acesso ao modo emergência.
- FR13 - Exibir instruções de primeiros socorros.
- FR14 - Exibir instruções do que não deve ser feito.
- FR15 - Permitir acesso rápido a orientações por botão de emergência.
- FR16 - Permitir triagem baseada em sintomas informados pelo usuário.
- FR17 - Permitir registro de ocorrências com descrição.
- FR18 - Permitir registro de localização da ocorrência.
- FR19 - Permitir visualização de ocorrências em mapa.
- FR20 - Permitir consulta de áreas de risco.
- FR21 - Permitir filtragem de ocorrências por tipo de animal.
- FR22 - Permitir acesso ao módulo educacional.
- FR23 - Permitir visualização de conteúdos educativos.
- FR24 - Permitir realização de quizzes.
- FR25 - Permitir acompanhamento de progresso do usuário.
- FR26 - Permitir emissão de certificados (se aplicável).
- FR27 - Permitir sistema de pontuação (XP).
- FR28 - Permitir conquista de badges.
- FR29 - Permitir visualização de ranking de usuários.
- FR30 - Permitir controle de sequência de uso (streak).
- FR31 - Permitir envio de notificações ao usuário.
- FR32 - Permitir alertas de áreas de risco com base em localização.
- FR33 - Permitir acesso ao dashboard administrativo.
- FR34 - Permitir gerenciamento de usuários.
- FR35 - Permitir gerenciamento de conteúdos.
- FR36 - Permitir gerenciamento de ocorrências.
- FR37 - Permitir visualização de estatísticas do sistema.
- FR38 - Permitir funcionamento básico offline (conteúdos essenciais).
- FR39 - Permitir sincronização de dados quando conexão for restabelecida.

## Non-Functional Requirements

- Performance: O sistema deve responder às requisições em até 2 segundos em condições normais de uso.
- Performance: O sistema deve suportar pelo menos 1000 usuários simultâneos.
- Performance: O carregamento inicial da aplicação deve ocorrer em até 3 segundos.<br><br>
  
- Security: O sistema deve garantir autenticação segura com criptografia de senha.
- Security: O sistema deve proteger dados sensíveis dos usuários.
- Security: O sistema deve possuir controle de acesso baseado em perfis.
- Security: O sistema deve prevenir ataques comuns (SQL Injection, XSS).<br><br>

- Usability: O sistema deve possuir interface intuitiva e de fácil navegação.
- Usability: O sistema deve ser utilizável por pessoas sem conhecimento técnico.
- Usability: O sistema deve possuir design responsivo (mobile e desktop).
- Usability: O sistema deve minimizar o número de ações para tarefas críticas (ex: emergência).<br><br>

