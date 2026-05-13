# Análise de Estado da Arte

## Objetivo
Investigar soluções semelhantes existentes.

---

## Soluções Encontradas

### Solução 1

- Nome: App RU — UFC
- Link: https://sti.ufc.br/sti-lanca-aplicativo-do-restaurante-universitario/
- Descrição: Permite consultar o cardápio do restaurante universitário nos três turnos (café, almoço e jantar), comprar créditos e verificar saldo e histórico do RU. Disponível inicialmente somente para dispositivos Android.
- Diferenças para nossa proposta: O App RU da UFC foi desenvolvido para uma única instituição e disponibilizado apenas para Android, sem versão web ou PWA. O PODE PAPAR é uma PWA compatível com qualquer dispositivo e navegador, e foi projetado com arquitetura modular que permite adoção por outras instituições sem reescrita de código.

### Solução 2

- Nome: Sistema de Controle de Restaurantes Universitários — UFSM
- Link: https://www.ufsm.br/orgaos-suplementares/ru/sistema-de-controle-de-restaurantes-universitarios
- Descrição: Sistema desenvolvido pelo Centro de Processamento de Dados da UFSM, em funcionamento desde 2008, na versão web com arquitetura JavaEE. Permite consultar saldo, agendar refeições, verificar cardápio e realizar transferências de créditos.
- Diferenças para nossa proposta: É um sistema legado, desenvolvido em tecnologia antiga (JavaEE) e fortemente acoplado à infraestrutura da UFSM, sem possibilidade de integração modular com outros sistemas. O PODE PAPAR utiliza tecnologias modernas (React.js, Node.js, API REST) e arquitetura desacoplada que facilita manutenção e evolução futura.

### Solução 3

- Nome: Aplicativo RU — UFG
- Link: https://ufg.br/n/122209-ufg-lanca-aplicativo-para-restaurante-universitario
- Descrição: Permite conferir o cardápio do dia, avaliar a refeição e ter informações sobre o saldo de créditos. Também é possível substituir a carteira por meio de um QR Code disponibilizado no app, disponível para Android e iOS.
- Diferenças para nossa proposta: O app da UFG foi desenvolvido internamente pela própria universidade em parceria com sua secretaria de TI, o que o torna exclusivo e não replicável para outras instituições. O PODE PAPAR foi concebido desde o início como uma solução white-label, podendo ser implantado em qualquer instituição que possua ou não sistema gerenciador próprio.

### Solução 4

- Nome: Bandexcred — USP
- Link: https://www5.usp.br/noticias/tecnologia-2/aplicativo-mobile-facilita-ida-ao-restaurante-universitario/
- Descrição: Aplicativo mobile gratuito para Android que permite consultar instantaneamente o número de refeições disponíveis no RU Card da USP. As recargas, porém, só podem ser realizadas presencialmente.
- Diferenças para nossa proposta: O Bandexcred resolve apenas a consulta de saldo, sem oferecer recarga remota, cardápio ou painel administrativo. O PODE PAPAR centraliza todas essas funcionalidades em uma única plataforma, incluindo recarga via Pix e cartão de crédito diretamente pelo app.

---

## Conclusão
As soluções existentes no cenário brasileiro de restaurantes universitários apresentam limitações comuns: são desenvolvidas para uma única instituição, utilizam tecnologias legadas de difícil manutenção, não oferecem recarga remota completa (Pix e cartão) ou são restritas a plataformas específicas (somente Android). Nenhuma das soluções analisadas adota arquitetura modular e desacoplada que permita reuso em outras instituições.
O PODE PAPAR se diferencia por combinar arquitetura API-First, tecnologias modernas, suporte a PWA (multiplataforma), recarga remota via Pix e cartão, painel administrativo integrado e potencial de comercialização white-label — características que, em conjunto, não foram identificadas em nenhuma das soluções analisadas.

---
