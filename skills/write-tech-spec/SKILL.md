---
name: write-tech-spec
description: Escreve uma especificação técnica (design doc) para implementar uma feature com arquitetura, dados, contratos, riscos, testes e plano de rollout. Use quando o usuário pedir planejamento técnico de implementação.
---

# Escrever Tech Spec

## Objetivo
Gerar tech spec aplicando exclusivamente as diretrizes do framework remoto.

## Entradas Obrigatórias
- Feature brief
- Feature spec (preferencial)
- Contexto de arquitetura existente

## Fonte do Framework
Usar como referência obrigatória:
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/06-especificacao-tecnica.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/08-matriz-decisao.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/09-boas-praticas.md`
Não usar fallback local. O repositório remoto é a única fonte de verdade.

## Procedimento Obrigatório
1. Buscar e ler os arquivos remotos listados em "Fonte do Framework".
2. Gerar a tech spec conforme estrutura e regras dos capítulos remotos.
3. Não adicionar template local concorrente ao template remoto.
4. Se qualquer arquivo remoto estiver indisponível, interromper a execução.
5. Em caso de indisponibilidade, responder com erro objetivo informando quais URLs falharam.

## Diretriz de Execução em Sandbox (Rede Restrita)
- Se a leitura remota falhar por limitação de rede/DNS do sandbox, tentar novamente usando comando com permissão escalada para as **mesmas URLs** canônicas (ex.: `curl -fsSL`).
- A tentativa com permissão escalada é um fallback de **transporte**, não de conteúdo: continua proibido usar cópia local ou fonte alternativa.
- Se mesmo com permissão escalada qualquer URL falhar, interromper e reportar erro objetivo com as URLs indisponíveis.
- Não gerar especificação parcial em nenhum cenário.

## Saída Esperada
- Criar o documento em `docs/features/<feature-name>/tech-spec.md`.
- Documento em português.
- Seções, metadados e decisões técnicas alinhados aos capítulos remotos.
- Riscos, trade-offs e rollout descritos conforme padrão remoto.
