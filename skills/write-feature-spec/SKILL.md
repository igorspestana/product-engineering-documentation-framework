---
name: write-feature-spec
description: Escreve especificação funcional detalhada com comportamento, regras, estados, permissões e critérios de aceitação. Use quando o usuário pedir criação de feature spec a partir de proposal, PRD ou discovery.
---

# Escrever Feature Spec

## Objetivo
Gerar feature spec aplicando exclusivamente as diretrizes do framework remoto.

## Entradas Obrigatórias
- Feature proposal
- PRD (quando disponível)
- Discovery notes (opcional)

## Fonte do Framework
Usar como referência obrigatória:
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/05-especificacao-funcionalidade.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/07-historias-usuario.md`
- `https://raw.githubusercontent.com/igorspestana/product-engineering-documentation-framework/main/09-boas-praticas.md`
Não usar fallback local. O repositório remoto é a única fonte de verdade.

## Procedimento Obrigatório
1. Buscar e ler os arquivos remotos listados em "Fonte do Framework".
2. Gerar a feature spec conforme estrutura e regras dos capítulos remotos.
3. Não adicionar template local concorrente ao template remoto.
4. Se qualquer arquivo remoto estiver indisponível, interromper a execução.
5. Em caso de indisponibilidade, responder com erro objetivo informando quais URLs falharam.

## Diretriz de Execução em Sandbox (Rede Restrita)
- Se a leitura remota falhar por limitação de rede/DNS do sandbox, tentar novamente usando comando com permissão escalada para as **mesmas URLs** canônicas (ex.: `curl -fsSL`).
- A tentativa com permissão escalada é um fallback de **transporte**, não de conteúdo: continua proibido usar cópia local ou fonte alternativa.
- Se mesmo com permissão escalada qualquer URL falhar, interromper e reportar erro objetivo com as URLs indisponíveis.
- Não gerar especificação parcial em nenhum cenário.

## Saída Esperada
- Criar o documento em `docs/features/<feature-name>/feature-spec.md`.
- Documento em português.
- Seções, metadados e critérios de aceitação alinhados aos capítulos remotos.
- Alinhamento explícito com PRD e histórias quando existirem.
