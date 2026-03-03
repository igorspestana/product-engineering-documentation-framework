## 2. Hierarquia de Documentação no Produto

### 2.1 Visão geral dos níveis


| Documento                                                                | Tipo                                       | Para que serve                            | Escopo                                        | Foco                    | Responde                                                                                                                             |
| ------------------------------------------------------------------------ | ------------------------------------------ | ----------------------------------------- | --------------------------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| SRS (Software Requirements Specification)                                | Documento de requisitos formais do sistema | Documentação formal completa do sistema   | Sistema inteiro formal                        | Requisitos formais      | Requisitos funcionais do sistema completo / Requisitos não funcionais / Regras de negócio globais / Interfaces externas / Restrições |
| Visão de Produto (Product Vision)                                        | Documento estratégico                      | Definir o produto como um todo            | Produto inteiro                               | Estratégia              | Qual problema resolvemos? / Para quem? / Qual posicionamento? / Quais objetivos estratégicos?                                        |
| PRD (Product Requirements Document)                                      | Documento de requisitos                    | Definir o que a iniciativa deve fazer     | Iniciativa ou módulo relevante                | Produto / comportamento | O que a iniciativa/funcionalidade deve fazer (em alto nível)                                                                         |
| Especificação de Funcionalidade (Feature Spec) | Documento funcional                        | Detalhar completamente uma funcionalidade | Funcionalidade específica                     | Funcional detalhado     | Como a funcionalidade funciona (fluxos, regras, exceções)                                                                            |
| Especificação Técnica (Tech Spec / Design Doc)                           | Documento técnico                          | Explicar como será implementado           | Funcionalidade específica (ou parte complexa) | Técnico                 | Como implementar (arquitetura, dados, contratos, compensações (trade-offs))                                                          |


No contexto ágil, normalmente é utilizado:

- 1 **Visão de Produto (Product Vision)** (produto inteiro)
- Vários **PRDs** (para grandes iniciativas)
- Várias **Especificações de Funcionalidade (Feature Specs)**
- Vários **Tech Specs**

E raramente um **SRS** completo (a menos que seja exigência formal).

### 2.2 Estratégia → Produto → Funcionalidade → Implementação

**Hierarquia de escopo das documentações:**

Visão de Produto (Product Vision)  
↓  
PRD  
↓  
Especificação de Funcionalidade (Feature Spec)  
↓  
Especificação Técnica (Tech Spec)

**Analogia simples (se o produto fosse um prédio):**

- Visão de Produto (Product Vision) → Por que estamos construindo o prédio
- PRD → Projeto do andar inteiro
- Especificação de Funcionalidade (Feature Spec) → Projeto detalhado de um apartamento
- Especificação Técnica (Tech Spec) → Como será feita a instalação elétrica
- História de usuário (user story) → Instalar uma tomada específica na sala

### 2.3 Relação entre Produto e Engenharia

- **Produto** define intenção, escopo e sucesso (problema, objetivo, o que entra/não entra, métricas).
- **Engenharia** define solução e execução segura (arquitetura, dados, contratos, riscos, testes, implantação).
- Especificação de Funcionalidade (Feature Spec) e Especificação Técnica (Tech Spec) funcionam como “contratos” complementares: **comportamento** (o que acontece) e **implementação** (como fazer).

