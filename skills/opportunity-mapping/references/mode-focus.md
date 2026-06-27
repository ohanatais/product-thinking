# Mode: Focus

Quando já há um campo ou 2–3 candidatas — de um `explore` anterior ou trazidas pelo
usuário — e é hora de afunilar com evidência real. Busca web ativa. Mapeia
concorrência, produtos mortos e realidade de canal de cada candidata, e estreita
iterativamente conforme o usuário reage. Função: ir de "algumas candidatas" para "a
escolhida", com fundamento.

## Restrições

1. **Toda afirmação sobre o mundo externo** (concorrente, pricing, demanda, canal,
   tração) precisa de fonte web. Sem fonte → marcar `[Inference]`.
2. **Mom Test obrigatório** ao analisar reviews/sinais: descartar elogio genérico,
   priorizar comportamento, dor e workarounds (planilhas = sinal forte).
3. **Sem teatro de número.** Tamanho de mercado só com fonte. Flag em receita
   autorrelatada ("self-reported").
4. **Output enxuto.** Tabelas > prosa. Meta: 2–3 telas.

## O convite de pesquisa profunda (característica desta skill)

O focus é onde a profundidade da pesquisa decide a qualidade. **Logo no início do
modo, avalie se a tarefa pede varredura ampla** (mapear concorrentes, mortos e canais
de várias candidatas costuma pedir). Se pedir, **pare e sinalize ao usuário** antes de
sair buscando:

> "Esta etapa fica muito mais forte com pesquisa profunda. Se você tiver o modo de
> pesquisa estendida disponível na interface, ative agora — vou fazer uma varredura
> ampla de concorrentes, produtos mortos e canais para as candidatas. Se preferir não
> ativar, sigo com busca web normal, que cobre o essencial com menos profundidade e
> menos fôlego de fontes. Qual você prefere?"

Notas sobre isso:
- O Claude **não consegue ativar** o modo de pesquisa estendida sozinho — é um controle
  do usuário. O papel da skill é sinalizar o melhor momento, não tentar acionar.
- A busca web normal (que o Claude dispara sozinho) cobre bem 6–15 buscas focadas. A
  pesquisa estendida faz dezenas e sintetiza — melhor para varreduras amplas.
- Se o usuário seguir sem o modo estendido, **não bloqueie**: faça a busca normal e
  nomeie o que ficou menos coberto.
- Respeite o controle do usuário e o tom das outras skills: oferecer, nomear o
  trade-off, não empurrar.

## Protocolo

### Passo 1: Confirmar as candidatas
Liste as 2–3 candidatas que entram no focus (do explore ou do usuário). Reafirme o
perfil do fundador em uma linha — o fit é sempre contra ele.

### Passo 2: Plano de pesquisa (mostrar antes de buscar)
5–10 perguntas concretas que a pesquisa vai responder, por candidata. Exemplos:
1. Quem são os 3–5 concorrentes diretos? Tração? Pricing?
2. Quais as reclamações recorrentes em reviews/threads?
3. Que produtos morreram neste espaço e por quê?
4. Qual o canal real de aquisição que funciona aqui para quem não tem audiência?
5. Há sinal de planilha/workaround (demanda não atendida)?
6. Pricing benchmark — o público paga?

Este plano vira a espinha do output. (É aqui, ou logo antes, que entra o convite de
pesquisa profunda do bloco acima.)

### Passo 3: Executar buscas
Princípios: queries curtas (1–6 palavras); buscar concorrentes específicos, não
conceitos; **buscar mortos/pivôs** (metade do aprendizado); buscar reviews
comportamentais (G2, Product Hunt, Reddit, IH, HN); buscar pricing pages diretas.
Aplicar Mom Test a tudo.

### Passo 4: Mapa competitivo por candidata
| Player | Tipo | Approach | Pricing | Tração (flag) | Gaps | Fonte |
|---|---|---|---|---|---|---|
Tipos: Direto / Indireto / Adjacente / Status quo. Status quo (planilha, nada) é
frequentemente o concorrente real.

### Passo 5: Realidade de canal por candidata
A pergunta que o focus existe para responder com evidência: **dado o alcance do
fundador, este produto é descobrível?** Busque casos reais de solo founders que
cresceram algo parecido partindo de zero audiência — que canal usaram, quanto demorou,
que MRR atingiram (flag self-reported). Isto alimenta o Channel Fit com fato, não
suposição.

### Passo 6: Pre-mortem por candidata (rápido)
Daqui a 12 meses, esta falhou. As 3 causas mais prováveis. Alimenta o risk e o score.

### Passo 7: Re-pontuar com a `fit-rubric.md`
Agora com evidência. As notas DEVEM mudar em relação ao explore se a pesquisa revelou
algo — Channel Fit e Market Pull especialmente. Aplique o override de Channel Fit.

### Passo 8: Estreitar e decidir
Ranking final das candidatas. Recomende a top 1 (ou diga "empate, e o desempate é X").
Se o usuário reagir e estreitar mais, itere — o focus é iterativo por natureza.

## Estrutura de output (template)

```
## Focus: [candidatas]

*Perfil do fundador (1 linha). Fit é sempre contra isso.*

### Plano de pesquisa
[5–10 perguntas]
[+ convite de pesquisa profunda, se aplicável]

### Por candidata
**[Candidata A]**
- Mapa competitivo [tabela]
- Realidade de canal [fato + fonte]
- Pre-mortem: [3 causas]
- **Fit Score** [4 componentes + total + verdict, com override se houver]

[repetir por candidata]

### Ranking e recomendação
[top 1 com 3 razões fundamentadas em evidência; ou empate + desempate]

### Próximo passo
[/market-research na escolhida, OU pressure-test se o usuário quer estressar antes de
comprometer, OU voltar ao explore se nenhuma passou]
```

## Anti-padrões (não fazer)
- Não marcar como "fato" o que não tem fonte. Inferência marcada está ok.
- Não fazer 30 buscas no modo normal sem ganho — se precisar de varredura ampla,
  é sinal de que o convite de pesquisa profunda deveria ter sido feito.
- Não copiar marketing de concorrente como análise — buscar o que o usuário fala.
- Não terminar sem ranking e recomendação. Empate é resposta; "precisa de mais
  pesquisa" sem veredito não é.
- Não deixar o Channel Fit como suposição quando há evidência de canal disponível.
