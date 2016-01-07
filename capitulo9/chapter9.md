#Patterns, masks, clip-path y symbol

##Patterns

Con los `patterns` vamos a rellenar un objeto con un patrón que previamente hemos definido. Los patrones se definen con la etiqueta `<pattern>` les daremos un ***ID*** para poder usarlos posteriormente sobre los elementos a los que queremos aplicar el patrón, esto lo haremos con `fill=”url(#nombreDelPatron)”`, es recomendable declarar los `patterns` dentro de las etiquetas `<defs>`.

Los atributos que tenemos disponibles para los ***patterns*** son los siguientes:

El atributo ***patternUnits*** tiene dos valores, el primero de ellos es ***userSpaceOnUse***, el cual hace que el patrón se repita a lo largo y ancho del objeto donde declaramos el patrón. El segundo es ***objectBoundingBox*** el cual hace que el patrón sólo se muestre una vez en el objeto  donde declaramos el patrón. El valor por defecto de este atributo es ***objectBoundingBox***.

Con el atributo ***patternTransform*** podemos añadir transformaciones como ***matrix translate scale skewX skewY*** a nuestros patrones.

Con el atributo ***x*** determinamos la posición del patrón en la coordenada del eje horizontal.

Con el atributo ***y*** determinamos la posición del patrón en la coordenada del eje vertical.

Con el atributo ***width*** determinamos la anchura del patrón.

Con el atributo ***height*** determinamos la altura del patrón.

Vamos a ver unos cuantos ejemplos con las diferentes opciones que tenemos a nuestra disposición.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-9/Capitulo-9-patterns.jpg)


~~~~~~~
<defs>
	<pattern id="patron" width="10" height="10" patternUnits="userSpaceOnUse">
	  <rect width="10" height="10" fill="white"/>
	  <rect width="10" height="5" fill="crimson"/>
	</pattern>
	<pattern id="patronDos" width="10" height="10" patternUnits="objectBoundingBox">
	  <rect y="50" width="100" height="50" fill="white"/>
	  <rect width="100" height="50" fill="crimson"/>
	</pattern>
	<pattern id="patronTres" width="40" height="40" patternUnits="userSpaceOnUse">
	  <circle cx="20" cy="20" r="20" fill="crimson"/>
	</pattern>
</defs>
<rect x="460" y="40" width="200" height="100" fill="url(#patron)" stroke="black" stroke-width=".5"/>
<rect x="460" y="160" width="200" height="100" fill="url(#patronDos)" stroke="black" stroke-width=".5"/>
<rect x="460" y="280" width="200" height="100" fill="url(#patronTres)" stroke="black" stroke-width=".5"/>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/EFycv/)

En el primer rectángulo el patrón tiene `patternUnits="userSpaceOnUse"` con lo cual el patrón se repetirá a lo largo del rectángulo.

En el segundo rectángulo el patrón tiene `patternUnits="objectBoundingBox"` con lo cual el patrón sólo se mostrará una vez, hay que tener en cuenta que para el ejemplo he modificado el tamaño del patrón, como se puede apreciar ocupa la mitad del rectángulo.

En el tercer rectángulo el patrón tiene `patternUnits="userSpaceOnUse"` pero en lugar de contener rectángulos en este caso contiene círculos.

####Soporte

![](images/soporte/primera.jpg)

##Mask

Con la etiqueta `<mask>` vamos a conseguir que cualquier objeto gráfico se pueda utilizar como una máscara alfa para la composición del objeto actual en el fondo. A la etiqueta `<mask>` le daremos un ***ID*** para para poder usarla posteriormente sobre los elementos a los que queremos aplicar `<mask>`, esto lo haremos con `mask=”url(#nombreDelMask)”`, es recomendable declarar los patterns dentro de las etiquetas `<defs>`.

Los atributos que tenemos disponibles para `<mask>` son los siguientes:

El atributo ***maskUnits*** define el sistema de coordenadas para los atributos ***x, y, width y height***  mediante el cuadro delimitador del elemento al que se aplica la máscara. El valor por defecto es ***objectBoundingBox***.

El atributo ***maskContentsUnits*** define el sistema de coordenadas de ***mask***. El valor por defecto es ***userSpaceOnUse***.

Con el atributo ***x*** determinamos la posición donde comenzará el `<mask>` en el eje horizontal. Por defecto su valor es de -10%.

Con el atributo y determinamos la posición donde comenzará el `<mask>` en el eje vertical. Por defecto su valor es de -10%.

Con el atributo ***width*** determinamos el ancho del `<mask>`. Por defecto su valor es de 120%.

Con el atributo ***height*** determinamos el alto del `<mask>`. Por defecto su valor es de 120%.

En el ejemplo que vamos a ver a continuación aplicamos el `<mask>` con forma de círculo a una imagen, he dejado por defecto todos los valores para que se aprecie mejor el resultado.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-9/Capitulo-9-mask.jpg)


~~~~~~~
<defs>
	<mask id="mask">
		<circle cx="50%" cy="50%" r="50%" fill="white"/>
	</mask>
</defs>
<image width="100%" height="100%" xlink:href="smilipostbox.svg" mask="url(#mask)"/>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/egqKC/)

####Soporte

![](images/soporte/primera.jpg)

##Clip-Path

Los trazados de recorte o máscaras de recorte se definen a través de la etiqueta `<ClipPath>`, para determinar cual es el trazado u objeto a recortar simplemente debemos de incluirlo dentro de la etiqueta `<ClipPath>`, a la cual añadiremos un ***ID*** para luego aplicar el resultado al objeto que nosotros queramos con `clip-path="url(#nombreDelClipPath)"`, es recomendable incluirla dentro de `<defs>`.

En el ejemplo que vamos a ver el trazado de recorte es un círculo que actúa sobre un rectángulo, el resultado es un semicírculo ya que en el trazado de recorte le hemos indicado que comience en la coordenada 390 del eje horizontal. Para que se aprecie mejor donde actúa el trazado de recorte he creado otro rectángulo de las mismas medidas pero solamente con un borde negro.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-9/Capitulo-9-clipPath.jpg)


~~~~~~~
<defs>
	<clipPath id="recorte">
		<circle cx="390" cy="120" r="60"/>
	</clipPath>
</defs>
<rect width="400" height="250" clip-path="url(#recorte)" fill="crimson"/>
<rect width="400" height="250" fill="none" stroke="black" stroke-width="1"/>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/bBaez/)


Vamos a ver otro ejemplo donde vamos a utilizar `<clipPath>` con texto, este recorte lo vamos a aplicar a un `<g>`, el cual esta compuesto por dos ***crimson*** y el otro de color ***yellowgreen***.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-9/Capitulo-9-clipPathtexto.jpg)


~~~~~~~
<defs>
	<clipPath id="texto">
		<text class="arial" x="100" y="100"> Hola que pasa que tal</text>
	</clipPath>
</defs>
<g clip-path="url(#texto)">
    <rect width="1000px" height="100px" fill="crimson"/>
    <rect x="0" y="78" width="1000px" height="100px" fill="yellowgreen"/>
</g>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/DuErx/)

####Soporte

![](images/soporte/primera.jpg)

##Symbol

El elemento ***symbol*** es usado para definir objetos gráficos que luego vamos a utilizar a través del elemento `<use>`, para ello primero tenemos que darle un ***id*** a `<symbol>` y referenciar ese ***id*** a través de `<use>` con `xlink:href=””` para que se muestre en el documento. Todo lo que está incluído dentro de las etiquetas `<symbol>` no se va a ver en el documento a no ser que como ya hemos dicho anteriormente utilicemos el elemento `<use>`. Tenemos a nuestra disposición los atributos ***viewBox*** y ***preserveAspectRatio***.

Vamos a ver un ejemplo donde creamos un rectángulo con cuatro rectángulos cada uno de un color diferente.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-9/Capitulo-9-symbol.jpg)


~~~~~~~
<symbol id="prueba">
	<rect x="0" y="0" width="50" height="50" fill="crimson"/>
	<rect x="50" y="0" width="50" height="50" fill="yellowgreen"/>
	<rect x="0" y="50" width="50" height="50" fill="beige"/>
	<rect x="50" y="50" width="50" height="50" fill="indigo"/>
</symbol>

<use xlink:href="#prueba" x="300" y="250"/>
<use xlink:href="#prueba" x="350" y="300"/>
<use xlink:href="#prueba" x="400" y="350"/>

~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/iwCuk/)

####Soporte

![](images/soporte/primera.jpg)