# Design Decisions

Este arquivo registra decisões importantes de UX/UI e Produto do projeto VAIDEBET 2.0.

Use este documento para evitar retrabalho, manter consistência entre telas e impedir que decisões já aprovadas sejam reabertas sem necessidade.

---

## Como usar este arquivo

Sempre que uma decisão de UX/UI ou Produto for tomada, registre:

- data;
- contexto;
- decisão;
- motivo;
- impacto nas telas, fluxos, produto ou operação;
- status;
- responsável, se necessário;
- relação com fluxos, telas, componentes ou agentes.

Os agentes devem consultar este arquivo antes de propor mudanças em fluxos, telas, componentes, padrões visuais, requisitos ou decisões de produto.

---

## Status possíveis

- `Proposta`: decisão sugerida, ainda não validada.
- `Em validação`: decisão em teste ou aguardando alinhamento.
- `Aprovada`: decisão vigente e deve ser respeitada.
- `Rejeitada`: decisão descartada e não deve ser sugerida novamente sem novo contexto.
- `Substituída`: decisão antiga mantida apenas como histórico.

---

## Regras de governança

- Decisões com status `Aprovada` não devem ser contraditas sem sinalização explícita.
- Se uma nova proposta entrar em conflito com decisão aprovada, registrar o conflito antes de sugerir alteração.
- Decisões antigas não devem ser apagadas; devem ser marcadas como `Substituída`, quando necessário.
- Toda decisão que impactar mais de uma tela, vertical, jornada ou agente deve ser registrada.
- Toda decisão que orientar handoff deve ser registrada.
- Preferir decisões objetivas e acionáveis, evitando justificativas vagas.

---

# Índice de decisões

| ID | Decisão | Status | Última atualização |
|---|---|---|---|
| DD-001 | Estrutura do Figma como pipeline visual | Aprovada | 2026-05-13 |
| DD-002 | Páginas principais do Figma — estrutura anterior | Substituída | 2026-05-13 |
| DD-003 | Handoff sem página separada de pré-handoff | Aprovada | 2026-05-13 |
| DD-004 | Apenas Ready for Dev é fonte da verdade para desenvolvimento | Aprovada | 2026-05-13 |
| DD-005 | Uso de três papéis de UX/UI no agente | Aprovada | 2026-05-13 |
| DD-006 | Registro de decisões de design e produto | Aprovada | 2026-05-13 |
| DD-007 | Padrão de nome para frames | Aprovada | 2026-05-13 |
| DD-008 | Card obrigatório por fluxo | Aprovada | 2026-05-13 |
| DD-009 | Estados obrigatórios por tela | Proposta | 2026-05-13 |
| DD-010 | Tratamento de erros em formulários | Proposta | 2026-05-13 |
| DD-011 | Componentes reutilizáveis como padrão | Proposta | 2026-05-13 |
| DD-012 | Clareza da ação principal | Proposta | 2026-05-13 |
| DD-013 | Modo especializado para variações de componentes iGaming | Proposta | 2026-05-13 |
| DD-014 | Páginas principais do Figma — VAIDEBET 2.0 | Aprovada | 2026-05-13 |
| DD-015 | Agentes independentes de ferramenta | Proposta | 2026-05-13 |
| DD-016 | Briefing estratégico do redesign VDB | Proposta | 2026-05-13 |
| DD-017 | Product Management Agent para VDB | Proposta | 2026-05-13 |
| DD-018 | VDB como plataforma híbrida de iGaming | Proposta | 2026-05-13 |
| DD-019 | Profundidade contextual de compliance no pipeline UX | Proposta | 2026-05-16 |
| DD-020 | Handoff em três níveis de fidelidade | Proposta | 2026-05-16 |

---

# Decisões

## DD-001 — Estrutura do Figma como pipeline visual

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI  
**Relacionado a:** Organização do Figma, handoff, governança de UX

### Contexto

O arquivo Figma precisa separar exploração, fluxo, wireframes, telas, revisão, handoff e histórico para reduzir ambiguidade operacional.

### Decisão

Organizar o Figma como pipeline visual de maturidade do trabalho.

### Motivo

Reduzir confusão, facilitar navegação, evitar implementação de telas erradas e melhorar preparação para handoff.

### Impacto

- Fluxos de navegação e jornada ficam em `04 Product Flows / Fluxo`.
- Wireframes ficam em `05 Product Flows / Wireframes`.
- Telas em alta fidelidade ou composições visuais ficam em `03 Product Flows / Screens`.
- Fluxos em validação ficam em `06 Product Flows / Review`.
- Fluxos candidatos ou prontos para desenvolvimento ficam em `07 Product Flows / Handoff`.
- Versões antigas ficam em `99 Archive / Deprecated`.

### Riscos ou observações

A estrutura só funciona se os status forem mantidos atualizados.

---

## DD-002 — Páginas principais do Figma — estrutura anterior

**Data:** 2026-05-13  
**Status:** Substituída  
**Responsável:** UX/UI  
**Relacionado a:** Organização do Figma

### Contexto

A estrutura anterior usava páginas mais genéricas para Product Flows.

### Decisão anterior

```txt
00 Cover / Index
01 Project Docs / Governance
02 Design System / Library
03 Product Flows / Working
04 Product Flows / Review
05 Product Flows / Handoff
90 Experiments / Playground
99 Archive / Deprecated
```

### Motivo da substituição

O projeto VAIDEBET 2.0 passou a usar organização mais granular, separando telas, fluxos, wireframes, revisão e handoff.

### Impacto

Esta decisão não deve mais orientar a organização atual do Figma.

### Riscos ou observações

Mantida apenas como histórico. A decisão vigente é a DD-014.

---

## DD-003 — Handoff sem página separada de pré-handoff

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI  
**Relacionado a:** Handoff, organização do Figma

### Contexto

Uma página separada de pré-handoff adicionaria complexidade.

### Decisão

Não criar página separada de pré-handoff. Usar a página `07 Product Flows / Handoff` com duas seções internas:

```txt
07.1 Handoff Candidates
07.2 Ready for Dev
```

### Motivo

Manter o processo profissional sem aumentar complexidade desnecessária.

### Impacto

- Fluxos quase prontos entram em `Handoff Candidates`.
- Fluxos finalizados entram em `Ready for Dev`.
- O pré-handoff existe como etapa interna, não como página própria.

### Riscos ou observações

`Handoff Candidates` não deve ser confundido com entrega final para desenvolvimento.

---

## DD-004 — Apenas Ready for Dev é fonte da verdade para desenvolvimento

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI  
**Relacionado a:** Handoff, desenvolvimento, governança

### Contexto

Múltiplas versões de telas no Figma podem confundir devs, PMs e stakeholders.

### Decisão

Apenas fluxos dentro de `07 Product Flows / Handoff > Ready for Dev` devem ser tratados como fonte da verdade para desenvolvimento.

### Motivo

Evitar implementação de versões erradas ou incompletas.

### Impacto

- Telas em `Fluxo`, `Wireframes`, `Screens`, `Review`, `Handoff Candidates`, `Playground` ou `Archive` não são fonte da verdade.
- Toda tela pronta para dev precisa estar em `Ready for Dev`.
- Comentários críticos devem estar resolvidos antes de mover para `Ready for Dev`.

### Riscos ou observações

Se um fluxo em `Ready for Dev` sofrer alteração relevante, seu status deve voltar para `Handoff Candidate` ou `Review`.

---

## DD-005 — Uso de três papéis de UX/UI no agente

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI  
**Relacionado a:** Agentes, processo de UX

### Contexto

Criar muitos agentes ou papéis de UX/UI aumenta complexidade antes da maturidade do processo.

### Decisão

Usar três papéis principais dentro do agente de UX/UI:

1. Orquestrador UX.
2. Revisor Crítico.
3. Especificador de Telas.

### Motivo

Manter o uso simples, focado e fácil de explicar.

### Impacto

- O Orquestrador UX organiza demandas e fluxos.
- O Revisor Crítico avalia problemas, inconsistências e riscos.
- O Especificador de Telas transforma fluxos em especificações para Figma.

### Riscos ou observações

Novos papéis só devem ser criados se uma tarefa repetitiva justificar separação. Modos especializados podem existir sem virar papel principal.

---

## DD-006 — Registro de decisões de design e produto

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI e Produto  
**Relacionado a:** Governança, documentação, agentes

### Contexto

Decisões importantes podem se perder em conversas, comentários do Figma ou reuniões.

### Decisão

Manter um arquivo de decisões em:

```txt
docs/ux/design-decisions.md
```

E refletir as principais decisões no Figma em:

```txt
01 Project Docs / Governance > Design Decisions
```

### Motivo

Criar histórico verificável e impedir que discussões resolvidas sejam reabertas sem necessidade.

### Impacto

- Decisões aprovadas orientam revisão de fluxos, telas, componentes e requisitos.
- Agentes devem consultar esse arquivo antes de sugerir mudanças relevantes.
- Conflitos com decisões aprovadas devem ser sinalizados.

### Riscos ou observações

O arquivo precisa ser atualizado continuamente para não perder confiabilidade.

---

## DD-007 — Padrão de nome para frames

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI  
**Relacionado a:** Organização do Figma, handoff

### Contexto

Nomes genéricos como `Final`, `Final 2`, `Tela nova` e `Frame 203` dificultam navegação e handoff.

### Decisão

Usar:

```txt
[Fluxo] / [Etapa] / [Tela] / [Estado]
```

Para variações de componente:

```txt
[Fluxo] / [Etapa] / [Componente] / [Estado]
```

### Motivo

Facilitar busca, leitura, revisão e comunicação com devs e PMs.

### Impacto

- Frames finais ou em revisão devem seguir esse padrão.
- Frames exploratórios podem ser menos formais, mas devem ser identificáveis.
- Frames em `Ready for Dev` obrigatoriamente seguem o padrão.

### Riscos ou observações

Nomes longos demais devem ser evitados, mas clareza é prioridade.

---

## DD-008 — Card obrigatório por fluxo

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI e Produto  
**Relacionado a:** Organização de fluxo, Figma, handoff

### Contexto

Fluxos no Figma podem ficar difíceis de entender sem contexto, status, responsável ou escopo.

### Decisão

Todo fluxo deve ter card no topo:

```txt
Fluxo:
Status:
Página atual:
Responsável UX:
Responsável Produto:
Responsável Dev:
Última atualização:

Objetivo:
Escopo:
Fora do escopo:

Dúvidas abertas:
Decisões relacionadas:
Link do ticket/backlog:
```

### Motivo

Permitir que qualquer pessoa entenda rapidamente contexto e maturidade do fluxo.

### Impacto

- Todo bloco de fluxo deve começar com card de contexto.
- Fluxos em `Review` e `Handoff` devem ter card completo.
- Fluxos em `Fluxo`, `Wireframes` e `Screens` podem ter card parcial, mas precisam de objetivo e status.

### Riscos ou observações

O card precisa ser atualizado quando o fluxo muda de status.

---

## DD-009 — Estados obrigatórios por tela

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** UX/UI  
**Relacionado a:** Handoff, qualidade de UX, especificação de telas

### Contexto

Telas costumam ser desenhadas apenas no estado ideal, gerando retrabalho no handoff.

### Decisão

Toda tela relevante deve considerar estados alternativos antes de ser considerada pronta.

### Motivo

Reduzir retrabalho, melhorar qualidade do protótipo e preparar implementação futura.

### Impacto

Sempre que aplicável, prever:

- default;
- loading;
- empty;
- error;
- success;
- disabled;
- validation;
- confirmation;
- cancellation;
- permission/blocked;
- edge cases.

### Riscos ou observações

Nem toda tela precisa de todos os estados, mas a ausência deve ser consciente e registrada.

---

## DD-010 — Tratamento de erros em formulários

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** UX/UI  
**Relacionado a:** Formulários, validação, acessibilidade

### Contexto

Erros em formulários precisam ser compreensíveis e fáceis de corrigir.

### Decisão

Mostrar erros próximos ao campo afetado e, quando houver múltiplos erros ou erro geral, exibir também resumo ou alerta visível.

### Motivo

Facilitar correção rápida, reduzir frustração e melhorar acessibilidade.

### Impacto

- Campos com erro devem ter mensagem clara.
- Mensagens devem explicar problema e, quando possível, como resolver.
- Não depender apenas de cor para indicar erro.
- Estados de erro precisam estar previstos no Figma.
- Em erro de envio, preservar dados preenchidos sempre que possível.

### Riscos ou observações

Evitar mensagens técnicas ou genéricas demais.

---

## DD-011 — Componentes reutilizáveis como padrão

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** UX/UI  
**Relacionado a:** Design System, componentes, consistência visual

### Contexto

Componentes duplicados ou variações sem necessidade aumentam inconsistência e dificultam manutenção.

### Decisão

Priorizar componentes reutilizáveis para elementos recorrentes.

### Motivo

Aumentar consistência, acelerar criação de telas e facilitar handoff futuro.

### Impacto

Componentes recorrentes devem ser tratados como padrão, especialmente:

- botões;
- inputs;
- selects;
- cards;
- modais;
- alerts;
- tabs;
- menus;
- navegação;
- estados de feedback;
- odds buttons;
- game cards;
- event cards;
- betslip;
- wallet components.

### Riscos ou observações

Evitar criar variações visuais sem necessidade real. Quando uma variação for necessária, documentar o motivo.

---

## DD-012 — Clareza da ação principal

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** UX/UI e Produto  
**Relacionado a:** UX, telas, conversão, clareza de fluxo

### Contexto

Telas com múltiplas ações concorrentes podem gerar dúvida e reduzir conclusão de tarefas.

### Decisão

Cada tela deve ter uma ação principal evidente, alinhada ao objetivo daquela etapa do fluxo.

### Motivo

Reduzir ambiguidade e aumentar a chance de o usuário concluir a tarefa.

### Impacto

- Evitar múltiplas CTAs concorrendo com mesmo peso visual.
- A ação principal deve estar visualmente destacada.
- Ações secundárias devem ter menor peso visual.
- Telas informativas devem deixar claro o próximo passo.
- Se uma tela tiver mais de uma ação principal, o objetivo da tela deve ser revisado.

### Riscos ou observações

Em telas de decisão, pode haver mais de uma ação relevante, mas a hierarquia precisa ser clara.

---

## DD-013 — Modo especializado para variações de componentes iGaming

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** UX/UI  
**Relacionado a:** VDB UX/UI Agent, Design System, componentes, Figma, iGaming

### Contexto

O redesign da VDB exige criação e avaliação recorrente de variações visuais de componentes no Figma.

### Decisão

Criar o modo especializado **VDB UI Variant Designer** dentro de `docs/ai/vdb-ui-agent.md`.

Esse modo não será tratado como quarto papel principal. Ele funciona como especialização do Revisor Crítico ou do Especificador de Telas.

### Motivo

Acelerar o redesign visual sem quebrar a governança de papéis.

### Impacto

- Variações exploratórias começam em `90 Experiments / Playground`.
- Telas com variações candidatas podem ser estruturadas em `03 Product Flows / Screens`.
- Fluxos ou comportamentos relacionados devem ser documentados em `04 Product Flows / Fluxo`.
- Componentes candidatos a padrão devem ser avaliados antes de entrar em `02 Design System / Library`.
- Toda variação precisa documentar motivo, contexto de uso, estados e critérios de aceite.
- Variações não são fonte da verdade antes de revisão.

### Riscos ou observações

Toda variação deve resolver problema real de clareza, hierarquia, reutilização, estado, conversão responsável ou adequação ao contexto de iGaming.

---

## DD-014 — Páginas principais do Figma — VAIDEBET 2.0

**Data:** 2026-05-13  
**Status:** Aprovada  
**Responsável:** UX/UI  
**Relacionado a:** Figma, organização do projeto, VAIDEBET 2.0, handoff

### Contexto

A organização real do Figma do projeto VAIDEBET 2.0 foi ajustada para separar melhor telas, fluxos, wireframes, revisão e handoff.

### Decisão

Usar:

```txt
00 Cover / Index
01 Project Docs / Governance
02 Design System / Library
03 Product Flows / Screens
04 Product Flows / Fluxo
05 Product Flows / Wireframes
06 Product Flows / Review
07 Product Flows / Handoff
90 Experiments / Playground
99 Archive / Deprecated
```

### Motivo

Separar trabalho por tipo e maturidade.

### Impacto

- Telas em alta fidelidade vão para `03 Product Flows / Screens`.
- Mapas de jornada e lógica de navegação vão para `04 Product Flows / Fluxo`.
- Estruturas de baixa/média fidelidade vão para `05 Product Flows / Wireframes`.
- Propostas em validação vão para `06 Product Flows / Review`.
- Entregas para desenvolvimento vão para `07 Product Flows / Handoff`.
- Experimentos visuais continuam em `90 Experiments / Playground`.
- Versões antigas vão para `99 Archive / Deprecated`.

### Riscos ou observações

`03 Product Flows / Screens` não é fonte da verdade para desenvolvimento. Apenas `07 Product Flows / Handoff > Ready for Dev` orienta implementação.

---

## DD-015 — Agentes independentes de ferramenta

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** UX/UI e Produto  
**Relacionado a:** Codex, Claude, agentes de IA, documentação

### Contexto

O mesmo agente será usado no Codex e no Claude. Manter instruções completas duplicadas em `AGENTS.md` e `CLAUDE.md` aumenta risco de divergência.

### Decisão

Separar as instruções principais dos agentes em arquivos neutros dentro de `docs/ai/`.

Manter:

```txt
AGENTS.md
CLAUDE.md
```

como wrappers específicos de ferramenta.

### Motivo

Garantir consistência entre ferramentas, reduzir manutenção duplicada e permitir evolução centralizada.

### Impacto

- `docs/ai/vdb-ui-agent.md` vira fonte principal do agente de UX/UI.
- `docs/ai/vdb-pm-agent.md` vira fonte principal do agente de Product Management.
- `AGENTS.md` e `CLAUDE.md` devem apontar para os mesmos arquivos de referência.
- O mesmo raciocínio estratégico deve ser preservado independentemente da ferramenta.

### Riscos ou observações

Se uma ferramenta não carregar arquivos referenciados automaticamente, o usuário deve abrir ou anexar manualmente os arquivos relevantes no início da sessão.

---

## DD-016 — Briefing estratégico do redesign VDB

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** Produto e UX/UI  
**Relacionado a:** Estratégia, UX/UI, Produto, Compliance, Métricas

### Contexto

O projeto precisa de uma fonte estratégica única para alinhar Produto, UX/UI, Pesquisa, Dados, CRM, Engenharia, Compliance e Liderança.

### Decisão

Usar:

```txt
docs/project/vdb-redesign-briefing.md
```

como fonte estratégica principal do redesign VAIDEBET 2.0.

### Motivo

Centralizar tese de produto, verticais, jornadas, métricas, riscos, backlog e plano de trabalho.

### Impacto

- Agentes de UX/UI e PM devem consultar o briefing.
- O briefing orienta estratégia de plataforma híbrida, arquitetura, métricas e riscos.
- Quando houver conflito com decisões registradas, prevalece `docs/ux/design-decisions.md`.

### Riscos ou observações

O briefing não substitui parecer jurídico, validação de compliance nem análise regulatória formal.

---

## DD-017 — Product Management Agent para VDB

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** Produto  
**Relacionado a:** Produto, requisitos, métricas, backlog, discovery, agentes de IA

### Contexto

O redesign precisa de apoio estruturado para decisões de produto, requisitos, priorização, métricas, discovery, critérios de aceite e análise de impacto.

### Decisão

Criar:

```txt
docs/ai/vdb-pm-agent.md
```

como agente de Product Management para o redesign VDB.

### Motivo

Separar responsabilidades de produto das responsabilidades de UX/UI sem criar conflito entre agentes.

### Impacto

- O PM Agent trabalha em paralelo ao UX/UI Agent.
- O PM Agent deve ser usado para PRDs, priorização, hipóteses, métricas, critérios de aceite e análise de impacto.
- O UX/UI Agent continua responsável por fluxos, telas, componentes, revisão visual e handoff.
- Demandas de benchmark, mercado e regulação devem usar o modo de inteligência de mercado e produto dentro do PM Agent.

### Riscos ou observações

O PM Agent não substitui aprovação final de Produto, Compliance, Jurídico, Engenharia, Dados ou Liderança.

---

## DD-018 — VDB como plataforma híbrida de iGaming

**Data:** 2026-05-13  
**Status:** Proposta  
**Responsável:** Produto e UX/UI  
**Relacionado a:** Home, navegação, cassino, live casino, sportsbook, carteira, promoções

### Contexto

A VDB tem força atual em cassino e live casino, mas sportsbook é uma frente estratégica de crescimento.

### Decisão

O redesign deve tratar a VDB como uma plataforma híbrida de iGaming.

```txt
Cassino e live casino = base atual de uso, retenção e recorrência.
Sportsbook = frente estratégica de crescimento.
Carteira, conta, suporte, promoções e jogo responsável = camadas transversais de confiança.
```

### Motivo

Evitar dois erros estratégicos:

1. Tratar a VDB como cassino com esporte escondido.
2. Tratar a VDB como sportsbook com cassino anexado.

### Impacto

- A home deve equilibrar cassino, live casino e esporte.
- Esporte não deve ficar escondido como vertical irrelevante.
- Cassino e live casino não devem perder eficiência para forçar crescimento de esporte.
- A carteira deve ser comum, transparente e neutra entre verticais.
- Promoções devem ser segmentadas por vertical e compreensíveis.
- O sucesso deve considerar crescimento de usuários híbridos sem queda relevante na retenção de cassino.

### Riscos ou observações

Toda mudança que aumente visibilidade de esporte deve monitorar impacto em retenção de cassino, uso de favoritos/recentes, conversão de carteira, suporte e jogo responsável.

---

## DD-019 — Profundidade contextual de compliance no pipeline UX

**Data:** 2026-05-16  
**Status:** Proposta  
**Responsável:** UX/UI e Produto  
**Relacionado a:** `docs/ai/vdb-ui-agent.md`, `docs/ai/vdb-pm-agent.md`, pipeline de maturidade, governança de compliance

### Contexto

A aplicação uniforme de todos os checklists, estados e guardrails de compliance em qualquer etapa do pipeline (Fluxo, Wireframes, Screens, Review, Handoff) trava a criação. Wireframe inicial é forçado a passar pelo mesmo escrutínio de Ready for Dev, e toda tela é forçada a prever 22 estados, mesmo quando não toca carteira, KYC, RG ou promoções.

### Decisão

Adotar profundidade de checagem **contextual**, baseada em duas dimensões:

1. **Etapa do pipeline** — cruzar pipeline com nível de checagem (matriz em §4.1 do UX/UI Agent).
2. **Tema da tela** — estados críticos iGaming só se aplicam quando a tela toca a vertical correspondente (§9.3 do UX/UI Agent).

Guardrails são separados em:

- **Inegociáveis** (§13.1) — valem em qualquer etapa, inclusive Fluxo/Wireframe.
- **Contextuais** (§13.2) — entram quando a tela toca o tema.

Compliance by design (PM Agent §5.5) é separado em:

- **Pré-requisitos críticos** (§5.5.1) — avaliar em qualquer iniciativa.
- **Avaliação contextual** (§5.5.2) — entra quando a iniciativa toca o tema.

### Motivo

A regulação e o jogo responsável continuam estruturais. O que muda é **onde** e **quando** a checagem completa é exigida. Concentrar checklist completo em Review/Handoff protege a regulação sem transformar todo wireframe em auditoria.

### Impacto

- Wireframes e telas exploratórias passam por guardrails inegociáveis apenas.
- Screens recebem checagem contextual se tocam carteira, KYC, RG, promoções, odds.
- Review e Handoff seguem com checklist completo + validação externa.
- Estados de tela são escolhidos em três camadas: base, expandidos, críticos iGaming.
- Agentes (UX/UI e PM) devem aplicar a matriz, não checagem universal.

### Riscos ou observações

- Risco: rotular uma tela como "não toca o tema" e perder uma checagem necessária. Mitigação: revisão obrigatória em Review independente do julgamento de tema.
- Decisões anteriores que implicavam aplicação universal de compliance ficam sobrepostas por esta, sem precisar marcá-las como `Substituída`, pois eram leitura interpretativa e não decisão explícita.

---

## DD-020 — Handoff em três níveis de fidelidade

**Data:** 2026-05-16  
**Status:** Proposta  
**Responsável:** UX/UI  
**Relacionado a:** `docs/ai/vdb-ui-agent.md` §14, pipeline de Handoff, DD-004, DD-007

### Contexto

Pedidos de "handoff" hoje são tratados de forma única, mas a entrega real varia conforme o estágio. Handoff em wireframe não exige a mesma profundidade de handoff em UI final. A ausência dessa distinção empurra todo pedido para o nível mais alto, gerando retrabalho e compliance excessivo em etapas iniciais.

### Decisão

Todo pedido de handoff deve começar pela pergunta de fidelidade. Três níveis:

| Nível | Entregável | Página Figma | Compliance |
|---|---|---|---|
| Baixa | Estrutura, hierarquia, conteúdo essencial | `05 Wireframes` | Apenas guardrails inegociáveis |
| Média | Estrutura + componentes identificados + estados-base | `03 Screens` ou `06 Review` | Inegociáveis + contextuais quando aplicável |
| Alta | Componentes separados prontos para dev, estados completos, regras, critérios de aceite | `07 Handoff > Ready for Dev` | Checklist completo + validação externa |

Para handoff de componente individual, o agente coleta contexto, sugere estados de comportamento por tipo × vertical (matriz em §14.3 do UX/UI Agent), valida com o usuário e gera spec usando o template §14.4.

### Motivo

Separar handoff por fidelidade reduz fricção em etapas exploratórias, mantém rigor em Ready for Dev e dá clareza sobre o que cada nível entrega. Componentes ganham especificação consistente com sugestão automatizada de estados, evitando esquecimento de estados críticos iGaming.

### Impacto

- Agente passa a perguntar fidelidade antes de qualquer handoff.
- Apenas nível Alta entra em `Ready for Dev` (consistente com DD-004).
- Templates de handoff (tela e componente) ficam padronizados em §14.4 e §14.5 do UX/UI Agent.
- Estados de componente são sugeridos por matriz contextual e validados antes da entrega final.

### Riscos ou observações

- Risco: usuário pedir "handoff alta" para um componente que ainda está em exploração, pulando Review. Mitigação: agente sinaliza maturidade insuficiente e recomenda Review primeiro.
- Componentes existentes já entregues sem essa estrutura não precisam ser refeitos retroativamente, apenas novos handoffs seguem o padrão.

---

# Template para novas decisões

## DD-000 — Nome da decisão

**Data:**  
**Status:** Proposta / Em validação / Aprovada / Rejeitada / Substituída  
**Responsável:**  
**Relacionado a:** Fluxo, tela, componente, agente, produto ou documentação relacionada

### Contexto

Explique o problema, cenário ou necessidade que levou à decisão.

### Decisão

Descreva a decisão de forma objetiva.

### Motivo

Explique por que essa decisão foi tomada.

### Impacto

Liste o que muda ou deve ser observado.

### Riscos ou observações

Liste riscos, exceções ou pontos que podem exigir revisão futura.

---

# Checklist para registrar uma decisão

Antes de registrar uma decisão, verifique:

- [ ] A decisão impacta mais de uma tela, fluxo, vertical ou agente?
- [ ] A decisão afeta handoff?
- [ ] A decisão evita retrabalho futuro?
- [ ] A decisão cria ou altera padrão?
- [ ] A decisão precisa ser conhecida por PM, dev, design, dados, CRM, compliance ou liderança?
- [ ] Existe decisão anterior que entra em conflito?
- [ ] O status está correto?
- [ ] O motivo está claro?
- [ ] O impacto está explícito?
