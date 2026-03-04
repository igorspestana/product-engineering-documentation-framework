# Skills de Documentação

Este diretório contém skills reutilizáveis para fluxos de documentação de produto e engenharia.

## Skills
- `doc-planner-from-brief`: decide quais documentos são necessários.
- `write-prd`: cria PRD a partir de feature brief e discovery.
- `write-feature-spec`: cria especificação funcional detalhada.
- `write-tech-spec`: cria especificação técnica/design.
- `review-doc-consistency`: valida consistência entre documentos.

## Ordem Sugerida de Uso
1. Executar `doc-planner-from-brief`.
2. Gerar documentos necessários (`write-prd`, `write-feature-spec`, `write-tech-spec`).
3. Executar `review-doc-consistency`.

## Uso com Repositório Remoto
As skills devem buscar diretamente o conteúdo remoto do framework via URLs `raw.githubusercontent.com`.
O repositório remoto deve ser tratado como fonte única de verdade, sem fallback local.
Se o remoto estiver indisponível, a execução deve ser interrompida com erro explícito.
