# Mode: Research

Análise com busca web ativa. Cada claim sobre mercado tem fonte. Foco: gerar veredicto fundamentado, não relatório bonito.

## Restrições

1. **Toda afirmação sobre o mundo externo** (competidor, pricing, demanda, reviews, churn) precisa de citação web. Sem fonte → marca como `[Inferência]`.
2. **Mom Test obrigatório** na análise de reviews: descartar elogio genérico, priorizar comportamento e dor.
3. **Sem teatro de número**: TAM/SAM/SOM só com fonte direta. Se não houver, dizer "não disponível com confiança".
4. **Orçamento duro de buscas: 6-10 queries.** Cada busca com pergunta clara que ela responde. Acima de 10 só com sinalização explícita ao usuário. Princípio: mais busca não compensa, melhor sintetizar bem o que tem.
5. **Output enxuto.** Tabelas > prosa. Sem repetir o que já está claro. Meta: 2-3 telas de leitura.

## Protocolo

### Passo 1: Reformular a ideia em 1 frase
(Igual ao modo quick — `references/mode-quick.md`, passo 1.)

### Passo 2: Plano de pesquisa (mostrar ao usuário antes de buscar)

Listar 5-10 perguntas concretas que a pesquisa vai tentar responder. Exemplos:

1. Quem são os 3-5 competidores diretos? Quantos usuários têm?
2. Quais são as reclamações mais frequentes em reviews?
3. Qual o pricing benchmark em produtos similares?
4. Há sinais de churn ou pivot em incumbentes?
5. Qual o tamanho/dinâmica do nicho-alvo?
6. Existem produtos mortos no espaço? Por quê morreram?
7. Que tendências regulatórias/tech afetam isso?

Esse plano vira a espinha do relatório.

### Passo 3: Executar buscas

Princípios de busca:

- **Queries curtas**, 1-6 palavras, sem operadores especiais.
- **Buscar competidores específicos**, não conceitos vagos. "Reflect notes review" > "AI note taking apps".
- **Buscar churn/pivot/morte de produtos** no espaço. Aprender com mortos é metade do trabalho.
- **Buscar reviews em fontes de comportamento real**: G2, Product Hunt, Reddit, App Store reviews recentes.
- **Buscar pricing pages** diretamente quando relevante.

### Passo 4: Mapeamento competitivo

Estrutura (adaptada do framework oficial Anthropic, simplificada):

**Direct competitors:** mesmo problema, mesmo público, mesmo approach.
**Indirect competitors:** mesmo problema, approach diferente.
**Adjacent competitors:** podem entrar no espaço amanhã (Notion AI, ChatGPT custom GPTs, etc).
**Status quo / non-consumption:** o que as pessoas fazem hoje (planilha, paper, nada).

Para cada competidor relevante (3-7 no total):

| Competidor | Approach | Pricing | Sinais positivos | Sinais negativos | Fonte |
|---|---|---|---|---|---|

Sinais positivos = sinais de tração real (não marketing).
Sinais negativos = reclamações de usuário, churn, problemas estruturais.

### Passo 5: Análise de demanda real

Não confiar em "growing market" abstrato. Buscar:

- **Reviews de produtos adjacentes** onde usuários pedem o que sua ideia oferece. Citar com fonte.
- **Threads em Reddit/HN/Twitter** sobre a dor. Citar.
- **Search volume signals** (se conseguir indícios).
- **Comunidades pagas** existentes no espaço (sinal de WTP).

Aplicar Mom Test: separar opinião ("would love this") de comportamento ("eu pago $20/mês pelo X que não resolve Y").

### Passo 6: Análise de viabilidade técnica

Foco em:

- APIs/serviços externos necessários e custo (especialmente LLM, vector DB, etc).
- Riscos técnicos específicos (acurácia, latência, custo por usuário).
- Comparar com como competidores resolveram problemas similares.

### Passo 7: Análise de monetização

- Pricing benchmark com fontes (pricing pages dos competidores).
- Modelos viáveis (SaaS, freemium, one-time, etc).
- Unit economics se possível estimar com âncoras.
- Para projeto pessoal: marcar N/A se aplicável.

### Passo 8: Pre-mortem (5 min)

Imagine que daqui a 12 meses o projeto fracassou. Liste as 3 causas mais prováveis. Esse exercício alimenta o risk register.

### Passo 9: Score + Verdict + Risk register + Perguntas

Score com `scoring-rubric.md`.
Risk register obrigatório, 5-7 linhas no modo research.
Verdict com 3 razões fundamentadas (cada uma referenciando evidência da pesquisa).

Top 3 perguntas críticas remanescentes:

- O que **ainda** não dá pra saber sem entrevistar usuários reais?
- Quais hipóteses precisam de teste antes de qualquer commit grande?
- Que kill criteria adicionais devem ser monitorados?

## Estrutura de output (template)

```
## Validação Research: [Nome da ideia]

**Em uma frase:** [reescrita estruturada]

### Plano de pesquisa
[5-10 perguntas guiando a investigação]

### Mapeamento competitivo
[tabela]

### Demanda real
**Fatos:**
- [claim com fonte]
- [claim com fonte]

**Inferências:**
- [leitura minha]

### Viabilidade técnica
[análise]

### Monetização
[análise + pricing benchmark com fontes]

### Pre-mortem: as 3 causas mais prováveis de fracasso
1. ...
2. ...
3. ...

### Score
[componentes + total + justificativa por componente]

### Risk Register
[tabela 5-7 linhas]

### Verdict: [BUILD | VALIDATE FIRST | KILL]
1. [razão com referência à evidência]
2. ...
3. ...

### Top 3 perguntas críticas remanescentes
1. ...
2. ...
3. ...

### Pivot Paths (se Verdict = KILL ou score < 55)
**Pivot 1: [nome curto]**
- Melhora: [qual componente do score]
- Por quê: [razão ancorada na pesquisa]
- Trade-off: [o que se perde]

**Pivot 2: [nome curto]**
- ...

(Listar 2-3. Pular esta seção se Verdict = BUILD ou VALIDATE FIRST com score ≥ 55.)

### Plano de validação sugerido (se Verdict = VALIDATE FIRST ou BUILD)
[3-5 ações concretas: entrevistas, landing page test, pretotype, etc]
```

## Anti-padrões (não fazer)

- Não escrever sem fonte e marcar como fato. Inferência marcada está OK; "fato" sem fonte é proibido.
- Não fazer 30 buscas. Mais de 15 sem ganho marginal é desperdício; melhor pedir orientação ao usuário.
- Não copiar marketing dos competidores como se fosse análise. Buscar o que usuário fala, não o que vendedor fala.
- Não terminar em "interessante, mas precisa de mais pesquisa" sem dar verdict. Verdict é obrigatório.
