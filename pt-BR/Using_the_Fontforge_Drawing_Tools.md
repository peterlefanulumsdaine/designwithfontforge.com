---
published: true
layout: bookpage_pt-BR
weight: 18
category: Getting To Know FontForge
title: Usando as Ferramentas de Desenho do FontForge
---

Projetar uma fonte no FontForge envolverá o uso de inúmeras ferramentas e utilidades, a começar com um
conjunto de ferramentas de desenho que podem parecer familiar para usuários com experiência em gráficos vetoriais &ndash;
existem diferenças notáveis, no entanto.  
Primeiro iremos buscar um entendimento de como curvas B&eacute;zier funcionam, antes de olhar as
ferramentas de desenho do FontForge em si.

## Entendendo curvas B&eacute;zier

O conceito de “curvas B&eacute;zier” refere-se a uma representação matemática em particular usada para
produzir curvas suaves digitalmente. Geralmente, ordens *Cúbicas* e *Quadráticas* dessas curvas são usadas
&mdash; contudo FontForge também suporta curvas *Spiro*, que são uma representação alternativa para
o designer.

Nesse capítulo, apenas discutiremos caminhos *Cúbicos*, uma vez que eles costumam ser usados quando se desenha
glifos. Caminhos *Spiro* serão discutidos no próximo capítulo, e curvas *Quadráticas* apenas são encontradas
em fontes TrueType, e raramente são usadas durante o desenho &ndash; elas são geradas no momento de fechamento.

Um típico caminho B&eacute;zier é composto de uma âncora, com duas alças que marcam a direção
geral &mdash; o comprimento de cada alça determina o comprimento da curva em cada lado &ndash;
veja abaixo.

### Diferentes tipos de pontos

#### Pontos de curva (exibidos como pontos circulares)

*Pontos de curva* possuem duas alças, uma ligada à outra de forma que a linha entre
elas sempre fique reta, para produzir uma curva suave em cada lado.

<img src="../en-US/images/tools-curve-point.png" alt>

<h4 class="quiet">Pontos de curva H/V (exibidos como pontos losangulares)</h4>

*Pontos de curva H/V* (‘horizontal/vertical’) são uma variação dos pontos de curva que se encaixam ao
eixo horizontal ou vertical &ndash; uma ferramenta essencial para tornar formas B&eacute;zier bem feitas
(mais sobre isso na próxima seção).

<img src="../en-US/images/tools-HV-point.png" alt>

#### Pontos de canto (exibidos como pontos quadrados)

*Cantos* podem ter 0, 1 ou 2 alças B&eacute;zier. A posição de cada alça é independente das
outras, tornando-as apropriadas para discontinuidades no contorno.  
Sem as alças, cantos irão produzir linhas retas.

<img src="../en-US/images/tools-square-point.png" alt>

<img src="../en-US/images/tools_corner_point_2.png" alt>

<img src="../en-US/images/tools-corner-point-3.png" alt>

#### Pontos de tangente (exibidos como pontos triangulares, ou ‘setas’)

Se você quer começar com uma linha reta que encurva suavemente, você vai querer usar
*pontos de tangente*.  
Uma *tangente* deixa uma linha reta em um lado, enquanto a alça B&eacute;zier do outro lado é
a sua direção &ndash; isso garante uma transição contínua entre a linha e a curva.

<img src="../en-US/images/tools-tangent-point.png" alt>

### Fazendo da forma certa

Para produzir curvas adequadas &ndash; com o mínimo de pontos de controle e uma rasterização facilitada, as
âncoras deveriam sempre ser inseridas **nos extremos da curva**, e a não ser em locais onde você
tem quebras na forma das letra, a linha que determina o caminho deveria ser **horizontal ou
vertical**.

<img src="../en-US/images/bezier_sample.png" alt>

<div class="note">
<p><b>Nota:</b> Se seus pontos de controle não estão nos extremos, FontForge irá indicar
o veradeiro extremo com um ícone de alvo:</p>

<img src="../en-US/images/bezier_sample_3.png" alt>

<p>Você pode então consertar copiando o contorno atual para uma outra camada, e movendo os pontos de
controle para que fiquem posicionados apropriadamente &ndash; do contrário a ferramenta de validação de FontForge
adicionará o ponto nos extremos automaticamente, até o ponto em que você possa mesclar sua âncora mal colocada com
<i>Clique direito > Merge</i>.<br>
Mais soubre isso será dito posteriormente no <a href="Making_Sure_Your_Font_Works_Validation.html">
capítulo de validação</a>.</p>
</div>

Para constar, existem dois caso em que você terá que desistir dos caminhos B&eacute;zier
horizontais/verticais:

- Se você quiser mudar a inclinação geral de sua curva, como na parte superior esquerda do ‘a’
  abaixo que está mantido quase plano:  
  <img src="../en-US/images/bezier_sample_2.png" alt>
- Se você quiser colocar quebras nas suas letras, como na parte inferior esquerda do ‘g’ abaixo
  &ndash; esse é um logar típico onde você quer usar um *Canto* (além de ser para desenhar linhas):  
  <img src="../en-US/images/bezier_sample_4.png" alt>

<p class="note"><b>Nota:</b> Como você pode ver, quando definindo quebras com um <i>Canto</i>, a
direção de cada alça deve ser tangente da curva em que ela chega.</p>

## Dominando as ferramentas de desenho do FontForge

Na janela principal, dê dois cliques na caixa de um glifo para abrir a Janela de Glifo.

<img src="../en-US/images/glyph_window.png" alt>

<div class="note">
<p><b>Nota:</b> Os números ao longo do topo de onde os eixos x e y se cruzam indicam, da esquerda para
direita:</p>

<ul>
<li>A localização atual (x,y) do cursor na tela de desenho</li>
<li>A localização do último ponto selecionado</li>
<li>A posição relativa do cursor para o ponto selecionado</li>
<li>A distância entre o cursor e o ponto selecionado</li>
<li>O ângulo do ponto selecionado para o cursor (relativo à linha de base)</li>
<li>O atual nível de zoom, seguido pelo nome da camada ativa.</li>
</ul>
</div>

<p class="warn"><b>Cuidado:</b> Às vezes, parece que o FontForge não está respondendo quando você está
na Janela de Glifo. Pode ser que tenha uma janela de diálogo escondida atrás &ndash; então basta
movê-la e proceder para a caixa de diálogo.</p>

Uma *Linha* consiste de 2 pontos.

<img src="../en-US/images/tools_line_points.png" alt>

Uma *Curva* consiste de 4 pontos: 2 pontos das extremidades e 2 ‘alças’, que descrevem a inclinação
da curva naquelas extremidades.

<img src="../en-US/images/tools_splines_points.png" alt>

### Copie, cole, corte e delete pontos, curvas e linhas

Bem como na maioria dos softwares de desenho, FontForge te permite Copiar, Cortar, Colar ou Deletar qualquer ponto, linha
ou curva. Esses comandos estão disponíveis no menu Editar, ou usando os atalhos de teclado típicos do seu Sistema Operacional  (também
indicados ao lado de cada comando no menu).

## Familiarizando-se com as ferramentas de desenho

Agora que você se localizou na tela de desenho, está na hora de conhecer as ferramentas.

### Ponteiro e Zoom

<img src="../en-US/images/point_zoom.png" alt>

Ponteiro e Zoom comportam-se semelhante às ferramentas equivalentes em outros aplicativos.  
O ponteiro é uma ferramenta de  seleção, usada para selecionar pontos, caminhos, e outros objetos na tela de desenho.  
A ferramenta de Zoom permite ampliar (Z) facilmente; para reduzir: vá para o menu Visualizar e selecione
*Reduzir* (X) or *Ajuste*.

Note que você também pode alternar temporariamente para a ferramenta de ponteiro enquanto estiver com alguma outra, pressionando
a tecla Control (Ctrl).

### Ferramenta de desenho livre

<img src="../en-US/images/freehand_tool.png" alt>

A ferramenta de desenho livre permite que você rascunhe caminhos irregulares.

Na área de desenho, clique e segure, então mova o mouse para desenhar. Volte para a ferramenta de ponteiro, e
você poderá selecionar pontos no caminho que você desenhou.

Quando você seleciona um dos pontos do caminho, ele se tornará um círculo amarelo. Se o ponto
selecionado está em uma curva, ele mostrará seus pontos de controle com uma alça magenta e outra ciano. Você
pode pegar qualquer alça e arrastar para mudar a forma da curva.

### As ferramentas de pontos

Ok, avora vamos ver sobre as ferramentas de pontos.

<img src="../en-US/images/point_tools_labelled.png" alt>

Para adicionar um ponto ao caminho, primeiro selecione qualquer uma dessas ferramentas, clique no caminho e dê um
pequeno empurrão. Você terá um novo ponto na linha.

A ferramenta de ponto na Curva é usada para adicionar um ponto em um segmento curvo.  
A ferramenta de Curva na horizontal ou na vertical obriga os novos pontos a terem os controladores apenas na
horizontal ou vertical &ndash; isso é importante para definir pontos extremos.  
A ferramenta de ponto no Canto permite fazer uma dobra afiada no caminho.  
A ferramenta de ponto Tangente permite a transição de um segmento reto para um segmento curvado ao longo
do caminho.

### A ferramenta de Caneta

<img src="../en-US/images/addpoint_tool.png" alt>

A ferramenta de Caneta permite adicionar um ponto na curva e arrastar seus controladores.

### Spiro

<img src="../en-US/images/spiro.png" alt>

Selecionar a ferramenta Spiro te coloca no modo de desenho Spiro. Desenhar com Spiro te permite fazer curvas
que se reajustam à medida que você reposiciona os nós. Algumas pessoas preferem esta à abordagem comum (conhecida como
edição de B&eacute;zier), mas se você está acostumado à edição de B&eacute;zier, você pode achar que essa ferramenta faz
algumas coisas inesperadas.

### Faca

<img src="../en-US/images/knife.png" alt>

A ferramenta de Faca permite cortar segmentos em dois. Isso vem a calhar se você desenhou uma forma, mas
só precisa de uma parte dela.

### Régua

<img src="../en-US/images/ruler.png" alt>

A ferramenta de Régua fornece informações de medida e coordenada. Quando você a usa, ela mostra uma
‘caixa de dica’ flutuante próxima ao cursor. Se você mover o cursor sobre um ponto, a caixa te dá
informações ainda mais detalhadas de medida e coordenada. Se você deixar perto de um segmento, ela
dará informações sobre curvatura e raio. O mais útil, se você clica e arrasta a ferramenta
de régua, você verá a distância que você arrastou o cursor, mais cada interseção que você tiver
cruzado.

### As ferramentas de transformação

Existem seis ferramentas de transformação:

<img src="../en-US/images/transform_tools_labelled.png" alt>

**Nota:** Em qualquer ferramenta de transformação, se você der dois cliques, você poderá digitar valores
numéricos.

A ferramenta de Escala te permite redimensionar um objeto à mão livre. Pressionando a tecla Shift permite que você redimensione
um objeto enquanto mantém sua proporção.

A ferramenta de Rotação te permite rotacionar um objeto livremente. Ela rotaciona o objeto selecionado em torno da posição
que você clicar.

A ferramenta de Rotação 3D permite rotacionar um objeto na terceira dimensão, e projeta o resultado no
plano x-y.

A ferramenta de Inversão permite espelhar a seleção horizontalmente ou verticalmente. O ponto no qual
você clica com o mouse é o ponto de origem da transformação.

**Nota:** Após inverter um ponto, você provavelvemte vai querer aplicar a função Elemento &gt; *Sentido Correto*.

A ferramenta de Inclinação permite inclinar horizontalmente a seleção tanto no sentido horário como anti-horário.
<!-- (withershins is how the dialog refers to counterclockwise). -->

A ferramenta de Perspectiva dá outro modo de distorcer a forma de maneira não linear.

**Nota:** Não há opção numérica para a transformção de perspectiva.

### As ferramentas Retângulo/Elipse e Polígono/Estrela

Essas ferramentas criam formas geométricas primitivas, o que é mais rápido do que construi-las
a partir de segmentos de linha separados.

<img src="../en-US/images/rectangle_poly_labelled.png" alt>

Clicando na área da seta dessas ferramentas te dá a opção de trocar para a outra ferramenta.
Se você der dois cliques em qualquer uma dessas ferramentas, você pode abrir as opções do tipo de forma.

Opções do Retângulo: Estilo de canto e Caixa limitante ou Fora do centro.

Opções da Elipse: Caixa limitante ou Fora do centro.

Opções do Polígono: Número de vértices.

Opções da Estrela: Número de pontos da estrela e profundidade dos pontos por porcentagem. Quanto maior o valor dessa
porcentagem, mais longos serão os braços da estrela.

### Mse1 e Mse2

<img src="../en-US/images/danger.png" alt>

Na parte inferior da barra de ferramentas, você pode ver a ferramenta atual e as operações disponíveis para ambos botões do mouse:

- Botão Esquerdo (Mse1)
- Botão Esquerdo + Ctrl (^Mse1)
- Botão da roda do Mouse (Mse2)
- Botão da roda do Mouse + Ctrl (^Mse2)

Dessa forma, você pode usar algumas ferramentas diferentes sem ter que repetidamente clicar na barra de ferramentas.

<p class="warn"><b>Cuidado:</b> Parece que atualmente a funcionalidade do Mse não funciona
corretamente.</p>

### Camadas

A área de desenho do FontForge tem três camadas por padrão: a camada Guia, a camada Fundo, e a
camada Frente. Camadas de Guia são usadas para inserir guias (como as guias altura de x e altura da caixa alta).
Ambas as camadas de Frente e de Fundo são usadas para desenhar, mas apenas a camada de Frente
superior será renderizada na sua fonte final.

<img src="../en-US/images/layers.png" alt>

Uma caixa de seleção indica se cada camada está visível, e você pode desmarcá-la para tornar a camada invisível. O ‘C’ (ou ‘Q’) indica se você esta usando curvas Cúbicas ou Quadráticas.

O #, B, ou F indica se o tipo da cada camada é Guia, de Fundo, ou
de Frente, o que é releveante se você adicionar mais camadas. Você pode criar e remover
camadas adicionais usando os botões mais (+) ou menos (&minus;) nessa parte da barra de ferramentas.
O tipo de camada e o tipo de curva também podem ser controlados com um clique direito (uma vez que você tenha camadas
adicionais).

## Basic drawing

Next we will go over some basic drawing workflows, which you often find yourself in need of.

### Cutting a shape within another

1. Start by using the Rectangle tool to draw a rectangle within the drawing area of the Glyph
   window.
2. Next, use the Ellipse tool to draw an ellipse within the rectangle you just drew.  
   <img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_010.png" alt>
3. Go to the Element menu and choose *Correct Direction*. You will see that the two shapes merged,
   and that you essentially punched a hole in the center of the rectangle.  
   <img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_011.png" alt>

### Remove overlap

1. Add a star that overlaps the corner of the rectangle.  
   <img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_012.png" alt>
2. Select the star and the earlier shape. You only need to select one point of each overlapping
   shape, but it is okay to select extra points.
3. Go to Element &gt; Overlap &gt; *Remove overlap*. You will see that your two shapes have become
   one.  
   <img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_013.png" alt>

### Add a Point

Using the Pen tool, click and hold in the middle of a line segment, then drag the mouse to change
the shape.

<img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_014.png" alt>

### Tangent points

Select the bottom-left corner point of your new shape (the intersection of the curve and the
straight line). From the Point menu, you will see that *Corner Point* is checked. Select *Tangent*.
This changes the square node to a triangle, but that is all it does until you do the next step:
extending control points.

To do so, choose Element &gt; *Get Info*, which opens the Point Info Window. From the Location tab
in that window, go to the Next CP field set and set the Distance to a large number, such as 75.
Click OK. You will see that the curve now smoothly enters the straight line.

<img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_015.png" alt>

### Transformation

Now select about a quarter of the shape &mdash; the star and part of the ellipse in the middle.

<img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_016.png" alt>

Choose the 3D Rotate tool, move to the middle of the selected area, and slowly click and drag until
you see something you like, then release. Here is an example of 3D Rotate used on the practice
image:

<img src="../en-US/images/O%20at%2079%20from%20Untitled1%20-_017.png" alt>

### Set stroke shape and width

So far you have used the Freehand drawing tool to draw a line. If you double-click the Freehand
tool, you get the Freehand dialog shown here, which contains a drawing window. This is where you
select pen shape and size. This dialog also appears when you choose the *Expand Stroke* option in
the Element menu.

<img src="../en-US/images/Freehand_018.png" alt>

Using the Corner tool, draw a polygon and click OK.

Now, draw a line with the Freehand drawing tool. When you release the mouse button, the new path is
automatically stroked with the shape you chose in the Freehand dialog, as shown here.

<img src="../en-US/images/Q%20at%2081%20from%20Untitled1%20-_019.png" alt>

## Keep drawing!

You should continue to experiment with the drawing tools until you feel comfortable that you can use
them to draw and transform whatever shapes you need. At this point, you are equipped to start
constructing the components of glyphs, but you should also take time to look at FontForge’s other
set of tools.  
The next chapter, [“Drawing with Spiro”], describes the Spiro drawing mode. Spiro drawing is
distinct enough from B&eacute;zier curve editing that it requires an explanation of its own.

[“Drawing with Spiro”]: Drawing_With_Spiro.html

# Further Reading

A [TypeDrawers Forum Discussion on Beziers](http://typedrawers.com/discussion/967) included these links shared by Nina Stössinger <a href="https://twitter.com/ninastoessinger/status/593687255341998080">on twitter</a>:

* [Bezier Curves and Type Design: A Tutorial](http://learn.scannerlicker.net/2014/04/16/bezier-curves-and-type-design-a-tutorial/) by Fábio Duarte Martins
* [So What’s the Big Deal with Horizontal &amp; Vertical Bezier Handles Anyway?](http://theagsc.com/community/tutorials/so-whats-the-big-deal-with-horizontal-vertical-bezier-handles-anyway/)
* [Hand Lettering: How to Vector Your Letterforms](http://design.tutsplus.com/tutorials/hand-lettering-how-to-vector-your-letterforms--cms-23248) by Scott Biersack
* [Type Basics](http://typeworkshop.com/index.php?id1=type-basics&amp;id2=&amp;id3=&amp;id4=&amp;id5=&amp;idpic=15#pictloader) by Underware
* [The Bézier Game](http://bezier.method.ac) by Marc MacKay
