![portada de Scalable, un libro sobre SVG](https://github.com/jorgeatgu/scalable/blob/master/portada-scalable.png)

A lo largo de 15 capítulos, 120 páginas y más de 70 ejemplos vamos a ver todo lo que podemos hacer con **SVG**.

[Disponible para descargar gratuitamente desde 0$ en Leanpub](https://leanpub.com/scalable/)


# 📕Acerca de este libro

## Historia

Desde que en 1996 [Chris Lilley](https://twitter.com/svgeesus) creo un documento con una serie de requisitos para la creación de un lenguaje vectorial **SVG** ha sido el patito feo de la web, marginado por usuarios ha visto como los navegadores no hacían ningún movimiento por implementar sus caracteristicas, a pesar de tener a todo y todos en su contra ha ido resistiendo el paso del tiempo gracias a un grupo de personas que siguieron trabajando concienzudamente en la especificación esperando una nueva nueva oportunidad, esta por fin ha llegado de la mano de **HTML5**.

## Contenido

A lo largo del libro vamos a ver las posibilidades que nos brinda **SVG** para la creación de gráficos vectoriales, durante los quince capítulos que tiene el libro vamos a ver desde la creación de formas básicas, patrones y degradados hasta como aplicar los diferentes filtros a nuestros elementos, también vamos a optimizar nuestros archivos, los haremos accesibles y veremos las opciones que tenemos para añadirlos a nuestros proyectos web.

Mas de setenta ejemplos alojados en [CodePen](http://codepen.io/collection/Gvcwd/) para que los puedas modificar como te de la gana.

Todos los ejemplos en un .zip para trastear con ellos en desde tu ordenador.

Un par de vídeos donde vamos a ver como se comporta **SVG** con dos herramientas para personas con discapacidad como VoiceOver y ChromeVox.

Para cualquier consulta puedes ponerte en contacto conmigo a través de [twitter](https://twitter.com/jorgeATGU) o en **scalable[arroba]jorgeatgu.com**

## Versiones

* **3/7/2014**: SCALABLE 1.0

> Libro publicado :)

* **9/9/2014**: SCALABLE 1.0.5

> Esta es la primera actualización que recibe el libro, he corregido unas cuantas faltas que tenía el libro, seguro que se me ha escapado una. También he cambiado las imágenes del soporte, en la versión anterior si un navegador no soportaba un elemento el icono del navegador no aparecía. La verdad es que no era nada práctico el tener que buscar que icono de navegador falta. Ahora al final de cada sección o capítulo aparece una tabla con todos los navegadores, si soporta el elemento un visto bueno sobre fondo verde, si no tiene soporte una cruz sobre fondo rojo. Mucho mejor ¿no? el anexo con el soporte en texto no lo he tocado.

* **27/10/2014**: SCALABLE 1.1

> La actualización consta de tres nuevas secciones todas ellas incluidas en el capitulo 11 del libro.

> El primer artículo es una adaptación del que escribí para octuweb y que podéis visitar http://octuweb.com/sprites-con-svg creo que a estas alturas todo el mundo estará al tanto de la idea de octuweb.

> El segundo artículo relata todas las maneras disponibles para dar estilos a nuestros archivos SVG a través de CSS. Es algo que se quedo en el tintero ya que casi siempre suelo utilizar los presentation attributes para dar estilos a mis SVG, no quiere decir que sea el mejor método simplemente es una manía heredada de exportar SVG con Adobe Illustrator.

> El tercer artículo y el más interesante trata sobre los "fragments identifiers" un método para incluir partes de nuestros SVG a través de HTML y de CSS. Lo curioso es que está soportado desde IE9, recordad que los sprites a través de SVG no están soportados en ninguna versión de IE y tenemos que echar mano de un polyfill. Pero por desgracia el soporte en otros navegadores es bastante reciente.

* **31/1/2015**: SCALABLE 1.2

> En el capítulo 2(página 11): He añadido un nuevo "fallback" para sustituir SVG por PNG a través de JavaScript.
> En el capítulo 4(página 23): He añadido RGBA para dar color a nuestros SVG.
> En el capítulo 11(página 113): He añadido un aviso para aquellos que vayan a adjuntar CSS a través de etiquetas XML en la cabecera de un SVG
> En el capítulo 12(a partir de la página 124): He añadido nuevos métodos para optimizar SVG, uno con Grunt y otro con una herramienta online basada en SVGO.
> Algunas correcciones en códigos que no se mostraban conforme es debido.


* **25/3/2015**: SCALABLE 1.3

> He creado una nueva demo para mostrar los efectos de filtro de SVG. He mejorado lo que había anteriormente, la anterior estaba construida con SMIL más SVG, la demo funcionaba pero el resultado no era muy bueno y daba errores con algún navegador. En esta nueva demo ademas de ver los efectos de filtros ahora podéis subir vuestros propios archivos en formato SVG, PNG, JPG y GIF, simplemente tenéis que hacer drag&drop con la imagen en la zona indicada en la demo. A los archivos que subáis también se les aplicarán los diferentes efectos de filtros.

> Por si queréis trastear el código aquí tenéis el repositorio de GitHub: https://github.com/jorgeatgu/SVG-FILTERS donde lo he alojado. Cualquier mejora o efecto de filtro que creáis que puede o debe estar ya sea porque es interesante o porque lo habéis creado vosotros mismos podéis hacer un fork del repositorio y hacer un pull request, cualquier ayuda siempre es bienvenida :)

> El enlace directo a la demo también en GitHub: http://jorgeatgu.github.io/svg-filters/ o a través del enlace en el libro en el final del capítulo 7.


* **5/1/2016**: SCALABLE 1.4

> En esta nueva versión he incluido en el capítulo 2 las nuevas opciones disponibles para exportar SVG desde la nueva versión de Adobe Illustrator(publicada a principios de diciembre de 2015). Una gran mejora.

> En el capítulo 7 he añadido la nueva version de FILDROP, una herramienta para ver los efectos de los diferentes filtros sobre archivos en formato PNG, JPEG y SVG. En esta nueva versión puedes modificar en vivo y en directo los valores de algunos filtros, para así hacer tus propios filtros. Todo el código generado lo puedes copiar fácilmente desde el desplegable. También puedes bajarte los archivos SVG y CSS para emplearlos fácilmente en cualquier proyecto.

> He borrado el capítulo borrador que hacia referencia a SVG 2, voy a esperar hasta que este todo definido. El roadmap(http://www.w3.org/Graphics/SVG/WG/wiki/Roadmap) del grupo de SVG de la W3C tiene previsto que se convierta en recomendación en diciembre de 2016, ya veremos.

* **25/04/2017**: SCALABLE 1.5

> Demasiado tiempo ha pasado desde la última versión. La idea era sacar esta versión las pasadas navidades pero no he podido sacar mucho tiempo para ello.

> Me hubiera gustado traer novedades con la nueva spec de SVG, la 2.0, pero parece ser que estamos en el mismo punto que cuando se publico la 1.1, los navegadores están pasando de implementar nada. Solo inkscape con Tav a la cabeza y Firefox están implementado las novedades que nos trae la 2.0. Así que tocara esperar de nuevo. Mientras tanto si tenéis algún interés podéis seguir como va la implementación en esta web del grupo de trabajo de la W3C: [SVG 2 feature support](https://nikosandronikos.github.io/svg2-info/svg2-feature-support/)

> Aún así traigo novedades. He añadido un nuevo capítulo de herramientas/software que no tiene cabida en otros capítulos. Es el capítulo 14. También he separado la parte de CSS en SVG en un capítulo nuevo. Es el capítulo 15. Por otra parte he eliminado el capítulo de soporte, las versiones de navegadores se habían quedado totalmente obsoletas y carecía de sentido.

> Ahora también se puede consultar SCALABLE desde la web http://jorgeatgu.com/scalable/ En un primer momento mi idea era publicar este libro con GitBook pero encontré Leanpub y me encanto la idea de poder tener todos los formatos en formato ebook, así que me olvidé de GitBook. Lo publico en GitBook ya que así la consulta para ciertas cosas puede resultar más cómodo que acudir al libro electrónico. Lo he intentado hacer con GitHub pero la verdad es que el resultado dejaba mucho que desear.

>Y ya por último para celebrar que SCALABLE ha superado las 1000 descargas encargue stickers para regalar a todo el mundo que quiera. Así que el que quiera que escriba un mail a scalable@jorgeatgu.com con sus datos y recibirá un sticker como este: https://www.instagram.com/p/BP8N6mqAB_i/

>Cualquier error o sugerencia podéis poneros en contacto conmigo a través de http://twitter.com/jorgeatgu también abriendo una issue en http://github.com/jorgeatgu/scalable o mandado un mail a scalable@jorgeatgu.com

>Un saludo y gracias por leer SCALABLE.
