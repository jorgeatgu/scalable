#WAI-ARIA en SVG
Antes de nada una pequeña introducción para aquellos que no sepan de que trata **WAI-ARIA**.

**WAI-ARIA** es el acrónimo de **Web Accessibility Initiate Accessible Rich Internet Application**, un standard de la **W3C** que tiene el fin de hacer que las webs sean accesibles para las personas con discapacidad. Para ello disponemos de una serie de atributos que funcionan como identificadores y que vamos a utilizar a lo largo de las diferentes etiquetas que tengamos en el **HTML**.

A continuación os dejo un enlace con una serie de indicaciones de la **W3C** para usar [WAI-ARIA en HTML5](http://www.w3.org/TR/2013/WD-aria-in-html-20131003/).

La incorporación de **WAI-ARIA** a la especificación de **SVG** será realidad en **SVG 2**, aún así podemos utilizar una serie de atributos y etiquetas para hacer más accesible nuestros archivos.

##SVG 1.1

Para hacer más accesibles nuestros **SVG** vamos a utilizar las etiquetas `<tittle>` y `<desc>`. Estas etiquetas sirven para añadir un título y una descripción a nuestro archivo. Para hacer más accesible nuestro documento las podemos utilizar a lo largo del documento en cualquier elemento gráfico o contenedor gráfico que vayamos a utilizar.

Como ya he dicho anteriormente el soporte de **WAI-ARIA** en **SVG** será oficial en **SVG 2** pero aunque no sea oficial podemos hacer uso de la etiquetas `aria-labelledby=””` en **SVG 1.1** para hacer más accesibles nuestros archivos para los navegadores, vamos a añadirla a la etiqueta principal de `<svg>` con los valores title y dec.

A continuación el código que he empleado con [VoiceOver](https://www.apple.com/es/accessibility/osx/voiceover/) y [ChromeVox](http://www.chromevox.com/)


~~~~~~~
<title id="title">Los patterns en SVG.</title>
<desc id="desc">A continuación vamos a ver tres ejemplos que utilizan la etiqueta patterns sobre elementos gráficos.</desc>
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
	<g>
	<title>Primer ejemplo. El rectángulo se rellena por completo con un pattern creado con un rectángulo blanco y otro rojo.</title>
		<rect x="460" y="40" width="200" height="100" fill="url(#patron)" stroke="black" stroke-width=".5"/>
    </g>
	<g>
	<title>En este segundo ejemplo solamente se rellena la mitad del rectángulo gracias al atributo patternUnits que tiene un valor de objectboundigBox.</title>
		<rect x="460" y="160" width="200" height="100" fill="url(#patronDos)" stroke="black" stroke-width=".5"/>
	</g>
	<g>
	<title>En el último ejemplo el rectángulo se rellena por completo con un pattern que consta de un círculo rojo. </title>
		<rect x="460" y="280" width="200" height="100" fill="url(#patronTres)" stroke="black" stroke-width=".5"/>
	</g>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/IKrGu/)

A continuación os dejo un enlace a un vídeo donde podéis ver el ejemplo en funcionamiento utilizando **VoiceOver de OSX con Safari 7, Firefox 30, Chrome 35 y Opera 22**.

[VoiceOver](http://vimeo.com/jorgeatgu/scalable-voiceover-wai-aria)

En el próximo vídeo vamos a ver en funcionamiento la extensión **ChromeVox** para **Google Chrome**.

[ChromeVox](http://vimeo.com/jorgeatgu/scalable-chrome-vox)

Tenemos que tener en cuenta que si utilizamos las etiquetas `<img>` `<object>` `<embed>` `<iframe>` los screenreaders no van a leer absolutamente nada del código que contenga nuestro archivo **SVG**.


##SVG 2

A día de hoy **SVG** 2 todavía no se ha convertido en recomendación de la **W3C**, aún se están discutiendo asuntos en las listas de correo y meetings de la **W3C**, y aunque el roadmap indicaba que sería para agosto al final se va a retrasar para finales de 2014. Así que por desgracia todavía queda un tiempo para que se implemente **WAI-ARIA** en **SVG**. Por ahora lo más interesante que podemos ver en la sección de **WAI-ARIA** es una tabla con toda la lista de elementos que tenemos disponibles en **SVG** y cada uno de ellos acompañado por su [atributo](https://svgwg.org/svg2-draft/struct.html#WAIARIAAttributes)

###Guía de accesibilidad de la **W3C** sobre **SVG**

Esta guía solamente es de carácter informativo, he seleccionado los puntos más relevantes, podéis ver todos en este [enlace](http://www.w3.org/TR/SVG/access.html).

####Acompañar los gráficos con texto.

Cuando el texto de un un gráfico explica su función, no necesitamos un texto.
Utiliza la etiqueta `<title>` cuando el significado de un texto no esté lo suficientemente claro.

Cuando un gráfico no incluye un texto explicativo. Si el texto es complicado podemos usar la etiqueta `<desc>`.

Si el gráfico está compuesto de varias partes podemos acompañar cada parte de una descripción.


####No confiar sólo en el color

No usar el color para transmitir información.

Asegurarse de utilizar un contraste adecuado. Utilizar **CSS** para los usuarios que necesitan cierta combinación de colores.

####Utilizar el lenguaje de marcado y CSS de manera adecuada.

El texto siempre debe de ir como texto, nunca como imagen o texto rasterizado.

Separar la estructura de la presentación.

Usar la etiqueta g y descripciones para estructurar nuestros documentos. Reutilizar objetos.

Utilizar unidades relativas en **CSS**.

Utilizar **MathML** para representar fórmulas matemáticas.

####Indicar el lenguaje que usamos

A través de la etiqueta `xml:lang` podemos identificar el contenido del lenguaje que vamos a utilizar.

####Responsive y accesibilidad

Si queremos hacer más accesibles nuestros **SVG** no deberíamos de hacer **responsive** nuestros archivos eliminando de la etiqueta principal `<svg>` los atributos ***width*** y ***height***, si suprimimos estos atributos los documentos se adaptan a la pantalla pero cualquier tipo de zoom que hagamos desde los navegadores no va a tener ningún efecto.

##Describler

Es una herramienta web creada por **Doug Scheepers** para hacer más accesibles nuestros **SVG**.

Una vez que estamos en la web de [describler](http://describler.com/) tenemos que subir nuestros archivos **SVG**, cuando lo hayamos subido veremos todo el código de nuestro archivo a la derecha, la propia herramienta se encarga de añadir `<title>` y `<desc>` a cada uno de nuestros elementos, podemos incluir un título y una descripción a nuestros elementos y una vez que hayamos terminado podemos escuchar lo que interpreta un ***screenreader***, la voz es en inglés, así que cualquier texto en castellano estará interpretado por una voz inglesa. Por último tenemos la opción de descargarnos el archivo con todas las etiquetas que hemos incluído. Mucho ojo ya que deja el ***width*** y el ***height*** 100% de tamaño lo cual inhabilita el zoom en los navegadores.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-13/wai-aria-describler.jpg)


