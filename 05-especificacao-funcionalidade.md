## 5. Especificação de Funcionalidade (Feature Spec)

### 5.1 O que é

Documento que detalha completamente uma funcionalidade específica.

### 5.2 Para que serve

Eliminar ambiguidades antes do desenvolvimento. Serve como referência funcional para implementação.

### 5.3 Nível de escopo

Funcionalidade específica dentro de um PRD (ou uma entrega independente).

### 5.4 Diferença entre PRD e Especificação de Funcionalidade (Feature Spec)

- **PRD**: iniciativa/módulo, visão de alto nível e critérios de sucesso.
- **Especificação de Funcionalidade (Feature Spec)**: descrição detalhada do comportamento de uma funcionalidade (fluxos, regras, exceções).

### 5.5 Estrutura recomendada

1. **Contexto da Funcionalidade**: onde se encaixa no produto.
2. **Objetivo**: o que resolve.
3. **Fluxo do Usuário**: passo a passo (fluxo principal e alternativos).
4. **Regras de Negócio**: condições, restrições, validações.
5. **Entidades Envolvidas (nível funcional)**: objetos do sistema, campos relevantes, estados (sem modelagem técnica).
6. **Perfis e Permissões**: quem pode fazer o quê.
7. **APIs / Rotas (visão funcional)**: endpoints envolvidos sem payload técnico completo.
8. **Casos de Exceção**: erros esperados, estados alternativos, validações.
9. **Critérios de Aceitação**: condições para considerar pronto.

### 5.6 Entidades no nível funcional

Liste entidades e campos relevantes para entendimento do comportamento (ex.: “Pedido”, “Status”, “Data de vencimento”), sem se comprometer com tipos, índices ou detalhes de persistência.

### 5.7 Perfis e permissões

Defina claramente perfis e suas ações permitidas, principalmente quando houver matriz de acesso ou fluxos com exceções por papel.

### 5.8 Critérios de aceitação

Critérios verificáveis que demonstrem que o comportamento esperado foi entregue (incluindo fluxos alternativos e erros importantes).

### 5.9 Cabeçalho de metadados

Inclua no topo do documento um bloco de metadados com:

- **PM responsável**: quem escreve e mantém o documento.
- **Designer responsável**: referência ao profissional de design envolvido.
- **Status**: rascunho / revisão / aprovado.
- **Última atualização**: data da versão corrente.
- **PRD de referência**: link para o PRD que originou a funcionalidade (quando existir).
- **Link para o Epic/histórias**: item na ferramenta de gestão de tarefas (Jira, Linear, ClickUp, etc.).
- **Link para o design**: arquivo no Figma ou ferramenta equivalente.