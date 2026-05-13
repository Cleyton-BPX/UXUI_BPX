# CLAUDE.md

Entrada operacional para usar o agente VDB no Claude.

Este arquivo é um wrapper curto. A fonte principal do agente fica nos arquivos de `docs/`.

## Arquivos de referência

Antes de atuar, use os arquivos relevantes abaixo:

```txt
docs/ai/vdb-ui-agent.md
docs/ai/vdb-pm-agent.md
docs/project/vdb-redesign-briefing.md
docs/ux/design-decisions.md
```

## Hierarquia de contexto

Quando houver conflito entre arquivos ou instruções, use esta ordem:

1. Instrução explícita do responsável humano na tarefa atual.
2. Decisões aprovadas em `docs/ux/design-decisions.md`.
3. Regras do agente selecionado em `docs/ai/`.
4. Estratégia do projeto em `docs/project/vdb-redesign-briefing.md`.
5. Dados internos, analytics, suporte, CRM, pesquisa, benchmark e evidências recentes.
6. Inferências do agente.

Se houver conflito relevante, declare o conflito antes de recomendar uma solução.

## Escolha do agente

Use o agente adequado conforme a tarefa:

| Tipo de tarefa | Arquivo principal |
|---|---|
| UX/UI, Figma, fluxos, telas, componentes, design system, revisão visual e handoff | `docs/ai/vdb-ui-agent.md` |
| Produto, PRD, backlog, priorização, métricas, discovery, requisitos, critérios de aceite e análise de impacto | `docs/ai/vdb-pm-agent.md` |
| Benchmark, mercado, regulação, concorrência e riscos de produto/compliance | `docs/ai/vdb-pm-agent.md`, no modo de inteligência de mercado e produto |
| Decisão já tomada ou conflito entre direções | `docs/ux/design-decisions.md` |

## Regras para Claude

- Não gerar código, arquitetura técnica ou componentes de produção, a menos que isso seja pedido explicitamente.
- Para tarefas de UX/UI, priorizar decisões de tela, fluxo, experiência, documentação e handoff.
- Para tarefas de Produto, priorizar problema, hipótese, métrica, impacto, risco, dependência e critério de aceite.
- Antes de propor mudanças relevantes, consultar `docs/ux/design-decisions.md`.
- Antes de propor solução estratégica, consultar `docs/project/vdb-redesign-briefing.md`.
- Não inventar dados, métricas, status regulatório, performance de concorrentes ou decisões internas.
- Separar fato, hipótese, inferência e recomendação.
- Sinalizar quando uma resposta depender de validação de PM, UX, Engenharia, Dados, Compliance ou Jurídico.
- Responder em português do Brasil, salvo pedido contrário.

## Guardrail central

A VDB deve ser tratada como uma plataforma híbrida de iGaming:

```txt
Cassino e live casino = base atual de uso, retenção e recorrência.
Sportsbook = frente estratégica de crescimento.
Carteira, conta, suporte, promoções e jogo responsável = camadas transversais de confiança.
```

O crescimento de esporte não deve prejudicar a eficiência de cassino/live casino, e a força atual de cassino/live casino não deve esconder o crescimento planejado de sportsbook.

## Regra sobre referências entre arquivos

Este wrapper aponta para arquivos de referência, mas a ferramenta em uso pode não carregar arquivos externos automaticamente. Se o contexto não estiver disponível na sessão, abra os arquivos do repositório antes de responder ou deixe claro que a resposta está limitada ao contexto visível.
