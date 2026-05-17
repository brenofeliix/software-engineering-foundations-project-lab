## 5. Assumptions (Premissas)

- Pressupõe-se que os usuários possuam seus smartphones.
- Pressupõe-se que os funcionários e gestores do estabelecimento tenham acesso ao sistema via smartphone, tablet, notebook ou desktop.
- Assume-se que funcionários e gestores possuam cadastro no banco de dados do sistema para realizar-se às autenticações.
- Exige-se que o estabelecimento tenha acesso a internet.
- Exige-se que os usuários tenham acesso à internet.
- Exige-se que todos os dispositivos eletrônicos/digitais do estabelecimento estejam conectados à internet.
- Assume-se que todas as mesas possuam QR Code do endereço da aplicação web e estejam devidamente sinalizadas.
- Assume-se que o estabelecimento possua maquininha de pagamentos.
- Assume-se que o usuário final possui um dispositivo com acesso estável à internet e um navegador moderno (Chrome, Safari, Edge ou Firefox) para garantir a performance de carregamento prevista.
- Pressupõe-se que os estabelecimentos utilizem terminais Smart POS ou hardware de rede compatíveis com os protocolos HTTP Local ou WebSockets para a automação física.
- Exige-se que o provedor de infraestrutura (Cloud/Servidor) suporte escalabilidade horizontal para absorver picos de 50% de demanda sem degradação de performance.
- Considera-se que o gateway de pagamento (PSP) escolhido ofereça suporte nativo a Webhooks e APIs baseadas em REST com certificação PCI DSS.  
- Assume-se que os gestores e a equipe da cozinha possuam treinamento básico para operar a interface administrativa e atualizar o status dos pedidos em tempo real.  
- Pressupõe-se que a base de dados de pratos e categorias já contenha imagens e descrições otimizadas para garantir o tempo de resposta nas buscas.  

## 6. Constraints (Restrições)   

- O sistema deve ser desenvolvido utilizando-se tecnologia web responsiva.  
- O sistema deve rodar nos principais navegadores (Chrome, Firefox, Safari, Edge).  
- O projeto deve ser entregue em até 6 meses.  
- O sistema deve realizar integrações com Payment Service Providers (PSPs) exclusivamente via APIs RESTful sobre HTTPS com TLS 1.2 ou superior.  
- O projeto deve implementar uma camada de abstração agnóstica para hardware, permitindo a comunicação com diferentes adquirentes e modelos de Smart POS via TEF ou SDKs.  
- O sistema deve utilizar obrigatoriamente comunicação via HTTP Local ou WebSockets para o envio de valores aos terminais, vedando a digitação manual.  
- O sistema deve processar pagamentos via Pix, cartões e carteiras digitais utilizando obrigatoriamente tokenização, sendo proibido o armazenamento de dados sensíveis de pagamento em servidores próprios.  
- O sistema deve garantir que o tempo de carregamento de qualquer página web seja inferior a 2 segundos.  
- O projeto deve assegurar que o motor de busca de pratos retorne resultados em menos de 1 segundo.  
- O sistema deve suportar a carga simultânea de até 1.000 usuários ativos sem perda de fluidez.
- O projeto deve manter uma disponibilidade mínima de 99,9% (Uptime).  
- O sistema deve criptografar toda a comunicação cliente-servidor através do protocolo HTTPS.  
- O projeto deve estar em conformidade estrita com a LGPD, informando a finalidade da coleta de dados e permitindo a exclusão dos mesmos mediante solicitação do usuário.  
- O sistema deve exigir autenticação obrigatória e segregação por níveis de permissão para todas as funcionalidades de gestão (RF13 a RF19).  
- O sistema deve ser desenvolvido com design responsivo, adaptando-se automaticamente a diferentes tamanhos de tela.  
- O projeto deve limitar o fluxo principal de pedido (da seleção ao pagamento) a, no máximo, 4 interações/cliques do usuário.  
- O sistema deve permitir atualizações de cardápio a quente (hot-swap), garantindo que as alterações de preços e pratos não interrompam o serviço ativo.  
- O sistema deve gerar automaticamente relatórios mensais consolidados, incluindo receita bruta, métricas de avaliação e sugestões algorítmicas de alteração de cardápio baseadas em baixo desempenho.  
- O sistema deve impor um fluxo de status obrigatório para os pedidos: "Em andamento" -> "Pronto para servir" -> "Servido" -> "Finalizado".  
