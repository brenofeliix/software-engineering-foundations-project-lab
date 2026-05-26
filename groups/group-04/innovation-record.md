# Registro de Inovação

## Nome da Solução
PODE PAPAR — Plataforma Digital do Restaurante Universitário da UFR.

---

## Problema
O Restaurante Universitário da Universidade Federal de Rondonópolis (UFR) opera com um modelo presencial de créditos pré-pagos que gera filas, burocracia e perda de tempo produtivo para estudantes e servidores. A ausência de uma interface digital impede a consulta remota de saldo, a recarga de créditos sem deslocamento ao campus e o acesso ágil ao cardápio semanal, comprometendo a eficiência do serviço e a permanência estudantil.

---

## Solução Proposta
Desenvolvimento de uma plataforma digital modular e desacoplada composta por dois módulos independentes: o Módulo de Interface (Frontend PWA), acessível via navegador ou instalável em dispositivos móveis, que permite ao usuário autenticar via SUAP, consultar saldo, visualizar cardápio, recarregar créditos via Pix ou cartão de crédito e receber notificações; e o Módulo Gerenciador (Backend + Painel Administrativo), que permite aos operadores do RU gerenciar usuários, créditos, cardápio e gerar relatórios visuais sem necessidade de conhecimento técnico.

---

## Diferencial Inovador
- Restaurantes universitários de instituições federais e estaduais que não possuem sistema digital próprio
- Universidades que possuem sistemas legados e necessitam apenas de uma interface moderna integrada via API
- Refeitórios de institutos federais (IFs) com perfil similar ao da UFR
- Modelo replicável para qualquer instituição pública que opere serviços de alimentação subsidiada com controle de créditos

---

## Potencial de Aplicação
- Restaurantes universitários de instituições federais e estaduais que não possuem sistema digital próprio
- Universidades que possuem sistemas legados e necessitam apenas de uma interface moderna integrada via API
- Refeitórios de institutos federais (IFs) com perfil similar ao da UFR
- Modelo replicável para qualquer instituição pública que opere serviços de alimentação subsidiada com controle de créditos

---

## Tecnologias Utilizadas

- React.js + Vite (Frontend PWA)  
- Node.js + Express (Backend API REST)  
- PostgreSQL (Banco de Dados)  
- Redis (Cache)  
- OAuth2 + JWT (Autenticação via SUAP)  
- Tailwind CSS (Estilização responsiva)  
- Workbox (Service Worker para PWA e notificações push)  
- Docker + Nginx (Infraestrutura e containerização)  
- GitHub Actions (CI/CD)  
- Figma (Prototipação)

---

## Possível Contribuição Científica ou Tecnológica

**Acadêmica:** o projeto demonstra na prática a aplicação de arquitetura desacoplada e padrões API-First no contexto de sistemas públicos, podendo servir como base para trabalhos de conclusão de curso, artigos e estudos de caso sobre modernização de serviços institucionais.

**Social:** contribui diretamente com a permanência estudantil ao reduzir barreiras de acesso à alimentação subsidiada, impactando populações em situação de vulnerabilidade econômica atendidas pelo RU.

**Comercial:** o modelo white-label permite que a solução seja licenciada ou adaptada para outras instituições, gerando potencial de receita e sustentabilidade para o projeto após sua implantação inicial na UFR.

---

## Data de Registro
12/05/2026 (doze de maio de dois mil e vinte e seis).

---

## Autores
- Anthonio Olioni
- Giovana Gomes da Silva
- Guilherme Freitas da Costa Lopes
- Gustavo Vinícius Coinete Silva
- Pedro Guilherme Mota Santos

---
