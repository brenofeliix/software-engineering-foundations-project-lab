### Performance (Desempenho)

- O sistema deve responder requisições em até 2 segundos.
- O sistema deve suportar até 1.000 usuários simultâneos.
- O sistema deve responder às requisições em até 2 segundos em condições normais de uso (RNF01).
- O sistema deve suportar múltiplos acessos simultâneos com perda mínima de desempenho, garantindo estabilidade em horários de pico (RNF02).
- O sistema deve estar disponível 99% do tempo, desconsiderando janelas de manutenção programada (RNF07).
- O sistema deve apresentar tempo de recuperação rápido em caso de falhas, minimizando interrupções ao usuário (RNF10).
---

### Security (Segurança)

- O sistema deve criptografar senhas utilizando hash seguro.
- O sistema deve implementar autenticação de usuários.
- O sistema deve restringir acesso por níveis de permissão.
- O sistema deve autenticar usuários exclusivamente via credenciais institucionais do SUAP, restringindo o acesso a membros da comunidade da UFR (RF01, RNF06).
- Os dados dos usuários devem ser armazenados com criptografia, protegendo informações sensíveis contra acessos não autorizados (RNF03).
- O sistema deve garantir a integridade dos dados durante operações de recarga e pagamento, prevenindo inconsistências financeiras (RNF08).
- O sistema deve possuir mecanismos de backup e recuperação de dados, assegurando a continuidade do serviço em situações de falha (RNF09).
- O acesso administrativo deve ser restrito a usuários com perfil de administrador, controlando as operações de cadastro, gestão de créditos e geração de relatórios (RF10, RF11, RF12, RF13).
---

### Usability (Usabilidade)

- A interface do sistema deve ser intuitiva e de fácil navegação, permitindo que estudantes e servidores realizem suas ações principais sem necessidade de treinamento (RNF05).
- O sistema deve ser compatível com dispositivos móveis, adaptando-se a diferentes tamanhos de tela (RNF04).
- O sistema deve oferecer recursos de acessibilidade, incluindo alto contraste e alternância entre tema claro e escuro (RNF11).
- O sistema deve possuir um modo para pessoas com deficiência visual, realizando a leitura de textos presentes na interface, garantindo inclusão a todos os usuários da comunidade acadêmica (RNF12).

---

## 4. User Stories (Histórias de Usuário)

**Usuário Final**

- Como estudante ou servidor, eu quero recarregar meu saldo via Pix ou cartão de crédito, para que eu possa adicionar créditos remotamente sem precisar ir ao guichê físico.
- Como estudante ou servidor, eu quero visualizar o cardápio semanal na aplicação, para que eu possa planejar minhas refeições com antecedência.
- Como estudante ou servidor, eu quero consultar meu saldo atual a qualquer momento, para que eu possa controlar meus gastos no restaurante universitário.
- Como estudante ou servidor, eu quero receber notificações do RU, para que eu fique informado sobre alterações no cardápio e comunicados importantes.
- Como estudante ou servidor, eu quero visualizar meu histórico de recargas, para que eu possa acompanhar minha movimentação financeira no RU.
- Como estudante ou servidor, eu quero enviar feedback sobre as refeições do dia, para que eu possa contribuir com a melhoria da qualidade da alimentação oferecida.
- Como estudante ou servidor, eu quero visualizar meu registro de check-in, para que eu possa confirmar meu histórico de refeições realizadas.

**Administrador**

- Como administrador, eu quero cadastrar e atualizar o cardápio semanal, para que os usuários tenham sempre acesso a informações corretas e atualizadas sobre as refeições.
- Como administrador, eu quero gerenciar o cadastro de usuários (criar, atualizar, excluir e consultar histórico de pagamentos), para que eu possa controlar os acessos e manter os registros dos usuários do RU atualizados.
- Como administrador, eu quero gerenciar os créditos dos usuários (adicionar, ajustar ou remover saldo), para que eu possa corrigir inconsistências e dar suporte a usuários com problemas financeiros.
- Como administrador, eu quero gerar relatórios semanais, mensais e anuais de uso do sistema, para que eu possa monitorar a demanda, o fluxo financeiro e o desempenho geral do RU.
- Como administrador, eu quero criar e enviar notificações para que eu possa transmitir informações importantes diretamente à comunidade usuária do RU.

---
