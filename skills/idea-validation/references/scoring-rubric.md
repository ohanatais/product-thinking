# Scoring Rubric

Rubrica para os 4 componentes do score. Cada componente vai de 0 a 25 (total 100). Sempre **justificar a nota** com 1-2 frases, não dar nota solta.

## 1. Demand (0-25)

Existe dor real, frequente e cara o suficiente para mover comportamento?

- **0-5**: Solução à procura de problema. Sem sinal de dor. "Seria legal ter."
- **6-10**: Dor existe mas é leve ou esporádica. Usuários convivem com ela.
- **11-15**: Dor recorrente em nicho identificado. Workarounds visíveis (planilhas, gambiarras, apps abertos em paralelo).
- **16-20**: Dor frequente, custosa, com gente já pagando por soluções parciais.
- **21-25**: Dor aguda, validada por uso ativo de alternativas inadequadas, comunidade reclamando publicamente, gasto comprovado.

**Sinais a procurar:** reviews negativos de produtos adjacentes ("eu queria que o Notion fizesse X"), threads em fóruns/Reddit, willingness to pay sinalizada, frequência de uso de alternativas.

## 2. Differentiation (0-25)

A ideia tem diferenciação defensável vs. o que existe, ou é só "mais um"?

- **0-5**: Replica produto existente sem ângulo novo. Late-mover sem vantagem.
- **6-10**: Pequena melhoria em produto existente. Fácil de copiar por incumbentes.
- **11-15**: Ângulo novo (público, UX, integração) mas defensibilidade fraca.
- **16-20**: Diferencial real (tech, dados, distribuição) com algum moat inicial.
- **21-25**: Wedge claro + caminho para defensibilidade (network effects, dados proprietários, switching cost alto).

**Sinais a procurar:** o que incumbentes (Notion, ChatGPT, etc) podem adicionar como feature em 1 sprint? Se sim, score baixo. Existe insight de mercado que os outros não têm?

## 3. Feasibility (0-25)

Dá pra construir um MVP que entrega valor, no nível de recurso disponível?

- **0-5**: Requer tech que não existe, ou equipe/capital que o usuário não tem.
- **6-10**: Tech existe mas integração é complexa. MVP demora 6+ meses solo.
- **11-15**: MVP factível em 2-3 meses solo com stack conhecida. Riscos técnicos médios.
- **16-20**: MVP em semanas, stack madura, riscos técnicos baixos.
- **21-25**: MVP em dias/poucas semanas, ferramentas prontas, low-code/no-code viável.

**Para vibe coding/projeto solo:** essa dimensão pesa mais. Considerar disponibilidade de APIs, custo de inferência LLM, complexidade de manutenção.

## 4. Monetization (0-25)

Existe caminho plausível para receita compatível com o custo de operar?

- **0-5**: Audiência sem disposição a pagar, custo unitário alto (ex: muita inferência LLM por usuário gratuito).
- **6-10**: Monetização possível mas longe (precisa escalar muito primeiro).
- **11-15**: Modelo plausível (freemium, SaaS) mas pricing não validado.
- **16-20**: Pricing benchmark existe em produtos similares, audiência paga.
- **21-25**: WTP comprovado, unit economics positivos desde cedo, múltiplos modelos viáveis.

**Para projeto pessoal sem objetivo comercial:** marcar como **N/A** e não somar no score. Total nesse caso é sobre 75. Indicar isso explicitamente.

## Agregado

Soma dos 4 (ou dos 3, se monetization for N/A).

## Mapeamento para Verdict

| Score (sobre 100) | Verdict |
|---|---|
| 0-39 | **KILL** |
| 40-64 | **VALIDATE FIRST** |
| 65-100 | **BUILD** |

| Score (sobre 75, projeto pessoal) | Verdict |
|---|---|
| 0-29 | **KILL** |
| 30-48 | **VALIDATE FIRST** |
| 49-75 | **BUILD** |

**Override permitido:** se um único componente é catastrófico (ex: Differentiation = 2 num mercado saturado), o verdict pode ser KILL mesmo com agregado mais alto. Override deve ser explicado.

## Formato de output do score

```
**Score:**
- Demand: 18/25 — [justificativa em 1 frase]
- Differentiation: 9/25 — [justificativa em 1 frase]
- Feasibility: 20/25 — [justificativa em 1 frase]
- Monetization: 12/25 — [justificativa em 1 frase]
- **Total: 59/100**

**Verdict: VALIDATE FIRST**
1. [Razão 1]
2. [Razão 2]
3. [Razão 3]
```
