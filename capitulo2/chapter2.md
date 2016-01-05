# Exportar y añadir SVG

Antes de empezar a ver todos los elementos que tenemos disponibles en la especificación vamos a ver cómo exportar archivos vectoriales en formato **SVG** con programas vectoriales de pago como **Adobe Illustrator y Sketch**, también con gratuitos como **Inkscape**. Recordad que por ahora **Sketch** solamente está disponible para **OSX**.

A continuación sólo vamos a ver el proceso de exportar desde cada programa y el código que genera cada uno de ellos, para este ejemplo he utilizado un archivo bastante simple que contiene un cuadrado, un cuadrado con esquinas redondeadas, un círculo y un pentágono.

## Adobe Illustrator 17.1.0

Una vez que tenemos abierto nuestro archivo vamos a ir al menú **Archivo** y vamos a hacer click en **Guardar como**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-menu-archivo-illustrator.jpg)

En el menú de **Guardar como**, vamos a la pestaña **formato** donde seleccionamos **SVG** y le damos a **Guardar**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-guardar-como-illustrator.jpg)

Ahora en el menú de **opciones SVG** vamos a ir a decimales y cambiamos **3 decimales por 1 decimal**, con esto conseguimos archivos con menos código ya que las medidas de los objetos y las coordenadas de los mismos solamente se van a exportar con 1 decimal, no vamos a perder precisión, podéis hacer la prueba comparando un archivo que este exportado con 7 decimales y otro con 1 decimal, no vais a notar la diferencia.

También tenemos la opción **flexible** que lo que hace es quitar de la etiqueta principal el ***width*** y el ***height***, con esto conseguimos que el archivo se vaya adaptando a la pantalla donde se muestra, las consecuencias de esta acción es que a nuestros archivos no vamos a poder aplicarles zoom desde los navegadores.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-opciones-illustrator.jpg)

La última opción que vamos a ver de este menú es la de código **SVG**, si pinchamos en ella nos abrirá nuestro editor de texto, en el caso de **OSX** se abre ***TextEdit*** y aquí vamos a previsualizar el código que va a generar el archivo.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-codigo-illustrator.jpg)

Por último vamos a hacer click en OK y ya tenemos guardado nuestro archivo en formato **SVG**.

## Novedades Adobe Illustrator 19.2

En diciembre de 2015 Adobe publicó la version 19.2 de Adobe Illustrator con una sustanciales mejoras a la hora de exportar **SVG**.

Todas estas novedades están disponibles a través de una nueva opción que esta situada en el menú Archivo > Exportar. Cuando seleccionamos esta opción simplemente tenemos que seleccionar en el desplegable la opción **SVG**. Una vez seleccionada se nos desplegará un menú como el que vemos en la imagen.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-svg-opciones.png)

Vamos a ver algunas de esta opciones.

### Estilo

En este desplegable tenemos tres opciones disponibles.

La primera de ellas es **atributos de presentación**, con esta opción utilizamos los atributos como ```fill``` y ```stroke``` directamente en el elemento.

La segunda opción es **CSS interno** con esta opción se añaden a nuestros elementos clases de **CSS** a través de la etiqueta ```<style>``` dentro de nuestro **SVG**. Esta opción no es nada recomendable.

La tercera opción es **estilo en línea**, con esta opción se añaden los atributos CSS directamente en nuestros elementos.

### Identificadores de objeto

En este desplegable también tenemos a nuestra disposición tres opciones.

La primera de ella es **nombres de capas**, lo que hace esta opción es añadir a cada elemento un id con el nombre que le hemos asignado a la capa en Adobe Illustrator.

La segunda es **mínimo**, tan mínimo que he estado haciendo pruebas y no añade absolutamente nada.

La tercera opción es **único**, y añade un id poco o nada amigable que genera Illustrator. Ejemplo: ```id="c9c9f046 dec6-492e-8dc3-58c8355c6e10"```

### Decimal

Ahora el valor por defecto ha cambiado de 3 a 2, debería de ser 1, así que modificadlo.

### Minimizar

Seleccionando esta opción vamos a suprimir todos los espacios en blanco que tiene el **SVG**.  Si vas a volver a modificar a mano el **SVG** mejor que no lo marques. Si no lo vas a volver a tocar marcala.

### Exportando selección

Si seleccionamos un elemento y vamos al menú Archivo veremos que se activa la opción de exportar selección, como su nombre indica solo nos exporta la selección.

### Rectángulos redondeados

Hasta ahora Illustrator a la hora de exportar un rectángulo redondeado siempre lo transformaba en un ```<path>``` a partir de **esta version** ya es capaz de exportar rectángulos redondeados con los atributos ```rx``` y ```ry```.

## Inkscape 0.48.2

Una vez que tenemos abierto nuestro archivo vamos a ir al menú **Archivo** y vamos a hacer click en **Guardar como**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-menu-archivo-inkscape.jpg)

En el menú de **Guardar como** vamos a la pestaña **formato**, tenemos varias opciones para elegir como **SVG de inkscape** y **SVG plano** estas dos opciones también tienen disponible su versión comprimida. Vamos a elegir **SVG de inkscape**.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-menu-guardar-inkscape.jpg)

Por último vamos a pinchar en **SAVE** y ya tenemos guardado nuestro archivo en formato **SVG**. Con **Inkscape** no tenemos opción alguna para modificar los parámetros del archivo.

## Sketch 3.0.3

Una vez que tenemos abierto nuestro archivo vamos a ir al menú **File** y vamos a hacer click en **Export**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-menu-sketch.jpg)

Con **Sketch** no nos va a saltar ningún menú, tenemos que ir a la parte derecha donde esta ubicada la sección **Export**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-menu-sketch2.jpg)

Ahora en la pestaña **formato** seleccionamos **SVG** y hacemos click en el botón donde pone **Export**

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-boton-sketch.jpg)

Ahora nos saltará un menú donde volvemos a pinchar en **Export** y ya tenemos nuestro archivo en formato **SVG**.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/exportar-sketch.jpg)

Desde su versión **3.0 Sketch** genera todas las medidas y coordenadas sin decimales, lo cual hace que nuestros archivos sean más legibles, tengan menos código y por lo tanto ocupen menos espacio.



## Añadir SVG al HTML

Vamos a ver las diferentes opciones que tenemos para añadir nuestros archivos **SVG** en el **HTML**.

Con la etiqueta `img`

{lang="html", linenos="off"}
~~~~~~~
<img src="smilipostbox.svg">
~~~~~~~

Con la etiqueta `object`

{lang="html", linenos="off"}
~~~~~~~
<object type="image/svg+xml" data="smilipostbox.svg"></object>
~~~~~~~

Con la propiedad `background-image` de **CSS**

{lang="html", linenos="off"}
~~~~~~~
<div class="background"></div>
~~~~~~~

{lang="css", linenos="off"}
~~~~~~~
.background {
width: 100%;
height: 310px;
background: url(smilipostbox.svg) no-repeat;
}
~~~~~~~

Con **HTML5** podemos incluir directamente el código entre las etiquetas `body` del **HTML**.

{lang="html", linenos="off"}
~~~~~~~
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="200" height="300" viewBox="0 0 200 300">
 <rect width="40" height="40" fill="navajowhite" stroke="crimson" stroke-width="20"/>
</svg>
~~~~~~~

####Soporte

![](images/soporte/primera.jpg)

En iOS 5.1.1 a través de la etiqueta `<object>` las medidas del SVG no son respetadas.


## Soporte para IE8 y Android 2.3

Ni **IE8** ni **Android 2.3** ni por supuesto sus versiones anteriores dan soporte a **SVG**. Para resolver este problema tenemos a nuestra disposición una librería de **JavaScript** como **SVGeezy** y otra de **jQuery** como **SVGMagic**, con ellas vamos a mostrar archivos en formato **PNG** cuando los navegadores no soporten archivos **SVG**.

### SVGeezy

La instalación es bastante sencilla, simplemente tenemos que añadir en nuestro **HTML** el siguiente código:

{lang="html", linenos="off"}
~~~~~~~
<script src="path/to/svgeezy.js"></script>
<script>
    svgeezy.init(false, 'png');
</script>
~~~~~~~

Hay que tener en la misma carpeta los archivos **SVG** y **PNG**. Los archivos deben de compartir el mismo nombre, por ejemplo si vamos a añadir el logo de CodePen tendremos que tener un archivo con la extensión **SVG** `codepen.svg` y otro con extensión **PNG** `codepen.png`

**SVGeezy** está disponible para [descargar desde GitHub](https://github.com/benhowdle89/svgeezy).

### SVGMagic

Con **SVGMagic** no necesitamos tener ninguna carpeta con los archivos en formato **PNG** ya que el propio plugin se encarga de enviar y transformar los **SVG**. También transforma los archivos **SVG** que utilizamos a través de `background-image`.

{lang="html", linenos="off"}
~~~~~~~
<script src="SVGMagic.min.js"></script>
<script>
    $(document).ready(function(){
        $('img').svgmagic();
    });
</script>
~~~~~~~


Si utilizamos **SVG** a través de `background-image` también tenemos que añadir el siguiente código:

{lang="html", linenos="off"}
~~~~~~~
<script src="SVGMagic.min.js"></script>
<script>
    $(document).ready(function(){
        $('.bgimage').svgmagic({
            backgroundimage: true
        });
    });
</script>
~~~~~~~

**SVGMagic** está disponible para [descargar desde GitHub](https://github.com/dirkgroenen/SVGMagic).

### Sustitur SVG por PNG con JavaScript

Vamos a ver un método para reemplazar **SVG** por **PNG** con la ayuda de **JavaScript** y **CSS**.

Con este script vamos a añadir el **PNG** a traves de la propiedad background de **CSS**.

Lo primero que vamos a ver es el script de **JavaScript**

{lang="html", linenos="off"}
~~~~~~~
<script>

var supportsSvg = function() {
  return document.implementation && document.implementation.hasFeature("http://www.w3.org/TR/SVG11/feature#Image", "1.1");
};

if (!supportsSvg()) {
  var inlineSvgs = document.getElementsByTagName('svg'), i;
  for (i = 0; i < inlineSvgs.length; i++) {
    if (inlineSvgs[i].getAttribute("class") === "icon") {
      var fallbackSpan = document.createElement("span");
      var spanClass = inlineSvgs[i].getAttribute("data-use");
      fallbackSpan.setAttribute("class", spanClass);
      inlineSvgs[i].parentNode.insertBefore(fallbackSpan, inlineSvgs[i]);
    };
  };

  i = inlineSvgs.length;
  while (i--) {
    inlineSvgs[i].parentNode.removeChild(inlineSvgs[i]);
  }
};

</script>
~~~~~~~

Lo que hace este script es comprobar si el navegador soporta **SVG**, en caso de que no tenga soporte reemplaza ``<svg data-use="aquí-la-clase-que-tiene-el-svg"`` por ``<span class="aquí-la-clase-del-css">``.

Lo que tenemos que hacer es añadir a nuestra etiqueta de **SVG** una clase data-use y icon. Se puede utilizar otros nombres pero acordaros de modificarlo en el script. Ahora en nuestro **CSS** vamos a añadir el **PNG** a través de un ``background``, la clase tendrá que tener el mismo nombre que hemos utilizado en el data-use e irá precedidad de un span. Vamos a ver un ejemplo

{lang="html", linenos="off"}
~~~~~~~
<svg class="icon" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" data-use="logo-jorge">
~~~~~~~

Ahora vamos a ver el **CSS**

{lang="css", linenos="off"}
~~~~~~~
span.logo {
background: url(logo-jorge.png) no-repeat;
}
~~~~~~~

A continuación un enlace a la demo en CodePen donde podeis comprobar que el **SVG** ha sido sustituido por su versión en **PNG** y se ve sin ningún problema en Internet Explorer 8. Si haceis click en la pestaña del editor y vais a la última opción *Open on CrossBrowserTesting* vais a poder testear el ejemplo en IE8, IE7 y Android 2.3.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/fallback-javascript.jpg)

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/pen/gbxEGr/)


## Añadir SVG a WordPress con Plugin

En su versión **3.9.1 Wordpress** no deja subir archivos en formato **SVG** a la galería.

Para solucionar todo esto contamos con el plugin [SVG Shortcode](http://wordpress.org/plugins/svg-shortcode/) su funcionamiento es bastante simple. Vamos a buscar el plugin en el apartado de plugins de Wordpress. Una vez que tenemos instalado el ***plugin*** vamos a subir nuestros archivos a nuestro propio servidor, por ejemplo a la carpeta images, así que ahora copiamos la dirección del enlace `images\nuestroarchivo.svg` ahora vamos al editor de **WordPress** y lo añadimos de la siguiente manera:

{lang="html", linenos="off"}
~~~~~~~
[svg]nuestroarchivo.svg[/svg]
~~~~~~~

También le podemos indicar las medidas de nuestro archivo a través de los atributos `width` y `height`

{lang="html", linenos="off"}
~~~~~~~
[svg width="40" height="20"]nuestroarchivo.svg[/svg]
~~~~~~~

## Añadir SVG a WordPress sin Plugin

Ahora vamos a ver como podemos activar la subida de **SVG** a la galería a través de unas cuantas líneas de códgio.

Vamos a ir al archivo `functions.php` que normalmente este ubicado en esta ruta `/wp-content/themes/tutema/functions.php` de nuestro tema, lo abrimos y vamos a añadir el siguiente código:

{lang="php", linenos="off"}
~~~~~~~
function cc_mime_types( $mimes ){
    $mimes['svg'] = 'image/svg+xml';
    return $mimes;
}
add_filter( 'upload_mimes', 'cc_mime_types' );
~~~~~~~

Ahora si vamos a la galería nos va a dejar permitir añadir archivos en formato **SVG**.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-2/wordpress-galeria-svg.jpg)
