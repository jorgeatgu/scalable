![portada de Scalable, un libro sobre SVG](https://github.com/jorgeatgu/scalable/blob/master/portada-scalable.png)

A lo largo de 15 capítulos, 120 páginas y más de 70 ejemplos vamos a ver todo lo que podemos hacer con **SVG**.

[Disponible para descargar gratuitamente desde 0$ en Leanpub](https://leanpub.com/scalable/)


#Acerca de este libro

##Historia

Desde que en 1996 [Chris Lilley](https://twitter.com/svgeesus) creo un documento con una serie de requisitos para la creación de un lenguaje vectorial **SVG** ha sido el patito feo de la web, marginado por usuarios ha visto como los navegadores no hacían ningún movimiento por implementar sus caracteristicas, a pesar de tener a todo y todos en su contra ha ido resistiendo el paso del tiempo gracias a un grupo de personas que siguieron trabajando concienzudamente en la especificación esperando una nueva nueva oportunidad, esta por fin ha llegado de la mano de **HTML5**.

##Contenido

A lo largo del libro vamos a ver las posibilidades que nos brinda **SVG** para la creación de gráficos vectoriales, durante los quince capítulos que tiene el libro vamos a ver desde la creación de formas básicas, patrones y degradados hasta como aplicar los diferentes filtros a nuestros elementos, también vamos a optimizar nuestros archivos, los haremos accesibles y veremos las opciones que tenemos para añadirlos a nuestros proyectos web.

Mas de setenta ejemplos alojados en [CodePen](http://codepen.io/collection/Gvcwd/) para que los puedas modificar como te de la gana.

Todos los ejemplos en un .zip para trastear con ellos en desde tu ordenador.

Un par de vídeos donde vamos a ver como se comporta **SVG** con dos herramientas para personas con discapacidad como VoiceOver y ChromeVox.

Para cualquier consulta puedes ponerte en contacto conmigo a través de [twitter](https://twitter.com/jorgeATGU) o en **scalable[arroba]jorgeatgu.com**

##Versiones

* **3/7/2014**: SCALABLE 1.0

> Libro publicado :)

* **9/9/2014**: SCALABLE 2.0

> Esta es la primera actualización que recibe el libro, he corregido unas cuantas faltas que tenía el libro, seguro que se me ha escapado una. También he cambiado las imágenes del soporte, en la versión anterior si un navegador no soportaba un elemento el icono del navegador no aparecía. La verdad es que no era nada práctico el tener que buscar que icono de navegador falta. Ahora al final de cada sección o capítulo aparece una tabla con todos los navegadores, si soporta el elemento un visto bueno sobre fondo verde, si no tiene soporte una cruz sobre fondo rojo. Mucho mejor ¿no? el anexo con el soporte en texto no lo he tocado.

* **27/10/2014**: SCALABLE 3.0

> La actualización consta de tres nuevas secciones todas ellas incluidas en el capitulo 11 del libro.

> El primer artículo es una adaptación del que escribí para octuweb y que podéis visitar http://octuweb.com/sprites-con-svg creo que a estas alturas todo el mundo estará al tanto de la idea de octuweb.

> El segundo artículo relata todas las maneras disponibles para dar estilos a nuestros archivos SVG a través de CSS. Es algo que se quedo en el tintero ya que casi siempre suelo utilizar los presentation attributes para dar estilos a mis SVG, no quiere decir que sea el mejor método simplemente es una manía heredada de exportar SVG con Adobe Illustrator.

> El tercer artículo y el más interesante trata sobre los "fragments identifiers" un método para incluir partes de nuestros SVG a través de HTML y de CSS. Lo curioso es que está soportado desde IE9, recordad que los sprites a través de SVG no están soportados en ninguna versión de IE y tenemos que echar mano de un polyfill. Pero por desgracia el soporte en otros navegadores es bastante reciente.

* **31/1/2015**: SCALABLE 4.0

> En el capítulo 2(página 11): He añadido un nuevo "fallback" para sustituir SVG por PNG a través de JavaScript.
> En el capítulo 4(página 23): He añadido RGBA para dar color a nuestros SVG.
> En el capítulo 11(página 113): He añadido un aviso para aquellos que vayan a adjuntar CSS a través de etiquetas XML en la cabecera de un SVG
> En el capítulo 12(a partir de la página 124): He añadido nuevos métodos para optimizar SVG, uno con Grunt y otro con una herramienta online basada en SVGO.
> Algunas correcciones en códigos que no se mostraban conforme es debido.


* **25/3/2015**: SCALABLE 5.0

> He creado una nueva demo para mostrar los efectos de filtro de SVG. He mejorado lo que había anteriormente, la anterior estaba construida con SMIL más SVG, la demo funcionaba pero el resultado no era muy bueno y daba errores con algún navegador. En esta nueva demo ademas de ver los efectos de filtros ahora podéis subir vuestros propios archivos en formato SVG, PNG, JPG y GIF, simplemente tenéis que hacer drag&drop con la imagen en la zona indicada en la demo. A los archivos que subáis también se les aplicarán los diferentes efectos de filtros.

> Por si queréis trastear el código aquí tenéis el repositorio de GitHub: https://github.com/jorgeatgu/SVG-FILTERS donde lo he alojado. Cualquier mejora o efecto de filtro que creáis que puede o debe estar ya sea porque es interesante o porque lo habéis creado vosotros mismos podéis hacer un fork del repositorio y hacer un pull request, cualquier ayuda siempre es bienvenida :)

> El enlace directo a la demo también en GitHub: http://jorgeatgu.github.io/svg-filters/ o a través del enlace en el libro en el final del capítulo 7.


* **5/1/2016**: SCALABLE 6.0

> En esta nueva versión he incluido en el capítulo 2 las nuevas opciones disponibles para exportar SVG desde la nueva versión de Adobe Illustrator(publicada a principios de diciembre de 2015). Una gran mejora.

> En el capítulo 7 he añadido la nueva version de FILDROP, una herramienta para ver los efectos de los diferentes filtros sobre archivos en formato PNG, JPEG y SVG. En esta nueva versión puedes modificar en vivo y en directo los valores de algunos filtros, para así hacer tus propios filtros. Todo el código generado lo puedes copiar fácilmente desde el desplegable. También puedes bajarte los archivos SVG y CSS para emplearlos fácilmente en cualquier proyecto.

> He borrado el capítulo borrador que hacia referencia a SVG 2, voy a esperar hasta que este todo definido. El roadmap(http://www.w3.org/Graphics/SVG/WG/wiki/Roadmap) del grupo de SVG de la W3C tiene previsto que se convierta en recomendación en diciembre de 2016, ya veremos.

##Indice de Contenido


1. [Introducción](https://github.com/jorgeatgu/scalable/blob/master/capitulo1/chapter1.md)
	1.1 [Un poco de historia](https://github.com/jorgeatgu/scalable/blob/master/capitulo1/chapter1.md#un-poco-de-historia)
	1.2 [Soporte](https://github.com/jorgeatgu/scalable/blob/master/capitulo1/chapter1.md#soporte)
	1.3 [Formato y ejemplos](https://github.com/jorgeatgu/scalable/blob/master/capitulo1/chapter1.md#formato-y-ejemplos)
2. [Exportar y añadir SVG](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md)
  	2.1 [Adobe Illustrator 17.1.0](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md#adobe-illustrator-1710)
  	2.2 [Inkscape 0.48.2](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md#inkscape-0482)
  	2.3 [Sketch 3.0.3](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md#sketch-303)
  	2.4 [Añadir SVG al HTML](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md#añadir-svg-al-html)
  	2.5 [Soporte para IE8 y Android 2.3](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md#soporte-para-ie8-y-android-23)
  	2.6 [Añadir SVG a WordPress con Plugin](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md#añadir-svg-a-wordpress-con-plugin)
  	2.7 [Añadir SVG a WordPress sin Plugin](https://github.com/jorgeatgu/scalable/blob/master/capitulo2/chapter2.md#añadir-svg-a-wordpress-sin-plugin)
3. [Etiqueta principal](https://github.com/jorgeatgu/scalable/blob/master/capitulo3/chapter3.md)
  	3.1 [Sistema de coordenadas y unidades de medida](https://github.com/jorgeatgu/scalable/blob/master/capitulo3/chapter3.md#sistema-de-coordenadas-y-unidades-de-medida)
  	3.2 [viewBox](https://github.com/jorgeatgu/scalable/blob/master/capitulo3/chapter3.md#viewbox)
  	3.3 [preserveAspectRatio](https://github.com/jorgeatgu/scalable/blob/master/capitulo3/chapter3.md#preserveaspectratio)
4. [Las formas básicas](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md)
  	4.1 [Fill](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#fill)
  	4.2 [Stroke](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#stroke)
  	4.3 [Rect](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#rect)
  	4.4 [Circle](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#circle)
  	4.5 [Ellipse](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#ellipse)
  	4.6 [Line](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#line)
  	4.7 [Polyline](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#polyline)
  	4.8 [Polygon](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#polygon)
  	4.9 [Path](https://github.com/jorgeatgu/scalable/blob/master/capitulo4/chapter4.md#path)
5. [Texto](https://github.com/jorgeatgu/scalable/blob/master/capitulo5/chapter5.md)
  	5.1 [Text](https://github.com/jorgeatgu/scalable/blob/master/capitulo5/chapter5.md#text)
  	5.2 [Tspan](https://github.com/jorgeatgu/scalable/blob/master/capitulo5/chapter5.md#tspan)
  	5.3 [textPath](https://github.com/jorgeatgu/scalable/blob/master/capitulo5/chapter5.md#textpath)
6. [Transformaciones](https://github.com/jorgeatgu/scalable/blob/master/capitulo6/chapter6.md)
  	6.1 [Translate](https://github.com/jorgeatgu/scalable/blob/master/capitulo6/chapter6.md#translate)
  	6.2 [Rotate](https://github.com/jorgeatgu/scalable/blob/master/capitulo6/chapter6.md#rotate)
  	6.3 [Scale](https://github.com/jorgeatgu/scalable/blob/master/capitulo6/chapter6.md#scale)
  	6.4 [SkewX](https://github.com/jorgeatgu/scalable/blob/master/capitulo6/chapter6.md#skewx)
  	6.5 [SkewY](https://github.com/jorgeatgu/scalable/blob/master/capitulo6/chapter6.md#skewy)
  	6.6 [Matrix](https://github.com/jorgeatgu/scalable/blob/master/capitulo6/chapter6.md#matrix)
7. [Filtros](https://github.com/jorgeatgu/scalable/blob/master/capitulo7/chapter7.md)
  	7.1 [feFlood]()
  	7.2 [feTurbulence]()
  	7.3 [feImage]()
  	7.4 [feColorMatrix]()
  	7.5 [feComponentTransfer]()
  	7.6 [feConvolveMatrix]()
  	7.7 [feGaussianBlur]()
  	7.8 [feDisplacementMap]()
  	7.9 [feMorphology]()
  	7.10 [feOffset]()
  	7.11 [Efectos de luz]()
  	7.12 [feDistantLight]()
  	7.13 [fePointLight]()
  	7.14 [feSpotLight]()
  	7.15 [feMerge]()
  	7.16 [feBlend]()
  	7.17 [feComposite]()
  	7.18 [feTile]()
  	7.19 [Efectos de filtro sobre una fotografía]()
8. [Degradados](https://github.com/jorgeatgu/scalable/blob/master/capitulo8/chapter8.md)
  	8.1 [linearGradient]()
  	8.2 [radialGradient]()
  	8.3 [spreadMethod]()
  	8.4 [gradientTransform]()
9. [Patterns, masks, clip-path y symbol](https://github.com/jorgeatgu/scalable/blob/master/capitulo9/chapter9.md)
  	9.1 [Patterns]()
  	9.2 [Mask]()
  	9.3 [Clip-Path]()
  	9.4 [Symbol]()
10. [Image](https://github.com/jorgeatgu/scalable/blob/master/capitulo10/chapter10.md)
  	10.1 [Links]()
11. [DRY con group, defs y use](https://github.com/jorgeatgu/scalable/blob/master/capitulo11/chapter11.md)
  	11.1 [Group]()
  	11.2 [Defs y use]()
	11.3 Usando CSS para aplicar estilos
  	11.4 [Sprites con SVG]()
  	11.5 [Métodos para aplicar estilos CSS a SVG]()
	11.6 Fragmentos identificadores
12. [Optimizar SVG](https://github.com/jorgeatgu/scalable/blob/master/capitulo12/chapter12.md)
  	12.1 [SVG CLEANER]()
  	12.2 [SVGO]()
  	12.3 [SVGO en jorgeatgu.com]()
  	12.4 [Optimizando SVG con Grunt]()
  	12.5 [SVGO ONLINE]()
13. [WAI-ARIA en SVG](https://github.com/jorgeatgu/scalable/blob/master/capitulo13/chapter13.md)
  	13.1 [SVG 1.1]()
  	13.2 [SVG 2]()
  	13.3 [Describler]()
14. [Anexo Soporte](https://github.com/jorgeatgu/scalable/blob/master/capitulo14/chapter14.md)
  	14.1 [Capítulo 2 - Exportar y añadir SVG]()
  	14.2 [Capítulo 3 - viewBox]()
  	14.3 [Capítulo 4 - Las formas básicas]()
  	14.4 [Capítulo 5 - Text]()
  	14.5 [Capítulo 6 - Transforms]()
  	14.6 [Capítulo 7 - Los filtros]()
  	14.7 [Capítulo 8 - gradients]()
  	14.8 [Capítulo 9 - Patterns]()
  	14.9 [Capítulo 10 - Images y Links]()
  	14.10 [Capítulo 11 - defs, use y group]()
15. Bibliografia
