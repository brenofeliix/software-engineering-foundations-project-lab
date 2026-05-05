## 5. Assumptions (Premissas)

- Assume-se que estudantes e servidores possuem cadastro ativo no SUAP da UFR.
- Assume-se que os usuários possuem acesso à internet (via Wi-Fi do campus ou dados móveis) para operar o sistema.
- Assume-se que os usuários possuem dispositivos compatíveis com navegadores modernos ou smartphones.
- Assume-se que usuários externos poderão utilizar o RU mediante pagamento de valor diferenciado, sem necessidade de cadastro institucional.
- Assume-se que a API do SUAP estará disponível e acessível para autenticação dos usuários institucionais.
- Assume-se que o sistema interno do RU da UFR expõe ou poderá expor uma API para integração com o módulo de interface.
- Assume-se a disponibilidade de uma API de pagamento externa para processamento de transações via Pix.
- Assume-se que funcionários autorizados do RU serão responsáveis por cadastrar e manter o cardápio atualizado no sistema.
- Assume-se que haverá ao menos um operador responsável pela gestão operacional do sistema no RU.
- Assume-se que o operador do painel administrativo é um usuário não técnico, responsável apenas pela gestão operacional.
- Assume-se que a manutenção técnica do sistema é responsabilidade da equipe de desenvolvimento.
- Assume-se que o controle de acesso físico (catracas e reconhecimento facial) continuará operando de forma independente.
- Assume-se que o módulo de interface será desenvolvido de forma agnóstica, consumindo dados via API independentemente da origem do sistema gerenciador.
- Assume-se que a arquitetura modular permitirá adoção por outras instituições, com ou sem sistema gerenciador próprio.
- Assume-se que instituições sem sistema de gestão próprio utilizarão o módulo gerenciador completo fornecido pela plataforma.



---

## 6. Constraints (Restrições)

Restrições Técnicas
- O sistema deve ser desenvolvido como aplicação web responsiva (PWA), compatível com dispositivos móveis e desktop.
- O sistema deve ser compátivel com as versões mais recentes, e duas versões anteriores, de navegadores como Chrome, Firefox, Edge e Safari.
- O sistema deve ter sua comunicação via HTTPS, garantindo a segurança dos dados trafegados.
- O sistema não deve armazenar senhas dos usuários institucionais, delegando a autenticação inteiramente ao SUAP, utilizando protocolo seguro, como OAuth2, sem armazenamento de credenciais no sistema.
- O sistema não substitui o controle físico de acesso ao RU (catracas e biometria), atuando apenas na gestão de créditos e informações.
- O sistema deve garantir consistência e integridade no gerenciamento de créditos dos usuários.

Restrições de Acesso, Permissões e Legais
- O login institucional é restrito ao SUAP; usuários externos não utilizam autenticação institucional.
- O operador não possui acesso a configurações técnicas do sistema, apenas às funcionalidades operacionais.
- A manutenção técnica, atualizações de infraestrutura e correções de sistema são de responsabilidade exclusiva da equipe desenvolvedora.
- O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD) no tratamento de dados de usuários institucionais e externos.
- Integrações com gateways de pagamento devem seguir as normas do Banco Central do Brasil para transações via Pix.

---
