# Análise de Estado da Arte

## Objetivo
Investigar soluções semelhantes existentes no mercado e na academia, identificando suas funcionalidades, limitações e oportunidades de inovação para o sistema proposto MapUFR.

---

## Soluções Encontradas

### Solução 1
- Nome:Google Maps
- Link: https://maps.google.com
- Diferenças para nossa proposta:
  - Não possui informações específicas sobre salas internas dos blocos da UFR
  - Não integra dados acadêmicos como grade horária, cardápio do RU ou horários de ônibus
  - Interface genérica, não otimizada para navegação indoor em campus universitário
  - Não oferece roteiro baseado nas disciplinas do aluno
  - Ausência de avisos geolocalizados contextuais

---

### Solução 2
- Nome: Mapas de Campus Universitários (ex: UFSC Map, UNICAMP Virtual, eMAP da USP)
- Link: https://www.ufsc.br/mapa (referência geral)
- Diferenças para nossa proposta:
  - Geralmente são mapas estáticos em PDF ou imagens, sem interatividade
  - Não integram informações de serviços (RU, ônibus) na mesma interface
  - Ausência de funcionalidade de busca por nome de sala
  - Não possuem geolocalização do usuário
  - Não oferecem roteiro personalizado com base na grade horária

---

### Solução 3
- *Nome:* Mapas Indoor com OpenGL (projetos acadêmicos e tutoriais)
- *Link:* Ex: GitHub repositories (search: "OpenGL indoor map")
- *Diferenças para nossa proposta:*
  - Geralmente são protótipos ou provas de conceito, sem completude funcional
  - Raramente integram dados externos (RU, ônibus) ou APIs de geolocalização
  - Não possuem sistema de busca de locais ou filtros por categorias
  - Ausência de user stories orientadas a calouros e veteranos
  - Não consideram aspectos de LGPD, segurança ou usabilidade mobile
  - Sem previsão de mural de avisos geolocalizados

## Conclusão
Explique o possível diferencial da proposta.
| Aspecto | Diferencial MapUFR |
| *Integração de serviços* | RU + ônibus + grade horária + avisos em um só lugar |
| *Roteiro acadêmico* | Rotas baseadas nas disciplinas do dia do aluno |
| *Geolocalização contextual* | Avisos relevantes conforme a posição do usuário |
| *Especificidade UFR* | Desenvolvido sob medida para o campus da universidade |
| *Tecnologia acessível* | Leve e compatível com hardware limitado |

---
