## 7. Histórias de Usuário (User Stories)

### 7.1 O que são

Histórias de usuário (user stories) são unidades pequenas de trabalho que descrevem uma necessidade do usuário e ajudam a fatiar a entrega em partes implementáveis e verificáveis.

### 7.2 Papel dentro do fluxo de desenvolvimento

- Traduzem um comportamento em lista de trabalho executável (backlog).
- Na hierarquia de backlog, ficam dentro de um Epic.
- Facilitam planejamento, priorização e acompanhamento.
- Funcionam melhor quando derivadas de uma Especificação de Funcionalidade (Feature Spec) (ou, em mudanças pequenas, diretamente do PRD/resumo).

### 7.3 Relação com PRD, Especificação de Funcionalidade e Especificação Técnica

- PRD alinha o “por quê” e o resultado esperado da iniciativa.
- A Especificação de Funcionalidade remove ambiguidades de comportamento.
- A Especificação Técnica reduz risco técnico e define implementação.
- Histórias de usuário representam a execução incremental, com critérios de aceitação e, quando necessário, referências aos documentos acima.

### 7.4 Estrutura recomendada (Como / Quero / Para)

- **Como** [perfil/persona]  
**Quero** [capacidade/ação]  
**Para** [benefício/resultado]

### 7.5 Critérios de aceitação

Defina critérios claros e verificáveis para a story, alinhados ao comportamento esperado (incluindo casos de erro quando relevante).

### 7.6 Quando uma história precisa de Especificação Técnica

Uma história precisa (ou deve referenciar) uma Especificação Técnica quando houver risco técnico relevante: mudança de arquitetura, migração, contratos usados por outros sistemas, integrações externas, desempenho/concorrência, ou compensações (trade-offs) técnicos não óbvios.