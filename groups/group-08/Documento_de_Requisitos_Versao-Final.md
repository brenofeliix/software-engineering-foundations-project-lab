#  Documento de Requisitos e Projeto de Software

---

## 1. Introdução

Este documento apresenta a definição dos requisitos e a visão geral do sistema **Serpy**, uma plataforma digital voltada para educação, prevenção e resposta a acidentes com animais peçonhentos.

O sistema tem como foco principal auxiliar a população na identificação de animais como serpentes, escorpiões e aranhas, além de fornecer orientações em situações de emergência e contribuir para o mapeamento de áreas de risco.

A proposta busca unir tecnologia e impacto social, oferecendo uma solução acessível tanto para o público geral quanto para profissionais que lidam diretamente com esse tipo de ocorrência.

---

### 1.1 Objetivo

O objetivo deste documento é descrever de forma clara e estruturada:

- As funcionalidades do sistema
- Os requisitos funcionais e não funcionais
- O comportamento esperado da aplicação
- As necessidades dos usuários

Além disso, este documento servirá como base para o desenvolvimento, validação e evolução do sistema ao longo do projeto.

---

### 1.2 Escopo

O sistema Serpy tem como escopo:

- Identificação de animais peçonhentos
- Disponibilização de informações educativas
- Orientação em casos de emergência
- Registro e visualização de ocorrências
- Mapeamento de áreas de risco
- Suporte a diferentes perfis de usuários (comum, profissional e administrador)

Fora do escopo do sistema:

- Atendimento médico direto
- Substituição de profissionais da saúde
- Diagnósticos clínicos oficiais
- Responsabilidade por decisões médicas

O sistema atua como ferramenta de apoio informativo e preventivo.

---

### 1.3 Definições, Acrônimos e Abreviações

- **Animais peçonhentos**: Animais que produzem veneno e possuem mecanismo para inoculação (ex: serpentes, escorpiões, aranhas).
- **Ocorrência**: Registro de encontro ou acidente envolvendo animal peçonhento.
- **Usuário comum**: Pessoa que utiliza o sistema para consulta e aprendizado.
- **Profissional**: Usuário com atuação na área (ex: saúde, bombeiros, agentes ambientais).
- **Administrador**: Responsável pela gestão do sistema.
- **LGPD**: Lei Geral de Proteção de Dados, que regula o uso de dados pessoais no Brasil.
- **API**: Interface que permite integração entre sistemas.
---

##  2. Product Vision

### 2.1 Problema
Em 2023, o Brasil registrou mais de 341 mil acidentes com animais peçonhentos, alta de 16% em relação ao ano anterior, segundo o Ministério da Saúde. O Instituto Butantan aponta que trabalhadores rurais estão entre os mais atingidos e que o tempo entre a picada e o atendimento é fator decisivo para a gravidade do caso. A falta de informação acessível sobre identificação de animais e procedimentos de emergência agrava diretamente esse cenário.

### 2.2 Solução
O Serpy é uma plataforma digital mobile e web que reúne identificação de animais peçonhentos, orientação em emergências, monitoramento de áreas de risco e educação preventiva em um único ambiente acessível a qualquer pessoa.

### 2.3 Público-Alvo
- Trabalhadores rurais, maior grupo de vítimas de acidentes no Brasil
- Profissionais de saúde, bombeiros, policiais e agentes ambientais
- Moradores de áreas urbanas próximas à vegetação
- Comunidades com acesso limitado a serviços de saúde
- Estudantes e população em geral

### 2.4 Proposta de Valor
A OMS classifica acidentes com animais peçonhentos como doença tropical negligenciada, e o Brasil se comprometeu a reduzir em 50% a mortalidade ofídica até 2030. O Serpy contribui para esse objetivo levando informação confiável e orientação de emergência para qualquer pessoa com um smartphone, reduzindo o tempo de resposta em situações críticas.

### 2.5 Diferencial
Soluções existentes são fragmentadas — sites informativos sem geolocalização, apps educativos sem modo emergência, conteúdos em redes sociais sem confiabilidade. O Serpy integra tudo em um único ambiente, com funcionamento offline para regiões com conexão limitada.

### 2.6 Funcionalidades principais (alto nível)
- Funcionalidade 1: Catálogo de animais peçonhentos com identificação por seleção manual ou imagem
- Funcionalidade 2: Modo emergência com instruções de primeiros socorros e triagem por sintomas
- Funcionalidade 3: Mapa colaborativo de ocorrências com alertas de risco por geolocalização
- Funcionalidade 4: Módulo educacional com conteúdos, quizzes e certificados
- Funcionalidade 5: Sistema de gamificação com pontuação, badges e ranking de usuários
- Funcionalidade 6: Painel administrativo para gestão de usuários, conteúdos e estatísticas
- Funcionalidade 7: Funcionamento offline com sincronização automática ao restabelecer conexão

---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
O sistema proposto, denominado Serpy, tem como objetivo auxiliar na educação, prevenção e resposta a acidentes envolvendo animais peçonhentos, com foco principal em serpentes. O problema abordado é a dificuldade da população em identificar corretamente esses animais e saber como agir em situações de risco ou acidentes, sendo as informações sobre esses animais decisivas nesse tipos de caso. Além disso, há uma carência de ferramentas acessíveis que integram informação, prevenção e monitoramento em um único ambiente. A proposta de solução consiste em um software (web e mobile) que permite ao usuário identificar animais peçonhentos, acessar informações confiáveis ​​sobre suas características e níveis de risco, receber orientações de primeiros socorros em situações de emergência e registrar ocorrências geolocalizadas. O sistema também incorpora funcionalidades de monitoramento de áreas de risco por meio de um mapa de ocorrências, além de um módulo educacional com conteúdos e treinamentos. Para aumentar o engajamento, são utilizados elementos de gamificação, como pontuação, conquistas e desafios.

### 3.2 Stakeholders
Os principais usuários do sistema são:

- Usuários comuns que buscam identificar animais e obter orientações (Trabalhadores rurais, moradores de áreas urbanas,estudantes)
- Profissionais da saúde, que utilizam o sistema como apoio informativo
- Administradores, responsáveis ​​pelo gerenciamento de dados e monitoramento do sistema

### 3.3 Conclusão
Dessa forma, o sistema integra praticidade, educação e tecnologia, oferecendo suporte tanto para o uso cotidiano quanto para situações de emergência, contribuindo para a redução de acidentes e aumento da conscientização da população.

---

##  4. Requisitos Funcionais

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

---

##  5. Requisitos Não Funcionais

### 5.1 Performance (Desempenho)
- O sistema deve responder requisições em até **2 segundos** em condições normais.
- O sistema deve suportar no mínimo **1.000 usuários simultâneos**.
- O carregamento de imagens deve ocorrer em até **3 segundos**.
- O sistema deve possuir disponibilidade mínima de **99% (uptime)**.
- As consultas ao banco de dados devem ser otimizadas para evitar lentidão.

### 5.2 Security (Segurança)
- O sistema deve criptografar senhas utilizando **hash seguro**.
- O sistema deve implementar **autenticação de usuários (login)**.
- O sistema deve possuir **controle de acesso por níveis**:
  - Usuário comum
  - Profissional
  - Administrador
- O sistema deve utilizar **HTTPS** para comunicação segura.
- O sistema deve seguir diretrizes da **LGPD** para proteção de dados.

### 5.2 Usability (Usabilidade)
- O sistema deve ser **intuitivo e fácil de navegar**.
- O sistema deve ser **responsivo** (adaptável a celular e desktop).
- O sistema deve fornecer **feedback visual** (ex: carregamento, confirmação).
- O sistema deve utilizar linguagem clara e acessível.
- O sistema deve possuir acesso rápido a **instruções de emergência**.
---

##  6. Requisitos Organizacionais

### 6.1 Ambientais
- O sistema deverá ser acessado via navegador web, sendo compatível com os principais navegadores, como Google Chrome, Mozilla Firefox e Microsoft Edge, em suas versões atualizadas.
- O sistema deverá ser compatível com sistemas operacionais Windows 10 ou superior, garantindo funcionamento adequado em desktops e notebooks.
- O sistema deverá ser acessível por dispositivos móveis (smartphones e tablets), sendo compatível com sistemas Android e iOS, por meio de navegadores web.
- A interface do sistema deverá ser responsiva, adaptando-se automaticamente a diferentes tamanhos de tela, garantindo usabilidade tanto em computadores quanto em dispositivos móveis.
- Por se tratar de um sistema baseado na web, deverá ser possível acessá-lo em qualquer ambiente que possua conexão com a internet, sem necessidade de instalação local.

- O sistema deverá ser hospedado em ambiente de servidor, podendo ser em infraestrutura local (on-premise) ou em nuvem.
- O sistema deverá exigir conexão com a internet para seu funcionamento, sendo recomendado o uso de conexão estável e de boa velocidade.
- O acesso ao sistema deverá ocorrer por meio de navegadores web, permitindo sua utilização em diferentes dispositivos conectados à rede.
- O sistema deverá utilizar protocolos seguros de comunicação (HTTPS), garantindo a proteção dos dados trafegados.

- O sistema deverá registrar logs das principais operações realizadas pelos usuários, incluindo autenticação (login e logout), cadastros, missões feitas e bônus por participação.
- O sistema deverá registrar logs de erros e falhas, permitindo a identificação e correção de problemas.
- Os logs deverão conter informações como data, hora, usuário e ação realizada.
- Os registros de logs deverão ser armazenados de forma segura e acessível apenas a usuários autorizados (ex: administradores).


### 6.2 Operacionais
- O sistema deverá registrar logs das principais operações realizadas pelos usuários, incluindo autenticação (login e logout), cadastros, missões feitas e bônus por participação.
- O sistema deverá registrar logs de erros e falhas, permitindo a identificação e correção de problemas.
- Os logs deverão conter informações como data, hora, usuário e ação realizada.
- Os registros de logs deverão ser armazenados de forma segura e acessível apenas a usuários autorizados (ex: administradores).
  
- O sistema deverá possuir mecanismos de monitoramento para verificar sua disponibilidade e funcionamento contínuo.
- Deverá ser possível identificar falhas, lentidão ou indisponibilidade do sistema.
- O sistema deverá possibilitar ações de próximos níveis para aprendizagem rápidas todas as vezes que eles passarem de um nível.
 

### 6.3 Desenvolvimento
- O código-fonte do sistema deverá ser gerenciado por meio de sistema de controle de versão, utilizando a ferramenta Git.
- O projeto deverá manter um repositório centralizado, permitindo o controle de alterações e o histórico de versões.
- As alterações no código deverão ser registradas por meio de commits organizados e documentados.

- O desenvolvimento do sistema deverá seguir padrões de codificação.
- O código deverá utilizar nomenclaturas padronizadas para variáveis, funções e estruturas.
- O projeto deverá manter uma estrutura organizada de arquivos e módulos.
- O código deverá ser documentado sempre que necessário para facilitar o entendimento por outros desenvolvedores.

- O sistema deverá incluir testes para validação de suas funcionalidades principais.
-  ser implementados testes unitários para verificar o funcionamento de componentes individuais.
- Sempre que possível, deverão ser realizados testes de integração para validar a comunicação entre diferentes partes do sistema.
- Os testes deverão ser executados regularmente durante o processo de desenvolvimento.

---
##  7. Requisitos Externos

### 7.1 Reguladores
O sistema deverá seguir regulamentações e diretrizes relacionadas à proteção de dados e segurança da informação.

- Conformidade com a **LGPD (Lei Geral de Proteção de Dados)**.
- Proteção de dados pessoais dos usuários.
- Consentimento para coleta de informações e localização.
- Adequação a normas de segurança digital e armazenamento de dados.
- Adequação às diretrizes do Ministério da Saúde relacionadas à divulgação de informações sobre acidentes com animais peçonhentos.


### 7.2 Éticos

- O sistema deverá garantir que todos os usuários tenham acesso igual às funcionalidades do aplicativo, sem distinção de idade, gênero, raça ou condição social.
- O aplicativo deverá apresentar conteúdos educativos utilizando linguagem respeitosa e inclusiva.
- O conteúdo educativo deverá representar diferentes regiões e contextos do Brasil de forma imparcial.
- O aplicativo deverá apresentar informações confiáveis sobre animais peçonhentos, baseadas em fontes oficiais ou especialistas.
- O sistema deverá explicar de forma simples como os dados dos usuários serão utilizados e armazenados.
- O aplicativo deverá apresentar referências ou fontes utilizadas nos conteúdos educativos sempre que possível.
- O sistema deverá informar claramente que o aplicativo possui finalidade educativa e preventiva.

### 7.3 Legais
 O sistema deverá atender às legislações brasileiras aplicáveis ao desenvolvimento e utilização de sistemas digitais, especialmente aquelas relacionadas à proteção de dados, direitos digitais e responsabilidade sobre informações disponibilizadas ao usuário.
- Lei Geral de Proteção de Dados Pessoais (LGPD - Lei nº 13.709/2018)
Responsável pela regulamentação da coleta, armazenamento, processamento e compartilhamento de dados pessoais dos usuários.
- Marco Civil da Internet (Lei nº 12.965/2014)
Define princípios, garantias, direitos e deveres para o uso da internet no Brasil, incluindo privacidade e proteção de registros dos usuários.
- Código de Defesa do Consumidor (Lei nº 8.078/1990)
Aplicável na transparência das informações fornecidas aos usuários e responsabilidade sobre os serviços digitais disponibilizados.
- Lei de Direitos Autorais (Lei nº 9.610/1998)
Relacionada ao uso legal de imagens, conteúdos educativos, materiais gráficos e demais mídias utilizadas no sistema.
- Constituição Federal de 1988 - Artigo 5º
Garantia dos direitos fundamentais relacionados à privacidade, intimidade e proteção de dados pessoais.
- Normas e diretrizes do Ministério da Saúde
Aplicáveis à divulgação de informações educativas e preventivas sobre acidentes com animais peçonhentos.
- Normas de Segurança da Informação (ISO/IEC 27001 - referência recomendada)
Utilizadas como referência para boas práticas de segurança digital, proteção e gerenciamento de informações.
- Diretrizes de acessibilidade digital (WCAG e eMAG)
Recomendadas para garantir acessibilidade e inclusão de usuários com deficiência no sistema.

### 7.4 Segurança Externa

O sistema deverá implementar mecanismos de segurança voltados à proteção contra ameaças externas, acessos não autorizados, vazamento de dados e ataques cibernéticos, garantindo a integridade, disponibilidade e confidencialidade das informações armazenadas.

- O sistema deverá utilizar comunicação segura por meio do protocolo HTTPS/TLS em todas as requisições realizadas entre cliente e servidor.

- O sistema deverá possuir mecanismos de proteção contra ataques comuns em aplicações web, incluindo:

*SQL Injection;

*Cross-Site Scripting (XSS);

*Cross-Site Request Forgery (CSRF);

*Brute Force;

*Upload de arquivos maliciosos.

- O sistema deverá limitar tentativas consecutivas de login inválidas, podendo bloquear temporariamente o acesso após múltiplas falhas de autenticação.

- O sistema deverá validar e sanitizar todos os dados recebidos de usuários antes do processamento ou armazenamento.

- O sistema deverá utilizar autenticação segura e controle de permissões baseado em níveis de acesso:

*Usuário comum;

*Profissional;

*Administrador.

- O sistema deverá registrar logs de segurança contendo:

*Tentativas de login;

*Alterações importantes no sistema;

*Acessos administrativos;

*Falhas e erros críticos.

- Os logs de segurança deverão ser armazenados de forma protegida e acessíveis apenas por administradores autorizados.

- O sistema deverá possuir mecanismos de backup periódico para prevenção contra perda de dados.

- O sistema deverá realizar auditorias periódicas de segurança para identificação de vulnerabilidades e possíveis falhas no sistema.

- O sistema deverá manter dependências, bibliotecas e frameworks atualizados para reduzir riscos de exploração de vulnerabilidades conhecidas.

- O sistema deverá proteger informações sensíveis dos usuários conforme as diretrizes da LGPD.

- O sistema deverá possuir mecanismos de monitoramento para detectar atividades suspeitas, acessos incomuns ou possíveis tentativas de invasão.  

### 7.5 Contábeis
O sistema deverá manter controle das funcionalidades financeiras e registros administrativos, caso existam serviços pagos.

- Registro de transações relacionadas a cursos e certificados.
- Geração de relatórios financeiros básicos.
- Histórico de pagamentos realizados.
- Controle de assinaturas e funcionalidades premium.
- Armazenamento seguro de comprovantes e registros administrativos.
---
