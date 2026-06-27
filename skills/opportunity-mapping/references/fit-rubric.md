# Fit Rubric

A rubrica desta skill não pontua a **ideia** — pontua o **fit** entre fundador,
mercado e canal. É isso que a diferencia de `idea-validation` (que pontua uma ideia
já escolhida). Quatro componentes, 0–25 cada, total 100. Sempre **justificar a nota**
com 1–2 frases, nunca dar nota solta.

A regra de ouro: a mesma ideia tem fits diferentes para fundadores diferentes. Uma
ideia que tira 22 em Market Pull e 6 em Channel Fit **não é uma boa oportunidade para
este fundador** — é uma armadilha. A rubrica existe para expor essa armadilha, não
para escondê-la atrás de uma média alta.

## 1. Founder Fit (0–25)

O fundador tem vantagem injusta real aqui, e isso o ensina o que ele quer aprender?

- **0–5**: Sem vantagem nenhuma. O fundador entra como qualquer estranho. Não ensina
  nada que ele queira aprender.
- **6–10**: Interesse genuíno, mas vantagem fraca ou genérica. Curva de aprendizado
  longa antes de qualquer diferencial.
- **11–15**: Alguma expertise ou acesso relevante. Ensina algo útil, mas o diferencial
  do fundador não é claramente superior ao de um concorrente mediano.
- **16–20**: Vantagem injusta real (domínio, skill, experiência vivida) que poucos
  têm. Construir isso desenvolve exatamente a habilidade que o fundador quer.
- **21–25**: Vantagem injusta forte E rara E difícil de copiar, num espaço onde o
  fundador joga no próprio campo. O projeto é simultaneamente o produto, o portfólio
  e o curso que ele queria fazer.

**Sinais a procurar:** o fundador já fez isso antes? Tem acesso que outros não têm
(comunidade, dados, rede, experiência de domínio)? O que ele aprende construindo isso
é o que ele declarou querer aprender? Cuidado com "vantagem imaginada" — interesse não
é vantagem.

## 2. Channel Fit (0–25) — o eixo decisivo

Dado o alcance REAL do fundador hoje, este produto é descobrível por ele? A maioria
das ideias morre aqui, não no mérito da ideia.

- **0–5**: O único caminho de distribuição é um que o fundador não tem e não consegue
  construir (ex.: exige audiência grande que ele não tem, ou vendas que ele não fará).
  "Build it and they'll come."
- **6–10**: Canal existe mas é hostil ao perfil do fundador (ex.: exige cold outbound
  de quem odeia vender, ou YouTube de quem não fará vídeo). Atrito alto, compõe devagar.
- **11–15**: Canal plausível e compatível com o temperamento do fundador, mas sem
  vantagem de distribuição — ele compete por atenção em igualdade com todos.
- **16–20**: Canal claro, compatível com o que o fundador topa fazer, com algum motor
  de composição (SEO, conteúdo, comunidade, free-tool, loop de teardown). Descobrível
  sem audiência pré-existente.
- **21–25**: Canal onde o fundador tem vantagem de distribuição específica — uma
  comunidade onde ele já está, um ângulo de conteúdo que joga no forte dele, um loop
  em que construir o produto JÁ é o marketing. Distribuição e produto se reforçam.

**Sinais a procurar:** qual é o canal CONCRETO (não "marketing")? Este fundador
específico consegue trabalhá-lo hoje, com o alcance e o temperamento que tem? Há
composição (cada esforço deixa um ativo) ou é aluguel (parou, morreu)? **Se o melhor
canal exige algo que o fundador disse que não fará, a nota é baixa — sem exceção.**

## 3. Market Pull (0–25)

Existe dor real, frequente e cara o suficiente, num espaço com gente pra alcançar e
não saturado a ponto de sufocar um entrante solo?

- **0–5**: Solução à procura de problema. Sem sinal de dor. "Seria legal ter."
- **6–10**: Dor leve ou esporádica; ou mercado tão saturado que não há brecha para um
  entrante solo (red ocean com incumbentes financiados em paridade).
- **11–15**: Dor recorrente em nicho identificável, com workarounds visíveis
  (planilhas, gambiarras). Espaço ocupado mas com wedge possível.
- **16–20**: Dor frequente e custosa, gente já pagando por soluções parciais, e um
  ângulo de entrada não saturado (nicho, idioma, público desatendido).
- **21–25**: Dor aguda validada por uso ativo de alternativas inadequadas, comunidade
  reclamando publicamente, gasto comprovado — E o espaço tem uma fenda clara que os
  incumbentes não cobrem por restrição estrutural própria.

**Sinais a procurar:** reviews negativos de produtos adjacentes, threads de
reclamação, planilhas como concorrente real, produtos mortos (por que morreram?),
disposição a pagar sinalizada. Aplicar Mom Test: comportamento > opinião.

## 4. Build & Monetize Fit (0–25)

Dá pra construir um MVP excelente e focado, sozinho, com custo de operação compatível
com o que dá pra cobrar?

- **0–5**: Exige tech/capital/equipe que o fundador não tem; OU unit economics
  negativos (ex.: muita inferência LLM por usuário grátis); OU audiência sem disposição
  a pagar.
- **6–10**: Construível mas complexo (6+ meses solo) ou monetização distante (precisa
  escalar muito antes de faturar). Margem apertada.
- **11–15**: MVP focado em 1–2 meses solo com stack conhecida; modelo de receita
  plausível (freemium, SaaS, info-produto) mas pricing não validado.
- **16–20**: MVP excelente em semanas, custo de tooling baixo, e benchmark de pricing
  existe em produtos similares com público que paga. Margem saudável cedo.
- **21–25**: Construível e polível rápido com ferramentas prontas/IA-assistido, custo
  marginal quase zero, e múltiplos caminhos de receita (ex.: info-produto + ferramenta)
  com WTP já demonstrado no espaço.

**Para projeto solo / vibe coding:** este componente pesa mais — considerar custo de
inferência, complexidade de manutenção, e se "fazer MUITO bem feito" é viável sozinho.
Simplicidade focada vale mais que escopo amplo.

## Agregado e mapeamento para Verdict

Soma dos 4 componentes (0–100).

| Score | Verdict |
|---|---|
| 0–39 | **PASS** (não persiga — o fit não está aqui) |
| 40–64 | **EXPLORE FURTHER** (fit parcial; estreite ou reformule antes de comprometer) |
| 65–100 | **PURSUE** (fit forte; leve para `/market-research` e valide) |

**Para projeto pessoal / side project**, o threshold de `PURSUE` cai para **≥ 58** —
mas isso deve ser dito explicitamente no output, porque baixa a régua deliberadamente.

## Override obrigatório (a regra que define a skill)

**Se Channel Fit ≤ 8, o verdict máximo é EXPLORE FURTHER — independente do agregado.**
Uma ideia com Market Pull 24, Founder Fit 22, Build 20 e Channel Fit 6 soma 72, mas é
uma armadilha: produto excelente que ninguém vai descobrir. Nesse caso, o verdict é
EXPLORE FURTHER com a recomendação explícita: "o gargalo é distribuição, não a ideia —
ou resolva o canal, ou escolha outra oportunidade." Todo override deve ser explicado.

Vale também o override clássico: se qualquer componente é catastrófico (≤ 4) num
contexto que o torna fatal, o verdict pode ser PASS mesmo com agregado mais alto.

## Formato de output do score

```
**Fit Score — [nome da oportunidade]:**
- Founder Fit: 19/25 — [justificativa em 1 frase]
- Channel Fit: 21/25 — [justificativa em 1 frase]
- Market Pull: 16/25 — [justificativa em 1 frase]
- Build & Monetize Fit: 18/25 — [justificativa em 1 frase]
- **Total: 74/100 — PURSUE**

[Se houver override, declarar aqui e explicar.]
```

## Nota sobre rankear vários

No modo `explore`, pontue de forma rápida e comparável (uma linha por componente) para
8–12 oportunidades numa tabela, e aprofunde a justificativa só para as top 3–4. No
`focus`, pontue a fundo as 2–3 candidatas com evidência web. No `pressure-test`,
re-pontue a candidata única depois do ataque aos três eixos — a nota deve mudar se o
ataque revelou algo. Uma nota que não se move depois de um pressure-test honesto é
sinal de que o teste foi fraco.
