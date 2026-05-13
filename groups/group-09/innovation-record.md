# Registro de Inovação

## Nome da Solução
Guia para Calouros: Mapeamento do Campus (MapUFR)

---

## Problema
Muitos estudantes, especialmente os calouros, enfrentam dificuldades significativas ao ingressar na UFR devido a:

- *Complexidade Estrutural:* Campus amplo com múltiplos blocos, laboratórios e secretarias sem uma sinalização digital adequada.
- *Perda de Tempo:* Atrasos em aulas e reuniões por dificuldade em localizar salas específicas.
- *Fragmentação de Informações:* Informações sobre o Restaurante Universitário (RU), horários de ônibus e processos administrativos estão dispersas em diferentes canais.

---

## Solução Proposta
Desenvolvimento de uma aplicação gráfica com OpenGL que integra em um único ambiente:

- Mapa interativo do campus com navegação, zoom e busca de salas/blocos
- Centralização de informações do RU (cardápio em tempo real) e horários de ônibus
- Roteiro entre salas baseado na grade horária do aluno
- Mural de avisos geolocalizados
- Funcionamento offline para navegação básica no mapa

A solução permite que o usuário visualize sua localização atual, busque por qualquer ponto do campus e receba informações contextuais sobre o local selecionado.

---

## Diferencial Inovador

| Aspecto | Diferencial |
|---------|-------------|
| *Integração* | Diferente de soluções existentes (Google Maps, mapas estáticos em PDF), o MapUFR combina mapa interativo + serviços acadêmicos + grade horária em um único aplicativo. |
| *Offline* | O mapa funciona sem conexão com internet, ao contrário de soluções baseadas exclusivamente em nuvem. |
| *Contextualização Acadêmica* | O sistema não apenas mostra onde fica a sala, mas também sugere rotas baseadas nas aulas do dia do aluno. |
| *Geolocalização de Avisos* | Avisos são exibidos com base na localização atual do usuário, aumentando a relevância da informação. |
| *Desenvolvimento Local* | Criado especificamente para a realidade do campus da UFR, considerando suas particularidades estruturais. |

---

## Potencial de Aplicação

- *Instituições de Ensino Superior:* Outras universidades com campus complexos podem adotar a solução.
- *Grandes Campi Corporativos:* Empresas com múltiplos prédios e setores.
- *Hospitais e Complexos de Saúde:* Para auxiliar pacientes e visitantes na localização de setores.
- *Shopping Centers e Grandes Centros Comerciais:* Navegação indoor para localização de lojas e serviços.
- *Eventos de Grande Porte:* Congressos, feiras e festivais que ocorrem em áreas extensas.

---

## Tecnologias Utilizadas

- *OpenGL:* Biblioteca gráfica para renderização do mapa interativo
- *C++ / Python:* Linguagens de programação para desenvolvimento da aplicação
- *JSON / XML:* Estrutura de dados para armazenamento do mapa e pontos de interesse
- *GPS / Geolocalização:* Para identificação da posição atual do usuário
- *Criptografia básica:* Proteção de dados sensíveis armazenados localmente

---

## Possível contribuição científica ou tecnológica

*Contribuição Técnica:*
- Desenvolvimento de uma arquitetura leve para mapas interativos offline com OpenGL, adaptável a dispositivos com hardware limitado.
- Modelo de integração entre dados acadêmicos (grade horária) egeolocalização para geração de rotas personalizadas.

*Contribuição Social:*
- Redução da ansiedade e desorientação de calouros no período de adaptação à universidade.
- Otimização do tempo dos alunos, que passam menos tempo se deslocando e mais tempo em atividades acadêmicas.
- Democratização do acesso à informação institucional, centralizando serviços dispersos.

*Contribuição Acadêmica:*
- Caso de estudo para disciplinas de Engenharia de Software, Requisitos e Desenvolvimento com OpenGL.
- Base para pesquisas sobre navegação indoor e sistemas de informação contextualizada em ambientes educacionais.

---

## Data de Registro
12/05/2026

---

## Autores

- Gabriel Souza Vieira
- Victor Sudário Cândido
- Marcos Ribeiro Rodrigues
- Matheus Cândido Goes
  
---
