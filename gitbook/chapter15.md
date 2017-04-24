# CSS en SVG

## Métodos para aplicar estilos CSS a SVG

A lo largo de libro hemos ido aplicando los estilos a través de los *presentation attributes* o atributos de presentación de tal manera que aplicamos el estilo en la propia etiqueta del elemento. Ahora vamos a ver otros métodos para aplicar diferentes estilos a nuestros **SVG**.

### A través de una etiqueta XML

Podemos aplicar una hoja de estilos directamente en nuestros archivos **SVG** a través de una etiqueta `xml`. Para ello vamos a colocar en la cabecera de nuestro **SVG** la siguiente etiqueta **XML**.

{lang="xml", linenos="off"}
~~~~~~~
<? xml-stylesheet href="style.css" type="text/css" ?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 2976.5 299">

<rect class="rectangulo" width="50" height="50"/>
</svg>
~~~~~~~

Ahora en nuestro archivo `style.css` aplicamos los estilos al rectángulo.

{lang="css", linenos="off"}
~~~~~~~
.rectangulo {
fill: crimson;
stroke: black;
}
~~~~~~~

Un aviso antes de que os volváis locos, este método no funciona en local. Tendréis que lanzar un servidor desde vuestro ordenador por ejemplo con Grunt, Gulp, CodeKit, GhostLab podéis ver como la hoja de estilos aplica los estilos al **SVG**. La otra opción es si disponéis de un servidor web subir el **SVG** y los **CSS** al servidor.

### A través del style en el HTML

Aquí otro método que seguramente suene a más de uno y como bien sabéis es poco o nada recomendable. Solamente tenemos que incluir los estilos **CSS** en el propio **HTML** a través de la etiqueta `style`.

{lang="html", linenos="off"}
~~~~~~~
<style type="text/css">
  <![CDATA[
 circle {
 fill: navajowhite;
 stroke: orange;
 }
  ]]>
</style>
<circle cx="50" cy="10" r="50"/>
~~~~~~~

### A través de la etiqueta style en SVG

Al igual que los *presentation attributes* también podemos usar estilos *inline* en **SVG** a través de `style`

{lang="html", linenos="off"}
~~~~~~~
<circle cx="50" cy="10" r="50" style="fill: ivory; stroke: snow;"/>
~~~~~~~

### A través de un archivo CSS externo

Y por último el método más conocido, aplicar los estilos a través de una hoja de estilos externa gracias a la etiqueta `link` en el head del **HTML**.

{lang="html", linenos="off"}
~~~~~~~

<link rel="stylesheet" href="turuta.css">


<circle cx="50" cy="10" r="50" class="circulo"/>
~~~~~~~

{lang="css", linenos="off"}
~~~~~~~

.circulo {
fill: tomato;
stroke: snow;
}

~~~~~~~
