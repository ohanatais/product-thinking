# Guia: Product Thinking antes de codar

> Este guia é lido dentro do Claude Code — ou em qualquer leitor Markdown.
> Cada módulo leva entre 20 e 60 minutos. Você pode parar e continuar de onde parou.

---

## Por que este guia existe

A maioria dos tutoriais de "construa com IA" começa no código.

Você instala o Claude Code, assiste um vídeo de 10 minutos, e começa a buildar. Uma semana depois tem um MVP rodando. Dois meses depois percebe que construiu a coisa certa para as pessoas erradas — ou a coisa errada para todo mundo.

Este guia existe para o que vem antes disso.

Não é sobre instalar ferramentas. É sobre as perguntas que, se respondidas antes da primeira linha de código, mudam completamente o que você constrói — e se vale a pena construir.

---

## O que você vai aprender

Cada módulo cobre uma etapa da jornada de produto. A ordem importa: cada resposta informa a próxima pergunta.

| Módulo | Pergunta central | Skill |
|---|---|---|
| [1. Pesquisa de mercado](#módulo-1-pesquisa-de-mercado) | O mercado existe? Quem mais está aqui? | `/market-research` |
| [2. Validação de ideia](#módulo-2-validação-de-ideia) | Essa ideia vale o esforço de construir? | `/validate-idea` |
| [3. Personas](#módulo-3-personas) | Para quem exatamente estou construindo? | `/personas` |
| [4. Posicionamento](#módulo-4-posicionamento) | Por que alguém escolheria isso, e não o resto? | `/positioning` |
| [5. PRD](#módulo-5-prd) | O que exatamente vou construir primeiro? | `/prd` |

Você não precisa usar as skills para seguir os guias. Mas as skills fazem o trabalho junto com você — dentro do Claude Code, no idioma que você falar.

---

## Como usar este guia

**Se você está começando do zero:** siga os módulos em ordem. Cada um tem uma seção de leitura (~10 min) e uma seção de prática (~20–40 min com a skill correspondente).

**Se você já está no meio do processo:** pule para o módulo onde está. Mas se algo parece confuso downstream, a resposta quase sempre está numa etapa que você pulou upstream.

**Se você quer só as skills:** cada módulo tem instruções de instalação e uso da skill correspondente. Você não precisa ler o guia inteiro.

---

## Módulo 1: Pesquisa de mercado

### O que é e por que importa

Pesquisa de mercado não é sobre confirmar que sua ideia é boa. É sobre entender o terreno antes de se comprometer com ele.

Quando você pesquisa um mercado, está respondendo três perguntas:

1. **Quem mais está aqui?** — concorrentes diretos, indiretos, adjacentes, e o status quo (o que as pessoas fazem hoje sem nenhuma ferramenta)
2. **O espaço está lotado ou há lugar?** — oceano vermelho vs. oceano azul, e se há um nicho que ainda não foi bem servido
3. **O mercado existe?** — há evidência de que pessoas estão ativamente procurando uma solução para esse problema, ou é um problema que você assumiu que existe?

### O erro mais comum

A maioria das pessoas pesquisa para confirmar o que já acredita. Procura dados que apoiam a ideia, ignora os que contradizem, e conclui que o mercado existe porque encontrou algumas pessoas com o problema.

O objetivo da pesquisa é o oposto: encontrar a evidência que derrubaria a ideia. Se você pesquisar honestamente e ela sobreviver, você tem algo.

### O que é oceano vermelho vs. azul

**Oceano vermelho:** muitos concorrentes brigando pelos mesmos clientes com produtos similares. A competição é feroz porque todo mundo está no mesmo espaço.

**Oceano azul:** um espaço onde há oportunidade real — um público mal servido, uma necessidade não atendida, ou uma combinação que ninguém fez ainda.

A maioria dos produtos está em algum ponto entre os dois. A pergunta útil não é "vermelho ou azul?" — é "há um nicho específico onde este produto teria uma vantagem clara sobre tudo que existe?"

### O que fazer agora

Instale a skill de pesquisa de mercado e rode `/market-research` com a descrição da sua ideia.

```bash
# Copiar para o seu projeto
cp -r path/to/pm-skills/market-research .claude/skills/

# No Claude Code:
/market-research
```

A skill vai perguntar seu nível de familiaridade com pesquisa de mercado e adaptar a profundidade da análise. Se for a primeira vez: modo guiado, com explicação de cada passo. Se você já sabe o que quer: vai direto à análise.

**O que você vai ter no final:** um mapa de quem está no espaço, um dimensionamento de mercado honesto (TAM/SAM/SOM), uma leitura de oceano, e uma implicação estratégica clara.

---

## Módulo 2: Validação de ideia

### O que é e por que importa

Pesquisa de mercado mapeia o terreno. Validação de ideia testa se a sua ideia específica tem fit com esse terreno.

São coisas diferentes. Um mercado grande com demanda comprovada não significa que *sua versão* do produto vai funcionar. Validação é sobre encontrar a suposição mais arriscada por baixo da ideia — a que, se estiver errada, muda tudo — e testá-la antes de construir.

### A diferença entre validação e feedback

"Eu mostrei pra cinco pessoas e todas adoraram."

Isso não é validação. Pessoas são educadas. Amigos e família são ainda mais. Elas dizem o que você quer ouvir, especialmente quando você está empolgado.

Validação real se parece com comportamento: alguém pagou por algo parecido. Alguém construiu uma gambiarra para resolver isso. Alguém reclamou especificamente desse problema em um fórum, sem saber que você estava ouvindo.

Opinião é fraca. Comportamento é forte. (Isso é a essência do Mom Test, do Rob Fitzpatrick.)

### O que é o Mom Test

O Mom Test é uma forma de fazer perguntas que revela comportamento real, não opiniões polidas.

A regra central: nunca pergunte o que as pessoas *fariam* — pergunte o que elas *fizeram*.

- ❌ "Você usaria um app que faz X?"
- ✅ "Como você lida com X hoje? Me conta uma situação recente."

A segunda pergunta revela o que a pessoa realmente faz, quanto o problema dói, e o que ela considera "bom o suficiente" hoje.

### O que fazer agora

```bash
cp -r path/to/pm-skills/validate-idea .claude/skills/

# No Claude Code:
/validate-idea
```

A skill tem três modos: **quick** (reação inicial sem pesquisa web), **research** (análise com buscas e fontes), e **deliverable** (output formatado para stakeholders).

Se você já tem pesquisa de mercado feita: compartilhe os documentos no início da sessão. A skill vai usá-los como evidência em vez de repetir o que já foi feito.

**O que você vai ter no final:** um score de 0–100 em quatro dimensões (demanda, diferenciação, viabilidade, monetização), um veredicto (Build / Validate First / Kill), um registro de riscos, e — se o veredicto for negativo — caminhos de pivô concretos.

---

## Módulo 3: Personas

### O que é e por que importa

Persona não é um cartão de perfil. Não é "mulher, 28 anos, PM em São Paulo, gosta de produtividade."

Isso não informa nenhuma decisão de produto.

Uma persona útil responde: **que trabalho essa pessoa está tentando realizar, e o que faria ela mudar o comportamento atual para usar algo novo?**

Essa é a diferença entre construir para um arquétipo e construir para um comportamento.

### O framework JTBD (Jobs to Be Done)

Jobs to Be Done é uma forma de entender por que pessoas "contratam" produtos — não quem elas são demograficamente, mas que progresso estão tentando fazer.

O formato de job statement: **"Quando [situação], quero [motivação], para que eu possa [resultado]."**

- ❌ "Quero um app de notas melhor."
- ✅ "Quando estou no fim do trimestre e preciso justificar meu trabalho pro gestor, quero ter um registro organizado do que fiz com contexto real, para que eu não passe 3 horas recompilando do zero e pareça mais preparada do que sinto que sou."

O segundo é um job statement. O primeiro é uma categoria de produto.

### O momento de gatilho

O elemento mais importante de uma persona não é o perfil — é o momento de gatilho.

O momento de gatilho é o evento específico — não um sentimento, um evento — que faz alguém passar de "isso é irritante" para "preciso encontrar uma solução agora."

Sem o gatilho, você não sabe quando seu usuário está pronto para ser alcançado nem o que o faz agir.

### O que a gambiarra revela

O que a pessoa faz hoje, sem o seu produto, é a sua concorrência real.

Não o Notion. Não o líder de categoria. A planilha específica que ela montou, o grupo de WhatsApp onde anota as coisas, ou a decisão de simplesmente não resolver o problema.

A gambiarra mostra quanto o problema dói (ela já faz esforço extra), o custo de troca (quanto mais elaborada, mais difícil mudar), e o benchmark de "bom o suficiente".

### O que fazer agora

```bash
cp -r path/to/pm-skills/personas .claude/skills/

# No Claude Code:
/personas
```

A skill detecta o que você tem: se tem entrevistas ou dados de usuários reais → modo comportamental. Se tem só hipóteses → modo hipótese (que torna suas suposições explícitas e testáveis). Se é a primeira vez → modo guiado.

**O que você vai ter no final:** 1–3 personas com job statement, momento de gatilho, gambiarra atual, dores comportamentais (não genéricas), e — para cada suposição sem evidência — uma nota do que precisaria ser validado.

---

## Módulo 4: Posicionamento

### O que é e por que importa

Posicionamento não é tagline. Não é missão. Não é lista de features.

É a resposta para: num mundo onde essas alternativas existem, por que alguém que se importa profundamente com [esse valor específico] escolheria este produto?

Sem uma resposta clara para isso, o seu copy vai soar genérico, a sua landing page vai parecer igual a dez outras, e os primeiros usuários vão entrar sem entender o que faz o produto ser diferente.

### O framework Dunford (cinco componentes)

April Dunford, em *Obviously Awesome*, define posicionamento em cinco componentes — sempre nessa ordem:

```
1. Alternativas competitivas   →  O que o cliente usa se isso não existir?
2. Atributos únicos            →  O que este produto tem que as alternativas não têm?
3. Valor                       →  O que esses atributos significam para a vida do cliente?
4. Clientes ideais             →  Quem mais se importa com esse valor específico?
5. Categoria de mercado        →  Qual frame torna esse valor óbvio?
```

A ordem é inegociável. Cada componente depende do anterior. Pule um e o posicionamento desmorona.

### A pergunta "e daí?"

Depois de cada atributo único, sempre pergunte: "e daí? O que isso significa para a vida do cliente?"

Só quando você chega numa resposta que faz alguém pensar "sim, é exatamente isso que eu preciso" — isso é o valor.

- Atributo: "Funciona offline"
- E daí? → "Você não perde trabalho quando a conexão cai"
- E daí? → "Você pode trabalhar em avião, porão, área rural sem ansiedade"
- Valor: "Confiabilidade que não depende da sua conexão"

O valor é o que o cliente compra. O atributo é o que o engenheiro constrói.

### Pré-PMF: rede grande, não rede de atum

Dunford é explícita: antes de product-market fit, mantenha o posicionamento **frouxo como uma rede grande**. Não se especialize antes de ver padrões reais de quem ama o produto e por quê.

O posicionamento que você produz aqui é uma tese — a melhor hipótese com as evidências que você tem. Não é uma declaração final.

### O que fazer agora

```bash
cp -r path/to/pm-skills/positioning .claude/skills/

# No Claude Code:
/positioning
```

A skill tem três modos: **guiado** (primeira vez, explica cada componente), **canvas** (tem personas e pesquisa, quer o canvas direto), e **stress-test** (tem posicionamento existente, quer encontrar fraquezas).

**O que você vai ter no final:** um canvas de cinco componentes preenchido, um positioning statement (para alinhamento interno, não para marketing), o que o posicionamento descarta, e as questões abertas que mudariam tudo se respondidas diferente.

---

## Módulo 5: PRD

### O que é e por que importa

O PRD — Product Requirements Document — responde: o que exatamente estou construindo, para quem, e por que esta versão (e não outra) faz sentido construir primeiro?

Para um builder solo, o PRD tem uma função que vai além de documentação: **contenção de escopo**. Cada feature que você adiciona ao MVP é uma semana de build que você não vai recuperar. Cada feature que você adia é uma semana de aprendizado que talvez consiga.

### O PRD solo builder vs. o PRD corporativo

Não é o mesmo documento.

O PRD corporativo tem 9+ seções, jornadas de usuário, épicos, glossário, publica no Confluence para alinhar equipes de 20 pessoas.

O PRD solo builder tem 4 seções, cabe numa única página, vive no repositório como `.md`, e é lido pelo Claude Code no início de cada sessão de build.

### As quatro seções — sempre as quatro

1. **Problema** — quem tem, o que o gatilha, o que a pessoa faz hoje
2. **Solução** — o que o produto faz, para quem, e por que essa versão
3. **Escopo do MVP** — exatamente o que está dentro — observável pelo usuário, sem detalhe técnico
4. **Fora do escopo** — exatamente o que não está nesta versão, com um motivo

A seção 4 é obrigatória. Um PRD sem out-of-scope explícito é um convite para construir tudo.

### O PRD como contexto do Claude Code

No início de cada sessão de build:

> "Aqui está o PRD do projeto: [cola o PRD]. Hoje estamos construindo [capacidade X da seção 3]. [Item Y da seção 4] está explicitamente fora do escopo."

Isso evita que o Claude Code adicione features não solicitadas, tome decisões arquiteturais por suposição, ou construa uma versão que não corresponde ao escopo validado.

### O que fazer agora

```bash
cp -r path/to/pm-skills/prd .claude/skills/

# No Claude Code:
/prd
```

A skill vai checar o que você já tem (personas, posicionamento, validação) e usar como base. Se não tiver nada, faz uma pergunta só: "Me conta em 2–3 frases: para quem é, qual o problema, e o que o MVP faz."

**O que você vai ter no final:** um PRD de 4 seções, pronto para ser usado como contexto em cada sessão de build com o Claude Code.

---

## Próximos passos

Com o PRD pronto, você tem tudo que precisa para começar a construir de forma informada.

O que vem depois deste repositório:

- **[build-with-claude](https://github.com/ohanatais/build-with-claude)** — Claude Code para não-técnicos: cada decisão técnica explicada, setup de ferramentas passo a passo, como trabalhar feature por feature
- **[brand-and-copy](https://github.com/ohanatais/brand-and-copy)** — identidade visual, tom de voz, copy de produto
- **[go-to-market](https://github.com/ohanatais/go-to-market)** — estratégia de lançamento, canais, primeiros usuários

---

*Feito por [Ohana Taís](https://github.com/ohanatais) — Senior PM, construindo em público.*
*Parte do ecossistema [build-from-zero](https://github.com/ohanatais/build-from-zero).*
