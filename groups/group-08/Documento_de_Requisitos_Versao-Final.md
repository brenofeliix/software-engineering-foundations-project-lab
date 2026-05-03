#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
Descrever o objetivo deste documento e do sistema.

### 1.2 Escopo
Descrever o que o sistema faz, seus limites e o que está fora do escopo.

### 1.3 Definições, Acrônimos e Abreviações
Liste termos importantes utilizados no documento.

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
Explique o sistema de forma resumida.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais

### RF01 - Nome do requisito
**Descrição:**  
Descreva a funcionalidade.

**Prioridade:** Alta / Média / Baixa  
**Entradas:**  
**Saídas:**  
**Regras de negócio:**  

---

### RF02 - Nome do requisito
(repita o padrão)

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
- O sistema deverá utilizar protocolos seguros de comuni

### 6.2 Operacionais
- Logs  
- Monitoramento  

### 6.3 Desenvolvimento
- Versionamento (Git)  
- Padrões de código  
- Testes automatizados  

---
