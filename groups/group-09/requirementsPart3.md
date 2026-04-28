## 5. Assumptions (Premissas)

Condições consideradas verdadeiras para o desenvolvimento do projeto. Estas premissas orientam as decisões técnicas e de escopo.

- Assume-se que os dispositivos dos usuários possuem suporte básico à biblioteca OpenGL (ou compatível via software, no caso de emulação). 
- Assume-se que os usuários terão acesso à internet pelo menos para a instalação inicial e eventuais atualizações de dados como cardápio do RU e horários de ônibus. 
- Assume-se que os dados acadêmicos (grade horária, localização de salas) utilizados pelo sistema serão fornecidos pela instituição ou por fontes públicas confiáveis. 
- Assume-se que os alunos utilizam predominantemente dispositivos móveis (Android, iOS, HyperOS) com telas sensíveis ao toque. 
- Assume-se que o mapa da universidade (blocos, salas, laboratórios) não sofre alterações estruturais frequentes, permitindo que o sistema seja desenvolvido com base em um levantamento inicial. 
- Assume-se que os usuários possuem habilidades básicas de interação com mapas digitais (zoom, arrastar, tocar em elementos). 
- Assume-se que a localização simulada ou real do usuário (FR09) pode ser obtida via GPS ou seleção manual, dependendo das permissões do dispositivo. 

---

## 6. Constraints (Restrições)

Limitações técnicas, legais, de projeto ou de negócio que restringem as soluções possíveis.

- O sistema deve ser desenvolvido utilizando **OpenGL** para renderização gráfica.
- O sistema deve funcionar nos sistemas operacionais: Windows, Linux, Android, iOS e HyperOS.
- O projeto deverá ser entregue dentro do prazo estipulado.
- O sistema não pode depender de serviços pagos de terceiros (ex: APIs de mapas proprietárias, serviços de geolocalização com custo). 
- O sistema deve ser auto-contido em termos de dados do mapa; não será permitida dependência exclusiva de conexão com a internet para funcionamento básico (mapa offline, sem localização em tempo real). 
- O sistema deverá tratar erros de entrada e falhas de renderização sem interromper a execução.
- A manutenção do mapa (adição de novos pontos) deve ser feita sem necessidade de recompilação sempre que possível. 
