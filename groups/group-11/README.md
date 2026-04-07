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

# Product Vision

## Problem

Micro e pequenas empresas brasileiras, especialmente as atendidas por escritórios de contabilidade, enfrentam dificuldades significativas na gestão integrada de suas finanças, obrigações fiscais e contabilidade. Os problemas principais incluem:

- **Fragmentação de ferramentas:** muitas empresas usam planilhas e sistemas separados para emissão de notas fiscais, controle financeiro e contabilidade, gerando retrabalho, inconsistência de dados e risco de erros.
- **Complexidade fiscal brasileira:** o Brasil possui uma das legislações tributárias mais complexas do mundo, com NF-e, NFS-e, CT-e, múltiplos regimes tributários e constantes mudanças regulatórias. Pequenos empresários não têm conhecimento técnico para lidar com isso sozinhos.
- **Falta de integração contábil-fiscal-financeira:** lançamentos financeiros não se refletem automaticamente na contabilidade, documentos fiscais não alimentam o estoque nem o fluxo de caixa, e o contador precisa importar dados manualmente de diversas fontes.
- **Dificuldade de acesso a tecnologia acessível:** as soluções ERP existentes são caras, complexas demais para o porte da empresa, ou focadas em e-commerce/varejo, sem atender adequadamente prestadores de serviço, agronegócio, clínicas e empresas do interior do Brasil.

## Target Users

O Plumer atende dois perfis principais de usuários:

1. **Escritórios de contabilidade** — Contadores e colaboradores que gerenciam dezenas de empresas clientes simultaneamente. Precisam de uma plataforma multi-empresa que centralize a gestão fiscal, financeira e contábil de todos os seus clientes em um só lugar.

2. **Micro e pequenos empresários** — Donos de clínicas odontológicas, prestadoras de serviço, empresas do agronegócio, transportadoras, indústrias alimentícias e empresas de engenharia. Precisam emitir notas fiscais, controlar contas a pagar e receber, gerenciar estoque e ter visibilidade financeira, sem a complexidade de ERPs corporativos.

## Proposed Solution

O **Plumer** é uma plataforma SaaS (web) de gestão empresarial integrada, desenvolvida para o ecossistema contábil-empresarial brasileiro. O sistema é composto por módulos interconectados:

- **Plumer Money** — Gestão financeira: contas bancárias, contas a pagar/receber, fluxo de caixa, DRE, investimentos, cobranças PIX automatizadas, importação inteligente de extratos com IA e relatórios gerenciais.
- **Plumer Box** — Hub fiscal: sincronização automática de NF-e/CT-e com a SEFAZ, NFS-e com a ADN Nacional, upload de XMLs, explorador de documentos, catálogo NCM e resumo fiscal.
- **Plumer Emissor** — Emissão de NFS-e e NF-e Modelo 55 com IA que preenche dados tributários, calcula retenções e aprende com o histórico do usuário.
- **Plumer Contábil** — Contabilidade em partidas dobradas: plano de contas, Livro Diário, Livro Razão, Balancete (IFRS/CPC 26), Balanço Patrimonial, DRE, encerramento de exercício e 13 indicadores financeiros. Inclui IA para sugestão automática de lançamentos.
- **Plumer Estoque** — Controle de estoque com entradas/saídas automáticas, ordens de produção, métodos de custo (Média Ponderada e PEPS/FIFO) e alertas de produtos críticos.

**Diferenciais:** gestão multi-empresa, 128+ tutoriais interativos, compartilhamento via WhatsApp/e-mail, licenciamento modular, log de auditoria, integração com Make.com, PWA e IA embarcada em todos os módulos.

## Competitors

| Concorrente | Foco Principal | Ponto Forte | Limitação frente ao Plumer |
|---|---|---|---|
| **Omie** | ERP para PMEs com foco no contador | Integração contábil forte, IA conversacional | Preço elevado, menos flexível para empresas pequenas do interior |
| **Bling** | ERP para e-commerce e varejo | Integrações com marketplaces | Focado em e-commerce, fraco em contabilidade integrada |
| **ContaAzul** | Gestão financeira para MPEs | Interface intuitiva | Sem módulo contábil completo, não atende contador multi-empresa |
| **Nibo** | BPO Financeiro e contabilidade | Conciliação bancária para contadores | Sem emissão fiscal integrada nem controle de estoque |
| **vhsys** | ERP para pequenas empresas | Maior homologação NFS-e nacional | Sem IA fiscal, sem contabilidade em partidas dobradas |
| **Tiny ERP** | Gestão básica para micro empresas | Simples e barato | Funcionalidades limitadas, sem contabilidade, sem IA |
