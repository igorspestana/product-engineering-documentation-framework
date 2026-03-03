# Framework de Documentação de Produto e Engenharia

Este framework define **quais documentos** usar em Produto e Engenharia, **quando** criar cada um e **como** estruturá-los. O objetivo é reduzir ambiguidades, alinhar decisões e diminuir retrabalho, mantendo a documentação **proporcional ao risco e ao impacto**.

## Skills para Agentes

O diretório [`skills/`](skills/) contém skills reutilizáveis que estendem agentes (Codex, Cursor, etc.) com capacidades especializadas de documentação. Cada skill descreve um fluxo, critérios e instruções para que o agente execute tarefas de forma consistente com o framework.

**Skills disponíveis:**
- `doc-planner-from-brief`: decide quais documentos (PRD, feature spec, tech spec) são necessários a partir de feature brief e discovery
- `write-prd`: cria PRD a partir de brief e discovery
- `write-feature-spec`: cria especificação funcional detalhada com comportamento, regras e critérios de aceitação
- `write-tech-spec`: cria especificação técnica (design doc) com arquitetura, dados, contratos e plano de rollout
- `review-doc-consistency`: valida consistência, rastreabilidade e lacunas entre PRD, feature spec, tech spec e histórias

**Utilidade para agentes:** ao carregar essas skills, o agente passa a seguir procedimentos padronizados em vez de improvisar. Isso garante saídas alinhadas ao framework, reduz inconsistências e permite automação confiável de fluxos como "planejar documentação → gerar documentos → revisar consistência". Consulte [skills/README.md](skills/README.md) para a ordem sugerida de uso e detalhes.

## Conteúdo

Use o índice ao lado (ou o [Summary](SUMMARY.md)) para navegar pelos capítulos:

1. **Introdução** – Objetivo do framework, por que documentar e princípios
2. **Hierarquia de Documentação** – Níveis (Visão, PRD, Feature Spec, Tech Spec) e relação Produto x Engenharia
3. **Visão de Produto (Product Vision)** – O que é, estrutura e quando criar ou revisar
4. **PRD** – Requisitos de iniciativa, estrutura e diferença para funcionalidade
5. **Especificação de Funcionalidade (Feature Spec)** – Detalhamento funcional, entidades, perfis e critérios de aceitação
6. **Especificação Técnica (Tech Spec)** – Design técnico, dados, APIs, riscos e trade-offs
7. **Histórias de Usuário** – Papel no fluxo, estrutura Como/Quero/Para e relação com os outros documentos
8. **Matriz de Decisão** – Quando criar PRD, Feature Spec e Tech Spec (impacto, complexidade)
9. **Boas Práticas** – Proporcionalidade, evitar burocracia, versionamento e documentação viva
10. **Fluxo Integrado** – Da Visão às histórias e exemplo ponta a ponta
11. **Glossário** – Termos, documento vs. artefato e siglas
