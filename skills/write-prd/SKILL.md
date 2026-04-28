---
name: write-prd
description: Escreve um Product Requirements Document a partir de feature proposal e discovery. Use quando o usuário pedir criação ou refinamento de PRD para iniciativa, módulo ou feature de alto impacto.
---

# Escrever PRD

## Objetivo
Produzir PRD aplicando exclusivamente as diretrizes do framework remoto.

## Entradas Obrigatórias
- Feature proposal
- Discovery notes (se disponível)

## Fonte do Framework
Usar como referência obrigatória:
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/04-prd.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/09-boas-praticas.md`
Não usar fallback local. O repositório remoto é a única fonte de verdade.

## Procedimento Obrigatório
1. Buscar e ler os arquivos remotos listados em "Fonte do Framework".
2. Gerar o PRD com base na estrutura e nas regras desses capítulos remotos.
3. Não adicionar template local concorrente ao template remoto.
4. Se qualquer arquivo remoto estiver indisponível, interromper a execução.
5. Em caso de indisponibilidade, responder com erro objetivo informando quais URLs falharam.

## Diretriz de Execução em Sandbox (Rede Restrita)
- Se a leitura remota falhar por limitação de rede/DNS do sandbox, tentar novamente usando comando com permissão escalada para as **mesmas URLs** canônicas (ex.: `curl -fsSL`).
- A tentativa com permissão escalada é um fallback de **transporte**, não de conteúdo: continua proibido usar cópia local ou fonte alternativa.
- Se mesmo com permissão escalada qualquer URL falhar, interromper e reportar erro objetivo com as URLs indisponíveis.
- Não gerar documento parcial em nenhum cenário.

## Saída Esperada
- Criar o documento em `docs/features/<feature-name>/prd.md`.
- Documento em português.
- Seções e metadados alinhados ao capítulo remoto de PRD.
- Referências explícitas para proposal/discovery/epico quando existirem.
