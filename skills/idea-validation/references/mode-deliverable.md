# Mode: Deliverable

Modo `research` + formatação para audiência externa. Output destinado a cliente, stakeholder, investidor ou outro PM — não a si mesmo.

## Quando usar

- PM levando análise para um cliente.
- Decisão de portfólio em comitê.
- Avaliação de proposta de stakeholder externo.
- Documento que será lido por alguém que não acompanhou a conversa.

## Restrições

1. **Tudo do modo research vale** (cada claim com fonte, Mom Test, sem teatro de número).
2. **Linguagem ajustada à audiência**: menos primeira pessoa, mais voz neutra/profissional.
3. **Executive Summary obrigatório** no topo (não no fim).
4. **Apêndices** com dados brutos da pesquisa (links, citações, tabelas completas) ao final.
5. **Tom honesto, mas profissional**: a postura adversarial do modo quick vira "análise crítica fundamentada".

## Protocolo

Executar todo o protocolo do modo `research` (`references/mode-research.md`), e adicionar:

### Passo 0: Confirmar audiência e contexto

Antes de produzir o output, perguntar (ou inferir se óbvio):

1. Para quem vai este documento? (cliente, investidor, comitê interno)
2. Qual a decisão que precisa ser tomada com base nele?
3. Há restrições de extensão ou formato?
4. O documento será compartilhado em qual canal? (email, deck, doc compartilhado)

### Passo final: Reformatar para entregável

Estrutura de output:

```
# Análise de Viabilidade: [Nome do produto/ideia]

**Preparado por:** [PM]
**Data:** [data]
**Decisão suportada:** [qual decisão este documento sustenta]

## Executive Summary

[3-5 parágrafos]
- Recomendação clara: BUILD / VALIDATE FIRST / KILL
- Score agregado
- Top 3 razões
- Próximos passos sugeridos

## 1. Contexto e Ideia

[Reescrita em 1 frase + descrição estruturada]

## 2. Mapeamento Competitivo

[Tabela formatada profissionalmente]

## 3. Análise de Demanda

[Fatos com fontes em notas de rodapé ou links inline]

## 4. Viabilidade Técnica

[Análise]

## 5. Monetização e Modelo de Negócio

[Análise + benchmark]

## 6. Risk Register

[Tabela formal com Impact × Likelihood × Mitigação × Owner sugerido]

## 7. Score e Justificativa

[Componentes + total]

## 8. Recomendação

[Verdict com 3 razões fundamentadas]

## 9. Plano de Validação / Próximos Passos

[Ações concretas com responsável e prazo sugeridos]

## 10. Caminhos Alternativos (se aplicável)

[Pivot Paths: 2-3 reformulações da ideia se Verdict for KILL ou score baixo. Cada uma com: melhoria esperada, fundamento de mercado, trade-off. Pular se Verdict = BUILD com score forte.]

## 11. Perguntas Críticas Remanescentes

[Lista numerada]

## Apêndices

### A. Fontes consultadas
[Lista com links]

### B. Reviews e citações analisadas
[Citações relevantes com fonte]

### C. Pricing benchmark detalhado
[Tabela completa]
```

## Notas de formatação

- **Sem primeira pessoa** ("eu acho", "minha leitura") — usar "a análise sugere", "a evidência indica".
- **Sem gírias ou postura adversarial explícita** — manter rigor sem soar combativo.
- **Honestidade preservada**: se o verdict é KILL, o documento diz KILL. Apenas a embalagem muda, não a substância.
- Apêndices podem ser longos; o corpo principal deve caber em 2-4 páginas.

## Anti-padrões (não fazer)

- Não suavizar o verdict para agradar a audiência. Verdict é verdict.
- Não inflar com gráficos decorativos ou seções vazias para parecer robusto.
- Não esconder limitações da análise. Se a evidência é fraca em algum ponto, dizer.
- Não usar buzzwords sem ancoragem ("disrupção", "inovação", "transformação" sem definição operacional).
