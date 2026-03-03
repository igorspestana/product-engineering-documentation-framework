---
name: review-doc-consistency
description: Revisa PRD, feature spec, tech spec e histórias para identificar inconsistências, lacunas, contradições e falta de rastreabilidade. Use quando o usuário pedir validação da qualidade documental antes da implementação.
---

# Revisar Consistência da Documentação

## Objetivo
Revisar consistência documental usando exclusivamente os critérios do framework remoto.

## Entradas
- PRD (opcional se não for necessário)
- Feature Spec (opcional se não for necessário)
- Tech Spec (opcional se não for necessário)
- User stories/epic links

## Fonte do Framework
Usar como referência obrigatória:
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/08-matriz-decisao.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/09-boas-praticas.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/10-fluxo-integrado.md`
Não usar fallback local. O repositório remoto é a única fonte de verdade.

## Procedimento Obrigatório
1. Buscar e ler os arquivos remotos listados em "Fonte do Framework".
2. Revisar os documentos usando os critérios desses capítulos remotos.
3. Não aplicar checklist local concorrente ao checklist remoto.
4. Se qualquer arquivo remoto estiver indisponível, interromper a execução.
5. Em caso de indisponibilidade, responder com erro objetivo informando quais URLs falharam.

## Diretriz de Execução em Sandbox (Rede Restrita)
- Se a leitura remota falhar por limitação de rede/DNS do sandbox, tentar novamente usando comando com permissão escalada para as **mesmas URLs** canônicas (ex.: `curl -fsSL`).
- A tentativa com permissão escalada é um fallback de **transporte**, não de conteúdo: continua proibido usar cópia local ou fonte alternativa.
- Se mesmo com permissão escalada qualquer URL falhar, interromper e reportar erro objetivo com as URLs indisponíveis.
- Não gerar revisão parcial em nenhum cenário.

## Formato de Saída
Retornar:
- `findings`: lista agrupada por severidade
- `missing_items`: seções ou links obrigatórios ausentes
- `consistency_score`: baixo/médio/alto com justificativa
- `recommended_actions`: próximos passos em ordem

## Regras Gerais
- Escrever revisão em português.
- Sempre referenciar o capítulo remoto usado na análise.
