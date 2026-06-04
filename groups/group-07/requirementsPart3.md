## 5. Assumptions (Premissas)

**ASSUMPTION-01** - As APIs de dados de satélite da AEB e do INPE estarão operacionais e acessíveis publicamente (ou via convênio) durante todo o ciclo de vida do sistema, mantendo frequência de atualização de imagens compatível com o monitoramento em tempo próximo ao real.

**ASSUMPTION-02** - Os dados históricos de queimadas fornecidos pelo INPE (programa BDQueimadas) e pela NASA (FIRMS) possuem qualidade, completude e granularidade suficientes para o treinamento e validação dos modelos de Inteligência Artificial.

**ASSUMPTION-03** - Os usuários finais (produtores rurais, fazendeiros e sitiantes) possuem acesso à internet móvel (3G ou superior) em suas propriedades, viabilizando o recebimento de alertas e o acesso ao dashboard em campo.

**ASSUMPTION-04** - Os usuários finais possuem smartphones com sistema operacional Android 10+ ou iOS 14+ e navegadores compatíveis com tecnologias web modernas (WebSockets, geolocalização, notificações push).

**ASSUMPTION-05** - Os limites geográficos das propriedades rurais cadastradas serão informados corretamente pelos próprios usuários ou obtidos via integração com bases públicas (ex: CAR — Cadastro Ambiental Rural), assumindo-se a veracidade dos dados fornecidos.

**ASSUMPTION-06** - As imagens de satélite utilizadas terão resolução espacial mínima suficiente para identificar focos de calor em áreas a partir de 1 hectare, conforme especificações dos sensores MODIS e VIIRS.

**ASSUMPTION-07** - O provedor de infraestrutura em nuvem escolhido (ex: AWS, GCP ou Azure) garantirá os SLAs de disponibilidade necessários para manter o uptime de 99,9% definido em RNF03.

**ASSUMPTION-08** - Os órgãos governamentais e cooperativas interessadas possuem equipe técnica mínima capaz de interpretar os dados de risco exibidos pelo dashboard e acionar os protocolos de resposta adequados.

---

## 6. Constraints (Restrições)

**CONSTRAINT-01** - O sistema deve estar em total conformidade com a LGPD (Lei nº 13.709/2018), garantindo consentimento explícito para coleta de dados pessoais, direito à exclusão e portabilidade de dados dos usuários.

**CONSTRAINT-02** - O sistema deve utilizar exclusivamente fontes de dados de satélite de acesso público ou disponibilizadas por convênio institucional (AEB, INPE, NASA), sendo vedada a aquisição de imagens de satélite comerciais pagas.

**CONSTRAINT-03** - A interface do sistema deve ser desenvolvida com abordagem Mobile-First e responsiva, sendo obrigatória a compatibilidade com navegadores Chrome, Firefox e Safari em suas duas últimas versões estáveis.

**CONSTRAINT-04** - Toda comunicação entre cliente e servidor deve utilizar o protocolo HTTPS (TLS 1.2 ou superior), sendo proibida a transmissão de dados em texto plano.

**CONSTRAINT-05** - O armazenamento de senhas deve utilizar exclusivamente algoritmos de hash seguros (BCrypt com fator de custo mínimo 12), sendo proibido o armazenamento de senhas em texto plano ou com algoritmos obsoletos (MD5, SHA-1).

**CONSTRAINT-06** - O sistema deve ser hospedado em infraestrutura de nuvem com data center localizado em território brasileiro, em conformidade com as exigências de soberania de dados aplicáveis a informações geoespaciais nacionais.

**CONSTRAINT-07** - O prazo de desenvolvimento do MVP (Minimum Viable Product) é limitado ao semestre acadêmico vigente, devendo ser entregue em versão funcional até a data de avaliação final da disciplina.

**CONSTRAINT-08** - O orçamento do projeto é limitado a recursos gratuitos ou de camada free-tier de serviços em nuvem, não havendo verba disponível para contratação de serviços pagos de infraestrutura ou APIs comerciais.

**CONSTRAINT-09** - Os modelos de Inteligência Artificial devem ser treinados utilizando frameworks open-source (ex: TensorFlow, PyTorch, Scikit-learn), sendo vedado o uso de soluções proprietárias de ML que gerem dependência de fornecedor (vendor lock-in).

**CONSTRAINT-10** - O esquema de cores do dashboard deve seguir obrigatoriamente o padrão semafórico (Verde/Amarelo/Vermelho) com contraste mínimo de 4.5:1 (WCAG AA), sem margem para escolhas de paleta que comprometam a legibilidade em ambientes de alta luminosidade.
