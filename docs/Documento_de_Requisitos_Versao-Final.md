#  Documento de Requisitos e Projeto de Software

---

##  1. Introdução

### 1.1 Objetivo
Descrever o objetivo deste documento e do sistema.

### 1.2 Escopo
Descrever o que o sistema faz, seus limites e o que está fora do escopo.

### 1.3 Definições, Acrônimos e Abreviações
Liste termos importantes utilizados no documento.

---

##  2. Product Vision

### 2.1 Problema
Qual problema o sistema resolve?

### 2.2 Solução
Descreva a solução proposta.

### 2.3 Público-Alvo
Quem utilizará o sistema?

### 2.4 Proposta de Valor
Por que esse sistema é importante?

### 2.5 Diferencial
O que torna esse sistema melhor que outros?

### 2.6 Funcionalidades principais (alto nível)
- Funcionalidade 1
- Funcionalidade 2

---

##  3. Visão Geral do Sistema

### 3.1 Descrição Geral
Explique o sistema de forma resumida.

### 3.2 Stakeholders
Liste os principais envolvidos:
- Usuários
- Clientes
- Desenvolvedores
- Outros

---

##  4. Requisitos Funcionais

### RF01 - Nome do requisito
**Descrição:**  
Descreva a funcionalidade.

**Prioridade:** Alta / Média / Baixa  
**Entradas:**  
**Saídas:**  
**Regras de negócio:**  

---

### RF02 - Nome do requisito
(repita o padrão)

---

##  5. Requisitos Não Funcionais

### 5.1 Usabilidade
- Interface intuitiva  
- Tempo de aprendizado < X minutos  
- Acessibilidade  

### 5.2 Eficiência
- Tempo de resposta < X segundos  
- Suporte a múltiplos usuários  

### 5.3 Desempenho
- Suporte a X usuários simultâneos  
- Estabilidade sob carga  

### 5.4 Espaço
- Limite de armazenamento  
- Uso eficiente de memória  

### 5.5 Confiabilidade
- Disponibilidade mínima (ex: 99,9%)  
- Recuperação de falhas  

### 5.6 Segurança (Proteção)
- Autenticação  
- Criptografia  
- Controle de acesso  

---

##  6. Requisitos Organizacionais

### 6.1 Ambientais
- Sistema operacional  
- Infraestrutura  

### 6.2 Operacionais
- Logs  
- Monitoramento  

### 6.3 Desenvolvimento
- Versionamento (Git)  
- Padrões de código  
- Testes automatizados  

---

##  7. Requisitos Externos

### 7.1 Reguladores
- LGPD  
- Normas específicas  

### 7.2 Éticos
- Não discriminação  
- Transparência  

### 7.3 Legais
- Leis aplicáveis  

### 7.4 Segurança Externa
- Proteção contra ataques  
- Auditorias  

### 7.5 Contábeis
- Registro de transações  
- Relatórios  

---

##  8. Arquitetura do Sistema

### 8.1 Visão Geral
Descreva a arquitetura (ex: monolito, microserviços).

### 8.2 Componentes
- Frontend  
- Backend  
- Banco de dados  
- APIs externas  

### 8.3 Tecnologias
- Linguagem  
- Framework  
- Banco de dados  

### 8.4 Decisões Arquiteturais
Explique como a arquitetura atende aos requisitos não funcionais:
- Desempenho  
- Segurança  
- Escalabilidade  

---

---

## 9. Casos de Uso e Diagramas UML

Esta seção deve representar visualmente e descritivamente o funcionamento do sistema.

Os diagramas ajudam na:
- modelagem do sistema;
- comunicação entre equipe;
- entendimento da arquitetura e funcionalidades;
- documentação técnica do projeto.

---

# 9.1 Casos de Uso

Os casos de uso representam as interações entre usuários (atores) e o sistema.

---

### UC01 - Realizar Login

**Ator:** Usuário  

**Descrição:**  
Permite que o usuário acesse o sistema utilizando credenciais válidas.

---

### Fluxo principal
1. Usuário acessa a tela de login  
2. Usuário informa e-mail e senha  
3. Sistema valida credenciais  
4. Sistema libera acesso  

---

### Fluxo alternativo
- Credenciais inválidas  
- Usuário esqueceu senha  

---

## Exemplo de Diagrama de Caso de Uso

[Usuário]

    |
    
    | ---- (Realizar Login)
    
    | ---- (Cadastrar Conta)
    
    | ---- (Recuperar Senha) 

---

## 9.2 Diagrama de Classes (UML)

O diagrama de classes representa:

- estrutura do sistema;
- entidades;
- atributos;
- métodos;
- relacionamentos.

---

### Exemplo

```text
+------------------+
|     Usuário      |
+------------------+
| - id             |
| - nome           |
| - email          |
| - senha          |
+------------------+
| + login()        |
| + logout()       |
+------------------+
```

---

### Exemplo com relacionamento

```text
+------------------+        +------------------+
|     Usuário      | 1    * |      Pedido      |
+------------------+--------+------------------+
| id               |        | id               |
| nome             |        | valor            |
+------------------+        +------------------+
```

---

## 9.3 Diagrama de Atividades (UML)

Representa o fluxo de execução de processos no sistema.

---

### Exemplo

```text
[Início]
   |
[Acessar sistema]
   |
[Inserir login]
   |
{Credenciais válidas?}
   | Sim
[Acessa sistema]
   |
[Fim]

   | Não
[Mensagem de erro]
```

---

## 9.4 Diagrama de Sequência (UML)

Representa a comunicação entre objetos ao longo do tempo.

---

### Exemplo

```text
Usuário -> Sistema: realizar login
Sistema -> Banco: validar usuário
Banco -> Sistema: usuário válido
Sistema -> Usuário: acesso liberado
```

---

## 9.5 Diagrama de Componentes

Representa os módulos e componentes principais do sistema.

---

### Exemplo

```text
[Frontend]
     |
     v
[API Backend]
     |
     v
[Banco de Dados]
```

---

## 9.6 Diagrama de Implantação (Deployment)

Representa onde o sistema será executado.

---

### Exemplo

```text
[Usuário]
     |
Internet
     |
[Servidor Web]
     |
[Servidor Banco de Dados]
```

---

## 9.7 Ferramentas Recomendadas

Os diagramas podem ser feitos utilizando:

- Draw.io
- Lucidchart
- StarUML
- Visual Paradigm
- PlantUML
- Mermaid
- Figma

---

## 9.8 Observações Importantes

- Os diagramas devem representar o sistema REAL do grupo;
- Evitem diagramas genéricos;
- Mantenham consistência entre requisitos e diagramas;
- Diagramas devem possuir nomes claros;
- Atualizem os diagramas conforme o sistema evoluir.

---

# Regra importante

> “Diagramas não são apenas desenhos: eles representam decisões arquiteturais e técnicas do sistema.”

---

##  10. Plano de Testes

### 10.1 Estratégia de Teste
Como o sistema será testado?

### 10.2 Tipos de Teste
- Unitário  
- Integração  
- Sistema  
- Aceitação  

### 10.3 Casos de Teste

#### CT01 - Nome
**Requisito relacionado:** RF01  
**Descrição:**  
**Entrada:**  
**Resultado esperado:**  

---

### 10.4 Testes de Requisitos Não Funcionais
- Performance (tempo de resposta)  
- Segurança  
- Usabilidade  

---

##  11. Critérios de Aceitação

Defina como validar os requisitos:
- Métricas  
- Testes  
- Condições de sucesso  

---

##  12. Restrições

- Tecnológicas  
- Legais  
- De prazo  

---

##  13. Premissas

- Usuário terá acesso à internet  
- Sistema será usado em dispositivos móveis  

---

##  14. Observações Finais

Informações adicionais relevantes.

---

#  Orientações importantes

- Requisitos devem ser claros, específicos e mensuráveis  
- Evite termos vagos como “rápido” ou “bom”  
- Requisitos não funcionais são obrigatórios  
- A arquitetura deve responder aos requisitos  
- Todo requisito deve ser testável  

---

# Regra de ouro

> Se não pode ser testado, não é um bom requisito.
