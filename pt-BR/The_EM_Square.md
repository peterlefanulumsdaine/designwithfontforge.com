---
published: true
layout: bookpage_pt-BR
weight: 12
category: workflow
title: A medida Eme - <em>Quadratim</em>
---

&mdash; Também chamado de 'tamanho do em'' ou UPM'.  
Em uma gonte, cada caractere é instalado em seu prórpio contêiner espacial. Em tipo um tipo 
de metal real de cada carácter. A altura de cada peça de um carácter era uniforme
permitindo que os caracteres fossem definidos de forma limpa em linhas e blocos (veja abaixo).

<img src="../en-US/images/MetalTypeZoomIn.JPG" alt>

A altura da peça de tipo é conhecima como 'em', ela se origina a partir da largura do caractere
‘M’ em maiúsculo; foi feito para que as proporções desta carta fossem quadradas (daí a denominação ‘em
quadrada’).  
O tamanho em é o tamanho do ponto do tipo de metal é calculado. Assim, um tipo de 10 pontos tem 10
pontos em (veja abaixo).

<img src="../en-US/images/em-metal-type.svg" alt>

Em tipo digiral, o em é uma quantidade de espaço digitalmente definida. Em uma fonte OpenType, o UPM &ndash;
ou em geralmente é definido em 1000 unidades. Em fontes TrueType, o UPM , por converção, um poder de dois,
geralmente configurado para 1024 ou 2048.

Quando a fonte é usada para definir o tipo, o em é dimensionado para o tamanho do ponto desejado. Isso significa que,
para o tipo de 10 pt, as 1000 unidades, por exemplo, são dimensionadas para 10 pt.

Então, se o seu 'maiúsculo' ‘H’ for 700 unidades de altura, ele terá 7 pt de altura em um tipo de 10 pt.

### Configurando isso na janela Glyph

Com o conhecimento de que sua fonte está usando um UPM 1000, 1024, ou 2048, você precisa configurar o desenho
de seus glifos para garantir que todos os aspectos do seu tipo de letra se encaixem adequadamente nesse quadrado UPM.

O tamanho do quadrado pode ser definido a partir de *Elemento > Informações de Fonte&hellip;* então clique na guia Geral
e você verá a configuração *EM*, cujo valor deve ser distribuído entre as alturas *Ascender* e
*Descender*, respectivamente alturas acima e abaixo da linha de base.

A Linha da Base:

<img src="../en-US/images/baseline.png" alt>

A altura do boné:

<img src="../en-US/images/capheight.png" alt>

A x-altura:

<img src="../en-US/images/xheight.png" alt>

Mias tarde, ao projetar o seu tipo, você terá que definir os valores azuis que servem para contornos PostScript
e também para o Autohinter FontForge &ndash; independentemente de quais tópicos você está trabalhando.
  
Você encontrará a configuração em *Elemento > Infomações de Fonte&hellip;*, na guia *PS Private*. O FontForge pode
inicialmente adivinhar os valores com base em seus contornos, mas você terá que editá-los para
overshoots/undershoots &mdash; estamos alguns capítulos à frente deste conceito (veja
[“Creating ‘o’ and ‘n’”]); Obtenha primeiro o FontForge e suas funcionalidades de desenho.

[“Creating ‘o’ and ‘n’”]: Creating_o_and_n.html
