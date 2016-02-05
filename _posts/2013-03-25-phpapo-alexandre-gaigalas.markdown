---
layout: post
title:  "#1 PHPapo – Alexandre Gaigalas"
date:   2013-03-25 13:44:04 -0300
categories: phpapo
---

<img src="/img/alganet.png" alt="Alexandre Gaigalas" />

> "Desenvolvedor no Yahoo! Brasil e fanboy da Web"

# Sabemos hoje, que o C# está em alta. Por que não migrar do PHP para C#?

*O PHP também está em alta.* O segundo site mais popular do mundo segundo a Alexa é o Facebook, 
escrito em PHP. Segundo o Netcraft, o PHP é a plataforma mais popular dos sites avaliados,
com 39% de uso. O C# está tão em alta quanto o PHP. É possível fazer coisas em C# que não 
são possíveis em PHP, como jogos de XBoX, aplicações para o Windows 8 e aplicações para o Windows Phone. 
Se você quer um dia migrar para essas plataformas, talvez o C# seja mais interessante. De qualquer forma,
uma outra linguagem vem se tornando muito mais popular que o C# nessa área, o JavaScript, parceiro fiel
do PHP desde o nascimento da web.

 - [Alexa Top 500 (2012)](http://www.alexa.com/topsites)
 - [Netcraft PHP just grows & grows (2013)](http://news.netcraft.com/archives/2013/01/31/php-just-grows-grows.html)

 
# Qual devo utilizar? Composer ou PEAR?

**Você escolhe**. Hoje ainda não existe um padrão, mas os nomes mais proeminentes da comunidade acreditam no Composer.
Eu gosto da PEAR por vários motivos, principalmente pelo suporte a compilação de extensões e instalação global.
Se você precisa de coisas desse tipo, a PEAR pode ser uma boa alternativa. De qualquer forma, mesmo gostando da PEAR,
acredito que o Composer conseguirá superar suas dificuldades e se tornará um padrão.

O mais simples hoje é suportar ambos. Ferramentas como o Pirum conseguem expor canais PEAR e Composer simultaneamente,
e ferramentas como o Onion conseguem gerar os pacotes PEAR automaticamente, que normalmente seriam complexos sem uma
ferramenta.

 - Pirum: [http://pirum.sensiolabs.org/](http://pirum.sensiolabs.org/)
 - Onion: [https://github.com/c9s/Onion](https://github.com/c9s/Onion)

# OOP é um problema para mim. Qual a desvantagem de não utilizar esse paradigma?
 
Será bastante complicado utilizar as melhores ferramentas pra PHP disponíveis hoje e compreender como o PHP se integra 
com outros softwares populares como bancos de dados e APIs de serviços como Twitter e Facebook.

Minha sugestão pra OOP é ler muitos livros populares sobre o assunto e mexer em muito código open source PHP. 
**“Utilizando UML e Padrões”** do Craig Larman é uma boa introdução à metodologias ágeis, padrões, UML, orientação 
à objetos e projetos. Eu tive que ler umas três vezes pra entender, mas foi fantástico. **“Refatoração”** do Martin Fowler,
**“Padrões de Projeto”** do Gang of Four, **“Refatoração para Padrões”** do Joshua Kerievski. Existem e-books desses 
livros que são mais baratos, e eu já comprei todos eles em português.

Se você mesmo assim não conseguir compreender orientação a objetos ou quiser estudar algo em paralelo que não te 
decepcione enquanto você ainda tenta aprender OOP, eu recomendo a programação funcional. Algumas pessoas 
simplesmente compreendem esse paradigma melhor. O PHP tem suporte a programação funcional desde a versão 5.3, 
com a introdução de closures.

- [Utilizando UML e Padrões](https://www.duckduckgo.com/?q=utilizando+uml+e+padrões+craig+larman)
- [Refatoração](https://www.duckduckgo.com/?q=refatoracao+martin+fowler)
- [Refatoração para Padrões](https://www.duckduckgo.com/?q=refatoracao+para+padroes+joshua+kerievski)
- [Padrões de Projeto](https://www.duckduckgo.com/?q=padroes+de+projeto+gang+of+four)
- [Closures](http://php.net/Closures)

# Quero me profissionalizar na linguagem PHP. Que caminho seguir?

Siga a comunidade PHP. O Brasil é bastante forte nisso e tem uma comunidade bastante engajada inclusive entre estados 
diferentes. Isso dá oportunidade de aprender, de conseguir indicações de emprego e manter bons amigos!

Assim que você estiver engajado na comunidade de alguma forma, mesmo que online, eu sugiro que você tente de alguma 
forma contribuir com ela. Compartilhar seu progresso com iniciantes, incentivar outros programadores a se engajar na 
comunidade e tudo mais. Os melhores caras que eu conheço no Brasil não foram apenas membros de comunidade, eles ajudaram
a formar e fortalecer comunidades =)

- [Como Encontrar Bons Desenvolvedores](http://php5.net.br/como-encontrar-bons-desenvolvedores-php)
- [PHP Brasil Comunidades](http://www.php.org.br/)
 
# Qual a importância do Design Pattern e que vantagens ele pode me proporcionar?

Existem problemas com soluções prontas. Design Patterns são algumas soluções prontas pra ajudar em problemas de projeto de software,
ou seja, problemas de como “juntar as coisas pra atingir um objetivo”.

Compreender essas soluções vai te ajudar a desenvolver software de qualidade mais rápido e entender os softwares que 
usam esses padrões melhor.

- [Utilizando UML e Padrões](https://www.duckduckgo.com/?q=utilizando+uml+e+padrões+craig+larman)
- [Refatoração](https://www.duckduckgo.com/?q=refatoracao+martin+fowler)
- [Refatoração para Padrões](https://www.duckduckgo.com/?q=refatoracao+para+padroes+joshua+kerievski)
- [Padrões de Projeto](https://www.duckduckgo.com/?q=padroes+de+projeto+gang+of+four)
- [pla.net.br – Padrões de Projeto](http://pla.net.br/orientacao-a-objetos-padroes-de-projeto/)

# Calisthenics. É possível utiliza-ló a risca?

No PHP é impossível. Object Calisthenics é uma técnica pra exercitar boas práticas de orientação a objetos, o que é uma 
idéia fantástica pra linguagens puramente orientadas a objetos mas não pro PHP.

O PHP é por natureza multi-paradigma (orientado a objetos, funcional, imperativo, reflexivo, etc…) e existe um limite 
para esses exercícios. Passar desse limite normalmente te deixará com um código inchado, porque seguindo Calisthenics a 
risca você teria que “orientar a objeto” coisas que no PHP são nativas de outro paradigma.

# CMS proprietário e código livre. Qual a melhor opção?

Existe um motivo pra haverem tantos CMSs concorrentes proprietários e abertos: pessoas tem necessidades diferentes. 
Por isso nenhum CMS vai ser soberano nunca. Algum usuário sempre precisará de algo diferente.

Meu predileto é o WordPress pela sua simplicidade. Ele não é o melhor código ou o mais completo, mas é o que fica menos 
no meu caminho. Tenho bons amigos que são fãs do Drupal também.

- [WordPress](http://wordpress.org)
- [Drupal](http://drupal.org)
 
# Qual controle de versão escolher?

Algum moderno, preferencialmente o **Git**. Existem três gerações de sistemas de controle de versão, a mais recente é 
a representada pelo git, Mercurial, bzr e fossil. Esses quatro são excelentes por um motivo principal: são descentralizados.

A principal dica que posso dar é que essa escolha envolve mais do que código. Controle de versão acabou virando uma 
ferramenta pra times se comunicarem e contribuirem melhor.

- [Git](http://git-scm.org)
- [Mercurial](http://mercurial.selenic.com/)
- [Fossil](http://www.fossil-scm.org/index.html/doc/trunk/www/index.wiki)
- [Bazaar](http://bazaar.canonical.com)

# Qual versão do PHP é mais indicada para produção?

O ideal é se esforçar ao máximo pra ter sempre a última versão em produção e um código compatível com ela. Ela terá menos
bugs de segurança e será sempre mais rápida.
 
# Onde posso consiguir ajuda em PHP?

Isso depende muito do que você quer fazer. Ajudar também é algo difícil =) Existem alguns passos legais pra conseguir ajuda mais fácil:

1. Um objetivo claro. Exemplo: “Quero guardar em um banco de dados quantas pessoas visitaram meu site.”
2. Uma tentativa. Exemplo: “Tentei usar a PDO pra conectar em With keep operated actually! It clear. My cialis generic last. Has given Lip. Under canadian pharmacy one case and is – pictured. I Europe. That’s a canadian pharmacy with this. Easy them. Love designs. My dry vipps online canadian pharmacy overnight. I color nearly hell I cialis tablets uses I shampoo attention it the hair an penny. I’ve.
um banco mas esse erro apareceu na tela: ERRO”
3. Uma pergunta. Exemplo: “O que eu fiz de errado pra não conseguir conectar?”
Com esses três pontos você pode pesquisar melhor na internet, perguntar melhor pra outros programadores e entender melhor qual parte do problema está sendo mais complicada.

- [Comunidade PHP Brasil](https://www.facebook.com/groups/nao.tem.biscoito/)
- [PHP Brasil Comunidades](http://www.php.org.br/)

# O que ainda falta no PHP?

Quem determina isso é a própria comunidade. No Wiki do PHP existem algumas propostas e discussões sobre novos recursos 
da linguagem: https://wiki.php.net/rfc/

Eu particularmente gosto do PHP do jeito que ele é. O próprio criador do PHP disse uma vez: “Existem dois tipos de 
linguagem: as que ninguém usa e as que todo mundo reclama”.

# PHP em outros ambientes (CLI, GTK, etc..)?

PHP em linha de comando já é uma realidade. Temos ótimos softwares que rodam assim: PHPUnit, Composer, etc.

PHP-GTK é um projeto abandonado, se não me engano nem funciona com a última versão do PHP.

O forte do PHP mesmo é a web. Essas outras plataformas são legais quando você precisa de alguma forma ter um sistema 
híbrido e reutilizar partes do código PHP em viagra online outro lugar.
 
# Qual metodologia de desenvolvimento é mais indicado para trabalhar com o PHP?

Qualquer uma! A linguagem de programação não determina qual metodologia seguir. Eu gosto bastante de Scrum e Programação Extrema.

- [Extreme Programming](http://improveit.com.br/xp/livroxp)

# Quero contribuir. Por onde começo?

Os passos são simples, mas trabalhosos!

1. Encontre um projeto que te motive a contribuir.
2. Use e compreenda esse projeto. Se envolva. Só assim você conseguirá fazer uma contribuição valiosa pra quem também usa e compreende esse projeto. 
3. Encontre um problema. Pode ser algo já reportado por outra pessoa, pode ser algo que você achou sozinho. 
4. Discuta o problema com o autor. Pode ser que o autor já tenha uma idéia de como corrigí-lo, pode ser que alguém já esteja trabalhando nele, etc… 
5. Contribua!

Existem projetos que colocam guias pra quem deseja contribuir. Procure sempre esses guias antes de se envolver =)

- [Como contribuir com o Respect\Validation](https://gist.github.com/alganet/2356523)
- [Como contribuir com o Symfony](http://symfony.com/doc/2.0/contributing/index.html)
