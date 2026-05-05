# Requirements Specification

## System Overview
O sistema proposto tem como objetivo resolver a falta de previsibilidade em áreas de pastagens, plantações e reservas ambientais que são propensas a incêndios. Atualmente, há dificuldade em antecipar focos de queimadas, o que pode gerar grandes prejuízos ambientais, econômicos e sociais.
A solução proposta consiste na criação de um sistema inteligente que utiliza dados fornecidos por constelações de nanosatélites da AEB e do INPE. Esses dados serão analisados e cruzados com históricos de ocorrências de queimadas, permitindo identificar padrões. A partir disso, será utilizada Inteligência Artificial para prever áreas com maior risco de incêndios, funcionando de forma semelhante a uma previsão do tempo, porém voltada para focos de fogo.
O sistema contará com um dashboard interativo que exibirá mapas de satélite com as regiões mais propensas a queimadas, facilitando a tomada de decisão preventiva.
Os principais usuários do sistema serão donos de terras e gestores, incluindo fazendeiros, pequenos agricultores, sitiantes e órgãos governamentais responsáveis pela gestão ambiental e prevenção de desastres.


## Functional Requirements

*FR01 - Coletar dados de satélites (AEB e INPE) para monitoramento ambiental.
*FR02 - Analisar dados históricos de queimadas para identificar padrões de risco.
*FR03 - Prever áreas propensas a incêndios utilizando algoritmos de Inteligência Artificial.
*FR04 - Exibir mapa interativo com regiões classificadas por nível de risco de queimadas.
*FR05 - Permitir visualização em dashboard com gráficos e indicadores de risco.
*FR06 - Permitir cadastro de usuários como fazendeiros, agricultores e órgãos governamentais.
*FR07 - Enviar alertas para usuários sobre áreas com alto risco de incêndio.

## Non-Functional Requirements

* Performance:
RNF01 - Tempo de Resposta: O sistema deve carregar as camadas de mapeamento e os polígonos de risco em no máximo 2 segundos após a solicitação do usuário.

RNF02 - Escalabilidade: A infraestrutura deve ser capaz de suportar até 10.000 usuários simultâneos mantendo a latência abaixo de 500ms.

RNF03 - Disponibilidade: O serviço deve possuir um índice de disponibilidade (Uptime) de 99,9%, operando 24 horas por dia, 7 dias por semana.
* Security:
RNF05 - Criptografia de Dados: Todos os dados sensíveis dos usuários e perímetros das propriedades devem ser armazenados utilizando criptografia AES-256.

RNF06 - Conformidade Legal: O sistema deve estar em total conformidade com a LGPD (Lei Geral de Proteção de Dados), garantindo o direito à exclusão de dados em até 48 horas após a solicitação.

RNF07 - Autenticação: Implementação de Autenticação de Dois Fatores (2FA) para acessos de contas governamentais e administradores de grandes terras.
* Usability:
RNF09 - Facilidade de Navegação: Um usuário leigo deve ser capaz de localizar sua área e visualizar o risco de incêndio com no máximo 3 cliques a partir da tela inicial.

RNF10 - Responsividade: A interface deve ser adaptável (Mobile-First), funcionando perfeitamente em telas a partir de 360px de largura, garantindo que o fazendeiro consiga usar o dashboard no celular em campo.

RNF11 - Acessibilidade Visual: O dashboard deve manter um contraste mínimo de 4.5:1 (padrão WCAG AA) para garantir a leitura sob luz solar intensa, comum em ambientes de campo e pastagens.
