## 6. Especificação Técnica (Tech Spec / Design Doc)

### 6.1 O que é

Documento técnico que descreve como a funcionalidade será implementada.

### 6.2 Nomenclatura (Tech Spec x Design Doc)

No mercado, **Tech Spec** e **Design Doc** são frequentemente usados como sinônimos.

Neste framework, tratamos os termos como equivalentes: ambos representam o documento técnico de decisões e implementação.

### 6.3 Para que serve

Tomar decisões de arquitetura, reduzir risco técnico e alinhar engenharia antes de codar.

### 6.4 Nível de escopo

Funcionalidade específica (ou parte complexa dela).

### 6.5 Diferença entre Especificação de Funcionalidade (Feature Spec) e Especificação Técnica (Tech Spec)

- **Especificação de Funcionalidade (Feature Spec)**: “o que acontece” do ponto de vista funcional (comportamento).
- **Especificação Técnica (Tech Spec)**: “como implementar” do ponto de vista técnico (arquitetura, dados, contratos, riscos).

### 6.6 Estrutura recomendada

1. **Contexto Técnico**: situação atual da arquitetura.
2. **Arquitetura da Solução**: componentes (back-end, front-end, banco, serviços externos) e diagramas.
3. **Modelagem de Dados**: tabelas, campos, tipos, índices, restrições (constraints).
4. **Contratos de API**: requisições/respostas, corpos das mensagens (payloads), códigos de status, versionamento.
5. **Regras Técnicas**: camadas intermediárias (middlewares), validações técnicas, processos assíncronos, registros (logs).
6. **Impactos no Sistema**: migrações, quebras de compatibilidade, desempenho.
7. **Estratégia de Testes**: unitários, integração, ponta a ponta (E2E).
8. **Riscos e compensações (trade-offs)**: decisões tomadas e alternativas descartadas.

### 6.7 Modelagem de dados

Quando houver persistência relevante, documente mudanças e migrações (inclusive preenchimentos retroativos e restrições (constraints)) e como serão aplicadas com segurança.

### 6.8 Contratos de API

Documente contratos com nível suficiente para evitar divergência entre consumidores (corpos das mensagens/payloads, códigos, versionamento e compatibilidade).

### 6.9 Regras técnicas

Centralize decisões de implementação que afetem consistência e operação (validações, filas/eventos, registros (logs) e observabilidade, idempotência, etc.).

### 6.10 Impactos técnicos e migrações

Liste impactos esperados e plano de execução quando houver risco (migrações, implantação gradual, compatibilidade, flags de funcionalidade).

### 6.11 Riscos e compensações (trade-offs)

Registre compensações (trade-offs) reais (2+ abordagens), critérios da decisão e riscos assumidos para reduzir retrabalho.