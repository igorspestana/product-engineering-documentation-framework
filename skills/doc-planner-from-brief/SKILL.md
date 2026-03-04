---
name: doc-planner-from-brief
description: Decide quais documentos de produto e engenharia são necessários a partir de feature brief e discovery doc opcional. Use quando o usuário pedir avaliação do que documentar antes da implementação ou planejamento de PRD, feature spec e tech spec.
---

# Planejador de Documentação

## Objetivo
Decidir quais documentos criar usando exclusivamente as regras do framework remoto.

## Entradas
- Obrigatório: feature brief, por uma das formas:
  - Arquivo `feature-brief.md`
  - Texto do feature brief escrito diretamente no chat
- Opcional: discovery doc (arquivo ou texto no chat)

### O que é o feature brief
O feature brief é a descrição inicial da funcionalidade ou iniciativa, antes dos documentos formais (PRD, Feature Spec, Tech Spec). Deve conter o suficiente para avaliar impacto e complexidade. Conteúdo típico:
- **Problema/oportunidade**: o que motiva a iniciativa
- **Objetivo**: resultado esperado em alto nível
- **Escopo resumido**: o que entra e o que fica de fora
- **Contexto**: stakeholders, integrações, restrições relevantes

## Fonte do Framework
Ler estes arquivos como fonte canônica:
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/02-hierarquia.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/08-matriz-decisao.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/10-fluxo-integrado.md`
Não usar fallback local. O repositório remoto é a única fonte de verdade.

## Procedimento Obrigatório
1. Buscar e ler os arquivos remotos listados em "Fonte do Framework".
2. Aplicar os critérios do framework remoto sem replicar ou adaptar regras locais.
3. Se qualquer arquivo remoto estiver indisponível, interromper a execução.
4. Em caso de indisponibilidade, responder com erro objetivo informando quais URLs falharam.
5. Não gerar decisão parcial sem a leitura completa dos arquivos remotos.

## Diretriz de Execução em Sandbox (Rede Restrita)
- Se a leitura remota falhar por limitação de rede/DNS do sandbox, tentar novamente usando comando com permissão escalada para as **mesmas URLs** canônicas (ex.: `curl -fsSL`).
- A tentativa com permissão escalada é um fallback de **transporte**, não de conteúdo: continua proibido usar cópia local ou fonte alternativa.
- Se mesmo com permissão escalada qualquer URL falhar, interromper e reportar erro objetivo com as URLs indisponíveis.
- Não gerar decisão parcial em nenhum cenário.

## Formato de Saída
Retornar:
- `required_documents`: ordered list
- `justification`: critérios acionados por documento com referência ao capítulo remoto
- `creation_order`: sequência recomendada
- `minimum_scope`: o que pode ser omitido para manter enxuto

## Notas de Execução
- Se o feature brief vier no chat (sem arquivo), tratar o texto fornecido como conteúdo do feature brief.
- Se o usuário pedir geração dos documentos, criar em `docs/features/<feature-name>/`.
- Para gerar os documentos, usar explicitamente as skills:
  - `write-prd` para PRD.
  - `write-feature-spec` para Feature Spec.
  - `write-tech-spec` para Tech Spec.
  - `review-doc-consistency` para revisão final de consistência.
- Gerar apenas os documentos listados em `required_documents`.
- Todo conteúdo de documentação deve estar em português.
- Manter proporcionalidade conforme orientação do framework remoto.
