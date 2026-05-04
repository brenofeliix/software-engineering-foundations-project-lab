# Requirements Specification

---

## 1. System Overview (Visão Geral do Sistema)

O sistema Conexao Comunitaria é uma plataforma de colaboração que integra, em um único lugar, o compartilhamento de recursos, alertas de segurança, troca de habilidades, visando conectar pessoas que precisam de apoio com voluntarios. O principal publico alvo inclui moradores, associações de bairro, centros comunitários e lideranças locais.

---

## 2. Functional Requirements (Requisitos Funcionais)

### Módulo 1 – Cadastro e Autenticação

FR01 – Permitir que o usuário se cadastre utilizando e-mail e senha.

FR02 – Solicitar, no momento do cadastro, o CEP e o nome do bairro para associar o usuário à sua região.

FR03 – Permitir que o usuário complemente seu perfil com foto, nome, telefone e lista de habilidades/interesses.

### Módulo 2 – Perfil e Reputação

FR04 – Permitir que o usuário edite seus dados pessoais e habilidades a qualquer momento.

FR05 – Exibir publicamente no perfil: nome, foto, bairro, data de ingresso na plataforma e reputação média.

FR06 – Calcular e exibir um índice de reputação (ex.: 0 a 5 estrelas) baseado em avaliações recebidas após trocas ou ajudas realizadas.

FR07 – Permitir que usuários avaliem uns aos outros ao final de cada interação de troca ou doação.

### Módulo 3 – Mapa da Solidariedade

FR08 – Exibir um mapa interativo com a localização dos usuários, pontos de doação, eventos e necessidades ativas na região.

FR09 – Permitir que o usuário visualize apenas os pontos geolocalizados dentro do seu bairro ou de bairros vizinhos (configurável).

FR10 – Permitir que o usuário publique um "ponto de ajuda" no mapa, informando categoria.

FR11 – Exibir, ao clicar em um ponto no mapa, um resumo da oferta/necessidade com botão para contato ou detalhamento.

FR12 – Permitir filtrar os pontos exibidos no mapa por categoria (ex.: doação de alimentos, ajuda com pets, reparos domésticos, eventos).

### Módulo 4 – Doações

FR13 – Permitir que o usuário publique itens para doação com foto, descrição, quantidade e condição (ex.: novo, usado, precisa de reparo).

FR14 – Permitir que o usuário interessado em um item manifeste interesse diretamente na publicação.

FR15 – Exibir um status para cada doação: "disponível", "reservado" ou "concluído".

FR16 – Remover automaticamente a publicação da lista após o status ser alterado para "concluído".

FR17 – Permitir que o usuário cancele uma doação publicada antes de ser concluída.

FR18 – Notificar o doador quando alguém manifestar interesse no item.

FR19 – Notificar o interessado se o doador cancelar a doação ou marcar como concluída com outro usuário.

### Módulo 5 – Eventos e Calendário Colaborativo

FR20 – Permitir que usuários criem eventos comunitários com título, data, horário, local, descrição e categoria (ex.: mutirão, bazar, palestra, feira de troca).

FR21 – Exibir os eventos em um calendário visual (formato mês/semana/lista).

FR22 – Permitir que outros usuários confirmem presença no evento.

FR23 – Enviar lembrete por notificação 24 horas antes do evento.

FR24 – Permitir que o criador do evento edite ou cancele o evento, gerando notificação automática aos confirmados.

### Módulo 6 – Alertas Comunitários

FR25 – Permitir que qualquer usuário cadastrado publique um alerta (ex.: "alagamento na Rua X", "animal perdido", "falta de energia").

FR26 – Classificar alertas em categorias predefinidas: segurança, emergência climática, serviços públicos, animal perdido, outros.

FR27 – Exibir alertas em uma lista ordenada por data e gravidade (alerta de alta urgência destaca-se visualmente).

FR28 – Enviar notificação para todos os usuários do bairro quando um alerta for publicado.

FR29 – Permitir que usuários confirmem ou contestem um alerta (ex.: botão "confirmo" / "é falso").

FR30 – Permitir que moderadores (líderes comunitários) removam ou arquivem alertas considerados inválidos.

---

## 3. Non-Functional Requirements (Requisitos Não Funcionais)

NFR01 – Todas as senhas devem ser armazenadas utilizando hash criptográfico.

NFR02 – O sistema deve implementar rate limiting: máximo de 5 tentativas de login por minuto por IP.

NFR03 – A interface deve ser responsiva, adaptando-se a smartphones e desktops.

NFR04 – O sistema deve fornecer feedback visual claro para ações do usuário (loading, mensagens de sucesso/erro).

NFR05 – A plataforma deve estar em conformidade com a LGPD.

NFR06 – Dados de localização (GPS) só podem ser coletados após autorização explícita do usuário.
