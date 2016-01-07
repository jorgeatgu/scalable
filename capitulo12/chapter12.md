# Optimizar SVG

A la hora de exportar tanto **Illustrator, Sketch y Inkscape** generan demasiado código que en el fondo no nos sirve para nada. A lo largo del libro hemos ido conociendo las diferentes etiquetas para así poder sustituir esos `<path>` imposibles por su forma básica correspondiente con el consecuente ahorro de líneas de código. Ahora vamos a comprimir más si cabe nuestros archivos utilizando dos programas para optimizar, eso sí, siempre con mucho cuidado y sabiendo de antemano que opciones tenemos a nuestra disposición para reducir nuestros archivos.

Antes de nada una recomendación que más bien es una obligación. Nunca paséis por estos programas vuestro archivos principales, pasad siempre una copia ya que sino luego es un galimatías el intentar entender todo el código que ha sido comprimido, también hay que comprobar el resultado de la compresión abriendo el archivo en un navegador y comparándolo con su versión sin comprimir. A veces la compresión puede destrozar algunos elementos.

A continuación vamos a ver dos soluciones gratuitas para llevar a cabo la optimización.

##SVG CLEANER

Lo primero que vamos a hacer es descargar el programa, en estos momentos va por su versión 0.6.2, para ello podemos ir a su repositorio de **GitHub** o por el contrario vamos directamente a qt-apps.org que es donde esta alojado, allí tenemos a nuestra diposición las versiones de [OSX, Linux y Windows](http://qt-apps.org/content/show.php/SVG+Cleaner?content=147974).

Una vez descargado e instalado vamos a abrir el programa, una vez que el programa este abierto vamos a pinchar en el primer icono el cual tiene forma de varita mágica, nos saltara un menú con seis opciones, ahora vamos a ir viendo por separado cada una de estas pantallas.

###FILES
Es la primera pantalla, arriba a la derecha tenemos dos iconos, el primero de ellos sirve para añadir archivos sueltos y el segundo de ellos para añadir carpetas, una vez añadidos los archivos vamos a verlos reflejados en la pantalla, si por lo que fuera se cuela algún archivo que no queremos optimizar tenemos la opción de borrarlo o de desmarcarlo para que no sea optimizado.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svg-cleaner-files.jpg)

En la parte inferior tenemos las tres opciones de las que disponemos para guardar los archivos. La primera guarda los archivos en la carpeta que le indiquemos, la segunda guardará los archivos en la misma carpeta que los originales pero nos da la opción de añadir un prefijo o sufijo al nombre del archivo para así no sobreescribir el original. La última opción que tenemos es la sobreescribir el archivo original, esta última la vamos a descartar a no ser que ya tengamos hecha una copia del original.

###Preferences
Aquí podemos indicar el nivel de optimización que queramos, puede ser ***basic, complete, extreme o custom***.
![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svg-cleaner-preferences.jpg)

###Elements
En primer lugar tenemos los elementos, destacar de todos ellos la limpieza que hace de los ***namespaces*** de los elementos que generan los programas que exportan **SVG**.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svg-cleaner-elements.jpg)

###Attributes
Ahora vamos con los atributos, cosas a destacar, que elimine todos los atributos que vengan con su valor por defecto y también aquellos que no tienen un valor declarado.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svg-cleaner-attributtes.jpg)

###Paths
Convierte las coordenadas absolutas en relativas. Elimina los símbolos que son innecesarios.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svg-cleaner-paths.jpg)

###Optimizations
Por último vamos con las optimizaciones, simplifica los colores que estén en hexadecimal, y hace algo que no me gusta que es convertir las formas básicas en trazados.

Las últimas tres opciones nos sirven para eliminar o redondear decimales, esto nos va a servir de gran utilidad si nuestros SVG proceden de programas como **Inkscape** en los que no tenemos la oportunidad de seleccionar con cuantos decimales queremos que se exporte nuestro **SVG**.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svg-cleaner-optimizations.jpg)

**SVGCLEANER** también está disponible para [descargar desde GitHub](https://github.com/RazrFalcon/SVGCleaner)


##SVGO

**SVG Optimizer** es una herramienta basada en **Node-JS** para optimizar **SVG**. Esta disponible como módulo de **Node-JS**, un módulo de Mimosa, como una tarea de **Grunt**, tarea de **Gulp**, como una carpeta de acción en **OSX** y por último tenemos la opción de utilizarlo en **OSX y Windows** con interfaz gráfica. Podemos descargarlo desde su **GitHub**.

Para el ejemplo he utilizado la versión con interfaz gráfica, en esta versión lo único que  podemos hacer es mandar los archivos que queremos comprimir dentro del programa, no tenemos disponible ninguna opción para configurar la optimización.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svgogui.jpg)

**SVGO** está disponible para [descargar desde GitHub](https://github.com/svg/svgo)

##SVGO en jorgeatgu.com

Por último vamos a ver una comparativa que hice a finales de enero de 2014 con los **SVG** que tengo en una sección de la web, para ello utilice **SVGO**.

Para llevar a cabo este ejemplo he utilizado la página de [trabajos de mi web](http://jorgeatgu.com/trabajos) ya que es la que más **SVG** contiene de toda mi web. He pasado por **SVGO** todos los **SVG**.
Para ver el impacto he clonado la página de trabajos y he colocado los **SVG** optimizados. Lo siguiente ha sido comparar las dos páginas en velocidad, para ello he utilizado [whichloadsfaster](http://whichloadsfaster.com/ ), que compara al mismo tiempo la velocidad de carga de dos webs. He hecho dos series para que no quede lugar a dudas. La primera serie ha sido de 10 repeticiones y el resultado es que después de pasar los **SVG** por **SVGO la página es un 56% más rápida, impresionante.**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-comparativa-diez.jpg)

La siguiente serie ha sido de 100 repeticiones y el resultado apenas ha variado, la página optimizada con **SVGO sigue siendo un 54% más rápida.**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-comparativa-cien.jpg)

El resultado como podéis apreciar es **impresionante**.

##Optimizando SVG con Grunt

Advertencia antes de seguir leyendo si todo esto de los *runner task* como **Grunt** o **Gulp** te suena raro o directamente no te suena te recomiendo este artículo de [introducción a Grunt](http://trip2themoon.com/primeros-pasos-con-grunt-para-disenadores-web/) publicado por [Felix Ortega](https://twitter.com/flodar).

Ahora que ya conocemos un poco más sobre Grunt vamos a instalar un plugin para optimizar SVG.

Lo primero que vamos a hacer es instalar [svgmin](https://github.com/sindresorhus/grunt-svgmin) desde el terminal.


~~~~~~~
$ npm install --save-dev grunt-svgmin
~~~~~~~

Ahora vamos a incluir la tarea en nuestro archivo gruntfile.js


~~~~~~~
svgmin: {
                 options: {
                     plugins: [

                     ]
                 },
                 dist: {
                     files: []
                }
             },
~~~~~~~

Y ahora vamos a configurar a nuestro antojo la optimización. Y este es lo mejor ya que podemos tener control absoluto sobre la optimización de nuestros **SVG**, cosa que como hemos visto anteriormente no podíamos llevar a cabo con **SVGO**

###removeViewBox

Para que no elimine el atributo viewBox.

###removeTitle y removeDesc

Para mí estos dos plugins son los más importantes. Si queremos que Google muestre un título y una descripción de nuestro SVG debemos de añadir las etiquetas ```<title>``` y ```<desc>``` para que lo muestre en los resultados. Con este plugin en false SVGO no eliminará estas dos etiquetas.

###removeUselessStrokeAndFill

Para que elimine los stroke y fill que no tengan valor alguno.

###cleanupIDs

Para que elimine los IDs que no contengan ningún script o estilo.

###removeEditorNSData

Para que elimine los namespaces que se crean al exportar desde Illustrator, Sketch y Inkscape

###cleanupNumericValues

Para que elimine las unidades por defecto. Si a los atributos no les asignamos ninguna unidad de medidad SVG tomará la unidad por defecto, la cual es el pixel. Así que no sirve de nada escribir px.

###convertColors

Para que convierta los colores en RGB y keywords a su valor hexadecimal,en caso de que el que color se pueda representar con tres valores(por ejemplo #000000 #ffffff) hexadecimales el plugin hará la conversión.

Por último dejo en mi Gist todo el código que he generado para [configurar **SVGmin**](https://gist.github.com/jorgeatgu/a0656c47a11e741befb2)


##SVGO ONLINE

A finales de enero de 2015 de la mano de [Jake Archibald](https://github.com/svg/svgo) nos llega la versión de SVGO online bajo el nombre de [SVGOMG](https://jakearchibald.github.io/svgomg/). La interfaz como podemos apreciar en la imagen es bastante simple y clara, esta herramienta es perfecta para aquellos a los que les da urticaria el terminal/consola, Grunt y Gulp.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-12/optimizar-svgo-online.jpg)


Tenemos una demo en forma de coche para ir probando las diferentes opciones.

La gran ventaja es que una vez que hemos importado el **SVG** vamos a tener pleno control sobre la optimización. A la derecha vamos a ver el panel con todas los plugins que trae **SVGO** para optimizar un **SVG**. La lista de plugins como acabamos de ver en la sección anterior es larga y extensa, merece la pena echar un ojo a todos los plugins que no hemos visto.

Otra de las opciones que tenemos en el panel derecho es la de comparar el **SVG** que estamos optimizando con su versión original. Y ya por último el apartado precisión nos dará pleno control sobre el tan manido tema de los decimales, mucho ojo ya que por defecto viene con tres decimales y ya sabéis que con uno es más que suficiente.

[SVGOMG](https://jakearchibald.github.io/svgomg/)