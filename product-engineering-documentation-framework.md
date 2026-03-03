# Framework de Documentação de Produto e Engenharia

## Índice

- [1. Introdução](#1-introducao)
  - [1.1 Objetivo do Framework](#11-objetivo-do-framework)
  - [1.2 Por que documentar?](#12-por-que-documentar)
  - [1.3 Princípios de Documentação (clareza, proporcionalidade, redução de risco)](#13-principios-de-documentacao-clareza-proporcionalidade-reducao-de-risco)
- [2. Hierarquia de Documentação no Produto](#2-hierarquia-de-documentacao-no-produto)
  - [2.1 Visão geral dos níveis](#21-visao-geral-dos-niveis)
  - [2.2 Estratégia → Produto → Funcionalidade → Implementação](#22-estrategia--produto--funcionalidade--implementacao)
  - [2.3 Relação entre Produto e Engenharia](#23-relacao-entre-produto-e-engenharia)
- [3. Visão de Produto (Product Vision)](#3-visao-de-produto-product-vision)
  - [3.1 O que é](#31-o-que-e)
  - [3.2 Para que serve](#32-para-que-serve)
  - [3.3 Nível de escopo](#33-nivel-de-escopo)
  - [3.4 Estrutura recomendada](#34-estrutura-recomendada)
  - [3.5 Quando criar ou revisar](#35-quando-criar-ou-revisar)
- [4. PRD (Product Requirements Document)](#4-prd-product-requirements-document)
  - [4.1 O que é](#41-o-que-e)
  - [4.2 Para que serve](#42-para-que-serve)
  - [4.3 Nível de escopo](#43-nivel-de-escopo)
  - [4.4 Diferença entre PRD e funcionalidade](#44-diferenca-entre-prd-e-funcionalidade)
  - [4.5 Estrutura recomendada](#45-estrutura-recomendada)
  - [4.6 Quando é necessário](#46-quando-e-necessario)
- [5. Especificação de Funcionalidade (Feature Spec)](#5-especificacao-de-funcionalidade-feature-spec)
  - [5.1 O que é](#51-o-que-e)
  - [5.2 Para que serve](#52-para-que-serve)
  - [5.3 Nível de escopo](#53-nivel-de-escopo)
  - [5.4 Diferença entre PRD e Especificação de Funcionalidade (Feature Spec)](#54-diferenca-entre-prd-e-especificacao-de-funcionalidade-feature-spec)
  - [5.5 Estrutura recomendada](#55-estrutura-recomendada)
  - [5.6 Entidades no nível funcional](#56-entidades-no-nivel-funcional)
  - [5.7 Perfis e permissões](#57-perfis-e-permissoes)
  - [5.8 Critérios de aceitação](#58-criterios-de-aceitacao)
- [6. Especificação Técnica (Tech Spec / TDD)](#6-especificacao-tecnica-tech-spec--tdd)
  - [6.1 O que é](#61-o-que-e)
  - [6.2 Para que serve](#62-para-que-serve)
  - [6.3 Nível de escopo](#63-nivel-de-escopo)
  - [6.4 Diferença entre Especificação de Funcionalidade (Feature Spec) e Especificação Técnica (Tech Spec)](#64-diferenca-entre-especificacao-de-funcionalidade-feature-spec-e-especificacao-tecnica-tech-spec)
  - [6.5 Estrutura recomendada](#65-estrutura-recomendada)
  - [6.6 Modelagem de dados](#66-modelagem-de-dados)
  - [6.7 Contratos de API](#67-contratos-de-api)
  - [6.8 Regras técnicas](#68-regras-tecnicas)
  - [6.9 Impactos técnicos e migrações](#69-impactos-tecnicos-e-migracoes)
  - [6.10 Riscos e compensações (trade-offs)](#610-riscos-e-compensacoes-trade-offs)
- [7. Histórias de Usuário (User Stories)](#7-historias-de-usuario-user-stories)
  - [7.1 O que são](#71-o-que-sao)
  - [7.2 Papel dentro do fluxo de desenvolvimento](#72-papel-dentro-do-fluxo-de-desenvolvimento)
  - [7.3 Relação com PRD, Especificação de Funcionalidade e Especificação Técnica](#73-relacao-com-prd-especificacao-de-funcionalidade-e-especificacao-tecnica)
  - [7.4 Estrutura recomendada (Como / Quero / Para)](#74-estrutura-recomendada-com--quero--para)
  - [7.5 Critérios de aceitação](#75-criterios-de-aceitacao)
  - [7.6 Quando uma história precisa de Especificação Técnica](#76-quando-uma-historia-precisa-de-especificacao-tecnica)
- [8. Matriz de Decisão de Documentação de Funcionalidades](#8-matriz-de-decisao-de-documentacao-de-funcionalidades)
  - [8.1 Avaliação por impacto de produto](#81-avaliacao-por-impacto-de-produto)
  - [8.2 Avaliação por complexidade funcional](#82-avaliacao-por-complexidade-funcional)
  - [8.3 Avaliação por complexidade técnica](#83-avaliacao-por-complexidade-tecnica)
  - [8.4 Combinações possíveis de documentos](#84-combinacoes-possiveis-de-documentos)
  - [8.5 Exemplos práticos de aplicação](#85-exemplos-praticos-de-aplicacao)
- [9. Boas Práticas](#9-boas-praticas)
  - [9.1 Documentação proporcional ao risco](#91-documentacao-proporcional-ao-risco)
  - [9.2 Evitar burocracia excessiva](#92-evitar-burocracia-excessiva)
  - [9.3 Versionamento e atualização de documentos](#93-versionamento-e-atualizacao-de-documentos)
  - [9.4 Documentação viva vs. documentação histórica](#94-documentacao-viva-vs-documentacao-historica)
- [10. Fluxo Integrado de Desenvolvimento](#10-fluxo-integrado-de-desenvolvimento)
  - [10.1 Da Visão de Produto às Histórias de Usuário](#101-da-visao-de-produto-as-historias-de-usuario)
  - [10.2 Como os documentos se conectam](#102-como-os-documentos-se-conectam)
  - [10.3 Exemplo completo de uma funcionalidade atravessando todos os níveis](#103-exemplo-completo-de-uma-funcionalidade-atravessando-todos-os-niveis)
- [11. Glossário](#11-glossario)
  - [11.1 Definições de termos](#111-definicoes-de-termos)
  - [11.2 Diferença entre documento e artefato](#112-diferenca-entre-documento-e-artefato)
  - [11.3 Siglas (PRD, SRS, TDD, etc.)](#113-siglas-prd-srs-tdd-etc)
 - [12. Referências Bibliográficas](#12-referencias-bibliograficas)

---

## 1. Introdução

### 1.1 Objetivo do Framework

Este framework define **quais documentos** usar em Produto e Engenharia, **quando** criar cada um e **como** estruturá-los. O objetivo é reduzir ambiguidades, alinhar decisões e diminuir retrabalho, mantendo a documentação **proporcional ao risco e ao impacto**.

### 1.2 Por que documentar?

- Alinhar liderança, stakeholders e times sobre **o porquê** e **o quê** será feito.
- Eliminar ambiguidades antes do desenvolvimento (especialmente em regras de negócio e fluxos).
- Reduzir risco técnico e operacional (migrações, integrações, desempenho, implantação).
- Aumentar previsibilidade, facilitar repasses entre pessoas/times e manter consistência ao longo do tempo.

### 1.3 Princípios de Documentação (clareza, proporcionalidade, redução de risco)

- **Clareza acima de completude**: o documento existe para apoiar decisão e execução.
- **Proporcionalidade**: quanto maior o risco/impacto, maior a necessidade de documentar.
- **Redução de risco**: o custo de não documentar (retrabalho, bugs, divergência, atrasos) deve guiar a escolha.

---

## 2. Hierarquia de Documentação no Produto

### 2.1 Visão geral dos níveis


| Documento                                                                | Tipo                                       | Para que serve                            | Escopo                                        | Foco                    | Responde                                                                                                                             |
| ------------------------------------------------------------------------ | ------------------------------------------ | ----------------------------------------- | --------------------------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| SRS (Software Requirements Specification)                                | Documento de requisitos formais do sistema | Documentação formal completa do sistema   | Sistema inteiro formal                        | Requisitos formais      | Requisitos funcionais do sistema completo / Requisitos não funcionais / Regras de negócio globais / Interfaces externas / Restrições |
| Visão de Produto (Product Vision)                                        | Documento estratégico                      | Definir o produto como um todo            | Produto inteiro                               | Estratégia              | Qual problema resolvemos? / Para quem? / Qual posicionamento? / Quais objetivos estratégicos?                                        |
| PRD (Product Requirements Document)                                      | Documento de requisitos                    | Definir o que a iniciativa deve fazer     | Iniciativa ou módulo relevante                | Produto / comportamento | O que a iniciativa/funcionalidade deve fazer (em alto nível)                                                                         |
| Especificação de Funcionalidade (Feature Spec / Especificação Funcional) | Documento funcional                        | Detalhar completamente uma funcionalidade | Funcionalidade específica                     | Funcional detalhado     | Como a funcionalidade funciona (fluxos, regras, exceções)                                                                            |
| Especificação Técnica (Tech Spec / TDD / Documento de Design Técnico)    | Documento técnico                          | Explicar como será implementado           | Funcionalidade específica (ou parte complexa) | Técnico                 | Como implementar (arquitetura, dados, contratos, compensações (trade-offs))                                                          |


No contexto ágil, normalmente é utilizado:

- 1 **Visão de Produto (Product Vision)** (produto inteiro)
- Vários **PRDs** (para grandes iniciativas)
- Várias **Especificações de Funcionalidade (Feature Specs)**
- Vários **Tech Specs**

E raramente um **SRS** completo (a menos que seja exigência formal).

### 2.2 Estratégia → Produto → Funcionalidade → Implementação

**Hierarquia de escopo das documentações:**

Visão de Produto (Product Vision)  
↓  
PRD  
↓  
Especificação de Funcionalidade (Feature Spec)  
↓  
Especificação Técnica (Tech Spec)

**Analogia simples (se o produto fosse um prédio):**

- Visão de Produto (Product Vision) → Por que estamos construindo o prédio
- PRD → Projeto do andar inteiro
- Especificação de Funcionalidade (Feature Spec) → Projeto detalhado de um apartamento
- Especificação Técnica (Tech Spec) → Como será feita a instalação elétrica
- História de usuário (user story) → Instalar uma tomada específica na sala

### 2.3 Relação entre Produto e Engenharia

- **Produto** define intenção, escopo e sucesso (problema, objetivo, o que entra/não entra, métricas).
- **Engenharia** define solução e execução segura (arquitetura, dados, contratos, riscos, testes, implantação).
- Especificação de Funcionalidade (Feature Spec) e Especificação Técnica (Tech Spec) funcionam como “contratos” complementares: **comportamento** (o que acontece) e **implementação** (como fazer).

---

## 3. Visão de Produto (Product Vision)

### 3.1 O que é

Documento estratégico que define a direção do produto como um todo. É a bússola do produto.

### 3.2 Para que serve

- Alinhar liderança/stakeholders sobre:
  - Problema que o produto resolve
  - Público-alvo
  - Diferencial competitivo
  - Objetivos de longo prazo
- Guiar decisões futuras
- Evitar desvio estratégico

### 3.3 Nível de escopo

Produto inteiro (visão macro e de longo prazo).

### 3.4 Estrutura recomendada

1. **Contexto**: cenário atual, situação do mercado, problema existente, oportunidade.
2. **Problema**: dor principal que será resolvida.
3. **Público-alvo**: segmentos, personas, maturidade.
4. **Proposta de Valor**: diferenciais e benefícios.
5. **Objetivos Estratégicos**: metas macro (crescimento, receita, retenção, expansão) e indicadores.
6. **Visão de Futuro**: onde queremos chegar em X anos (roteiro macro, evolução, expansão).

### 3.5 Quando criar ou revisar

- Criar quando houver definição (ou redefinição) da estratégia do produto.
- Revisar quando houver mudança relevante em mercado, posicionamento, público-alvo ou objetivos estratégicos.
- Revalidar periodicamente para garantir alinhamento (ex.: ciclos trimestrais/semestrais), especialmente antes de iniciativas grandes.

---

## 4. PRD (Product Requirements Document)

### 4.1 O que é

Documento que define os requisitos de uma iniciativa relevante dentro do produto (módulo, grande funcionalidade, capacidade).

### 4.2 Para que serve

Alinha Produto, Design e Engenharia sobre uma grande iniciativa para traduzir estratégia em algo construível.

### 4.3 Nível de escopo

Iniciativa ou módulo relevante (acima de funcionalidade individual).

### 4.4 Diferença entre PRD e funcionalidade

- **PRD**: descreve “o que” uma **iniciativa** precisa entregar (objetivo, escopo, requisitos em alto nível, métricas, dependências).
- **Especificação de Funcionalidade (Feature Spec)**: descreve “como funciona” uma **funcionalidade específica**, detalhando fluxos, regras e exceções.

### 4.5 Estrutura recomendada

1. **Contexto**: por que a iniciativa é necessária.
2. **Problema**: qual problema específico será resolvido.
3. **Objetivo**: resultado esperado (ex.: reduzir inadimplência em 20%).
4. **Escopo**: o que entra e o que não entra (limites para evitar “scope creep”).
5. **Requisitos Funcionais (alto nível)**: comportamentos esperados sem detalhar implementação.
6. **Requisitos Não Funcionais**: performance, segurança, escalabilidade, conformidade.
7. **Métricas de Sucesso**: como medir se deu certo.
8. **Dependências**: times envolvidos, integrações, limitações e riscos.

---

## 5. Especificação de Funcionalidade (Feature Spec)

### 5.1 O que é

Documento que detalha completamente uma funcionalidade específica.

### 5.2 Para que serve

Eliminar ambiguidades antes do desenvolvimento. Serve como referência funcional para implementação.

### 5.3 Nível de escopo

Funcionalidade específica dentro de um PRD (ou uma entrega independente).

### 5.4 Diferença entre PRD e Especificação de Funcionalidade (Feature Spec)

- **PRD**: iniciativa/módulo, visão de alto nível e critérios de sucesso.
- **Especificação de Funcionalidade (Feature Spec)**: descrição detalhada do comportamento de uma funcionalidade (fluxos, regras, exceções).

### 5.5 Estrutura recomendada

1. **Contexto da Funcionalidade**: onde se encaixa no produto.
2. **Objetivo**: o que resolve.
3. **Fluxo do Usuário**: passo a passo (fluxo principal e alternativos).
4. **Regras de Negócio**: condições, restrições, validações.
5. **Entidades Envolvidas (nível funcional)**: objetos do sistema, campos relevantes, estados (sem modelagem técnica).
6. **Perfis e Permissões**: quem pode fazer o quê.
7. **APIs / Rotas (visão funcional)**: endpoints envolvidos sem payload técnico completo.
8. **Casos de Exceção**: erros esperados, estados alternativos, validações.
9. **Critérios de Aceitação**: condições para considerar pronto.

### 5.6 Entidades no nível funcional

Liste entidades e campos relevantes para entendimento do comportamento (ex.: “Pedido”, “Status”, “Data de vencimento”), sem se comprometer com tipos, índices ou detalhes de persistência.

### 5.7 Perfis e permissões

Defina claramente perfis e suas ações permitidas, principalmente quando houver matriz de acesso ou fluxos com exceções por papel.

### 5.8 Critérios de aceitação

Critérios verificáveis que demonstrem que o comportamento esperado foi entregue (incluindo fluxos alternativos e erros importantes).

---

## 6. Especificação Técnica (Tech Spec / TDD)

### 6.1 O que é

Documento técnico que descreve como a funcionalidade será implementada.

### 6.2 Para que serve

Tomar decisões de arquitetura, reduzir risco técnico e alinhar engenharia antes de codar.

### 6.3 Nível de escopo

Funcionalidade específica (ou parte complexa dela).

### 6.4 Diferença entre Especificação de Funcionalidade (Feature Spec) e Especificação Técnica (Tech Spec)

- **Especificação de Funcionalidade (Feature Spec)**: “o que acontece” do ponto de vista funcional (comportamento).
- **Especificação Técnica (Tech Spec)**: “como implementar” do ponto de vista técnico (arquitetura, dados, contratos, riscos).

### 6.5 Estrutura recomendada

1. **Contexto Técnico**: situação atual da arquitetura.
2. **Arquitetura da Solução**: componentes (back-end, front-end, banco, serviços externos) e diagramas.
3. **Modelagem de Dados**: tabelas, campos, tipos, índices, restrições (constraints).
4. **Contratos de API**: requisições/respostas, corpos das mensagens (payloads), códigos de status, versionamento.
5. **Regras Técnicas**: camadas intermediárias (middlewares), validações técnicas, processos assíncronos, registros (logs).
6. **Impactos no Sistema**: migrações, quebras de compatibilidade, desempenho.
7. **Estratégia de Testes**: unitários, integração, ponta a ponta (E2E).
8. **Riscos e compensações (trade-offs)**: decisões tomadas e alternativas descartadas.

### 6.6 Modelagem de dados

Quando houver persistência relevante, documente mudanças e migrações (inclusive preenchimentos retroativos e restrições (constraints)) e como serão aplicadas com segurança.

### 6.7 Contratos de API

Documente contratos com nível suficiente para evitar divergência entre consumidores (corpos das mensagens/payloads, códigos, versionamento e compatibilidade).

### 6.8 Regras técnicas

Centralize decisões de implementação que afetem consistência e operação (validações, filas/eventos, registros (logs) e observabilidade, idempotência, etc.).

### 6.9 Impactos técnicos e migrações

Liste impactos esperados e plano de execução quando houver risco (migrações, implantação gradual, compatibilidade, flags de funcionalidade).

### 6.10 Riscos e compensações (trade-offs)

Registre compensações (trade-offs) reais (2+ abordagens), critérios da decisão e riscos assumidos para reduzir retrabalho.

---

## 7. Histórias de Usuário (User Stories)

### 7.1 O que são

Histórias de usuário (user stories) são unidades pequenas de trabalho que descrevem uma necessidade do usuário e ajudam a fatiar a entrega em partes implementáveis e verificáveis.

### 7.2 Papel dentro do fluxo de desenvolvimento

- Traduzem um comportamento em lista de trabalho executável (backlog).
- Facilitam planejamento, priorização e acompanhamento.
- Funcionam melhor quando derivadas de uma Especificação de Funcionalidade (Feature Spec) (ou, em mudanças pequenas, diretamente do PRD/resumo).

### 7.3 Relação com PRD, Especificação de Funcionalidade e Especificação Técnica

- PRD alinha o “por quê” e o resultado esperado da iniciativa.
- A Especificação de Funcionalidade remove ambiguidades de comportamento.
- A Especificação Técnica reduz risco técnico e define implementação.
- Histórias de usuário representam a execução incremental, com critérios de aceitação e, quando necessário, referências aos documentos acima.

### 7.4 Estrutura recomendada (Como / Quero / Para)

- **Como** [perfil/persona]  
**Quero** [capacidade/ação]  
**Para** [benefício/resultado]

### 7.5 Critérios de aceitação

Defina critérios claros e verificáveis para a story, alinhados ao comportamento esperado (incluindo casos de erro quando relevante).

### 7.6 Quando uma história precisa de Especificação Técnica

Uma história precisa (ou deve referenciar) uma Especificação Técnica quando houver risco técnico relevante: mudança de arquitetura, migração, contratos usados por outros sistemas, integrações externas, desempenho/concorrência, ou compensações (trade-offs) técnicos não óbvios.

---

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

---

## 9. Boas Práticas

### 9.1 Documentação proporcional ao risco

Use a matriz de decisão (seção 8) para ajustar o nível de documentação ao impacto e ao risco. Documentar demais aumenta burocracia; documentar de menos aumenta retrabalho e risco de produção.

### 9.2 Evitar burocracia excessiva

- Prefira documentos objetivos e orientados a decisão/execução.
- Quando a mudança é pequena e clara, histórias com bons critérios de aceitação podem ser suficientes.

### 9.3 Versionamento e atualização de documentos

- Trate documentos como referências vivas: atualize quando decisões mudarem.
- Registre mudanças relevantes (escopo, regras, contratos) para evitar divergência entre times.

### 9.4 Documentação viva vs. documentação histórica

- Documentos de decisão (compensações (trade-offs), riscos) devem ser fáceis de localizar e manter.
- Quando necessário, mantenha histórico de mudanças (o mínimo suficiente para auditoria e aprendizagem).

---

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

---

## 11. Glossário

### 11.1 Definições de termos

- **Documento**: artefato com propósito de alinhamento/decisão/execução, mantido como referência.
- **Artefato**: qualquer saída de trabalho (documento, ticket, diagrama, planilha), nem sempre estruturada como documento.
- **Critérios de aceitação (AC)**: condições verificáveis que definem quando algo está “pronto”.
- **Stakeholder**: pessoa/grupo impactado pela decisão/entrega (usuário, negócio, operação, compliance, etc.).
- **Escopo**: limites do que entra e do que fica de fora.
- **Trade-off**: escolha entre alternativas com benefícios e custos.

### 11.2 Diferença entre documento e artefato

Um documento é um artefato, mas nem todo artefato é um documento. O que diferencia é a **intenção** (servir de referência) e a **estrutura** (facilitar consumo e manutenção).

### 11.3 Siglas (PRD, SRS, TDD, etc.)

- **SRS**: Software Requirements Specification
- **PRD**: Product Requirements Document
- **Especificação de Funcionalidade (Feature Spec)**: Especificação Funcional (Functional Specification)
- **Especificação Técnica (Tech Spec / TDD)**: Documento de Design Técnico (Technical Design Document)
- **AC**: Acceptance Criteria

---

## 12. Referências Bibliográficas

Esta seção lista as principais referências utilizadas como base conceitual para este framework de documentação de produto e engenharia.

### 12.1 Produto, visão de produto e gestão de produto

- **Atlassian – Agile Product Management**  
  ATLASSIAN. *Agile product management*. Disponível em: `https://www.atlassian.com/agile/product-management/`.  
  Acesso em: 2026.

- **Marty Cagan – Inspired / Inspirado**  
  CAGAN, Marty. *Inspired: How to Create Tech Products Customers Love*. 2. ed. Wiley, 2017.  
  Edição em português:  
  CAGAN, Marty. *Inspirado: como criar produtos de tecnologia que os clientes amam*. São Paulo: Editora Autêntica, 2018.  
  Referência: `https://www.amazon.com.br/Inspirado-criar-produtos-tecnologia-clientes/dp/8550813826`.

### 12.2 PRD, Especificação de Funcionalidade e Especificação Técnica

- **Karl Wiegers & Joy Beatty – Software Requirements**  
  WIEGERS, Karl; BEATTY, Joy. *Software Requirements*. 3. ed. Microsoft Press, 2013.  
  Referência: `https://www.amazon.com/Software-Requirements-Developer-Best-Practices/dp/0735679665`.

- **Clements et al. – Documenting Software Architectures**  
  CLEMENTS, Paul; BACHMANN, Felix; BASS, Len; GARLAN, David; IVERS, James; LITTLE, Reed; NORD, Robert; STAFFORD, Judith.  
  *Documenting Software Architectures: Views and Beyond*. 3. ed. Addison-Wesley, 2023.  
  Referência: `https://www.amazon.com.br/Documenting-Software-Architectures-Portable-Documents-ebook/dp/B0CLL14ZNN`.

