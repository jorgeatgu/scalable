# Las formas básicas

En este capítulo vamos a ver las diferentes formas y trazados que tenemos a nuestra disposición para dibujar en **SVG**. Las formas básicas son la pieza fundamental para dibujar todo tipo de figuras y trazados.

Antes de comenzar a ver las diferentes formas básicas vamos a ver dos atributos que tienen en común y que vamos a ir viendo a lo largo del libro como ***fill*** y ***stroke***.

## Fill

Para añadir color a los diferentes objetos lo vamos a hacer a través del atributos ***fill*** para rellenar objetos y ***stroke*** para rellenar los bordes, podemos hacerlo utilizando diferentes métodos.


~~~~~~~
	fill=”rgba(255,255,255,0.75)”
	fill=”rgb(255,255,255)”
	fill=”rgb(100%,100%,100%)”
	fill=”#FFFFFF”
	fill=”#FFF”
	fill=”white”
~~~~~~~


Además de poder rellenarlos con color, los atributos ***fill*** y ***stroke*** también admiten `<gradients>`, `<text>` y `<patterns>`, todos estos elementos los iremos viendo en capítulos posteriores.

La opacidad del relleno la podemos modificar a través del atributo `fill-opacity=””`

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-fill-opacity.jpg)


~~~~~~~
<rect x="410" y="50" fill="coral" width="300" height="100" fill-opacity=".9"/>
<rect x="410" y="210" fill="coral" width="300" height="100" fill-opacity=".5"/>
<rect x="410" y="370" fill="coral" width="300" height="100" fill-opacity=".2"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/GfDEy/)

También tenemos la posibilidad a través del atributo ***fill-rule*** de determinar si una parte del trazado forma parte del relleno o esta fuera de el, para ello tenemos ***nonzero*** que es su valor por defecto y ***evenodd***, con el cual conseguimos el efecto del primer rectángulo que vemos en la imagen.

En el ejemplo a través de un `<path>` he dibujado dos rectángulos, en el código lo he diferenciado añadiendo un retorno para que queden bien diferenciadas uno del otro, otra manera de saber cuando termina un trazado es buscar en el código la letra Z o z, esta corresponde al comando closepath(que vamos a ver más adelante) y con este comando le decimos que cierre el trazado.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-fill-rule.jpg)


~~~~~~~
<path fill="crimson" fill-rule="evenodd" d="M423.7,472.1H165.1c-6.6,0-12-5.4-12-12V201.5c0-6.6,5.4-12,12-12h258.6c6.6,0,12,5.4,12,12v258.6 C435.7,466.7,430.3,472.1,423.7,472.1z

M353.4,401.8h-118c-6.6,0-12-5.4-12-12v-118c0-6.6,5.4-12,12-12 h118c6.6,0,12,5.4,12,12v118C365.4,396.4,360,401.8,353.4,401.8z"/>

<path fill="crimson" fill-rule="nonzero" d=" M423.7,472.1H165.1c-6.6,0-12-5.4-12-12V201.5c0-6.6,5.4-12,12-12h258.6c6.6,0,12,5.4,12,12v258.6 C435.7,466.7,430.3,472.1,423.7,472.1z

M353.4,401.8h-118c-6.6,0-12-5.4-12-12v-118c0-6.6,5.4-12,12-12 h118c6.6,0,12,5.4,12,12v118C365.4,396.4,360,401.8,353.4,401.8z"/>
~~~~~~~

La primera figura tiene la propiedad evenodd por lo tanto el segundo rectángulo se va a quedar sin rellenar.

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/bEBHm/)


## Stroke

Con el atributo ***stroke*** es con el que vamos a definir el borde de los objetos y también su relleno, forma, acabado y grosor.

Con el atributo ***stroke-width*** vamos a definir el grosor de la línea.

Con el atributo ***stroke-opacity*** vamos a definir la opacidad que va a tener la línea.

Con el atributo ***stroke-dasharray*** vamos a definir la longitud de las líneas y el espacio que las separa a través de dos valores.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-stroke-dasharray.jpg)


~~~~~~~
<line x1="100" x2="500" y1="50" y2="50" stroke="crimson" stroke-width="15" stroke-dasharray="15 10"/>
<line x1="100" x2="500" y1="100" y2="100" stroke="coral" stroke-width="15" stroke-dasharray="10 15"/>
<line x1="100" x2="500" y1="150" y2="150" stroke="green" stroke-width="15" stroke-dasharray="15 5"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/EnpBv/)

Con el atributo ***stroke-dashoffset*** vamos a definir la distancia a la que queremos que comiencen los guiones. Este atributo admite valores negativos y lo podemos expresar en porcentajes.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-stroke-dashoffset.jpg)


~~~~~~~
<line x1="100" x2="500" y1="50" y2="50" stroke="crimson" stroke-width="15" stroke-dasharray="15 10" stroke-dashoffset="0" />
<line x1="100" x2="500" y1="100" y2="100" stroke="coral" stroke-width="15" stroke-dasharray="15 10" stroke-dashoffset="-405"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/ptzhK/)

Con el atributo ***stroke-linecap*** podemos modificar la forma inicial y final de la línea, para ello disponemos de tres opciones, la primera es ***butt*** que es el valor por defecto, la segunda ***round*** que redondea la forma y aumenta el tamaño de la línea y por último ***square*** que mantiene la forma rectangular pero también aumenta el tamaño de la línea.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-stroke-linecap.jpg)


~~~~~~~
<line x1="100" x2="500" y1="50" y2="50" stroke="crimson" stroke-width="25"/>
<line x1="100" x2="500" y1="100" y2="100" stroke="coral" stroke-width="25" stroke-linecap="round"/>
<line x1="100" x2="500" y1="150" y2="150" stroke="green" stroke-width="25" stroke-linecap="square"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/msxhd/)

Con el atributo ***stroke-line-join*** vamos a determinar la forma que van a tener las esquinas de los trazados y de las formas básicas. Su valor por defecto es ***miter***, para redondearlas tenemos ***round*** y para que tengan forma de bisel tenemos ***bevel***.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-stroke-linejoin.jpg)


~~~~~~~
<rect width="200" height="200" x="120" y="150" fill="none" stroke="crimson" stroke-width="40" stroke-linejoin="miter"/>
<rect width="200" height="200" x="500" y="150" fill="none" stroke="coral" stroke-width="40" stroke-linejoin="round"/>
<rect width="200" height="200" x="880" y="150" fill="none" stroke="green" stroke-width="40" stroke-linejoin="bevel"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/IalzF/)


Con el atributo ***stroke-miterlimit*** vamos a comparar la longitud del ángulo con la anchura del trazado. Cuando se supere el valor que le hemos dado la unión sera biselada. Su valor por defecto es de 4.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-stroke-miterlimit.jpg)


~~~~~~~
<polyline points="100,100 140,60 180,100 220,60 260,100 300,60 340,100" fill="none" stroke="crimson" stroke-width="20" stroke-miterlimit="1"/>
<g transform="translate(0,100)">
<polyline points="100,100 140,60 180,100 220,60 260,100 300,60 340,100" fill="none" stroke="crimson" stroke-width="20" stroke-miterlimit="4"/>
</g>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/KirLC/)

## Rect

Para generar rectángulos tenemos la etiqueta `<rect>`. A continuación vamos a ver los diferentes atributos que admite esta etiqueta.

Con el atributo ***x*** determinamos la posición de la coordenada en el eje horizontal.

Con el atributo ***y*** determinamos la posición de la coordenada en el eje vertical.

Con el atributo ***width*** determinamos la anchura del rectángulo.

Con el atributo ***height*** determinamos la altura del rectángulo.

Con el atributo ***fill*** determinamos el color de relleno del rectángulo.

Con el atributo ***stroke*** determinamos el color de relleno del borde del rectángulo.

Con el atributo ***stroke-width*** determinamos el grosor del borde del rectángulo.

Para que los rectángulos tengan las esquinas redondeadas tenemos los atributos `rx=””` para el eje horizontal, y `ry=””` para el eje vertical. Si solamente indicamos un valor en `rx=””` este también servirá para `ry=””`.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-rect.jpg)


~~~~~~~
<rect x="500" y="100" width="150" height="150" fill="crimson" stroke="blue" stroke-width="10"/>
<rect x="500" y="300" width="150" height="150" fill="blue" stroke="crimson" stroke-width="10" rx="50"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/rBwfo/)


## Circle

Para generar círculos tenemos la etiqueta `<circle>`. A continuación vamos a ver los diferentes atributos que admite esta etiqueta.

Con el atributo ***cx*** determinamos la posición central del círculo en la coordenada del eje horizontal.

Con el atributo ***cy*** determinamos la posición central del círculo en la coordenada del eje vertical.

Con el atributo ***r*** determinamos el radio que tendrá el círculo.

Con el atributo ***fill*** determinamos el color de relleno del círculo.

Con el atributo ***stroke*** determinamos el color de relleno del borde del círculo.

Con el atributo ***stroke-width*** determinamos el grosor del borde del círculo.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-circle.jpg)


~~~~~~~
<circle r="90" cx="630" cy="230" fill="crimson" stroke="navajowhite" stroke-width="10"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/Frlnx/)

## Ellipse

Para generar elipses tenemos la etiqueta `<ellipse>`. A continuación vamos a ver los diferentes atributos que admite esta etiqueta.

Con el atributo ***cx*** determinamos la posición central de la elipse en la coordenada del eje horizontal.

Con el atributo ***cy*** determinamos la posición central de la elipse en la coordenada del eje vertical.

Con el atributo ***rx*** determinamos el radio que tendrá la elipse a lo largo del eje horizontal.

Con el atributo ***ry*** determinamos el radio que tendrá la elipse a lo largo del eje vertical.

Con el atributo ***fill*** determinamos el color de relleno de la elipse.

Con el atributo ***stroke*** determinamos el color de relleno del borde de la elipse.

Con el atributo ***stroke-width*** determinamos el grosor del borde de la elipse.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-ellipse.jpg)


~~~~~~~
<ellipse rx="90" ry="230" cx="630" cy="280" fill="crimson" stroke="navajowhite" stroke-width="10"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/Gbzit/)

## Line

Para dibujar líneas tenemos la etiqueta `<line>`. A continuación vamos a ver los diferentes atributos que admite esta etiqueta.

A la etiqueta `<line>` le asignamos los siguientes atributos:

Con el atributo ***x1*** determinamos la posición donde comienza la línea a lo largo del eje horizontal.

Con el atributo ***y1*** determinamos la posición donde comienza la línea a lo largo del eje vertical.

Con el atributo ***x2*** determinamos la posición donde finaliza la línea a lo largo del eje horizontal.

Con el atributo ***y2*** determinamos la posición donde finaliza la línea a lo largo del eje vertical.

Con el atributo ***stroke*** determinamos el color de relleno de la línea.

Con el atributo ***stroke-width*** determinamos el grosor de la línea.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-line.jpg)


~~~~~~~
<line x1="400" y1="200" x2="700" y2="200" stroke="crimson" stroke-width="10"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/dFLlh/)

Tenemos un camino más fácil para generar solamente una línea, para ello tenemos que utilizar los atributos ***x2*** e ***y2***, hay que tener en cuenta que de esta manera no vamos a poder obtener una línea recta.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-lineDos.jpg)


~~~~~~~
<line x2="700" y2="200" stroke="crimson" stroke-width="10"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/zAFoJ/)


## Polyline

Para generar varias líneas seguidas tenemos la etiqueta `<polyline>`. A continuación vamos a ver los diferentes atributos que admite esta etiqueta.

Con el atributo ***points*** determinamos las coordenadas en las que queremos dibujar las líneas. Este atributo funciona con pares de coordenadas que van separados por comas, el primer valor corresponde a la coordenada ***x***, el segundo valor corresponde a la coordenada ***y***. Para utilizar esta etiqueta necesitaremos como mínimo un par de coordenadas.

Con el atributo ***fill*** determinamos el color de relleno del polyline.

Con el atributo ***stroke*** determinamos el color de relleno del borde del polyline.

Con el atributo ***stroke-width*** determinamos el grosor del borde del polyline.

Antes de continuar voy a hacer una aclaración, como podéis ver en la lista de atributos tenemos a nuestra disposición ***fill***, el cual como hemos visto en varias ocasiones sirve para rellenar el fondo de un elemento del color que le indicamos, en `<polyline>` y aunque el trazado no está cerrado por defecto nos va a aplicar un relleno de color negro, pero ¿que rellena? pues traza una línea imaginaria desde el último punto hasta el primer punto y la rellena de negro, así que hay que decirle que `fill=”none”` o indicarle el color que nosotros queramos.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-polyline.jpg)


~~~~~~~
<polyline points="100,140 140,140 140,180 180,180 180,220 220,220 220,260" fill="none" stroke="crimson" stroke-width="20" />
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/zLvEk/)


## Polygon

Para generar una forma poligonal tenemos la etiqueta `<polygon>`. A continuación vamos a ver los diferentes atributos que admite esta etiqueta.

El atributo ***points*** funciona con pares de coordenadas que van separados por comas, el primer valor corresponde a la coordenada ***x***, el segundo valor corresponde a la coordenada ***y***. La propia etiqueta será la encargada de cerrar el trazado.

Con el atributo ***fill*** determinamos el color de relleno del polígono.

Con el atributo ***stroke*** determinamos el color de relleno del borde del polígono.

Con el atributo ***stroke-width*** determinamos el grosor del borde del polígono.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-polygon.jpg)


~~~~~~~
<polygon points="200,100 250,180 10,210" fill="none" stroke="crimson" stroke-width="20"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/HbJlq/)

## Path

La etiqueta `<path>` es la piedra angular de las formas básicas, es la que suelen utilizar los programas de gráficos vectoriales como **Adobe Illustrator, Sketch y Inkscape** a la hora de exportar **SVG**. Esta etiqueta no es nada fácil de usar por la cantidad de comandos que tenemos a nuestra disposición, siendo honesto la verdad es que he recurrido pocas veces a sus uso por la complejidad que conlleva el dibujar a mano este tipo de trazados.

A continuación vamos a ver una serie de comandos para dibujar con `<path>`, todos ellos están representado con una letra, y esta puede ser en mayúscula o en minúscula, la letra mayúscula representa coordenadas absolutas para el sistema de coordenadas actual, y la letra minúscula es relativa, lo cual quiere decir que es relativa con la posición del último comando que dibujo en el trazado. Vamos a ver un ejemplo que nos va a aclarar a la perfección esta pequeña pero gran diferencia.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-path-absolutas-relativas.jpg)

Estas dos líneas como podemos apreciar en el código comparten las mismas coordenadas, la única diferencia que podemos ver es que las coordenadas del primer `<path>` están acompañadas por letras mínusculas lo cual las convierte en coordenadas relativas aumentando considerablemente la longitud del trazado, la primera coordenada le dice que comience en 425,225 y la segunda coordenada que se desplace 475pixels a lo largo de la coordenada horizontal y 175pixels a lo largo de la coordenada vertical. Las coordenadas del segundo `<path>` están acompañadas por letras mayúsculas lo cual las convierte en absolutas, así el trazado comienza igualmente en 425,225 pero solamente se desplaza hasta la coordenada 475,275, es decir 50pixels en su coordenada horizontal y otros 50 en su coordenada vertical.


~~~~~~~
<path stroke-width="10" d="m425,225 l475,275 l575,175 l675,275" stroke="crimson" fill="none"/>
<path stroke-width="10" d="M425,225 L475,275 L575,175 L675,275" stroke="blue" fill="none"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/KLsjI/)


### Moveto

Con el comando ***moveto*** movemos un punto a una coordenada(x, y) sin dibujar ningún trazado.

Los comandos en mayúsculas indican posiciones absolutas.
Los comandos en minúsculas indican posiciones relativas.

| Comando  | Coordenada | Nombre
| ------------- | ------------- | -------------
| M | x y  | moveto
| m  | x y  | moveto

### Lineto

Con el comando ***lineto*** creamos una línea hasta la coordenada(x y) indicada.

Los comandos en mayúsculas indican posiciones absolutas.
Los comandos en minúsculas indican posiciones relativas.

| Comando  | Coordenada | Nombre
| ------------- | ------------- | -------------
| L | x y  | lineto
| l  | x y  | lineto

A continuación vamos a ver un ejemplo utilizando ***moveto*** y ***lineto***.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-moveto.jpg)


~~~~~~~
<path stroke-width="10" d="M425,225 L475,275 L575,175 L675,275" stroke="crimson" fill="none"/>
~~~~~~~

Con `M424,225` = le indicamos que el path comience en las coordenadas `x=”424” y=”225”`

Con `L475,275` = le indicamos que dibuje una línea hasta la coordenada `x=”475 y=”275”`

Con `L575,175` = le indicamos que dibuje una línea hasta la coordenada `x=”575 y=”175”`

Con `L675,275` = le indicamos que dibuje una línea hasta la coordenada `x=”675 y=”275”`

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/vHAKB/)

### Horizontal Lineto

Con el comando ***horizontal lineto*** creamos una línea horizontal hasta la coordenada ***x*** que le indiquemos.

Los comandos en mayúsculas indican posiciones absolutas.
Los comandos en minúsculas indican posiciones relativas.

| Comando  | Coordenada | Nombre
| ------------- | ------------- | -------------
| H | x | horizontal lineto
| h  | x | horizontal lineto

### Vertical lineto

Con el comando ***vertical lineto*** creamos una línea vertical hasta la coordenada ***y*** que le indiquemos.

Los comandos en mayúsculas indican posiciones absolutas.
Los comandos en minúsculas indican posiciones relativas.

| Comando  | Coordenada | Nombre
| ------------- | ------------- | -------------
| V | y | vertical lineto
| v  | y | vertical lineto

Vamos a ver los dos comandos en el mismo ejemplo.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-path-horizontalto.jpg)


~~~~~~~
<path stroke-width="10" d="M300,10 H790" stroke="crimson"/>
<path stroke-width="10" d="M300,10 V500" stroke="blue"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/pLCts/)

### Curveto

Con el comando ***curveto*** creamos un curva ***Bezier*** con las coordenadas ***x1 y1 x2 y2 x y*** que le indiquemos.

Los comandos en mayúsculas indican posiciones absolutas.
Los comandos en minúsculas indican posiciones relativas.

| Comando  | Coordenada | Nombre
| ------------- | ------------- | -------------
| C | x y x1 y1 x2 y2 | curveto
| c  | x y x1 y1 x2 y2 | curveto

En el ejemplo que vamos a ver a continuación el trazado comienza con `M130,130`. La curva se empieza a generar con `C440,440` continúa con `560,540` y finaliza con `770,430`.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-curveTo.jpg)


~~~~~~~
<path stroke-width="10" d="M130 130 C440 440, 560 540, 770 430" stroke="crimson" fill="none"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/GvEIe/)

### Smooth curveto

Con el comando ***smooth curveto*** creamos una curva más suave hasta la coordenadas ***x y x2 y2*** que le indiquemos.

Los comandos en mayúsculas indican posiciones absolutas.
Los comandos en minúsculas indican posiciones relativas.

| Comando  | Coordenada | Nombre
| ------------- | ------------- | -------------
| S | x y x2 y2 | smooth curveto
| s  | x y x2 y2 | smooth curveto

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-smoothCurveTo.jpg)


~~~~~~~
<path stroke-width="10" d="M130 130 s440 440, 560 50" stroke="crimson" fill="none"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/cApLg/)

### Quadratic Bezier curveto y Smooth quadratic bezier curveto

Con el comando ***quadratic Bezier curveto*** creamos una curva(***quadratic Bezier***) hasta la coordenada ***x1,y1 x,y*** que le indiquemos.

Con el comando ***smooth quadratic bezier curveto*** creamos una curva(quadratic Bezier) suave hasta la coordenada ***x,y*** que le indiquemos.

Los comandos en mayúsculas indican posiciones absolutas.
Los comandos en minúsculas indican posiciones relativas.

El trazado comienza en `200,300`.

La primera coordenada de Q(quadratic bezier) corresponde a ***x1,y1*** en este caso va hasta `400,50`.

La segunda coordenada de Q(quadratic bezier) corresponde a ***x,y*** en este caso va hasta `600,30`.

La coordenada de T(smooth quadratic bezier) corresponde a ***x,y*** en este caso se prolonga hasta `1000,300`.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-smoothCuadraticCurveTo.jpg)


~~~~~~~
<path stroke-width="10" d="M200,300 Q400,50 600,300 T1000,300" fill="none" stroke="crimson" stroke-width="2"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/Jfgjh/)

### Elliptical arc curve

Con el comando ***arc*** dibujamos un arco elíptico desde las coordenadas ***x*** e ***y***. El tamaño y la orientación de la elipse están definidos por dos radios ***rx*** e ***ry*** y un eje de rotación ***x***. El centro de la elipse se determina con ***cx*** y ***cy***.

| Comando  | Coordenada | Nombre
| ------------- | ------------- | -------------
| A | rx ry x-eje large-arc-flag sweep-flag | smooth curveto
| a  | rx ry x-eje large-arc-flag sweep-flag | smooth curveto

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-4/Capitulo-4-path-arc.jpg)


~~~~~~~
<path stroke-width="10" d="M343,267 A150,203 0 1,0 31,359 z" stroke="crimson" fill="none"/>
~~~~~~~

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/oyuir/)

Este arco lo he realizado con una herramienta online creada por **Benjamin Ranck** que ayuda bastante a comprender el funcionamiento de este comando, a continuación os dejo el [enlace](http://blog.benjaminranck.com/2011/07/28/arc-paths-in-svg).


### Closepath

Y para terminar con el `<path>` y  las formas básicas vamos a ver el comando ***closepath***, simplemente tenemos que añadir al final de nuestras coordenadas una  ***Z*** o ***z***, con este comando cerramos el trazado actual trazando una línea recta que va desde el último punto al punto inicial del trazado.

####Soporte

![](images/soporte/primera.jpg)

En este capítulo el soporte de los navegadores es total a todas las formas básicas que hemos visto a lo largo del capítulo.
