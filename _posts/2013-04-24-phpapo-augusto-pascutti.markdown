---
layout: post
title:  "#2 PHPapo – Augusto Pascutti"
date:   2013-04-24 13:44:04 -0300
image:  /img/augustohp.png
categories: phpapo
---

<img src="/img/augustohp.png" alt="Augusto Pascutti" />

> “ZCE, Co-fundador PHPSP, desenvolvedor web, entusiasta de software livre e envagelista do XKCD.”

# Desenvolver do zero, ou usar Framework? Qual o melhor caminho?

Usar um framework não significa apenas usar uma ferramenta de desenvolvimento, significa também utilizar o conhecimento 
e os “testes” de muitos outros desenvolvedores.

Por “conhecimento” acho importante esclarecer a idéia de que mais “cabeças” significam também mais casos de uso cobertos.

Com relação aos “testes” o importante é saber que isso não toca somente os diferentes tipos de teste existentes (unitário, 
funcional, comportamento e integração), mas também a quantidade de diferentes pessoas utilizando e aferindo que aquele código 
funcione propriamente (clientes acessando o sistema).

Tendo tudo isso em mente, fica (pelo menos em minha concepção de mundo) difícil comparar um framework próprio (desenvolver do zero) 
com um que possui uma base de conhecimento maior. Jamais uma pessoa conseguirá produzir algo que funcione para a grande 
maioria de pessoas tão bem quanto um grupo de pessoas. Logo a escolha é óbvia: **vá para um framework existente.**

A próxima pergunta que você deveria se perguntar é: **Qual framework?**

A resposta deve vir (na minha opinião) em conjunto com as respostas à outras perguntas:

1. Qual o conhecimento da equipe que irá trabalhar no projeto? 
    (É importante levar em consideração a curva de aprendizado de uma “nova” ferramenta.)
 
2. O framework possui boas ferramentas disponíveis para as necessidades do projeto? 
(Se sim, elas são largamente utilizadas em conjunto com o framework? Por quanto, provavelmente, elas serão mantidas?)

***Resumindo:*** *você nunca criará um framework melhor do que qualquer dos demais sozinho. Vá para um framework existente 
que mais lhe agrade e contribua com ele. Acredite, o pessoal criando ele pensa exatamente da mesma forma que você.*
 
# Qual o maior problema de usar variável global?

Colocando em palavras BEM cretinas: A arquitetura de software é a ciência de controlar diferentes escopos de informação.
É essencial pra arquitetura de software (e consequentemente pro desenvolvimento de software) que existam escopos: 
diferentes grupos de informação que só tem sentido dentro deste conjunto.

Todo conceito de escopo gira em torno de UMA limitação *– eu gosto de limites, é muito mais fácil explicar coisas usando
limites (que são coisas que qualquer pessoa consegue entender, no sentido mais primitivo [e consequentemente literal/etimológico] da coisa) –*
como em um diagrama de Venn, você SEMPRE terá um grupo que é (normalmente) MAIOR do que todas as partes que o compõe.

Não existe nenhum escopo que englobe todos os outros. Na ciência como um todo. Uma camada de abstração (podemos 
pobremente relacionar aos escopos) nunca antinge diretamente todas as camadas inferiores à ela. Elas têm de pagar 
o preço de ir de uma camada (de abstração) à outra uma por uma. Falhou uma em cem mil, ótimo: falhou, não funcionou, 
ERROR, blue screen of death, kernel panic, fuck, cliente puto, nego te chamando de inútil, etc.

UMA variável global sacrifica TODOS os diferentes escopos que ela toca. TODOS.

Resumindo (de novo): nosso trabalho gira em torno de validar e separar (BEM) diferentes grupos dentro de uma aplicação 
(usuários, vendas, produtos, itens, pedidos). Uma variável global sacrifica toda essa separação (e muito mais). 
É praticamente impossível controlar uma aplicação que possui UMA variável global, mais de uma? Desista. 
Isso é uma coisa que o TDD deixa bem claro: você jamais consequirá reproduzir todos os possíveis diferentes casos 
envolvemento uma variável global.

**PS: vejo um problema similar (ao uso das variáveis globais) com aplicações assíncronas.**

# Porque MVC deixa a desejar em ambiente web?

O MVC funciona muito bem para aplicações desktop ou “locais”. Exemplos comums são o iOS e o Android: 
existem várias resoluções, de diferentes tamanhos. A abstração da visualização é necessária, clara. Fazendo o 
análogo à web disso, nós sempre apresentamos HTML (tá, trafegamos alguns JSONs e XMLs mas eles não são formas de 
visualizações. Um usuário nunca visualiza eles). Temos o CSS para tratar as diferentes resoluções e tamanhos 
de dispositivo. Nos JÁ temos e usamos a melhor solução/abstração pra isso! Porque abstrair isso de novo criando uma view? 
Só pra que programadores de linguagens mais antigos e baixas não zombem da gente? Fodam-se.

Quanto ao Controller: o próprio protocolo HTTP faz todo o “suposto” trabalho dos controllers. Ele valida, ele fornece meios 
de entregar difentes representações e de encontrá-las. De novo: porquê refazer isso? Fodam-se, de novo.

Quanto ao Model ou a camada de negócios: (na minha opinião) a abstração que chega mais próxima do negócio é a relacional 
(MySQL, Oracle, Postgres, etc.). Se utilizarmos a Orientação a Objetos (que é, hoje, o paradigma mais eficiente em relação 
à durabilidade) então sabemos que não existe nenhuma relação simples entre um objeto (e suas relações) e os relacionamentos 
do modelo relacional. Não existe padrão ou algoritmo próprio para resolver este problema. Esse é nosso trabalho, é esse 
cara que realmente devemos nos esforçar e entregar. O conceito mais próximo e tangente às models que conheço é o 
**“Domain Driven Development”**.

***Concluindo:*** *a web te fornece tudo que pode ser automatizado (views e controllers) da melhor forma existente. 
Se concentre no problema de verdade e consuma o resto. Economize código e trabalho.*
 
# Como saber qual framework escolher para um projeto em especifico?

Como comentei em outra pergunta: *é importante conhecer o time que irá desenvolver a solução*. Levar em consideração 
o prazo do projeto e a curva de aprendizado de cada nova ferramenta é imprescindível para o sucesso dele.

Saber quais as fundações do projeto: quais os problemas quais as soluções (à longo prazo) ele visa resolver. 
Quanto tempo o projeto irá durar e qual investimento pode ser utilizado são, também, importantes.

Depois de levar em consideração o time, tenha certeza de que o tempo de vida da versão estável do framework (e quanto ela irá durar) 
pelo menos seja maior do que o tempo de desenvolvimento do projeto.

Quase todos os frameworks possuem uma empresa que dê suporte além da própria comunidade Open Source, se investimento 
nesse suporte não é um problema, analisar essas empresas (e qual é a melhor ou tem mais experiência nos problemas que você irá lidar)
é uma questão bastante considerável também.

# Quais certificações são de maior valia para um profissional PHP?

Considero que um profissional PHP é um desenvolvedor. Que ele não está preso à linguagens de programação nem paradigmas.
Que ele tem facilidade em enteder diferentes paradigmas e pensar neles de forma natural, mesmo tendo conhecido eles há segundos.

Se você levar isso em consideração, então nenhuma certificação realmente importa. Pelo simples fato de não existir nenhuma 
forma de medir conhecimento.

Se você, agora, considerar que um “profissional PHP” é uma pessoa que realmente possui grande experiência e conhecimento da linguagem;
então a ***ZCE*** é essencial. A ***ZCE*** consegue cobrar bem o que um desenvolvedor PHP/web realmente deve saber. Outras ceritificações 
interessantes seriam as ***LPI*** (bem comum entre desenvolvedores) e as de ***MySQL*** (raras, mesmo entre pessoas dedicadas ao MySQL).

# Quando estamos trabalhando com algum cms, somos forçados a seguir uma linha de programação e fazer coisas que não são aconselháveis. Como podemos contornar isso?

Serei BEM filho da puta (e preguiçoso) nessa resposta (e eu me odeio por isso): não acho que seja importante ou essencial 
mudar esse jeito “forçado” de fazer as coisas. Entenda que um CMS ou um framework é uma quebra-cabeças bem complicado de 
soluções de diversos problemas. As pessoas familiares à eles (aos cms/frameworks) estão acostumadas à esperar determinadas 
coisas. Tire isso delas (e de você) e você terá (muito) mais trabalho para entender e manter as coisas que você simplesmente 
não espera. No fim, acho que ninguém quer ter MAIS trabalho.

Muitos frameworks e (quase todos) CMS(es) usam o paradigma Orientado a Objetos mas ao mesmo tempo fica claro que eles não 
entenderam o paradgima. Eles não usam direito composição e agregação, que são os conceitos mais básicos da coisa. 
Tão básicos que eles vêm antes (em simplicidade e complexidade) da herança e a única coisa que esses frameworks chegam 
a usar é a herança.

# O que um programador PHP tem que conhecer para ser um bom profissional?

Conhecer o ambiente web como um todo é o mínimo. PHP é uma linguagem para WEB, portanto conhecer o protocolo e as ferramentas
que compões a Internet é essencial.

Além disso, o PHP faz uso de várias ferramentas Open Source do ambiente Unix então qualquer conhecimento nesse sentido é
um diferencial poderoso.

O PHP é multi paradigma, ele possui ótimo suporte à Orientação a Objetos e aos paradigmas imperativo e procedural.
Saber a diferença e o objetivo de cada paradigma vai melhorar (muito) o consumo deles. Em versões mais novas (>=5.4) o paradigma
funcional da linguagem ganhou construções poderosas, como os “Generators”.

O PHP é desenvolvido por uma comunidadem composta por: core developers, frameworks, desenvolvedores, comunidades (ou grupos de usuários) 
e empresas: faça parte disso! Esteja ciente da situação atual da linguagem e dos próximos passos. Um excelente começo para
isso é o ***PHP the right way***!

Resumindo: um bom programador PHP é aquele que está envolvimento, de alguma forma, com a comunidade que faz o PHP. Seja 
essa comunidade um framework, um grupo de usuários, uma lista de discussão ou empresa que realmente vive (e produz) Open Source.
 
# Dicas para quem está tentando entrar no mundo php.

Entre no loop: leia, teste (código), contribua.

Ler sobre as novidades da linguagem, do ambiente web e testá-las é importante. Se possível, evite desenvolver sozinho: 
várias cabeças pensam mais do que uma.

Evite o pensamento “eu não sei o bastante para contribuir”. A contribuição começa com a disposição de contribuir. 
Em vários anos acompanhando o Open Source eu jamais vi o fato de alguém querendo contribuir ser deixado de lado ou mal 
tratado pelo falta de conhecimento.

Pense nisso: O Open Source é a melhor faculdade que alguém pode querer: não custa nada! Não tem horários. Nem provas ou
algo cobrando de você alguma coisa. Ensina muito mais, e de quebra você ainda contribui com a necessidade de muitos. 
Fazer parte disso é uma escolha só sua e ela jamais está ligada ao seu conhecimento (ou limite dele).
 
# Sei que meu código está uma zona, mas não tenho tempo de fazer refactory. O que fazer?

Ao meu ver existem duas alternativas que tornarão as coisas melhores:

1. Vender côco na praia.
2. Refatorar.

O preço de manter o código da forma que está será pago pela equipe e quanto mais esse código continuar evoluindo 
(em direção ao caos) pior será a tarefa de organizá-lo. Problemas se tornarão mais difíceis de encontrar e corrigir, 
novas funcionalidades mais difícieis de inserir até chegar no limite do “Highlander”, em que só uma pessoa tem condições 
de entender a coisa toda (na maior parte das vezes porque ela era a única presente desde do princípio) e dar continuidade.

Minha opinião é que se você já chegou a presenciar o estado Highlander da coisa, você conseguiu ir longe demais.

Nosso trabalho como desenvolvedores é basicamente resolver problemas. Não se resolve um problema criando outro. “Outro” 
problema normalmente é simplesmente o código que ninguém mais entende, nem mesmo o autor após o tempo.

O maior problema no refactor desses códigos esta na mudança. Ninguém aceita bem mudanças, mas por sorte temos padrões ou 
as chamadas PSR (PHP Standard Recomendation).

Se seu código é Orientado a Objetos, a refatoração é mais fácil. Caso ele (o código) não seja, vá em busca de componentes 
de terceiros que fazem o que você precisa e já faz. Mesmo que de forma diferente. É muito mais fácil manter temporariamente 
somente a “ponte” entre os diferentes componentes do que criar ou manter algo que você a partir do zero. Faça uso do conhecimento 
coletivo e do trabalho de outras pessoas. Economize tempo, esforço e problemas. Você, com certeza, já tem o suficiente disso.

Não tenha medo da mudança. Melhor mudar pra algo que você sabe o quanto irá durar do que colocar esforço em algo que já está arruinado. 
Considere o código como um organismo vivo: o código que não é mantido deteriora e morre, inevitavelmente. Logo, evitar o 
problema do refactor ou da reorganização é como acelerar o processo de morte de todo o projeto.

# Posso codar um DataAccess usando traits?

***Sim.***

Agora, se isso é adequado ou não, acho que é outra pergunta. 

A resposta rápida para essa “nova” pergunta é: existe pouco espaço (senão nenhum) na Orientação a Objetos para a 
herança horizontal (traits). Logo, para qualquer problema do ponto de vista Orientado a Objetos, as traits são um 
acessório e não uma necessidade.

# Estou aprendendo muito sobre o php e tudo que o envolve. Porém, no dia a dia, não tenho como colocar em prática. Como posso usar meu conhecimento no dia a dia?

Existem diversos projetos Open Source, de diversos tamanhos e diversas necessidades precisando sempre de contribuição. 
Encontre um que vá de encontro com suas necessidades e/ou interesses e contribua: com perguntas, documentação, tradução, 
testes, código, etc. ;)

***O dia dura 24h para todo mundo, o que fazer com essas 24h é uma questão só sua.***

A questão de conseguir colocar as coisas que você aprende em prática pode estar intimamente ligada ao fato de você não 
entender apropriadamente o problema (ou os problemas) que o(s) envolve(m). Penso nos problemas como diagramas de Venn: 
às vezes você simplesmente não possui experiência ou conhecimento o suficiente para enxergar (tanger) e interpretar 
(estar no mesmo grupo) que aquelas palavras realmente siginificam, ou quais problemas determinadas soluções realmente 
pretendem resolver. Essa confusão é comum, e se você fizer tudo certo, ela nunca desaparecerá. Você sempre verá o quão 
ignorante é em relação à tudo e o quanto, cada vez mais, precisa se aplicar e estudar.

Um remédio para experiência é o Open Source: não existe contrato, não exitem cobranças nem limites além da sua decisão 
de contribuir. A web é Open Source, logo não existe lugar melhor para praticar isso do que numa linguagem cujo objetivo 
é a Web como um todo. Sem a prática então fica impossível mudar a forma de você pensar, de entender as coisas. É como 
conhecer só uma ferramenta (o martelo) e usar ela para todos os problemas, uma vez que você descobre uma ferramenta 
nova (uma enchada, por exemplo) você realmente entende quanto tempo estava perdendo usando a ferramenta errada para fazer 
algo que não é próprio dela.
