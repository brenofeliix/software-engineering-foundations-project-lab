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
