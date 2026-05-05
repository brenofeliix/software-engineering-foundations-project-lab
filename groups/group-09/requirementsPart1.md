# *Requirements Specification*

Este documento descreve de forma estruturada os requisitos do sistema a ser desenvolvido. Ele deve ser claro, objetivo e completo, servindo como base para desenvolvimento, testes e validação do software.

---

## *1. System Overview (Visão Geral do Sistema)*

O sistema proposto consiste em uma aplicação gráfica desenvolvida com OpenGL que tem como objetivo realizar o mapeamento visual da universidade, facilitando a locomoção e orientação de estudantes, especialmente calouros, dentro do campus.

Atualmente, muitos alunos enfrentam dificuldades para localizar salas, blocos, setores administrativos e outros pontos importantes da universidade, principalmente no início do período letivo. A ausência de um sistema visual interativo pode causar atrasos, desorientação e perda de tempo.

A solução proposta é a criação de um mapa interativo em ambiente gráfico 2D ou 3D, no qual o usuário poderá visualizar a estrutura da universidade, identificar locais importantes e obter informações básicas sobre cada ponto do campus. O sistema permitirá navegação visual e interação com os elementos exibidos.

O público-alvo do sistema são estudantes da universidade (principalmente ingressantes), além de visitantes e servidores que necessitem de orientação dentro do campus.

---

## *2. Functional Requirements (Requisitos Funcionais)*

FR01: O sistema deve exibir um mapa gráfico da universidade utilizando OpenGL.

FR02: O sistema deve permitir a navegação pelo mapa (movimentação de câmera ou viewport).

FR03: O sistema deve permitir aplicar zoom para aproximar e afastar a visualização.

FR04: O sistema deve exibir identificações (nomes) dos blocos, salas e locais importantes.

FR05: O sistema deve permitir selecionar pontos do mapa para visualizar informações detalhadas.

FR06: O sistema deve destacar visualmente o local selecionado.


FR07: O sistema deve permitir a exibição de categorias de locais (ex: salas, laboratórios, cantina, secretaria).

FR08: O sistema deve permitir ativar e desativar a visualização de determinadas categorias.

FR09: O sistema deve exibir a localização atual do usuário (quando aplicável ou simulada).

FR10: O sistema deve permitir buscar locais pelo nome.

FR11: O sistema deve centralizar o mapa automaticamente no local buscado.

FR12: O sistema deve permitir reiniciar a visualização para a posição inicial do mapa.

FR13: O sistema deve permitir interação via mouse e teclado, além de touch screen para celulares.

---

## *3. Non-Functional Requirements (Requisitos Não Funcionais)*

RNF01: O sistema deve renderizar o mapa com no mínimo 30 FPS para garantir fluidez.

RNF02: O sistema deve responder às interações do usuário em até 1 segundo.

RNF03: A interface deve ser intuitiva e de fácil aprendizado para novos usuários.

RNF04: O sistema deve apresentar elementos visuais claros e legíveis.

RNF05: O sistema deve permitir navegação simples utilizando mouse e teclado.

RNF06: O sistema deve ser compatível com sistemas operacionais Windows e Linux, para celulares como Android, IOS e HyperOS.

RNF07: O sistema deve funcionar em computadores com suporte básico a OpenGL.

RNF08: O sistema deve ser estruturado de forma modular para facilitar manutenção e expansão.

RNF09: O código deve seguir boas práticas de programação e ser documentado.

RNF10: O sistema deve evitar falhas durante a execução, mesmo com uso contínuo.

RNF11: O sistema deve tratar erros de entrada do usuário sem interromper a execução.

RNF12: O sistema deve permitir a adição de novos pontos no mapa sem necessidade de grandes alterações no código.
