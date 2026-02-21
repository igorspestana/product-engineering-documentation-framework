## 8. Matriz de Decisão de Documentação de Funcionalidades

### 8.1 Avaliação por impacto de produto

Crie um PRD quando pelo menos **2** itens forem verdade:

- Impacta **métricas** (conversão, receita, retenção, churn, NPS)
- Tem **stakeholders** fora do time (CS, vendas, compliance, direção)
- Mexe em **escopo de módulo/iniciativa** (não é só um ajuste local)
- Envolve decisões de prioridade e **compensações de escopo (trade-offs)** (“o que fica de fora”)
- Pode gerar **mudança de comportamento** para muitos usuários (implantação gradual e comunicação)

Objetivo do PRD: alinhar “por quê”, “o quê”, escopo e sucesso.

### 8.2 Avaliação por complexidade funcional

Crie **Especificação de Funcionalidade (Feature Spec)** quando pelo menos **2** itens forem verdade:

- Existem **regras de negócio** com exceções (“se…, então…, senão…”)
- Existem **múltiplos perfis/permissões** ou matriz de acesso
- Existem **muitos estados** (status, transições, validações)
- Existem **fluxos alternativos** e casos de erro importantes
- Engenharia/QA/Design fariam suposições diferentes sem um detalhamento

Objetivo: remover ambiguidade do comportamento antes de codar.

### 8.3 Avaliação por complexidade técnica

Crie **Especificação Técnica (Tech Spec)** quando pelo menos **1** item for verdade:

- Vai mexer em **arquitetura** (novos serviços, filas, eventos, módulos)
- Vai alterar **modelo de dados** de forma relevante (migração, restrições (constraints), preenchimento retroativo (backfill))
- Vai criar/alterar **APIs públicas** ou contratos usados por outros sistemas
- Há risco de **performance**, concorrência, consistência, escalabilidade
- Integra com **serviços externos** (pagamento, email, SSO, etc.)
- Existem **compensações (trade-offs) técnicas** reais (2+ abordagens possíveis)
- Precisa de plano de **implantação gradual**, flag de funcionalidade, migração gradual, compatibilidade

Objetivo: alinhar implementação, reduzir risco e retrabalho.

### 8.4 Combinações possíveis de documentos

Regras rápidas:

- **PRD + Especificação de Funcionalidade + Especificação Técnica**: quando impacta produto + regras + arquitetura.
- **Especificação de Funcionalidade + Especificação Técnica**: quando o “por que fazer” já está claro, mas comportamento e implementação são complexos.
- **Especificação de Funcionalidade somente**: quando o risco é mais de comportamento/regra do que técnico.
- **Especificação Técnica somente**: quando o comportamento é simples, mas há mudança técnica grande (ex.: migração/infra).
- **Nenhum dos três (só histórias + AC)**: quando é mudança pequena, baixa ambiguidade e baixo risco.

### 8.5 Exemplos práticos de aplicação

Um “gate” final para decidir:

> Se eu não escrever esse documento, qual o custo provável?
>
> - Retrabalho?
> - Bug em produção?
> - Divergência entre times?
> - Atraso por decisões técnicas tardias?

Se o custo esperado for alto, documente.