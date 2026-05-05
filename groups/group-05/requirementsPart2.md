### Performance (Desempenho)

-	O sistema deve responder a qualquer requisição do usuário em até 2 segundos em condições normais de uso.
- O sistema deve suportar até 500 usuários simultâneos sem degradação perceptível de desempenho.
- O carregamento inicial do dashboard não deve ultrapassar 3 segundos em conexões de banda larga.
- Operações de busca e filtro de produtos devem retornar resultados em menos de 1 segundo.
- A geração de relatórios de até 12 meses de histórico deve ser concluída em no máximo 5 segundos.

### Security (Segurança)

- O sistema deve criptografar senhas utilizando algoritmo de hash seguro (bcrypt com salt).
- O sistema deve implementar autenticação com bloqueio após 5 tentativas incorretas consecutivas.
- O sistema deve restringir o acesso às funcionalidades conforme o perfil do usuário (administrador, operador, visualizador).
- Todas as comunicações devem ser realizadas via HTTPS (TLS 1.2 ou superior).
- Tokens de sessão devem expirar após 8 horas de inatividade, exigindo novo login.
- O sistema deve registrar logs de auditoria para ações críticas como exclusão de produtos e alterações de estoque.

---

### Usability (Usabilidade)

- A interface deve ser intuitiva, permitindo que novos usuários realizem tarefas principais sem treinamento prévio.
- O sistema deve ser totalmente responsivo, adaptando-se a dispositivos móveis, tablets e desktops.
- O usuário deve conseguir registrar uma entrada ou saída de estoque em no máximo 3 cliques a partir do menu principal.
- O sistema deve exibir mensagens de erro claras e orientações de correção sempre que uma ação falhar.
- O dashboard principal deve apresentar os indicadores mais importantes de forma visual e de fácil interpretação.

---

## 4. User Stories (Histórias de Usuário)

- Como gerente de loja, eu quero cadastrar produtos com SKU e categoria, para que eu possa organizar meu estoque de forma eficiente.
- Como operador de estoque, eu quero registrar entradas e saídas de produtos, para que o saldo do estoque permaneça preciso e atualizado.
- Como gerente, eu quero receber alertas automáticos quando um produto atingir o estoque mínimo, para que eu possa fazer o pedido de reposição antes de acabar.
- Como administrador, eu quero gerenciar usuários e seus níveis de acesso, para que eu possa controlar quem pode visualizar ou modificar os dados do estoque.
- Como dono da loja, eu quero visualizar um dashboard com os principais indicadores de estoque, para que eu possa tomar decisões mais rápidas e embasadas.
- Como operador de estoque, eu quero buscar e filtrar produtos por nome ou categoria, para que eu possa encontrar itens rapidamente em períodos de alta demanda.
- Como gerente, eu quero gerar relatórios de movimentação por período ou produto, para que eu possa analisar o desempenho do estoque e identificar tendências.
- Como vendedor de e-commerce, eu quero controlar o estoque em múltiplos depósitos, para que eu possa gerenciar o inventário de diferentes canais de venda.
- Como dono da loja, eu quero importar dados de produtos via CSV, para que eu possa migrar meu estoque existente sem precisar cadastrar tudo manualmente.
- Como usuário, eu quero recuperar minha senha por e-mail, para que eu possa recuperar o acesso ao sistema caso esqueça minhas credenciais.

## Considerações Finais

Este documento deve ser tratado como referência central ao longo de todo o ciclo de desenvolvimento. Para garantir sua efetividade, é importante que ele seja:

- Claro e organizado — redigido de forma que qualquer membro da equipe consiga compreender o escopo do sistema.
- Fácil de entender por qualquer membro da equipe — independente de sua área de atuação (desenvolvimento, design, negócios).
- Utilizado como base para desenvolvimento e testes — servindo de referência tanto para a implementação quanto para a validação e homologação do sistema.
- Versionado e atualizado — mantido com registro das alterações a cada mudança de escopo aprovada.

