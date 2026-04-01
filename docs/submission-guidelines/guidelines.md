## 📦 Diretrizes de Submissão (Como Entregar as Atividades)

Para garantir padronização e facilitar a avaliação, todos os grupos devem seguir rigorosamente os passos abaixo ao realizar cada entrega do projeto.

---

### 🚀 1. Fazer Fork do Repositório

- Clique em **Fork** no repositório principal
- Trabalhe apenas dentro do seu fork

---

### 🌿 2. Criar uma Branch

Cada entrega deve ser feita em uma nova branch seguindo o padrão:

group-XX-nome-da-etapa: 

exemplos

group-01-product-vision

group-02-requirements

group-03-modeling

group-04-architecture

group-05-testing


---

### 📁 3. Estrutura de Arquivos

Todos os arquivos devem ser criados dentro da pasta do seu grupo:

groups/group-XX/



Cada etapa deve ser entregue em um arquivo separado:

| Etapa | Nome do Arquivo |
|------|----------------|
| Product Vision | product-vision.md |
| Requirements | requirementsPartX.md |
| Modeling | modeling.md |
| Architecture | architecture.md |
| Testing | testing.md |

Exemplo: groups/group-02/product-vision.md


---

### ⚠️ REGRAS IMPORTANTES

- ❌ NÃO entregar atividade no README.md
- ❌ NÃO modificar arquivos fora da pasta do seu grupo
- ❌ NÃO criar arquivos em locais incorretos
- ✅ Entregar apenas o arquivo correspondente à etapa atual

---

### ✍️ 4. Pull Request (PR)

Após realizar o commit:

1. Abra um Pull Request (PR)
2. Utilize o padrão correto no título:

Group XX nome da etapa

exemplo: Group 02 product vision


---

### 📝 5. Template do PR

O PR deve conter obrigatoriamente:


Description

Descreva o que foi feito.

Checklist
 Documentação atualizada
 Estrutura do repositório seguida
 Revisado antes do envio
Related Issue

Closes #numero-da-issue


---

### ✅ 6. Validação

Seu PR só será aceito se:

- Passar na validação automática (GitHub Actions)
- Seguir o padrão de nomes
- Estiver na pasta correta
- Estiver estruturado corretamente

---

### 🔁 7. Correção de Erros

Se o PR falhar:

- Leia atentamente a mensagem de erro
- Corrija os problemas
- Faça novo commit na mesma branch
- O PR será atualizado automaticamente

---

### 🎯 Objetivo

Este processo simula um fluxo real de desenvolvimento de software:

- Controle de versão (Git)
- Revisão de código (Pull Request)
- Integração contínua (CI)
- Trabalho em equipe
