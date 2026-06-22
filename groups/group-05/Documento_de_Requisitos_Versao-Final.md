#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
Este documento tem como objetivo descrever os requisitos funcionais e não funcionais do sistema StockFácil, um software web voltado à gestão de estoque de pequenas empresas e e-commerces varejistas. O sistema foi desenvolvido com foco na simplicidade de uso, permitindo que qualquer usuário opere a plataforma sem necessidade de treinamento prévio.
### 1.2 Escopo
O StockFácil é uma plataforma web que permite às empresas controlar o fluxo de estoque de forma digital e centralizada. O sistema contempla o cadastro de produtos, fornecedores e usuários, o registro de entradas e saídas, a geração de relatórios, alertas automáticos e um painel de indicadores em tempo real.
Está fora do escopo deste sistema:
- Emissão de notas fiscais ou integração com sistemas contábeis.
- Funcionalidades de ponto de venda (PDV).
- Gestão financeira ou contas a pagar/receber.
- Integração nativa com plataformas de e-commerce de terceiros.

### 1.3 Definições, Acrônimos e Abreviações
Para garantir o alinhamento de toda a equipe e facilitar a leitura deste documento, definem-se os seguintes termos: 

- SKU: Stock Keeping Unit – código único de identificação de produto.
- RF: Requisito Funcional.
- RNF: Requisito Não Funcional.
- CNPJ: Cadastro Nacional da Pessoa Jurídica.
- Dashboard: Painel visual com indicadores e resumo de informações do sistema.
- bcrypt: Algoritmo de hash criptográfico utilizado para armazenamento seguro de senhas.
- TLS: Transport Layer Security – protocolo de criptografia de dados.

---

##  2. Product Vision

### 2.1 Problema
Muitas empresas e pequenos negócios enfrentam dificuldades no controle de estoque interno, como falta de organização, erros manuais, perda de produtos, dificuldade em acompanhar entradas e saídas e ausência de dados em tempo real. Esses problemas podem gerar prejuízos financeiros, desperdício de recursos e baixa eficiência operacional.

### 2.2 Solução
O StockFácil permite que as empresas monitorem o fluxo de estoque em tempo real, acompanhando as entradas e saídas de produtos. Além disso, o sistema gera relatórios personalizados com base nesses dados como listas de saldos atuais e resumo de movimentações e oferece alertas automáticos para estoque abaixo do nível mínimo configurado ou acima do esperado.

### 2.3 Público-Alvo
Os principais usuários do aplicativo serão:
-	Pequenos comerciantes com lojas físicas e/ou virtuais (e-commerce)
-	Empreendedores do varejo que precisam controlar produtos, entradas e saídas.
-	Equipes de almoxarifado
-	Gestores de microempresas que desejam substituir controles manuais ou planilhas
-	Equipes de estoque com múltiplos operadores e necessidade de controle de acesso

### 2.4 Proposta de Valor
O StockFácil oferece a pequenas empresas acesso a um sistema moderno e acessível para controle de estoque, substituindo planilhas desorganizadas e processos manuais por uma plataforma centralizada, visual e de fácil operação. O sistema entrega visibilidade em tempo real sobre os produtos, reduzindo perdas, evitando rupturas de estoque e aumentando a eficiência operacional.

### 2.5 Diferencial
O principal diferencial do StockFácil é a simplicidade de uso. A interface foi projetada para ser intuitiva e autoexplicativa, dispensando treinamentos formais para a operação do dia a dia. Diferentemente de sistemas ERP complexos, o StockFácil foca exclusivamente na gestão de estoque, com fluxos simplificados e alertas proativos que apoiam a tomada de decisão mesmo por usuários sem experiência com software de gestão.

### 2.6 Funcionalidades principais (alto nível)
- Cadastro e gestão de produtos com código SKU, categoria e unidade de medida.
- Registro de entradas e saídas de estoque com histórico completo.
- Dashboard com indicadores em tempo real: saldo total, produtos críticos e últimas movimentações.
- Alertas automáticos de estoque mínimo e excesso.
- Geração de relatórios por período, produto ou categoria.
- Controle de acesso por perfis de usuário (administrador, operador, visualizador).
- Importação e exportação de dados em CSV/Excel.
---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
O StockFácil é um aplicativo web para gestão de estoque de pequenas empresas e e-commerces varejistas. A plataforma permite registrar e monitorar movimentações de produtos em tempo real, com alertas de reposição e relatórios dinâmicos, substituindo planilhas manuais e processos desorganizados. O sistema é acessível via navegador web em dispositivos desktop e móveis, garantindo flexibilidade operacional para equipes de estoque.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais
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

**Detalhamento dos requisitos principais:**

### RF01 - Cadastro de usuario
**Descrição:**  
Permitir o cadastro de usuários com diferentes perfis de acesso (administrador, operador, visualizador).

**Prioridade:** Alta  
**Entradas:** Nome completo, e-mail, senha, perfil de acesso selecionado. 
**Saídas:** Usuário cadastrado e ativo no sistema, com permissões aplicadas conforme o perfil.
**Regras de negócio:**
Apenas administradores podem criar, editar ou excluir usuários. O e-mail deve ser único por conta. Não é possível excluir o último administrador ativo.

---

### RF03 - Cadastro de produtos
**Descrição:**  
O sistema deve permitir o cadastro, edição e exclusão de produtos, incluindo os campos: nome, código SKU, categoria, unidade de medida, descrição, quantidade mínima e custo de compra.

**Prioridade:** Alta  
**Entradas:** Nome do produto, SKU, categoria, unidade de medida, descrição, quantidade mínima, custo unitário.
**Saídas:** Produto criado, editado ou removido do catálogo. Saldo inicial registrado.
**Regras de negócio:**
O código SKU deve ser único por empresa. A exclusão de produto só é permitida se não houver movimentações vinculadas. Somente administradores e operadores podem cadastrar ou editar produtos.

---

### RF04 - Registro de Entradas e Saídas
**Descrição:**  
O sistema deve permitir o registro de movimentações de estoque (entrada ou saída), informando o produto, a quantidade, a data e o usuário responsável. O saldo do produto deve ser atualizado automaticamente.

**Prioridade:** Alta  
**Entradas:** Tipo de movimentação (entrada/saída), produto, quantidade, data, observação opcional. 
**Saídas:** Movimentação registrada, saldo atualizado em tempo real, histórico atualizado.
**Regras de negócio:**
Não é permitido registrar saída com quantidade superior ao saldo disponível. Movimentações não podem ser excluídas, apenas estornadas. O usuário responsável é registrado automaticamente pela sessão ativa.

---

### RF06 - Alertas Automáticos de Estoque
**Descrição:**  
Permitir o cadastro de usuários com diferentes perfis de acesso (administrador, operador, visualizador).

**Prioridade:** Alta  
**Entradas:** Nome completo, e-mail, senha, perfil de acesso selecionado. 
**Saídas:** Usuário cadastrado e ativo no sistema, com permissões aplicadas conforme o perfil.
**Regras de negócio:**
Os limites mínimo e máximo são definidos individualmente por produto. Alertas repetidos para o mesmo produto não devem ser gerados mais de uma vez por hora.

---

### RF07 - Geração de Relatórios
**Descrição:**  
O sistema deve permitir a geração de relatórios de movimentação de estoque, podendo ser filtrados por período, produto ou categoria. Os relatórios devem ser exportáveis em PDF e CSV.

**Prioridade:** Média
**Entradas:** Filtros selecionados: período (data inicial e final), produto e/ou categoria.
**Saídas:** Relatório exibido em tela e disponível para download em PDF ou CSV.
**Regras de negócio:**
Relatórios de períodos superiores a 12 meses devem exigir confirmação do usuário. Apenas administradores e visualizadores têm acesso à geração de relatórios completos.

---

### RF11 - Dashboard de Indicadores
**Descrição:**  
O sistema deve exibir um painel visual com os principais indicadores do estoque: total de itens cadastrados, produtos com estoque crítico (abaixo do mínimo), produtos com excesso, valor total do estoque e as últimas movimentações realizadas.

**Prioridade:** Alta  
**Entradas:** Dados consolidados do banco de dados em tempo real
**Saídas:** Painel atualizado automaticamente com gráficos e números-chave do estoque.
**Regras de negócio:**
O dashboard deve ser a primeira tela exibida após o login. Deve ser carregado em no máximo 3 segundos. Os dados devem refletir o estado atual do estoque sem necessidade de atualização manual.

---

##  5. Requisitos Não Funcionais

### 5.1 Usabilidade
- O sistema deve ser totalmente responsivo, adaptando-se a dispositivos móveis, tablets e desktops.
- O usuário deve conseguir registrar uma entrada ou saída de estoque em no máximo 3 cliques a partir do menu principal.
- O sistema deve exibir mensagens de erro claras e orientações de correção sempre que uma ação falhar.
- O dashboard principal deve apresentar os indicadores mais importantes de forma visual e de fácil interpretação.
- O sistema deve seguir padrões de acessibilidade WCAG 2.1 nível AA.

---

### 5.2 Eficiência
- O sistema deve responder a qualquer requisição do usuário em até 2 segundos em condições normais de uso.
- O sistema deve suportar até 500 usuários simultâneos sem degradação de desempenho.
- Operações de busca e filtro de produtos devem retornar resultados em menos de 1 segundo.

### 5.3 Desempenho
- •
- O carregamento inicial do dashboard não deve ultrapassar 3 segundos em conexões de banda larga.
- A geração de relatórios de até 12 meses de histórico deve ser concluída em no máximo 5 segundos.
- O sistema deve processar o registro de uma movimentação e atualizar o saldo em menos de 1 segundo.

### 5.4 Espaço
- Cada empresa contratante terá uma cota inicial de armazenamento de até 5 GB para dados e históricos de movimentações.
- Arquivos importados via CSV/Excel não devem ultrapassar 10 MB por operação.
- O sistema deve utilizar compressão de dados e paginação para minimizar o consumo de memória nas consultas.
- Logs de auditoria devem ser retidos por no mínimo 12 meses e arquivados automaticamente após esse período.

### 5.5 Confiabilidade
- O sistema deve ter disponibilidade mínima de 99,5% ao mês, exceto em manutenções programadas com aviso prévio.
- Em caso de falha, o sistema deve se recuperar automaticamente sem perda de dados já confirmados.
- Todas as operações críticas (registros de movimentação, alterações de cadastro) devem utilizar transações atômicas no banco de dados.
- O sistema deve realizar backups automáticos diários dos dados com retenção de 30 dias.

### 5.6 Segurança (Proteção)
- O sistema deve criptografar senhas utilizando algoritmo de hash seguro (bcrypt com salt).
- O sistema deve implementar autenticação com bloqueio após 5 tentativas incorretas consecutivas.
- O sistema deve restringir o acesso às funcionalidades conforme o perfil do usuário (administrador, operador, visualizador).
- Todas as comunicações devem ser realizadas via HTTPS (TLS 1.2 ou superior).
- Tokens de sessão devem expirar após 8 horas de inatividade, exigindo novo login.
- O sistema deve registrar logs de auditoria para ações críticas, como exclusão de produtos e alterações de estoque.

---

##  6. Requisitos Organizacionais

### 6.1 Ambientais
- •	O sistema deve ser hospedado em infraestrutura de nuvem (AWS, GCP ou Azure), utilizando serviços gerenciados de banco de dados e balanceamento de carga.
- •	O ambiente de produção deve ser separado dos ambientes de desenvolvimento e homologação.
- •	O sistema deve ser compatível com os navegadores Google Chrome, Mozilla Firefox, Microsoft Edge e Safari nas duas versões mais recentes.
- •	O servidor de aplicação deve operar em Linux (Ubuntu 22.04 LTS ou superior).

### 6.2 Operacionais
- O sistema deve registrar logs de acesso, erros e ações críticas em formato estruturado (JSON) para facilitar a análise e auditoria.
- Deve haver monitoramento contínuo de disponibilidade e desempenho, com alertas automáticos para a equipe de operações em caso de incidentes.
- Manutenções programadas devem ser comunicadas com pelo menos 48 horas de antecedência e realizadas preferencialmente fora do horário comercial.
- O sistema deve disponibilizar uma página de status pública informando a saúde dos serviços em tempo real.

### 6.3 Desenvolvimento
- O versionamento do código-fonte deve ser realizado com Git, utilizando o modelo de branches GitFlow (main, develop, feature, hotfix).
- O código deve seguir os padrões de clean code, com nomenclatura clara, funções com responsabilidade única e ausência de duplicação desnecessária.
- Devem ser implementados testes automatizados unitários e de integração, com cobertura mínima de 80% nas funcionalidades críticas.
- O processo de CI/CD deve garantir que todo código mesclado na branch principal seja validado automaticamente antes da implantação em produção.
- A documentação técnica das APIs deve ser mantida atualizada utilizando o padrão OpenAPI (Swagger).

---

##  7. Requisitos Externos

### 7.1 Reguladores
- O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018), garantindo que os dados pessoais dos usuários.
- O sistema deve manter registros de consentimento e logs de acesso a dados pessoais para fins de auditoria regulatória.

### 7.2 Éticos
- O sistema não deve adotar qualquer mecanismo que discrimine usuários com base em raça, gênero, idade, localização ou qualquer outro fator pessoal no acesso às funcionalidades.
- O sistema não deve coletar dados além do estritamente necessário para o funcionamento da plataforma.
- Em caso de alterações nos termos de uso ou política de privacidade, os usuários devem ser notificados com antecedência e de forma clara.

### 7.3 Legais
- O sistema deve estar em conformidade com o Marco Civil da Internet (Lei nº 12.965/2014), respeitando as diretrizes de privacidade, neutralidade e responsabilidade no ambiente digital.
- Os contratos de uso da plataforma devem estar alinhados ao Código de Defesa do Consumidor (Lei nº 8.078/1990), garantindo clareza nas condições de serviço.
- O armazenamento e o tratamento de dados devem respeitar as legislações brasileiras vigentes sobre proteção de dados e segurança da informação.

### 7.4 Segurança Externa
- O sistema deve possuir mecanismos de proteção contra invazoes, vazamento de dados e acessos não autorizados, ultilizando sistemas de criptografia, altenticadores e sistemas de monitoramento.
- Deve ser realizada pelo menos uma auditoria de segurança externa anualmente, com relatório de vulnerabilidades e plano de correção.

### 7.5 Contábeis
- O sistema deve registrar todas as movimentações de estoque com data, hora e usuário responsável, garantindo rastreabilidade completa para fins contábeis.
- O sistema deve permitir a exportação dos dados de movimentação em formatos compatíveis com ferramentas contábeis (CSV e Excel).

---
