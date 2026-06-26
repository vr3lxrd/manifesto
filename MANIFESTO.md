# Manifesto sobre uso de LLMs como ferramentas de ultra-produtividade

## Sumário

1. [Por que escrever um manifesto?](https://app.notion.com/p/Por-que-escrever-um-manifesto-37f20098f51580eb98f9fc933554bdce?pvs=21) 
2. [Qual é o estado atual das IAs?](https://app.notion.com/p/Qual-o-estado-atual-das-IAs-38020098f5158088a56df964e5693d77?pvs=21) 
3. [E o que isso tem a ver comigo e com o banco?](https://app.notion.com/p/E-o-que-isso-tem-a-ver-comigo-e-com-o-banco-38020098f51580d1b6efeec1d3965559?pvs=21) 
4. [Boas práticas](https://app.notion.com/p/Boas-pr-ticas-38020098f515800eaaf1dfb2ee2afa17?pvs=21) 
    1. [Trending na comunidade](https://app.notion.com/p/Trending-na-comunidade-38020098f515800db1a8f525c4368480?pvs=21) 
        1. [Glossário](https://app.notion.com/p/Gloss-rio-37f20098f51580289a2ac3ab033cd61d?pvs=21) 
        2. [Spec-Driven Development e suas ramificações](https://app.notion.com/p/Spec-Driven-Development-e-suas-ramifica-es-38020098f5158024a7aadee4b0412996?pvs=21) 
        3. [Karpathy](https://app.notion.com/p/Karpathy-38020098f5158059b620d8997c45247b?pvs=21) 
        4. [O problema da complexidade](https://app.notion.com/p/O-problema-da-complexidade-38020098f5158053afede1bc032a3e90?pvs=21) 
        5. [Cautela com o que seguir](https://app.notion.com/p/Cautela-com-o-que-seguir-38020098f5158075bc75dab187db05aa?pvs=21) 
    2. [Minha contribuição para o Inner Source e algumas dicas pessoais](https://app.notion.com/p/Minha-contribui-o-para-o-Inner-Source-e-algumas-dicas-pessoais-38020098f515803eb22de7b3786996b3?pvs=21) 
    3. [Links relevantes](https://app.notion.com/p/Links-relevantes-38020098f51580f484ebc9bbfc1bb320?pvs=21) 

## Por que escrever um manifesto?

Não é sempre que inventamos uma roda, mas de vez em quando passamos pela invenção de um motor a vapor ou de um tear mecânico. Essas evoluções tecnológicas foram altamente disruptivas e representaram uma grande mudança na organização estrutural do trabalho e consequentemente da sociedade como um todo. É fácil entender a relação apresentada aqui: as LLMs (genericamente chamadas de “IAs”) chegam com o mesmo impacto destrutivo no modelo de trabalho atual e principalmente, no que chamo de “trabalho de escritório”. O trabalho de escritório é em sua grande maioria baseado na informática/computação, surgiu com o início da Quarta Revolução Industrial – mesmo que a sua profissão base não tenha surgido necessariamente junto com os computadores, como as ciências contábeis – e essa relação é o que importa para este contexto.

É complicado especular qual será o estado final da computação, mas entendo que é impossível remar contra a maré tecnológica e principalmente, corporativa. Promessas de produtividade nas alturas, do engenheiro 10x e de um funcionário trabalhando 24/7 fazem brilhar os olhos do capital, mas precisamos ter cautela e principalmente muita vontade de estudar para entender esse mercado que precisa vender produtos para recuperar os investimentos trilionários que receberam nos últimos anos [[ref](https://forbes.com.br/forbes-tech/2025/12/os-maiores-acordos-do-mundo-da-ia-em-2025/)]. Vejo como perigoso a ideia de que podemos ter um agent autônomo fazendo o mesmo que um ser humano apenas com alguns arquivos markdown, não apenas pela ótica social mas também pela viabilidade tecnológica de algo desse tipo. O ganho prometido de produtividade usando LLMs é tão alto que chega a assustar, vislumbrar, mas uma questão relevante que vou trabalhar nesse texto é: o que é essa suposta produtividade? Como ficar mais produtivo com uma IA?

Agora chegamos na pergunta: Por que escrever um manifesto? Minha resposta é a seguinte: precisamos estabelecer entre nossos pares e lideranças conversas recorrentes e com visões embasadas na prática do dia a dia e com o que o mercado/comunidade open source tem de melhor para **alinharmos as expectativas sobre o que essa ferramenta pode nos oferecer**, usarmos a IA de forma consciente e evitar erros graves de entendimento. Além disso, considero importante desmistificar algumas ideias vendidas aos montes nas redes sociais e desmontar viéses que chegam como vicios do trabalho corporativo e que não devemos levar em consideração. A consultora global Gartner desenvolveu um modelo gráfico chamado “Hype Cycle”, que tem como objetivo mapear fases de adoção de uma tecnologia emergente. Na minha opinião, hoje estamos dentro do banco na fase “ápice das expectativas infladas” – o nome é autoexplicativo, porém recomendo a leitura completa desse resumo sobre o Hype Cycle [[ref](https://www.gartner.com/en/research/methodologies/gartner-hype-cycle)].

Gostaria de pontuar que escrevo como Engenheiro de Software e por isso não entrarei em detalhes ao longo do resto do texto sobre quaisquer outras implicações que não envolvam diretamente o meu trabalho. Nos ultimos 6 meses eu venho testando diversas formas de integrar essa ferramenta maravilhosa – este elogio vem como um segundo disclaimer: minhas críticas nos parágrafos anteriores são baseadas em uma visão realista de quem a usa no dia a dia e já abraçou essa revolução – e gostaria de apresentar aos colegas minha visão de como devemos tratar as IAs, LLMs, Agents, Desenvolvedores Autônomos, etc.

## Qual é o estado atual das IAs?

Já está inteirado sobre as tecnologia mais recentes? Pule para o próximo tópico [E o que isso tem a ver comigo e com o banco?](https://app.notion.com/p/E-o-que-isso-tem-a-ver-comigo-e-com-o-banco-38020098f51580d1b6efeec1d3965559?pvs=21) 

Se você testou os primeiros modelos GPT ou o autocomplete do Github Copilot alguns anos atrás e concluiu que não era uma boa ferramenta, provavelmente você é uma pessoa sã e racional. Agora, se você nunca mais teve no mínimo a curiosidade de testar os “Frontier Models” de 2025 para cá, ai sim é um problema. A evolução dos modelos de IA não ocorreram apenas na quantidade de usuários fruto de um marketing acelerado, a qualidade de treinamento e os investimentos em pesquisa e hardware fizeram com que, em escala comercial, cada usuário tivesse acesso à modelos espetaculares. Na minha opinião, para o desenvolvimento de software, o conceito de “agente” foi a grande virada de chave, workflow muito diferente daquele de jogar um texto no chat e esperar uma resposta.

Ao trabalhar com agents, o seu codebase e/ou seu contexto de trabalho está ao alcance da IA, contando com diversas ferramentas que possibilitam ao mesmo tempo dar autonomia e controlar com rédeas curtas (ou frouxas, como preferir) para um modelo. Você pode pedir que o agent procure pela causa raiz de um bug específico, dando liberdade de leitura dos logs do container, avaliando diversas classes, funções e arquivos em paralelo, propondo assim uma solução que deve ser aprovada pelo usuário. Alternativamente, pode pedir para que o agent melhore seu coverage de testes unitários, possibilitando que ele rode comandos no seu terminal para validar o próprio trabalho e só pare quando atingir a meta. Esse não é o “vibecode” que ficou popular em 2025, esse modelo de trabalho é conhecido como programação agêntica e ele espera que você entenda o que está acontecendo por debaixo dos panos.

Alguns dos principais players da programação agêntica do mercado hoje são: Claude Code (Anthropic), Codex (OpenAI), Cursor e Github Copilot, mas obviamente a variedade é muito grande. O primeiro ponto que quero trazer é: **testem**. Não repitam opiniões e jargões de outras pessoas, evitem preconceitos e testem todos os modelos disponíveis, softwares especializados e formas de trabalhar/workflows. Não fiquem presos no primeiro sucesso ou na primeira falha, insista.

## E o que isso tem a ver comigo e com o banco?

O segundo ponto e pra mim o mais importante é: **não existe um jeito “certo” de trabalhar com a IA, por isso a experimentação, o estudo e a prática são tão importantes nesse momento.** Obviamente podemos falar de guidelines, guardrails que no geral são [Boas práticas](https://app.notion.com/p/Boas-pr-ticas-38020098f515800eaaf1dfb2ee2afa17?pvs=21), mas é importante evitarmos definir leis escritas em pedra, obrigatoriedades e padrões rígidos de uso, até por que a magia está nisso: a customização dos agentes é tão flexível que permite que cada pessoa monte um workflow para cada necessidade do seu dia a dia. Na minha visão, estamos de certa forma atrasados e caminhando na direção errada como banco, visão corporativa, na forma com que é estimulado o uso desses modelos. Superestimado para tarefas simples, ignorado para tarefas complexas onde a tecnologia seria assertiva.

![boris-slider.gif](Manifesto%20sobre%20uso%20de%20LLMs%20como%20ferramentas%20de%20ul/boris-slider.gif)

Precisamos urgentemente começarmos a debater menos sobre “como podemos integrar a IA nos nossos serviços?” e muito mais sobre “como podemos integrar a IA no dia a dia com uma visão AI first?”. Vou dar alguns exemplos que clarificam o que seria esse segundo ponto:

- Na hora de executar um projeto, a escolha da linguagem de programação usada passa por um crivo importante: o domínio da squad com aquele linguagem. Com a possibilidade de uso da IA para escrita e manutenção do código, por que não damos prioridade para a linguagem com a melhor performance? Conseguimos imaginar qual seria a economia de custo e melhoria de performance migrando Lambdas de Python (interpretado) para Go ou Rust (compilados)? Karpathy tem um tweet falando sobre isso [[ref](https://x.com/karpathy/status/2023476423055601903)].
- Logs nos ajudam na hora do debug, de incidentes, acompanhamentos, são ótimos! Mas eles estão otimizados para leitura do um agent? A capacidade cognitiva humana tem a notável característica de reconhecer padrões, mas será que somos melhores que um modelo de Machine Learning treinado para reconhecer e prever padrões? Usando um exemplo pessoal, em dois incidentes que tivemos quem encontrou o erro utilizando os logs foi o Claude, mas quantos tokens (dinheiro/tempo) eu poderia ter economizado se planejasse logs otimizados para leitura?
- O ponto mais importante para os agents dentro do banco: informação burocrática. Usamos e reutilizamos dezenas de produtos diferentes ao longo do dia, como podemos garantir que o agent tenha consciência sobre como uma pipeline XPTO funciona? Temos uma vantagem: as documentações são escritas em markdown que é um formato interessante para a IA, mas como podemos garantir que um agent rodando em um container docker ou isolado do meu ambiente via web tenha acesso à documentação da pipeline XPTO? Novamente Karpathy tem algo a dizer sobre o assunto: [[ref](https://x.com/karpathy/status/2026360908398862478)].

O ponto que quero chegar é: um agent não deve ser pensado como uma “peça” ou um “serviço” como uma API ou um Job Glue, muitas vezes integrar um agent em um fluxo sai muito mais caro do que pedir para esse mesmo agent desenhar um fluxo de automação mais confiável para substituí-lo. Por exemplo, modelos de machine learning feitos pelos queridos Cientistas de Dados existem a muito tempo para cálculos e tomadas de decisão, o uso de uma IA generativa (agent) para esses casos não faz sentido. O mercado adotou a programação agêntica por um motivo, é importante seguirmos a trend com responsabilidade e zelo

![image.png](Manifesto%20sobre%20uso%20de%20LLMs%20como%20ferramentas%20de%20ul/image.png)

Dentro do banco, por razões óbvias e com as quais eu concordo, temos diversas limitações na hora de usar agents, mas temos que resistir e seguir em dois pontos:

- Divulgar ao máximo para pares e parceiros esse estudo aprofundado de IA e programação agêntica, é importante saber (e conseguir) surfar na crista da onda e não deixar que uma visão errada, enviesada por quem quer vender um produto e não aprofundada sobre o que a IA significa tome conta das discussões. **Agents não rodam sozinhos e definitivamente precisam de babás**. A opinião do Karpathy é super relevante e importante de replicar para lideranças e responsáveis técnicos:
    
    > The models definitely still make mistakes and if you have any code you actually care about I would watch them like a hawk. […] The most common category is that the models make wrong assumptions on your behalf and just run along with them without checking. - [A few random notes from claude coding quite a bit last few weeks.](https://x.com/karpathy/status/2015883857489522876)
    > 
- Nos ajudarmos com inner source, dicas, macetes e contribuições para homologações seguras das tecnologias mais recentes. Sabemos que existe uma certa instabilidade tanto tech quanto burocrática, mas faz parte do jogo.

## Boas práticas

Este documento está sendo escrito no mês de junho de 2026, se fosse escrito no mês anterior já teriam diferenças nas recomendações feitas pela comunidade open source e os especialistas. Por isso, é importante manter-se atualizado; ao longo desse tópico, vou apresentar alguns canais relevantes para esse objetivo.

Vale reforçar novamente a mensagem que eu quis passar em boa parte deste suposto manifesto: nenhuma dessas dicas deve ser entendida como obrigatório. Utilize-as para montar um primeiro workflow, entender conceitos da programação agêntica e modelar um ou vários workflows que atendam a sua necessidade no dia a dia.

### Trending na comunidade

#### Glossário

Ao longo do texto citei e citarei algumas pessoas e acho que faz sentido dar nomes aos bois:

- Boris Cherny → Criador do Claude Code e atual Head do produto; Ex-Meta
- Andrej Karpathy → Pesquisador pioneiro em deep learning, professor, co-fundador da OpenAI e atualmente na Anthropic; Ex-Tesla
- Michael Truell → Co-fundador e CEO da Cursor
- Matt Pocock → Educador & influencer tech sobre IA; Criador de skills populares
- Peter Steinberger → Criador do OpenClaw

#### Spec-Driven Development e suas ramificações

O SDD, Spec-Driven Development, é um framework onde usamos como base documentos, escritos em linguagem natural, para desenvolver um novo projeto. Esse modelo tem muita sinergia com a programação agêntica, pois as especificações desses documentos serão lidas pelos agents que assim terão uma boa contextualização e poderão atuar na codificação de maneira assertiva [[ref](https://learn.microsoft.com/pt-br/training/modules/spec-driven-development-github-spec-kit-greenfield-intro/2-what-spec-driven-development?pivots=video)]. No geral, o SDD baseia em: documentar → planejar → executar → revisar, não existindo um consenso hoje sobre um workflow “ideal” ou “melhor”, muito pelo contrário, assim como as outras discussões, cada especialista compartilha os casos que consideraram melhor em seus testes, exemplo:

![[https://x.com/mattpocockuk/status/2066451514672009337](https://x.com/mattpocockuk/status/2066451514672009337) ](Manifesto%20sobre%20uso%20de%20LLMs%20como%20ferramentas%20de%20ul/image%201.png)

[https://x.com/mattpocockuk/status/2066451514672009337](https://x.com/mattpocockuk/status/2066451514672009337) 

É importante entender o que é SDD e as formas de implementar esse framework no desenvolvimento e manutenção de código

![Comentário bônus feito no tweet anterior](Manifesto%20sobre%20uso%20de%20LLMs%20como%20ferramentas%20de%20ul/image%202.png)

Comentário bônus feito no tweet anterior

#### Karpathy

Já citei Karpathy várias vezes nesse texto, provavelmente um dos nomes mais importantes para acompanhar. Não apenas suas opiniões sobre IA que são publicadas no X (ex-twitter) são interessantes de ler, mas toda a discussão e ambiente que são criados nos comentários e quotes podem ter conversas riquíssimas em conhecimento. Obs: é importante filtrar os bots e marketeiros dessa lista.

Um tweet dele viralizou no começo desse ano e o texto completo abriu diversas discussões, gostaria de destrinchar um pouco sobre: [A few random notes from claude coding quite a bit last few weeks.](https://x.com/karpathy/status/2015883857489522876)

> This is easily the biggest change to my basic coding workflow in ~2 decades of programming and it happened over the course of a few weeks. I'd expect something similar to be happening to well into double digit percent of engineers out there, while the awareness of it in the general population feels well into low single digit percent.
> 

> LLMs are exceptionally good at looping until they meet specific goals and this is where most of the "feel the AGI" magic is to be found. Don't tell it what to do, give it success criteria and watch it go. Get it to write tests first and then pass them. Put it in the loop with a browser MCP. Write the naive algorithm that is very likely correct first, then ask it to optimize it while preserving correctness. Change your approach from imperative to declarative to get the agents looping longer and gain leverage.
> 
- Dê liberdade para o agent rodar comandos e validar o próprio trabalho, de preferência mantenha um ambiente containerizado e isolado para esses testes. Para que ele entenda o que é o “sucesso”, defina os critérios de aceite com o comando /goal, default da maioria dos agents
- Fala-se muito sobre o SDD (Spec Driven Development) que é ótimo para o desenvolvimento com agents, mas você ainda pode utilizar qualquer outro framework “tradicional” como o TDD.

> Fun. I didn't anticipate that with agents programming feels *more* fun because a lot of the fill in the blanks drudgery is removed and what remains is the creative part. […]
Armed with LLMs, do generalists increasingly outperform specialists? LLMs are a lot better at fill in the blanks (the micro) than grand strategy (the macro).
> 
- Use o tempo ganho codando menos e evitando trabalhos repetitivos para melhorar skills generalistas, melhorar sua escrita, estimular a criatividade, estudar

#### O problema da complexidade

> One common issue with personalization in all LLMs is how distracting memory seems to be for the models. A single question from 2 months ago about some topic can keep coming up as some kind of a deep interest of mine with undue mentions in perpetuity. Some kind of trying too hard. - [https://x.com/karpathy/status/2036836816654147718](https://x.com/karpathy/status/2036836816654147718)
> 

> 
> 
> 
> Experimenting today with:
> 
> - /to-prd to create a PRD
> - /goal to implement
> - "autoCompactWindow": 180000 to stay approximately in the smart zone
> 
> Let's see how it goes.
> 
> ---
> 
> The compacting is going great. Great to see it operating so much of the time at 80-120K tokens. Since task tracking is preserved between compacts (I think?) it actually does well at staying on track.
> Overall, it was fine! Pretty pleased and will try this again.
> 
> ---
> 
> Yep, the point of the PRD is that you have work that spans multiple sessions
> [https://x.com/mattpocockuk/status/2064328721230647608](https://x.com/mattpocockuk/status/2064328721230647608)
> 

Algumas discussões sobre memória e contexto trazem um ponto importante: alucinação e performance dos agents em sessões longas. Alguns conceitos são:

- Smart zone
    - No começo de uma sessão, o agent está na “smart zone”, ele está focado e possui zero viés. A partir do momento que a sessão cresce, ele entra em uma “dumb zone”, fica mais desleixado, confuso com as perguntas anteriores e consequentemente comete mais erros e alucinações. Existe um debate sobre aonde a dumb zone começa, mas o estimado pelo Matt Pocockuk é que seria por volta dos 180k tokens de contexto. O recomendado é limpar ou compactar esse contexto quando chegar nesse ponto, dai a configuração de autoCompact.
- PRD → product requirements document
    - Similar ao que conhecemos como “História”. É um documento com os requisitos de negócio para uma tarefa específica. O nome é uma convenção da comunidade.
- Memória entre sessões
    - Como citado na smart zone, o acúmulo de memória entre sessões pode ser uma faca de dois gumes: ao mesmo tempo que o agent tem um suposto maior conhecimento do que ele está lidando, é mais provável que ele esqueça outros fatores mais importantes para a task atual. Prefira manter as informações em documentações do que em memória.

Concluindo, **um workflow complexo traz maior chances de erros**. Um fluxo otimizado é um fluxo bem dividido em tarefas concisas e bem documentado. Para isso, em outra discussão é sugerido o uso de uma skill chamada /handoff: [https://github.com/mattpocock/skills/blob/main/skills/productivity/handoff/SKILL.md](https://github.com/mattpocock/skills/blob/main/skills/productivity/handoff/SKILL.md). O objetivo é compactar a sessão sem perder o acompanhamento, em conjunto com o PRD também citado no tweet acima: [https://github.com/mattpocock/skills/blob/main/skills/engineering/to-prd/SKILL.md](https://github.com/mattpocock/skills/blob/main/skills/engineering/to-prd/SKILL.md).

#### Cautela com o que seguir

No tweet abaixo, o criador da ferramenta OpenClaw ironiza uma fala do Boris Cherny. Além de uma rivalidade entre OpenAI e Anthropic, podemos entender um fato: pessoas associadas a grandes empresas muitas vezes vão tentar engajar tendências que beneficiem o lucro destas tais empresas, é importante ter discernimento para separar o joio do trigo.

> 
> 
> 
> Here’s your monthly reminder that you shouldn’t be prompting coding agents anymore. You should be designing loops that prompt your agents. - [https://x.com/steipete/status/2063697162748260627](https://x.com/steipete/status/2063697162748260627)
> 

![image.png](Manifesto%20sobre%20uso%20de%20LLMs%20como%20ferramentas%20de%20ul/image%203.png)

Outro exemplo relevante é a fala do CEO da Cursor, que define uma nova era da IA 100% autônoma. Curiosamente, uma era que traria muito lucro para a empresa da IDE agêntica.

> Now a third era is arriving. It is defined by agents that can tackle larger tasks independently, over longer timescales, with less human direction. […]
Many of us at Cursor are already working this way. More than one-third of the PRs we merge are now created by agents that run on their own computers in the cloud. A year from now, we think the vast majority of development work will be done by these kinds of agents. - [https://x.com/mntruell/status/2026736314272591924](https://x.com/mntruell/status/2026736314272591924)
> 

Segundo a Oracle (e diversas outras discussões sobre o assunto), manter um humano no processa agêntico combina a eficiência da IA com o supervisionamento e entendimento de contexto humano é essencial. Este conceito é chamado de Human in the Loop, abreviado para HITL ou HIL [[ref](https://docs.oracle.com/en/cloud/paas/application-integration/human-loop/overview-human-loop-agentic-ai.html)].

### Minha contribuição para o Inner Source e algumas dicas pessoais

Melhore seus workflows a cada dia, não se prenda em uma v0. Faça “fine tuning” das suas próprias instruções, não limite o uso de agents apenas para codificar, organize suas notas, documentos, documentações, faça engenharia reversa para entender processos etc

- Mapa com as documentações do banco para o Agent (e para humanos rs)
- Script para setup de devcontainer
    - Preparação de ambiente
    - Setup de linguagens
    - Setup de skills
- Modelo base de dotfiles com as boas práticas dos especialistas

### Links relevantes

Alguns links relevantes para estudo mas que não entrarei em detalhes:

- Guidelines para IA criada com base nos tweets e falas do Karpathy: [https://github.com/multica-ai/andrej-karpathy-skills/blob/main/.cursor/rules/karpathy-guidelines.mdc](https://github.com/multica-ai/andrej-karpathy-skills/blob/main/.cursor/rules/karpathy-guidelines.mdc)
- Curso mantido pela comunidade para programação agêntica: [https://github.com/walkinglabs/learn-harness-engineering](https://github.com/walkinglabs/learn-harness-engineering)
- Skills generalistas relevantes para ficar de olho (conseguimos usar no banco)
    - [https://github.com/mattpocock/skills/blob/main/skills/engineering/grill-with-docs/SKILL.md](https://github.com/mattpocock/skills/blob/main/skills/engineering/grill-with-docs/SKILL.md)
    - [https://github.com/mattpocock/skills/blob/main/skills/productivity/caveman/SKILL.md](https://github.com/mattpocock/skills/blob/main/skills/productivity/caveman/SKILL.md)
        - Modelo de workflow baseado no caveman: [https://github.com/JuliusBrussee/cavekit](https://github.com/JuliusBrussee/cavekit)
    - [https://github.com/mattpocock/skills/blob/main/skills/productivity/write-a-skill/SKILL.md](https://github.com/mattpocock/skills/blob/main/skills/productivity/write-a-skill/SKILL.md)
- Projetos que considero que valem a pena ficar de olho:
    - [https://github.com/chopratejas/headroom](https://github.com/chopratejas/headroom)
    - [https://github.com/jdx/mise](https://github.com/jdx/mise)
- Tutoriais da empresa responsável pelo Claude: [https://www.anthropic.com/learn](https://www.anthropic.com/learn)
- Repositório mantido pela comunidade com boas práticas/dicas da própria comunidade e de engenheiros da Anthropic: [https://github.com/shanraisshan/claude-code-best-practice](https://github.com/shanraisshan/claude-code-best-practice)

![image.png](Manifesto%20sobre%20uso%20de%20LLMs%20como%20ferramentas%20de%20ul/image%204.png)