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
2. **Glossário Contextual** *(opcional)*: termos específicos do domínio ou serviço externo que o leitor precisa conhecer antes de ler o restante.
3. **Serviços Externos / Dependências** *(quando aplicável)*: APIs de terceiros consumidas, contratos externos, SDKs, limites de uso e pontos de falha.
4. **Arquitetura da Solução**: componentes (back-end, front-end, banco, serviços externos) e diagramas.
5. **Modelagem de Dados**: tabelas, campos, tipos, índices, restrições (constraints).
6. **Contratos de API**: requisições/respostas, corpos das mensagens (payloads), códigos de status, versionamento.
7. **Regras Técnicas**: camadas intermediárias (middlewares), validações técnicas, processos assíncronos, registros (logs).
8. **Impactos no Sistema**: migrações, quebras de compatibilidade, desempenho.
9. **Estratégia de Testes**: unitários, integração, ponta a ponta (E2E).
10. **Riscos e compensações (trade-offs)**: decisões tomadas e alternativas descartadas.

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

### 6.12 Glossário contextual

Use quando o documento introduzir terminologia específica de um domínio, serviço externo ou protocolo que não seja de conhecimento geral da equipe. Defina apenas os termos necessários para compreender o documento — não replique o glossário global do framework (seção 11).

### 6.13 Serviços externos e dependências

Documente cada serviço externo consumido com:

- **Nome e versão da API** (ex.: Stripe API v1, AWS SES).
- **Finalidade**: o que o sistema usa desse serviço.
- **Endpoints ou métodos principais** consumidos.
- **Autenticação**: tipo de credencial e onde será armazenada.
- **Limites e comportamento esperado**: rate limits, timeouts, SLA do fornecedor.
- **Pontos de falha e contingência**: o que acontece se o serviço estiver indisponível.

### 6.14 Cabeçalho de metadados

Inclua no topo do documento um bloco de metadados com:

- **Tech Lead responsável**: quem escreve e mantém o documento.
- **PM de referência**: PM da funcionalidade relacionada.
- **Time envolvido**: pessoas que participaram da elaboração ou revisão.
- **Status**: rascunho / revisão / aprovado.
- **Última atualização**: data da versão corrente.
- **Feature Spec de referência**: link para a especificação funcional relacionada (quando existir).
- **Link para o Epic**: item na ferramenta de gestão de tarefas (Jira, Linear, ClickUp, etc.).
- **Links técnicos relevantes**: ADRs, referências de arquitetura, documentação do serviço externo.