# Briefing UX/UI para Redesign da Plataforma VDB

> **Projeto:** Redesign completo da plataforma Vaidebet / VDB  
> **Contexto:** Casa de apostas regulamentada no Brasil, com base atual forte em cassino e cassino ao vivo, e plano estratégico de fortalecer apostas esportivas.  
> **Objetivo:** Criar uma interface competitiva com os principais players do mercado, equilibrando cassino, cassino ao vivo e esporte sem perder eficiência, confiança e clareza.  
> **Versão:** v1  
> **Data:** 13/05/2026  
> **Uso recomendado:** briefing interno para Produto, UX/UI, Pesquisa, Dados, CRM, Engenharia, Compliance e Liderança.  
> **Observação:** este documento é uma base estratégica e operacional. Não substitui parecer jurídico, validação de compliance nem análise regulatória formal.

---

## 1. Resumo executivo

A VDB deve ser redesenhada como uma **plataforma híbrida de iGaming**, não como uma plataforma puramente casino-first nem como uma plataforma sportsbook-first.

A leitura correta do contexto é:

> **Cassino e cassino ao vivo são a base atual de retenção e uso.**  
> **Apostas esportivas são uma frente estratégica de crescimento.**

O redesign precisa resolver três coisas ao mesmo tempo:

1. **Proteger a força atual do cassino e do live casino.**
2. **Dar espaço real para o sportsbook crescer.**
3. **Unificar tudo em uma experiência simples, confiável, regulada e mobile-first.**

A VDB não deve parecer:

> “Um cassino com uma aba de esportes escondida.”

Nem:

> “Uma casa de apostas esportivas com um cassino anexado.”

A direção mais saudável é:

> **Uma plataforma completa de entretenimento com dinheiro real, onde cassino, cassino ao vivo e esporte têm jornadas fortes, integradas e fáceis de entender.**

---

## 2. Premissas do projeto

### 2.1 Premissas de negócio

- A VDB já possui base relevante em **cassino** e **cassino ao vivo**.
- A vertical de **apostas esportivas** hoje representa uma fatia menor da base, mas existe intenção estratégica de crescimento.
- O redesign deve buscar competitividade contra players líderes do mercado brasileiro.
- O crescimento em esporte não pode prejudicar a experiência dos usuários atuais de cassino.
- A plataforma precisa operar dentro do ambiente regulado brasileiro, com atenção a pagamentos, jogo responsável, publicidade, dados, prevenção à lavagem de dinheiro e transparência.

### 2.2 Premissas de experiência

- O usuário não deve precisar entender a estrutura interna da empresa para usar a plataforma.
- Cassino, live casino e sportsbook devem ter **identidades de seção**, mas uma **linguagem visual única**.
- A carteira deve ser uma camada comum, confiável e transparente.
- A home deve ser modular e adaptável ao comportamento do usuário.
- O redesign deve reduzir fricção, aumentar confiança e melhorar descoberta.

### 2.3 Premissas de design

- Mobile-first.
- Clareza antes de estética.
- Velocidade percebida como parte da experiência.
- Compliance by design.
- Personalização sem exploração de vulnerabilidade.
- Métricas e pesquisa para orientar decisões, não gosto pessoal.

---

## 3. Contexto do mercado regulado no Brasil

### 3.1 Situação regulatória

As apostas de quota fixa no Brasil foram legalizadas no âmbito das apostas esportivas pela Lei nº 13.756/2018 e, no âmbito dos jogos online, pela Lei nº 14.790/2023. Para operar nacionalmente, as empresas precisam de autorização prévia da Secretaria de Prêmios e Apostas do Ministério da Fazenda, a SPA/MF.[^1]

Desde **1º de janeiro de 2025**, apenas empresas autorizadas pela SPA podem operar nacionalmente. Cada autorização permite até **três marcas**, e sites com autorização federal utilizam a extensão **“.bet.br”**.[^1]

A lista oficial de empresas autorizadas é pública e foi atualizada pelo Ministério da Fazenda em **06/05/2026**.[^2]

### 3.2 Indicadores do mercado regulado

O relatório periódico da SPA/MF com dados de **1º de janeiro a 30 de dezembro de 2025** mostra um mercado brasileiro de grande escala:

| Indicador | Valor |
|---|---:|
| CPFs únicos que apostaram | 25.245.319 |
| Contas ativas em operadores/empresas | 87.671.439 |
| Contas ativas em marcas/bets | 100.775.427 |
| GGR do período | R$ 36.959.783.379,70 |
| Destinações legais, 12% | R$ 4.532.797.794,92 |
| Autoexclusões centralizadas | Mais de 217 mil |

Esses números indicam um mercado amplo, com forte multihoming: muitos usuários possuem conta em mais de uma marca ou operador.[^3]

### 3.3 Como a regulação ajuda o mercado

A regulação ajuda o setor em cinco frentes principais:

| Frente | Como ajuda |
|---|---|
| **Legalidade e confiança** | Separa operadores autorizados de operadores ilegais e fortalece o ambiente “.bet.br”. |
| **Dados e monitoramento** | O SIGAP permite regulação, monitoramento e fiscalização do mercado com base em dados reportados pelos operadores.[^4] |
| **Pagamentos rastreáveis** | Regras para Pix, TED, cartão de débito e pré-pago aumentam identificação e rastreabilidade das transações.[^5] |
| **Jogo responsável** | A Portaria SPA/MF nº 1.231/2024 estrutura diretrizes para prevenir, identificar e tratar comportamentos problemáticos.[^6] |
| **Certificação e transparência dos jogos** | Jogos online e estúdios ao vivo precisam atender critérios de certificação, aleatoriedade, quota fixa e tabelas de pagamento claras.[^7] |

### 3.4 Impactos diretos para UX/UI

A regulação não é apenas tema jurídico. Ela muda o desenho da experiência.

O UX/UI precisa incorporar:

- clareza sobre operador autorizado e ambiente confiável;
- transparência em saldo, bônus, saque e prazos;
- mensagens claras sobre métodos de pagamento permitidos;
- regras de depósito e saque compreensíveis;
- ferramentas de autolimitação e autoexclusão acessíveis;
- comunicação responsável sobre apostas;
- termos promocionais fáceis de entender;
- diferenciação entre dinheiro real, bônus, saldo bloqueado e saldo disponível;
- prevenção contra padrões obscuros, promessas enganosas e pressão excessiva.

A regra de pagamentos, por exemplo, permite transferências via Pix, TED, cartões de débito ou pré-pagos, desde que os recursos venham da conta cadastrada do apostador, e veda aportes em dinheiro, boleto, criptoativos, cartão de crédito e instrumentos pós-pagos. Também fixa o prazo máximo de **120 minutos** para pagamento de prêmios após o encerramento do evento ou sessão aplicável.[^5]

---

## 4. Estratégia de redesign para VDB

### 4.1 Tese central

A nova VDB deve ser desenhada como uma plataforma com **dois motores principais**:

| Motor | Papel |
|---|---|
| **Cassino + cassino ao vivo** | Base atual, retenção, recorrência, hábito e receita. |
| **Esportes** | Crescimento, aquisição, ativação de usuários híbridos e fortalecimento competitivo. |

O papel do redesign é construir uma ponte entre esses motores.

### 4.2 Princípio de equilíbrio

> Toda decisão de interface deve proteger a eficiência do cassino, aumentar a descoberta do esporte e manter a plataforma simples para o usuário.

Esse princípio deve orientar decisões como:

| Decisão | Direção recomendada |
|---|---|
| Navegação | Esportes precisa de espaço fixo e claro, sem deslocar cassino e live casino. |
| Home | Modular, personalizada e equilibrada por comportamento. |
| Cassino | Acesso rápido a recentes, favoritos, categorias e busca. |
| Live casino | Área forte, com informações de mesa e status ao vivo. |
| Sportsbook | Jornada clara, menos intimidadora e com betslip eficiente. |
| Carteira | Única, transparente e neutra entre verticais. |
| Promoções | Segmentadas por vertical e explicadas sem ambiguidade. |
| Compliance | Integrado ao fluxo, não escondido em rodapé. |

### 4.3 O que o redesign precisa evitar

1. **Copiar sportsbook de concorrente sem considerar a base atual da VDB.**
2. **Transformar a home em um mural de banners.**
3. **Esconder esporte como se fosse uma seção secundária irrelevante.**
4. **Priorizar estética em detrimento de velocidade e clareza.**
5. **Criar cassino, live casino e sportsbook como produtos visualmente desconectados.**
6. **Deixar carteira, saque, bônus e promoções confusos.**
7. **Tratar jogo responsável como obrigação burocrática.**
8. **Lançar redesign sem métrica, teste e design QA.**

---

## 5. Missão do UX/UI em iGaming na VDB

Uma descrição interna adequada seria:

> O UX/UI da VDB é responsável por redesenhar e evoluir a experiência da plataforma como um ecossistema completo de iGaming, equilibrando cassino, cassino ao vivo e apostas esportivas, com foco em descoberta, conversão, retenção, confiança financeira, compliance, jogo responsável e competitividade mobile-first.

Em termos práticos, esse profissional ou time deve atuar em cinco níveis:

| Nível | Responsabilidade |
|---|---|
| **Estratégia de experiência** | Traduzir objetivos de negócio em jornadas e arquitetura. |
| **Pesquisa e diagnóstico** | Entender comportamento real, atritos, oportunidades e expectativas. |
| **Arquitetura e produto** | Organizar verticais, fluxos, navegação, carteiras e promoções. |
| **Interface e design system** | Criar uma linguagem visual consistente e escalável. |
| **Medição e evolução** | Testar, acompanhar métricas, aprender e iterar. |

---

## 6. Funções principais do UX/UI focado em iGaming

### 6.1 Estrategista de experiência

O UX/UI deve definir como a VDB quer ser percebida e usada.

Perguntas que precisa responder:

- A VDB quer competir por simplicidade, velocidade, variedade, confiança, promoções, esporte, live casino ou experiência premium?
- Qual é o papel da home?
- Qual é o espaço ideal para cassino, live casino e esporte?
- Como incentivar usuários de cassino a conhecerem esporte sem interromper seu hábito?
- Como tornar o sportsbook mais acessível para usuários menos experientes?
- Como manter a plataforma confiável em um mercado regulado e sensível?

### 6.2 Arquiteto da informação

Responsável por organizar:

- navegação principal;
- menus;
- categorias;
- lobby de cassino;
- lobby de live casino;
- sportsbook;
- carteira;
- promoções;
- perfil;
- suporte;
- jogo responsável.

A arquitetura precisa permitir que o usuário encontre rapidamente:

- seus jogos recentes;
- favoritos;
- jogos populares;
- cassino ao vivo;
- eventos esportivos;
- betslip;
- promoções;
- depósito;
- saque;
- histórico;
- limites;
- suporte.

### 6.3 Designer de jornadas críticas

As jornadas mais importantes para a VDB são:

1. Cadastro.
2. Login.
3. Verificação/KYC.
4. Primeiro depósito.
5. Primeiro jogo de cassino.
6. Entrada em live casino.
7. Primeira aposta esportiva.
8. Uso do betslip.
9. Saque.
10. Ativação de promoção.
11. Consulta de histórico.
12. Configuração de limites.
13. Autoexclusão ou pausa.
14. Contato com suporte.

### 6.4 Designer de confiança financeira

Em iGaming, dinheiro é parte central da experiência.

O UX/UI deve garantir clareza sobre:

- saldo real;
- saldo bônus;
- saldo bloqueado;
- saldo disponível para saque;
- depósito via Pix;
- saque;
- histórico;
- prazos;
- erros;
- validações;
- status de transação;
- documentação pendente;
- regras promocionais.

Usuário que não entende saldo ou saque perde confiança rapidamente.

### 6.5 Designer de crescimento saudável

O UX/UI deve ajudar a aumentar:

- ativação de novos usuários;
- conversão de primeiro depósito;
- primeira aposta esportiva;
- uso de favoritos;
- retorno a jogos recentes;
- entrada em live casino;
- retenção;
- adoção de esporte;
- formação de usuários híbridos.

Mas deve evitar padrões que incentivem uso problemático ou escondam mecanismos de controle.

### 6.6 Designer de compliance by design

Compliance deve entrar desde o início do design.

O UX/UI deve evitar:

- comunicação que sugira enriquecimento fácil;
- bônus ou incentivos apresentados de forma ambígua;
- dificuldade artificial para saque;
- fricção desnecessária em limites e autoexclusão;
- ocultação de termos relevantes;
- uso excessivo de urgência;
- loops manipulativos;
- confusão entre saldo real e bônus.

### 6.7 Dono da consistência visual

A VDB precisa parecer uma plataforma única.

O UX/UI deve construir e manter:

- design system;
- tokens visuais;
- botões;
- cards de jogos;
- cards de eventos;
- botões de odds;
- betslip;
- modais;
- alerts;
- tabs;
- filtros;
- banners;
- campos de formulário;
- estados de loading;
- estados vazios;
- estados de erro;
- padrões de responsividade.

---

## 7. Perfis de usuário para orientar o redesign

A VDB não deve tratar todos como “apostadores” genéricos.

### 7.1 Perfis principais

| Perfil | Comportamento | Necessidade de UX |
|---|---|---|
| **Cassino recorrente** | Entra para jogar slots, crash games ou jogos favoritos. | Acesso rápido, favoritos, recentes, categorias e carteira clara. |
| **Live casino player** | Busca roleta, blackjack, game shows e mesas ao vivo. | Informações de mesa, status, limites e entrada rápida. |
| **Sports bettor atual** | Já aposta em esporte, mas é minoria na base. | Odds claras, eventos fáceis, betslip eficiente e histórico. |
| **Usuário híbrido** | Alterna entre cassino e esporte. | Navegação fluida, saldo unificado e promoções bem segmentadas. |
| **Usuário de cassino com potencial para esporte** | Ainda não aposta em esporte, mas pode experimentar. | Educação leve, eventos populares, apostas simples e baixo atrito. |
| **Usuário novo** | Ainda está formando percepção de confiança. | Onboarding simples, carteira clara, segurança e orientação contextual. |

### 7.2 Oportunidade estratégica

A VDB pode crescer em esporte por duas vias:

1. **Aquisição de usuários que já apostam em esporte.**
2. **Ativação gradual de usuários atuais de cassino para comportamento híbrido.**

A segunda via exige cuidado. O produto deve apresentar esporte de forma contextual e útil, não invasiva.

---

## 8. Arquitetura da informação recomendada

### 8.1 Navegação principal mobile

Uma estrutura equilibrada poderia ser:

| Item | Função |
|---|---|
| **Início** | Hub personalizado com atalhos para cassino, live casino, esportes, promoções e carteira. |
| **Cassino** | Slots, crash games, instant games, populares, favoritos e provedores. |
| **Ao Vivo** | Roleta, blackjack, game shows, mesas ao vivo e dealers. |
| **Esportes** | Eventos ao vivo, pré-jogo, futebol, competições, favoritos e betslip. |
| **Carteira** | Depósito, saque, saldo, bônus e histórico. |

Conta, suporte, notificações, segurança e jogo responsável podem ficar em menu de perfil.

### 8.2 Home modular

A home deve ser modular e adaptável.

Módulos recomendados:

| Módulo | Objetivo |
|---|---|
| Saldo + depósito rápido | Resolver ação financeira principal. |
| Continue jogando | Retomar jogos recentes de cassino/live. |
| Eventos esportivos em destaque | Dar visibilidade a esporte sem dominar tudo. |
| Cassino popular | Manter força da vertical principal. |
| Ao vivo agora | Destacar live casino e esporte ao vivo. |
| Promoções segmentadas | Separar ofertas de cassino, live e esporte. |
| Favoritos | Acesso rápido ao comportamento recorrente. |
| Novidades | Jogos, eventos ou campanhas novas. |
| Busca global | Ajudar usuário a encontrar jogos, times, campeonatos e promoções. |

### 8.3 Personalização por comportamento

| Tipo de usuário | Home deve priorizar |
|---|---|
| Cassino recorrente | Recentes, favoritos, categorias preferidas, live casino e promoções de cassino. |
| Sports bettor | Eventos ao vivo, próximos jogos, campeonatos favoritos, betslip e promoções esportivas. |
| Usuário híbrido | Módulos balanceados, saldo, promoções por interesse e atalhos para ambas as verticais. |
| Novo usuário | Explicação simples, categorias principais, depósito, segurança e oferta inicial permitida. |
| Usuário inativo | Retorno ao último comportamento, novidades e mensagem de confiança. |

---

## 9. UX/UI de plataforma

### 9.1 Responsabilidades

- Definir arquitetura geral.
- Desenhar home.
- Organizar navegação.
- Criar lógica de menus.
- Integrar verticais.
- Criar padrões comuns.
- Garantir consistência entre cassino, live casino, esporte, carteira, conta e promoções.

### 9.2 Objetivo

> Fazer a VDB parecer uma plataforma única, não três produtos colados.

### 9.3 Decisões críticas

| Tema | Decisão |
|---|---|
| Home | Modular e personalizada, não apenas banners. |
| Navegação | Cassino, Ao Vivo e Esportes com presença clara. |
| Carteira | Camada comum e sempre acessível. |
| Promoções | Segmentadas e compreensíveis. |
| Perfil | Centralizar conta, segurança, suporte e jogo responsável. |
| Busca | Considerar busca global ou busca por vertical, dependendo da viabilidade técnica. |

---

## 10. UX/UI de cassino

### 10.1 Responsabilidades

- Lobby de cassino.
- Busca de jogos.
- Categorias.
- Favoritos.
- Recentes.
- Jogos populares.
- Provedores.
- Novidades.
- Cards de jogos.
- Estados de loading.
- Estados de erro.
- Página/estado de carregamento do jogo.
- Recomendações.

### 10.2 Objetivo

> Reduzir o tempo entre entrar na plataforma e iniciar o jogo desejado.

### 10.3 Componentes essenciais

| Componente | Função |
|---|---|
| Busca forte | Encontrar jogo por nome, provedor, categoria ou termo aproximado. |
| Favoritos | Criar retorno rápido e hábito. |
| Recentes | Diminuir fricção para usuários recorrentes. |
| Categorias | Organizar por intenção: slots, crash, roleta, blackjack, novos, populares. |
| Provedores | Atender usuários que buscam jogos por fornecedor. |
| Cards de jogo | Reconhecimento rápido, toque fácil e bom carregamento. |
| Estados de erro | Explicar indisponibilidade, manutenção ou falha de sessão. |

### 10.4 Cuidados

- Não esconder jogos favoritos atrás de banners.
- Não depender apenas de provedores como categoria principal.
- Não usar carrosséis infinitos sem hierarquia.
- Não prejudicar performance com imagens pesadas.
- Não misturar cassino e esporte sem intenção clara.

---

## 11. UX/UI de cassino ao vivo

### 11.1 Responsabilidades

- Lobby de live casino.
- Mesas ao vivo.
- Game shows.
- Roleta.
- Blackjack.
- Baccarat, se aplicável.
- Filtros por tipo de jogo.
- Informação de mesa.
- Status ao vivo.
- Entrada e saída de mesa.
- Estados de stream/carregamento.
- Mensagens de indisponibilidade.

### 11.2 Objetivo

> Fazer o usuário entender rapidamente onde entrar, quanto pode apostar e o que está acontecendo na mesa.

### 11.3 Informações importantes em cards de live casino

| Informação | Por que importa |
|---|---|
| Nome do jogo/mesa | Reconhecimento. |
| Tipo de jogo | Roleta, blackjack, game show etc. |
| Mínimo e máximo | Ajuda a decidir antes de entrar. |
| Status | Aberta, cheia, rodada em andamento, indisponível. |
| Idioma | Relevante para dealer e entendimento. |
| Provedor | Pode influenciar preferência. |
| CTA claro | Entrar, assistir, jogar ou indisponível. |

### 11.4 Cuidados

- Live casino não deve ser apenas “mais uma categoria” dentro do cassino.
- Usuário precisa perceber que há algo acontecendo agora.
- O tempo de carregamento do stream deve ter feedback visual claro.
- A saída da mesa e o retorno ao lobby precisam ser simples.

---

## 12. UX/UI de sportsbook

### 12.1 Responsabilidades

- Home de esportes.
- Eventos em destaque.
- Apostas ao vivo.
- Pré-jogo.
- Navegação por modalidade.
- Futebol como prioridade.
- Campeonatos.
- Times favoritos.
- Mercados.
- Odds.
- Betslip.
- Múltiplas.
- Histórico.
- Cash out, se aplicável.
- Busca por times, eventos e competições.
- Explicações contextuais para usuários menos experientes.

### 12.2 Objetivo

> Transformar esporte em uma vertical clara, competitiva e menos intimidadora, sem limitar usuários experientes.

### 12.3 Principais desafios de UX em esporte

| Desafio | Solução de UX |
|---|---|
| Muitas informações | Hierarquia: principais mercados primeiro. |
| Odds mudando | Feedback visual claro e confirmação antes de apostar. |
| Betslip confuso | Valor, seleção, retorno potencial e confirmação evidentes. |
| Usuário novo | Educação contextual, não tutorial pesado. |
| Eventos demais | Favoritos, populares, campeonatos e busca. |
| Apostas ao vivo | Separar “agora” de “próximos eventos”. |

### 12.4 Estrutura recomendada para sportsbook

| Área | Função |
|---|---|
| Destaques | Grandes jogos, eventos ao vivo e campeonatos relevantes. |
| Futebol | Principal vertical esportiva no Brasil. |
| Ao vivo | Eventos acontecendo agora. |
| Próximos | Agenda de jogos. |
| Favoritos | Times, campeonatos ou modalidades preferidas. |
| Busca | Encontrar time, liga, evento ou mercado. |
| Betslip | Confirmação de seleções e valores. |
| Minhas apostas | Abertas, finalizadas, ganhas, perdidas, canceladas. |

### 12.5 Pontos de entrada para esporte

| Momento | Solução possível |
|---|---|
| Grande jogo do dia | Módulo na home com evento em destaque. |
| Usuário abre promoções | Separar promoções esportivas de cassino. |
| Usuário novo | Card simples explicando como apostar em futebol. |
| Usuário já depositou | Mostrar eventos populares sem bloquear jornada de cassino. |
| Usuário segue futebol | Permitir favoritar time ou campeonato. |
| Usuário híbrido | Mostrar esporte e cassino de forma balanceada. |

---

## 13. UX/UI de carteira

### 13.1 Responsabilidades

- Saldo.
- Depósito.
- Saque.
- Pix.
- Histórico.
- Status de transações.
- Bônus.
- Saldo bloqueado.
- Saldo disponível.
- Erros.
- Validações.
- KYC relacionado a saque.
- Comprovantes.
- Limites.
- Regras financeiras relevantes.

### 13.2 Objetivo

> Criar uma experiência financeira transparente, previsível e confiável.

### 13.3 Elementos obrigatórios de clareza

| Elemento | O que precisa comunicar |
|---|---|
| Saldo real | Valor disponível para apostar ou sacar. |
| Saldo bônus | Valor promocional e suas regras. |
| Saldo bloqueado | Por que está bloqueado e como liberar. |
| Saque | Status, prazo, método e eventual pendência. |
| Depósito | Método, confirmação e feedback. |
| Histórico | Transações, apostas, prêmios e movimentações. |
| Erros | Motivo e próximo passo. |
| KYC | O que falta, por que falta e como resolver. |

### 13.4 Princípio

A carteira deve ser **neutra entre cassino e esporte**. Ela é a infraestrutura comum da plataforma.

---

## 14. UX/UI de promoções e CRM

### 14.1 Responsabilidades

- Vitrine de promoções.
- Segmentação visual.
- Detalhes da campanha.
- Regras.
- Elegibilidade.
- Progresso.
- Banners.
- Mensagens in-app.
- Notificações.
- Campanhas de cassino.
- Campanhas de live casino.
- Campanhas esportivas.
- Campanhas híbridas.

### 14.2 Objetivo

> Ajudar a vender cassino, live casino e esporte sem gerar confusão, frustração ou percepção de engano.

### 14.3 Estrutura recomendada para uma promoção

Toda promoção deve responder claramente:

1. O que eu ganho?
2. O que preciso fazer?
3. Qual é o prazo?
4. Quais jogos, eventos ou mercados contam?
5. Existe rollover ou requisito?
6. Como acompanho meu progresso?
7. Como resgato?
8. Quais são as restrições principais?
9. Onde vejo os termos completos?

### 14.4 Segmentação por vertical

| Tipo | Exemplos |
|---|---|
| Cassino | Rodadas, campanhas de slots, missões, torneios. |
| Live casino | Game shows, roleta, rankings, cashback. |
| Esporte | Freebet permitida, odds aumentadas, múltiplas, eventos especiais. |
| Híbrida | Campanhas que conectam esporte e cassino com regras simples. |

### 14.5 Cuidados

- Não esconder termos.
- Não usar urgência falsa.
- Não misturar regras de cassino e esporte sem separação clara.
- Não criar banners com promessa ambígua.
- Não sobrecarregar a home com campanhas repetidas.

---

## 15. UX/UI de conta, segurança e KYC

### 15.1 Responsabilidades

- Cadastro.
- Login.
- Recuperação de senha.
- Dados pessoais.
- Reconhecimento facial, quando aplicável.
- Verificação documental.
- Autenticação.
- Dispositivos.
- Segurança da conta.
- Preferências.
- Bloqueios.
- Suporte.
- Mensagens de erro.

### 15.2 Objetivo

> Reduzir abandono sem fragilizar segurança.

### 15.3 Boas práticas

| Área | Boa prática |
|---|---|
| Cadastro | Pedir apenas o necessário no momento certo. |
| KYC | Explicar por que o dado é necessário. |
| Erros | Dizer o que aconteceu e como corrigir. |
| Segurança | Tornar ações críticas claras e confirmáveis. |
| Suporte | Ajudar antes que o usuário precise abrir chamado. |

---

## 16. UX/UI de jogo responsável

### 16.1 Responsabilidades

- Limites de depósito.
- Limites de gasto.
- Limites de tempo.
- Pausas.
- Autoexclusão.
- Histórico de atividade.
- Alertas de sessão.
- Mensagens preventivas.
- Acesso a ajuda.
- Ferramentas de controle.
- Sinais de comportamento de risco.

### 16.2 Objetivo

> Tornar proteção e controle fáceis de encontrar, fáceis de entender e difíceis de manipular contra o usuário.

### 16.3 Princípios

| Princípio | Aplicação |
|---|---|
| Fácil de encontrar | Jogo responsável deve aparecer em Conta, Carteira e momentos críticos. |
| Linguagem clara | Evitar juridiquês. |
| Sem dark patterns | Não dificultar limites, pausas ou autoexclusão. |
| Feedback imediato | Confirmar alterações e explicar efeitos. |
| Proteção contextual | Alertas no momento certo, não só em página isolada. |

### 16.4 Ferramentas esperadas

- Definir limite.
- Alterar limite.
- Pausar conta.
- Autoexcluir.
- Ver histórico.
- Consultar ajuda.
- Receber alertas.
- Entender riscos.

---

## 17. UI Design e design system

### 17.1 Objetivo

> Criar uma linguagem visual única, moderna, confiável e escalável para cassino, live casino, sportsbook, carteira, promoções e conta.

### 17.2 Componentes necessários

| Componente | Aplicação |
|---|---|
| Botões | CTAs gerais, jogar, apostar, depositar, sacar. |
| Cards de jogos | Cassino e live casino. |
| Cards de eventos | Sportsbook. |
| Botões de odds | Eventos e mercados esportivos. |
| Betslip | Seleções, valores e confirmação. |
| Modais | Depósito, saque, confirmação, erro. |
| Banners | Campanhas e destaques. |
| Tabs | Categorias, mercados, filtros. |
| Chips/filtros | Jogos, provedores, esportes, ligas. |
| Alerts | Odds alteradas, erro, sucesso, aviso regulatório. |
| Inputs | Cadastro, KYC, valores, busca. |
| Estados | Loading, vazio, erro, sucesso, indisponível. |
| Navegação | Bottom nav, menu, header, perfil. |

### 17.3 Camadas de identidade

A interface deve ter três camadas:

| Camada | Função |
|---|---|
| **Marca VDB** | Cores, tipografia, botões, ícones, tom visual e componentes. |
| **Vertical** | Diferenciar cassino, ao vivo, esportes, carteira e promoções. |
| **Contexto** | Adaptar experiência por comportamento, campanha, saldo, evento ou estágio do usuário. |

### 17.4 Cuidados de UI

- Evitar excesso de cores competindo.
- Garantir contraste e legibilidade.
- Não sacrificar acessibilidade por impacto visual.
- Criar hierarquia clara entre conteúdo, ação e dinheiro.
- Evitar interface “gritada” demais, que pode reduzir confiança.
- Garantir consistência entre mobile web, app e desktop, se aplicável.

---

## 18. UX Writing

### 18.1 Objetivo

> Reduzir dúvida, ansiedade, erro e suporte por meio de textos claros, diretos e responsáveis.

### 18.2 Áreas críticas

| Área | Por que é crítica |
|---|---|
| Saque | Usuário precisa confiar no prazo e no status. |
| Bônus | Regras confusas geram frustração. |
| Promoções | Ambiguidade vira reclamação. |
| Betslip | Erro pode gerar perda de confiança. |
| Odds | Mudança precisa ser compreensível. |
| KYC | Recusa de documento exige orientação clara. |
| Pix | Erro de pagamento precisa de ação recomendada. |
| Jogo responsável | Controle precisa ser simples e acolhedor. |

### 18.3 Exemplos de situações que exigem texto claro

| Situação | O texto precisa explicar |
|---|---|
| Odd mudou | O que mudou e qual ação o usuário pode tomar. |
| Mercado suspenso | Por que não é possível apostar agora. |
| Aposta recusada | Motivo e próximo passo. |
| Saque pendente | Status, prazo e possível pendência. |
| Bônus ativo | O que falta para liberar. |
| Jogo indisponível | Manutenção, restrição ou falha temporária. |
| Limite alterado | Quando passa a valer e qual efeito. |
| Autoexclusão | Consequências e duração. |

---

## 19. UX Research

### 19.1 Objetivo

> Separar opinião interna de evidência real de usuário.

### 19.2 Pesquisas recomendadas

| Pesquisa | Objetivo |
|---|---|
| Auditoria heurística | Encontrar problemas de navegação, clareza, consistência e confiança. |
| Teste de usabilidade atual | Ver onde usuários travam nos fluxos atuais. |
| Entrevistas com usuários | Entender motivação, hábitos, confiança e barreiras. |
| Análise de suporte | Mapear dúvidas recorrentes sobre saque, bônus, login e apostas. |
| Benchmark competitivo | Comparar jornadas com players líderes. |
| Card sorting | Validar categorias de cassino e navegação. |
| Tree testing | Validar arquitetura da informação. |
| Teste de protótipo | Medir compreensão antes de desenvolvimento. |
| Análise quantitativa | Usar funis e eventos para identificar abandono e oportunidade. |

### 19.3 Perguntas de pesquisa

- Por que usuários atuais escolhem a VDB?
- Quais jogos eles procuram primeiro?
- O que torna uma plataforma confiável para eles?
- Onde a carteira gera dúvida?
- O que impede parte da base de experimentar esporte?
- Como usuários entendem odds, betslip e múltiplas?
- O que faz um usuário abandonar o depósito?
- Quais promoções são compreendidas e quais geram confusão?
- Quais funcionalidades os usuários usam todo dia?
- Quais telas mais geram contato com suporte?

---

## 20. Benchmark competitivo

### 20.1 Como escolher os players

“Top 5 players” deve ser definido por critério. Pode significar:

- maior base ativa;
- maior GGR;
- maior tráfego;
- maior share of voice;
- melhor produto de cassino;
- melhor sportsbook;
- melhor app;
- melhor live casino;
- melhor CRM;
- melhor experiência de pagamento.

A recomendação é montar um benchmark com:

1. Players autorizados oficialmente.
2. Players com força de marca.
3. Players fortes em cassino.
4. Players fortes em sportsbook.
5. Players com boa experiência mobile.

A lista oficial da Fazenda deve ser a primeira referência para validar operadores autorizados.[^2]

### 20.2 Framework de análise

| Jornada | O que comparar |
|---|---|
| Home | Hierarquia, banners, módulos, personalização, saliência de esporte e cassino. |
| Cassino | Categorias, busca, favoritos, recentes, provedores, cards. |
| Live casino | Informação de mesa, status, filtros, entrada rápida. |
| Sportsbook | Eventos, odds, mercados, betslip, ao vivo, busca, favoritos. |
| Carteira | Depósito, saque, saldo, bônus, histórico, status. |
| Promoções | Clareza, segmentação, regras, progresso, termos. |
| Conta/KYC | Cadastro, verificação, erros, segurança. |
| Jogo responsável | Limites, autoexclusão, visibilidade, linguagem. |
| UI | Consistência, legibilidade, responsividade, performance percebida. |
| UX Writing | Clareza de mensagens críticas. |

### 20.3 Scorecard sugerido

| Critério | Peso | Nota VDB atual | Nota concorrente | Gap | Ação |
|---|---:|---:|---:|---|---|
| Home equilibrada | 10 |  |  |  |  |
| Cassino: descoberta | 10 |  |  |  |  |
| Live casino: clareza | 8 |  |  |  |  |
| Sportsbook: betslip | 10 |  |  |  |  |
| Carteira: confiança | 10 |  |  |  |  |
| Promoções: entendimento | 8 |  |  |  |  |
| Jogo responsável | 8 |  |  |  |  |
| Design system | 8 |  |  |  |  |
| Performance mobile | 10 |  |  |  |  |
| UX Writing | 8 |  |  |  |  |

---

## 21. Métricas do redesign

### 21.1 Métricas de cassino

- tempo até iniciar jogo;
- uso de favoritos;
- uso de recentes;
- taxa de busca com resultado;
- taxa de clique em jogos;
- abandono no carregamento;
- retenção de usuários de cassino;
- participação de live casino;
- reclamações sobre jogos indisponíveis;
- jogos iniciados por sessão.

### 21.2 Métricas de live casino

- entrada em mesa;
- abandono antes de carregar;
- troca de mesa;
- uso de filtros;
- clique em game shows;
- erro de stream;
- tempo até primeira aposta em live;
- retorno ao lobby.

### 21.3 Métricas de esporte

- usuários que acessam sportsbook;
- usuários que adicionam seleção ao betslip;
- conversão do betslip;
- primeira aposta esportiva;
- uso de apostas ao vivo;
- uso de busca por time/campeonato;
- uso de favoritos;
- repetição de aposta;
- abandono por etapa;
- usuários de cassino que experimentam esporte.

### 21.4 Métricas transversais

- conversão de cadastro;
- conversão de primeiro depósito;
- taxa de saque concluído;
- tempo percebido de saque;
- chamados de suporte;
- erros de Pix;
- entendimento de bônus;
- NPS/CSAT por jornada;
- uso de limites;
- autoexclusões;
- usuários híbridos;
- receita por vertical;
- retenção por cohort;
- impacto de promoções por vertical.

### 21.5 Métrica-chave para este momento

> Crescimento de usuários híbridos sem queda relevante na retenção de cassino.

---

## 22. Experimentação

### 22.1 Hipóteses prioritárias

| Hipótese | Como testar |
|---|---|
| Dar mais visibilidade a esporte aumenta ativação sem reduzir cassino. | Teste A/B de módulos esportivos na home. |
| Separar live casino melhora navegação. | Testar live como item próprio versus categoria dentro de cassino. |
| Melhor busca aumenta jogos iniciados. | Medir busca, clique, início de jogo e busca sem resultado. |
| Betslip mais simples aumenta conversão. | Testar versões do betslip. |
| Promoções segmentadas reduzem confusão. | Medir ativação, suporte e reclamações. |
| Favoritos aumentam retenção. | Medir retorno e frequência de uso. |
| Carteira mais clara reduz suporte. | Medir chamados sobre saldo, bônus e saque. |

### 22.2 Cuidados

- Não testar mudanças críticas sem controle de risco.
- Separar impacto por vertical.
- Medir efeitos colaterais em cassino ao introduzir esporte.
- Não otimizar apenas clique; medir qualidade, retenção e suporte.
- Validar compliance antes de testes com campanhas e incentivos.

---

## 23. Entregáveis esperados do UX/UI

### 23.1 Discovery

- Auditoria UX/UI da plataforma atual.
- Mapeamento de jornadas.
- Análise de dados.
- Análise de suporte.
- Benchmark competitivo.
- Pesquisa com usuários.
- Diagnóstico de problemas e oportunidades.

### 23.2 Estratégia

- Princípios de experiência.
- Nova arquitetura da informação.
- Mapa de perfis de usuário.
- Matriz de prioridades.
- Definição de métricas.
- Estratégia de home modular.
- Estratégia de crescimento de esporte sem perda em cassino.

### 23.3 Design

- Wireframes de baixa fidelidade.
- Protótipos navegáveis.
- UI final mobile-first.
- Design system.
- Componentes por vertical.
- Fluxos de carteira.
- Fluxos de promoção.
- Fluxos de jogo responsável.
- UX Writing.
- Estados de erro, loading, vazio e sucesso.

### 23.4 Handoff

- Especificação de componentes.
- Regras de responsividade.
- Critérios de aceite.
- Documentação de eventos de tracking.
- Checklist de compliance.
- Design QA.
- Registro de decisões.

---

## 24. Backlog inicial sugerido

### 24.1 Épicos P0

| Épico | Objetivo |
|---|---|
| Arquitetura e navegação | Criar equilíbrio entre cassino, live e esporte. |
| Home modular | Substituir home genérica por hub adaptável. |
| Carteira | Melhorar depósito, saque, saldo, bônus e histórico. |
| Cassino lobby | Melhorar descoberta, busca, favoritos e recentes. |
| Sportsbook básico competitivo | Melhorar home esportiva, eventos, odds e betslip. |
| Design system | Padronizar componentes e acelerar evolução. |
| Jogo responsável | Tornar limites, pausas e autoexclusão acessíveis. |

### 24.2 Épicos P1

| Épico | Objetivo |
|---|---|
| Live casino avançado | Melhorar informação de mesa e experiência ao vivo. |
| Promoções segmentadas | Separar campanhas por vertical e reduzir confusão. |
| Busca global | Encontrar jogos, eventos, times e promoções. |
| Personalização | Adaptar home por comportamento. |
| UX Writing crítico | Melhorar mensagens de saque, bônus, odds, erros e KYC. |

### 24.3 Épicos P2

| Épico | Objetivo |
|---|---|
| Recomendações | Personalizar jogos e eventos de forma responsável. |
| Educação esportiva | Guias contextuais para usuários de cassino experimentarem esporte. |
| Favoritos avançados | Times, ligas, jogos, provedores e mesas. |
| Central de histórico | Consolidar apostas, jogos, transações e promoções. |
| Painel de comportamento | Ajudar usuário a visualizar atividade e limites. |

---

## 25. Checklist de compliance aplicado à UX

### 25.1 Interface e comunicação

| Item | Checklist |
|---|---|
| Publicidade | Não sugere enriquecimento fácil. |
| Influenciadores | Campanhas precisam ser compatíveis com regras de publicidade responsável. |
| Bônus | Termos claros, requisitos visíveis e sem ambiguidade. |
| Saldo | Diferença clara entre dinheiro real, bônus e bloqueios. |
| Saque | Prazos, pendências e status claros. |
| Pagamento | Métodos permitidos e recusados explicados corretamente. |
| Jogo responsável | Limites e autoexclusão acessíveis. |
| Usuários vulneráveis | Evitar comunicação exploratória. |
| Odds e apostas | Confirmação clara em caso de alteração. |
| Dados pessoais | Linguagem clara sobre coleta e validação. |

### 25.2 Produto

| Item | Checklist |
|---|---|
| Jogos online | Apenas jogos certificados e permitidos. |
| Live casino | Estúdios e jogos com certificação aplicável. |
| Esportes | Eventos e modalidades permitidas. |
| P2P/fantasy/habilidade | Não tratar como jogo online autorizado quando vedado. |
| Pagamentos | Sem boleto, dinheiro, cripto, cartão de crédito ou pós-pago. |
| PLD/FT | Fluxos compatíveis com identificação, monitoramento e controle. |

---

## 26. Plano de trabalho recomendado

### Fase 1 — Diagnóstico

Duração sugerida: 2 a 4 semanas.

Entregas:

- auditoria UX/UI;
- análise de dados;
- análise de suporte;
- benchmark;
- mapa de jornadas;
- relatório de problemas;
- oportunidades priorizadas.

### Fase 2 — Estratégia e arquitetura

Duração sugerida: 2 a 3 semanas.

Entregas:

- nova arquitetura da informação;
- princípios de experiência;
- estrutura da home;
- estratégia por vertical;
- fluxos principais;
- definição de métricas.

### Fase 3 — Wireframes e testes

Duração sugerida: 3 a 5 semanas.

Entregas:

- wireframes mobile-first;
- protótipo navegável;
- teste com usuários;
- ajustes baseados em evidência;
- validação com produto, compliance e engenharia.

### Fase 4 — UI e design system

Duração sugerida: 4 a 8 semanas.

Entregas:

- design system;
- UI final;
- componentes por vertical;
- padrões de estados;
- documentação;
- handoff.

### Fase 5 — Construção e design QA

Duração sugerida: conforme engenharia.

Entregas:

- acompanhamento de implementação;
- QA visual;
- QA funcional;
- ajustes;
- validação de tracking;
- preparação de rollout.

### Fase 6 — Lançamento e otimização

Entregas:

- acompanhamento de métricas;
- testes A/B;
- correções rápidas;
- roadmap de evolução;
- relatório de impacto.

---

## 27. Agente de inteligência de mercado e produto

Como o objetivo maior é criar um agente com informações relevantes sobre o mercado, o redesign pode alimentar e ser alimentado por um agente interno.

### 27.1 Missão do agente

> Apoiar decisões de produto, UX, marketing, compliance e estratégia com informações atualizadas sobre mercado, regulação, concorrência, comportamento e oportunidades em iGaming no Brasil.

### 27.2 Blocos de conhecimento

| Bloco | Conteúdo |
|---|---|
| Regulação | Portarias, leis, agenda regulatória, lista de autorizadas, regras de pagamento, jogo responsável. |
| Mercado | Dados públicos, relatórios, GGR, CPFs, contas, bloqueios, tendências. |
| Concorrência | Benchmarks de UX, campanhas, navegação, sportsbook, cassino, live casino, pagamentos. |
| Produto VDB | Métricas internas, funis, problemas, hipóteses, decisões e backlog. |
| Usuários | Pesquisas, entrevistas, perfis, feedback, suporte e reclamações. |
| Compliance | Checklists, políticas, riscos de campanhas e boas práticas. |
| UX/UI | Design system, padrões, componentes, guidelines e resultados de testes. |

### 27.3 Fontes prioritárias

| Fonte | Uso |
|---|---|
| SPA/MF | Regulação, lista de autorizadas, orientações e agenda. |
| SIGAP / relatórios públicos | Indicadores de mercado regulado. |
| Diário Oficial da União | Portarias e normas novas. |
| Ministério do Esporte | Modalidades e regras de eventos esportivos. |
| Banco Central | Estudos de pagamentos e movimentações financeiras. |
| Anatel | Bloqueios de sites ilegais, quando aplicável. |
| Senacon / Ministério da Justiça | Consumidor, reclamações e proteção. |
| CONAR | Publicidade e autorregulação. |
| Dados internos VDB | Funis, retenção, conversão, suporte, CRM e comportamento. |
| Benchmark manual | Prints, fluxos e scorecards de concorrentes. |

### 27.4 Perguntas que o agente deve responder

- O que mudou na regulação esta semana?
- Quais mudanças afetam produto, UX, marketing ou compliance?
- Quais operadores foram autorizados, suspensos ou alteraram marcas?
- Quais riscos existem em uma campanha de cassino, esporte ou live casino?
- Quais concorrentes têm melhor home, carteira, cassino ou sportsbook?
- O que devemos observar nos top players?
- Quais fluxos da VDB têm mais atrito?
- Quais métricas indicam que esporte está crescendo sem prejudicar cassino?
- Quais componentes do design system precisam existir para cada vertical?
- Quais termos promocionais precisam de maior clareza?
- O que pode gerar risco de jogo problemático ou comunicação inadequada?

### 27.5 Templates de resposta do agente

#### Template — mudança regulatória

```markdown
## Mudança identificada

**Fonte:**  
**Data:**  
**Tema:**  
**Resumo:**  

## Impacto para VDB

| Área | Impacto |
|---|---|
| Produto |  |
| UX/UI |  |
| Marketing/CRM |  |
| Compliance |  |
| Engenharia |  |
| Dados |  |

## Ações recomendadas

1. 
2. 
3. 

## Riscos

- 

## Fontes

- 
```

#### Template — benchmark competitivo

```markdown
## Benchmark: [Player]

### Home

**Pontos fortes:**  
**Pontos fracos:**  
**Oportunidades para VDB:**  

### Cassino

**Pontos fortes:**  
**Pontos fracos:**  
**Oportunidades para VDB:**  

### Live casino

**Pontos fortes:**  
**Pontos fracos:**  
**Oportunidades para VDB:**  

### Sportsbook

**Pontos fortes:**  
**Pontos fracos:**  
**Oportunidades para VDB:**  

### Carteira

**Pontos fortes:**  
**Pontos fracos:**  
**Oportunidades para VDB:**  

### Nota geral

| Critério | Nota |
|---|---:|
| Home |  |
| Cassino |  |
| Live casino |  |
| Sportsbook |  |
| Carteira |  |
| Promoções |  |
| Jogo responsável |  |
```

#### Template — avaliação de campanha

```markdown
## Avaliação de campanha

**Campanha:**  
**Vertical:** Cassino / Live casino / Esporte / Híbrida  
**Público-alvo:**  
**Objetivo:**  

## Pontos de UX

- Clareza da oferta:
- Regras:
- CTA:
- Jornada:
- Risco de confusão:

## Pontos de compliance

- Comunicação responsável:
- Termos visíveis:
- Restrições:
- Risco de promessa indevida:
- Jogo responsável:

## Recomendação

Aprovada / Ajustar / Reprovar

## Ajustes necessários

1.
2.
3.
```

### 27.6 Guardrails do agente

O agente não deve:

- sugerir exploração de usuários vulneráveis;
- orientar práticas para burlar regulação;
- recomendar ocultação de saque, saldo, termos ou limites;
- criar comunicação que prometa ganho garantido;
- substituir compliance ou jurídico;
- usar dados internos sensíveis sem controle;
- tratar correlação como causalidade;
- usar fontes sem data e sem origem.

O agente deve:

- citar fontes;
- sinalizar incertezas;
- separar fato, inferência e recomendação;
- indicar impacto por área;
- manter histórico de decisões;
- preservar privacidade e segurança de dados.

---

## 28. Definição de sucesso

O redesign será bem-sucedido se a VDB conseguir:

1. Manter ou melhorar retenção de cassino.
2. Aumentar ativação de esporte.
3. Aumentar usuários híbridos.
4. Melhorar conversão de depósito.
5. Reduzir dúvidas sobre saque, bônus e saldo.
6. Melhorar conversão do betslip.
7. Reduzir atritos em KYC.
8. Melhorar percepção de confiança.
9. Aumentar uso de favoritos e recentes.
10. Reduzir suporte por problemas de compreensão.
11. Fortalecer compliance e jogo responsável na experiência.
12. Criar design system escalável.
13. Ser comparável aos melhores players em mobile, carteira, cassino, live casino e sportsbook.

---

## 29. Glossário rápido

| Termo | Significado |
|---|---|
| **iGaming** | Ecossistema de jogos e apostas online com dinheiro real. |
| **Sportsbook** | Produto de apostas esportivas. |
| **Cassino online** | Jogos online de quota fixa, como slots, crash e instant games, quando permitidos e certificados. |
| **Live casino** | Jogos com transmissão ao vivo, dealers ou estúdios, sujeitos a certificação. |
| **GGR** | Gross Gaming Revenue; receita bruta de jogo, geralmente apostas menos prêmios pagos. |
| **Betslip** | Bilhete de aposta esportiva. |
| **KYC** | Know Your Customer; processo de verificação de identidade. |
| **PLD/FT** | Prevenção à lavagem de dinheiro e financiamento do terrorismo. |
| **Autoexclusão** | Ferramenta em que o usuário se exclui de apostar por prazo definido ou indeterminado. |
| **Rollover** | Requisito de movimentação associado a bônus ou promoção. |
| **Cash out** | Retirada antecipada de uma aposta esportiva, quando disponível. |
| **Quota fixa** | Modalidade em que o fator de multiplicação do prêmio é definido no momento da aposta. |

---

## 30. Fontes e referências

[^1]: Ministério da Fazenda — Apostas de Quota Fixa. Página informa legalização, autorização prévia da SPA, operação nacional apenas por autorizadas desde 01/01/2025, limite de até três marcas por autorização e uso da extensão “.bet.br”. https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/apostas-de-quota-fixa

[^2]: Ministério da Fazenda — Lista de empresas autorizadas a ofertar apostas de quota fixa em âmbito nacional. Página atualizada em 06/05/2026. https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/lista-de-empresas

[^3]: Ministério da Fazenda / SPA — Panorama Periódico do Mercado Regulado de Apostas de Quota Fixa, dados de 1º de janeiro a 30 de dezembro de 2025. Indicadores: CPFs únicos, contas ativas, GGR, destinações legais e autoexclusões. https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/apresentacoes/apresentacao-spa-mf-relatorio-periodico-2026.pdf

[^4]: Ministério da Fazenda — Sistema de Gestão de Apostas, SIGAP. Página descreve o sistema como solução tecnológica para regulação, monitoramento e fiscalização do mercado de apostas. https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/sistema-de-gestao-de-apostas-sigap

[^5]: Ministério da Fazenda — Regras para transações de pagamento realizadas pelos operadores de apostas. Página informa métodos permitidos, métodos vedados, prazo de 120 minutos para pagamento de prêmios e segregação de recursos. https://www.gov.br/fazenda/pt-br/assuntos/noticias/2024/abril/fazenda-publica-regras-para-transacoes-de-pagamento-realizadas-pelos-operadores-de-apostas

[^6]: Ministério da Fazenda — Jogo Responsável. Página informa a Portaria SPA/MF nº 1.231/2024 e diretrizes para prevenir, identificar e tratar comportamentos problemáticos relacionados a apostas. https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/jogo-responsavel

[^7]: Ministério da Fazenda — Regras para jogos online e estúdios de jogos ao vivo. Página informa que jogos online devem ter caráter aleatório, gerador randômico, tabelas de pagamento antes da aposta, quota fixa e certificação. https://www.gov.br/fazenda/pt-br/assuntos/noticias/2024/julho/ministerio-da-fazenda-publica-portaria-com-regras-para-jogos-on-line

[^8]: Ministério da Fazenda — Agenda Regulatória SPA 2026–2027. Página indica revisão e complementação de marcos de autorização, fiscalização e sancionamento, além de temas como afiliados, terminais digitais físicos e monitoramento de perfis de risco. https://www.gov.br/fazenda/pt-br/composicao/orgaos/secretaria-de-premios-e-apostas/agenda-regulatoria/agenda-regulatoria-spa-2026-2027

---

## 31. Próximo passo recomendado

Para transformar este documento em plano executável, o próximo passo é criar três artefatos:

1. **Mapa de jornadas VDB**  
   Cadastro, depósito, cassino, live casino, esporte, saque, promoções, jogo responsável e suporte.

2. **Scorecard de benchmark dos top players**  
   Avaliação estruturada por jornada e critério, com prints, notas e oportunidades.

3. **Roadmap UX/UI do redesign**  
   Épicos, prioridades, dependências, métricas, owners e entregáveis por fase.
