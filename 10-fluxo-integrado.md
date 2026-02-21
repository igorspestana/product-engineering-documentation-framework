## 10. Fluxo Integrado de Desenvolvimento

### 10.1 Da Visão de Produto às Histórias de Usuário

Fluxo típico:

Visão de Produto (direção)  
→ PRD (iniciativa e sucesso)  
→ Especificação de Funcionalidade (comportamento detalhado)  
→ Especificação Técnica (design técnico e riscos)  
→ Histórias de usuário (execução incremental + critérios de aceitação)

### 10.2 Como os documentos se conectam

- O PRD define escopo, métricas e dependências.
- A Especificação de Funcionalidade detalha fluxo, regras, exceções, perfis e critérios de aceitação.
- A Especificação Técnica define arquitetura, dados, contratos, testes e plano de implantação.
- As histórias referenciam as partes relevantes para execução (sem duplicar texto desnecessariamente).

### 10.3 Exemplo completo de uma funcionalidade atravessando todos os níveis

Exemplo ilustrativo:

- **Visão de Produto**: reduzir inadimplência em escolas com gestão financeira simples.
- **PRD**: iniciativa “Cobrança e conciliação”, com meta de reduzir inadimplência em 20%.
- **Especificação de Funcionalidade**: “Emissão de boletos”, com fluxos principais, erros e regras (ex.: cancelamento apenas quando status = PENDENTE).
- **Especificação Técnica**: integrações com provedor de pagamento, modelagem de dados, contratos, estratégia de testes e implantação.
- **Histórias**: “Como financeiro, quero gerar boleto para cobrar mensalidade, para reduzir atrasos”, com critérios de aceitação.