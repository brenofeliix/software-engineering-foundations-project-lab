### Performance (Desempenho)

• O sistema deve garantir uma experiência fluida, respondendo a requisições de carregamento de tela em até 2 segundos em conexões 4G ou Wi-Fi.

• O timer do Método Pomodoro deve iniciar ou pausar em no máximo 300ms após o comando do usuário, garantindo precisão imediata nas sessões de foco.

• Para manter o fluxo de aprendizado sem interrupções, os Flashcards devem carregar e exibir seu conteúdo em até 1 segundo.

• O relatório de métricas de estudo deve ser gerado e exibido em até 1,5 segundos se os dados estiverem em cache local, ou até 3 segundos mediante o uso de uma animação de carregamento para otimizar a percepção de espera.

• Em termos de escalabilidade, a infraestrutura do backend deve suportar 10.000 usuários simultâneos sem qualquer degradação de performance.

• O sistema deve ser capaz de absorver picos de até 15.000 usuários simultâneos por períodos de até 10 minutos, garantindo a estabilidade em momentos de alta demanda.

• O sistema de alertas deve ser altamente confiável, disparando notificações com uma tolerância máxima de atraso de apenas 5 segundos em relação ao horário configurado pelo estudante.

• No que diz respeito ao Mini Game, o desempenho gráfico deve ser estável, mantendo uma taxa de atualização mínima de 30 FPS em dispositivos Android 8+ ou iOS 13+.

• O aplicativo deve permitir o funcionamento pleno em modo offline para as funções de cronograma, flashcards e Pomodoro, garantindo a continuidade dos estudos sem internet.

• O tamanho total do pacote de instalação (APK/IPA) deve ser mantido em até 80MB, utilizando técnicas de compressão de assets, especialmente para os elementos do mini game.

• O sistema deve garantir a acessibilidade, sendo totalmente compatível com leitores de tela e seguindo padrões de contraste WCAG 2.1 para assegurar a inclusão de todos os usuários



### Security (Segurança)

- O sistema deve exigir autenticação
segura por meio de login e senha,
podendo incluir biometria. 
- As senhas dos usuários devem ser
armazenadas utilizando criptografia com
hash seguro. 
- O sistema deve bloquear
temporariamente o acesso após
múltiplas tentativas inválidas.
- Os dados do usuário devem ser
protegidos contra acessos não
autorizados. 
- O aplicativo deve seguir a LGPD.
---

### Usability (Usabilidade)

- O sistema deve apresentar uma interface intuitiva e de fácil navegação, adequada ao público estudantil. 

- As principais funcionalidades devem ser acessadas em até 5 interações do usuário. 

- O sistema deve fornecer feedback visual imediato após ações realizadas. 

- O sistema deve possuir design simples e organizado, reduzindo distrações durante o uso. 

---

## 4. User Stories (Histórias de Usuário)

- Como um estudante, quero criar e gerenciar um cronograma de estudos, para que eu possa organizar minha rotina de forma eficiente.
- Como um estudante, quero utilizar o temporizador Pomodoro, para que eu consiga manter o foco durante as sessões de estudo.
- Como um estudante, quero receber notificações sobre tarefas e revisões, para que eu não esqueça minhas atividades de estudo.
- Como um estudante, quero criar e revisar flashcards, para que eu possa melhorar meu processo de aprendizagem.
- Como um estudante, quero acompanhar meu desempenho nos estudos, para que eu possa identificar meus pontos fortes e fracos.
- Como um estudante, quero realizar quizzes gerados a partir dos meus flashcards, para que eu possa testar meu conhecimento.
- Como um estudante, quero personalizar meu avatar, para que eu me sinta mais engajado com o aplicativo.
- Como um estudante, quero ganhar pontos e recompensas, para que eu me sinta motivado a manter a constância.
---

