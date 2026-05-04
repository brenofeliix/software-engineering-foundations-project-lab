# Group 11

## Project Name

Plumer

## Team Members

Ernani Plumer Santos Pinto

## Repository Structure

/docs

  01-product-vision

  02-requirements

  03-modeling

  04-architecture

  05-testing

  06-prototype

---

# Requirements Specification

## 1. System Overview (Visão Geral do Sistema)

O **Plumer** é uma plataforma SaaS (web/PWA) de gestão empresarial integrada, desenvolvida para resolver o problema da fragmentação de ferramentas financeiras, fiscais e contábeis enfrentada por micro e pequenas empresas brasileiras e seus escritórios de contabilidade. A solução unifica cinco módulos principais — Money (financeiro), Box (documentos fiscais), Emissor (emissão de NF-e/NFS-e), Contábil (contabilidade em partidas dobradas) e Estoque (controle de inventário) — em uma única plataforma com inteligência artificial embarcada. O público-alvo são contadores que gerenciam múltiplas empresas simultaneamente e micro/pequenos empresários que precisam de gestão financeira e fiscal sem a complexidade de ERPs corporativos.

---

## 2. Functional Requirements (Requisitos Funcionais)

### Módulo Geral / Autenticação

- **FR01:** O sistema deve permitir o cadastro de usuários com nome, e-mail, CPF, telefone e senha.
- **FR02:** O sistema deve permitir login com autenticação por e-mail e senha.
- **FR03:** O sistema deve permitir a gestão de múltiplas empresas (entidades) em uma única conta de usuário, com alternância entre elas.
- **FR04:** O sistema deve permitir a configuração de perfis de acesso com permissões granulares por módulo (Money, Box, Emissor, Contábil, Estoque).
- **FR05:** O sistema deve registrar todas as ações dos usuários em um log de auditoria com data, hora, módulo, ação e descrição.
- **FR06:** O sistema deve permitir o compartilhamento de documentos fiscais via WhatsApp e e-mail.
- **FR07:** O sistema deve funcionar como PWA (Progressive Web App), permitindo instalação como aplicativo no celular e desktop.

### Módulo Money (Financeiro)

- **FR08:** O sistema deve permitir o cadastro de contas bancárias (corrente, poupança, caixa, investimento) com saldo de abertura.
- **FR09:** O sistema deve permitir o registro de contas a pagar com descrição, valor, vencimento, categoria, fornecedor e status de pagamento.
- **FR10:** O sistema deve permitir o registro de contas a receber com descrição, valor, vencimento, categoria, cliente e status de recebimento.
- **FR11:** O sistema deve permitir a liquidação parcial de contas com registro de juros, multa e desconto.
- **FR12:** O sistema deve gerar cobranças PIX automatizadas com QR Code e código Copia e Cola, integrado com C6 Bank e Sicoob.
- **FR13:** O sistema deve permitir a importação inteligente de extratos bancários com categorização automática por IA.
- **FR14:** O sistema deve gerar relatório DRE (Demonstração do Resultado do Exercício) por período.
- **FR15:** O sistema deve gerar relatório de Fluxo de Caixa realizado e projetado.
- **FR16:** O sistema deve permitir o cadastro e acompanhamento de investimentos com aportes e resgates.
- **FR17:** O sistema deve permitir transferências entre contas bancárias da mesma entidade.
- **FR18:** O sistema deve permitir a configuração de despesas e receitas recorrentes (fixas/mensais).
- **FR19:** O sistema deve exibir um dashboard financeiro com saldo atual, receitas, despesas, resultado líquido e inadimplência.
- **FR20:** O sistema deve permitir o cadastro de clientes e fornecedores com CPF/CNPJ, nome, contato e endereço.
- **FR21:** O sistema deve permitir a seleção e operação em lote de múltiplos lançamentos.
- **FR22:** O sistema deve gerar e enviar comprovantes de pagamento e recibos de recebimento.
- **FR23:** O sistema deve permitir o cadastro de vendedores e vinculação a contas a receber.
- **FR24:** O sistema deve gerar relatório gerencial completo com faturamento, despesas e inadimplência.

### Módulo Box (Documentos Fiscais)

- **FR25:** O sistema deve sincronizar automaticamente NF-e e CT-e com a SEFAZ utilizando certificado digital A1.
- **FR26:** O sistema deve sincronizar automaticamente NFS-e com a ADN Nacional.
- **FR27:** O sistema deve permitir o upload manual de arquivos XML de documentos fiscais (NF-e, CT-e, NFS-e).
- **FR28:** O sistema deve permitir a busca de documentos fiscais pela chave de acesso de 44 dígitos.
- **FR29:** O sistema deve exibir um explorador de documentos fiscais com filtros por tipo, período e status.
- **FR30:** O sistema deve gerar resumo fiscal do período com totais de notas emitidas, valores e impostos (ICMS, PIS, COFINS, ISS).
- **FR31:** O sistema deve disponibilizar um catálogo de códigos NCM com busca e importação em lote via planilha Excel.
- **FR32:** O sistema deve permitir a importação de documentos fiscais via planilha Excel.

### Módulo Emissor (Emissão Fiscal)

- **FR33:** O sistema deve permitir a emissão de NFS-e (Nota Fiscal de Serviço Eletrônica) com transmissão para a prefeitura.
- **FR34:** O sistema deve permitir a emissão de NF-e Modelo 55 (Nota Fiscal Eletrônica de produtos) com transmissão para a SEFAZ.
- **FR35:** O sistema deve preencher automaticamente dados tributários da NFS-e utilizando IA, aprendendo com o histórico do usuário.
- **FR36:** O sistema deve calcular e sugerir automaticamente as retenções fiscais na fonte (PIS, COFINS, CSLL, IRRF, INSS).
- **FR37:** O sistema deve permitir a criação e gerenciamento de rascunhos de notas fiscais.
- **FR38:** O sistema deve permitir o cancelamento de notas fiscais emitidas dentro do prazo legal.
- **FR39:** O sistema deve gerar o DANFSE (PDF da NFS-e) e DANFE (PDF da NF-e) para download e envio.
- **FR40:** O sistema deve permitir o envio automático do DANFSE por e-mail ao tomador após a emissão.
- **FR41:** O sistema deve exibir erros de emissão com sugestões de correção geradas por IA.
- **FR42:** O sistema deve permitir o cadastro de produtos para emissão de NF-e com NCM, CFOP, CST e dados tributários.
- **FR43:** O sistema deve gerar relatório de notas emitidas por período, filtráveis por tipo e status.
- **FR44:** O sistema deve permitir a geração, impressão e envio de recibos de venda com vinculação a vendedores.

### Módulo Contábil

- **FR45:** O sistema deve permitir a criação de lançamentos contábeis em partidas dobradas (débito e crédito).
- **FR46:** O sistema deve manter um Plano de Contas estruturado por grupo e natureza (Ativo, Passivo, Receita, Despesa).
- **FR47:** O sistema deve gerar o Livro Diário contábil com todos os lançamentos do período.
- **FR48:** O sistema deve gerar o Livro Razão por conta contábil específica.
- **FR49:** O sistema deve gerar o Balancete de Verificação com saldo anterior conforme IFRS/CPC 26.
- **FR50:** O sistema deve gerar o Balanço Patrimonial sintético e a DRE (Demonstração do Resultado do Exercício).
- **FR51:** O sistema deve permitir o fechamento e reabertura de períodos contábeis mensais.
- **FR52:** O sistema deve executar o encerramento de exercício conforme CPC 26.
- **FR53:** O sistema deve calcular automaticamente 13 indicadores financeiros (Liquidez Corrente, Seca, Imediata, Geral, entre outros).
- **FR54:** O sistema deve utilizar IA (Gemini) para sugerir lançamentos contábeis automaticamente a partir de dados financeiros.
- **FR55:** O sistema deve sincronizar automaticamente dados dos módulos Money, Box e Emissor com o módulo Contábil.

### Módulo Estoque

- **FR56:** O sistema deve permitir o cadastro de produtos com controle de estoque mínimo, máximo e ponto de reposição.
- **FR57:** O sistema deve registrar movimentações de estoque (entradas, saídas e ajustes) manuais.
- **FR58:** O sistema deve registrar entrada automática de estoque ao processar NF-e de compra no Plumer Box.
- **FR59:** O sistema deve registrar saída automática de estoque ao emitir recibo de venda no Plumer Emissor.
- **FR60:** O sistema deve permitir a criação de ordens de produção com consumo de insumos e geração de produto acabado.
- **FR61:** O sistema deve suportar os métodos de custo Média Ponderada e PEPS/FIFO.
- **FR62:** O sistema deve exibir dashboard de estoque com indicadores de produtos ativos, críticos e sem estoque.
- **FR63:** O sistema deve gerar relatório de posição atual do estoque, movimentações por período e valorização.
- **FR64:** O sistema deve emitir alertas quando um produto atingir o estoque mínimo definido.

---

## 3. Non-Functional Requirements (Requisitos Não Funcionais)

### Usabilidade

- **NFR01:** O sistema deve ter interface responsiva, adaptando-se a dispositivos desktop, tablet e smartphone.
- **NFR02:** O sistema deve ser instalável como PWA (Progressive Web App) nos navegadores Chrome e Safari.
- **NFR03:** O sistema deve disponibilizar tutoriais interativos integrados para cada módulo, com passo a passo visual.

### Desempenho

- **NFR04:** O sistema deve carregar o dashboard principal em no máximo 3 segundos em conexões de banda larga.
- **NFR05:** A emissão de uma NFS-e deve ser processada e transmitida à prefeitura em no máximo 10 segundos.
- **NFR06:** A sincronização de documentos fiscais com a SEFAZ deve processar no mínimo 50 documentos por minuto.

### Segurança

- **NFR07:** O sistema deve utilizar autenticação por e-mail e senha com hash seguro (bcrypt ou similar).
- **NFR08:** O sistema deve utilizar comunicação criptografada via HTTPS/TLS em todas as requisições.
- **NFR09:** O certificado digital A1 deve ser armazenado de forma criptografada no servidor.
- **NFR10:** O sistema deve manter log de auditoria completo e imutável de todas as ações dos usuários.
- **NFR11:** O sistema deve implementar controle de acesso por perfis (ADMIN_MASTER, ADMIN_ENTIDADE, USUARIO, SUPORTE) com permissões granulares.

### Disponibilidade

- **NFR12:** O sistema deve estar disponível 99,5% do tempo (uptime), permitindo no máximo 3,65 horas de indisponibilidade por mês.
- **NFR13:** O sistema deve ser hospedado em infraestrutura cloud com backups automáticos diários.

### Compatibilidade

- **NFR14:** O sistema deve ser compatível com os navegadores Google Chrome, Mozilla Firefox, Safari e Microsoft Edge em suas versões mais recentes.
- **NFR15:** O sistema deve integrar-se com APIs bancárias do C6 Bank e Sicoob para cobranças PIX automáticas.
- **NFR16:** O sistema deve integrar-se com a plataforma Make.com para automações externas via webhooks.

### Escalabilidade

- **NFR17:** O sistema deve suportar a gestão de no mínimo 50 entidades (empresas) simultâneas por conta de usuário administrador.
- **NFR18:** O sistema deve suportar no mínimo 100 usuários simultâneos sem degradação perceptível de desempenho.

### Conformidade Legal

- **NFR19:** O sistema deve estar em conformidade com a legislação fiscal brasileira vigente (NF-e, NFS-e, CT-e, SPED).
- **NFR20:** O sistema deve atender às normas contábeis brasileiras (CPC/IFRS) para geração de demonstrações financeiras.
- **NFR21:** O sistema deve gerar documentos contábeis (Livro Diário, Livro Razão, Balancete) em conformidade com o CPC 26.
