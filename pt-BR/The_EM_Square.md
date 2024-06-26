---
published: true
layout: bookpage_pt-BR
weight: 12
category: workflow
title: A medida Eme
---

&mdash; Também chamado de ‘tamanho do eme’, ‘UPM’ (**U**nidades **P**or e**M**e).
Em uma fonte, cada caractere é inserido em seu próprio contêiner espacial. Nos tradicionais tipos de metal, esse
contêiner era o próprio bloco de metal de cada caractere (o clichê tipográfico). A altura de cada chichê era
uniforme, permitindo que os caracteres fossem definidos de forma limpa em linhas e blocos (veja abaixo).

<img src="../en-US/images/MetalTypeZoomIn.JPG" alt>

A altura do clichê é conhecima como ‘eme’, e ela se origina a partir da largura do caractere
‘M’ em maiúsculo; isso foi feito para que as proporções desta letra fossem quadradas (daí a denominação ‘quadrado
eme’).
É a partir do tamanho eme que é calculado o tamanho do ponto do tipo de metal. Assim, um tipo de 10 pontos tem 10
pontos eme (veja abaixo).

<img src="../en-US/images/em-metal-type.svg" alt>

Na tipografia digital, o eme é uma quantidade de espaço definida digitalmente. Em uma fonte OpenType, o UPM &mdash;
ou eme geralmente é definido em 1000 unidades. Em fontes TrueType, o UPM, por converção, é uma potência de dois,
geralmente configurado para 1024 ou 2048.

Quando a fonte é usada para definir o tipo, o eme é dimensionado para o tamanho de ponto desejado. Isso significa que para
um tipo de 10 pt, as 1000 unidades são dimensionadas para 10 pt.

Então, se o seu ‘H’ maiúsculo possuir 700 unidades de altura, ele terá 7 pt de altura em um tipo de 10 pt.

### Configurando na janela Glyph

Considerando que sua fonte está usando um UPM de 1000, 1024, ou 2048, você precisa preparar o desenho
de seus glifos para garantir que todos os aspectos da sua família se encaixem adequadamente nesse UPM.

O tamanho do quadrado eme pode ser definido a partir de "_**Elemento**&nbsp;⇨&nbsp;**Informações&nbsp;da&nbsp;Fonte&hellip;**_" e então clique na aba
"_**General**_" e você verá a configuração *EM&nbsp;Size*, cujo valor deve ser distribuído entre as alturas *Ascent* e
*Descent*, respectivamente alturas acima e abaixo da linha de base (baseline).

A Linha da Base (Baseline):

<img src="../en-US/images/baseline.png" alt>

A altura das maiúsculas (Cap Height):

<img src="../en-US/images/capheight.png" alt>

A altura de x (x-height):

<img src="../en-US/images/xheight.png" alt>

Mais tarde, ao projetar o seu tipo, você terá que definir os *valores azuis* (*Blue&nbsp;values*) que servem para contornos
do PostScript e também para o autohinter do FontForge &mdash; independente de em quais contornos você está
trabalhando.
Você encontrará a configuração em "_**Elemento**&nbsp;⇨&nbsp;**Informações&nbsp;da&nbsp;Fonte&hellip;**_", na aba "_**PS&nbsp;PrivaDO**_". O FontForge pode
inicialmente adivinhar os valores com base em seus contornos, mas você terá que editá-los para
adicionar uma compensação ótica &mdash; estamos alguns capítulos à frente deste conceito (veja
[“Criando ‘o’ e ‘n’”][“Creating ‘o’ and ‘n’”]); primeiro vamos dominar o FontForge e suas ferramentas de desenho.

[“Creating ‘o’ and ‘n’”]: Creating_o_and_n.html
