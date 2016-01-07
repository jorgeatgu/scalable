#Image

Con la etiqueta `<image>` vamos a importar imágenes dentro de nuestros archivos **SVG**, podemos incluir **JPEG**, **PNG** e incluso otros archivos en formato **SVG**. Para incluir la imagen utilizaremos `xlink:href=”aquíVaLaRutaDondeEstaTuImagen”` también tenemos a nuestra disposición una serie de atributos que vamos a ver a continuación.

Con el atributo ***x*** determinamos la posición de la coordenada en el eje horizontal.

Con el atributo ***y*** determinamos la posición de la coordenada en el eje vertical.

Con el atributo ***width*** determinamos la anchura de la imagen.

Con el atributo ***height*** determinamos la altura de la imagen.

También tenemos a nuestra disposición el atributo ***preserveAspectRatio***, por defecto y aunque no lo declaremos su valor será de ***xMidYMid meet***.

##Links

Con la etiqueta `<a>` vamos a crear enlaces en nuestros documentos **SVG**. Al igual que hemos visto en `<image>` para incluir un enlace vamos a hacerlo también con `xlink:href=”LaDirecciónWeb”`, podemos encerrar un `<rect>` en una etiqueta `<a>` para crear un enlace a otra página, y si le añadimos la propiedad **CSS** `cursor=”pointer”` vamos a modificar el puntero así cuando el ratón pase por encima de nuestro enlace será como si pasara por encima de un botón.



~~~~~~~
<a xlink:href="http://jorgeatgu.com" cursor="pointer">
	<rect x="400" y="250" width="200" height="50" fill="crimson" stroke="navajowhite"  stroke-width="1"/>
	<text x="440" y="280" fill="white">jorgeATGU</text>
</a>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/DItFB/)

Podemos agregar un título o una descripción al enlace a través del atributos `xlink:title=””` aunque desde la propia **W3C** nos recomiendan que para agregar un título es mejor utilizar la etiqueta ***title*** que hemos visto anteriormente.

Por último un ejemplo con todos los atributos que tenemos disponible para `target=””`


~~~~~~~
<a xlink:href="http://jorgeatgu.com" cursor="pointer" target="_replace">
	<rect x="30" y="250" width="150" height="50" fill="crimson" stroke="navajowhite"  stroke-width="1"/>
	<text x="70" y="280" fill="white">_replace</text>
</a>
<a xlink:href="http://jorgeatgu.com" cursor="pointer"  target="_self">
	<rect x="200" y="250" width="150" height="50" fill="crimson" stroke="navajowhite"  stroke-width="1"/>
	<text x="240" y="280" fill="white">_self</text>
</a>
<a xlink:href="http://jorgeatgu.com" cursor="pointer"  target="_parent">
	<rect x="370" y="250" width="150" height="50" fill="crimson" stroke="navajowhite"  stroke-width="1"/>
	<text x="410" y="280" fill="white">_parent</text>
</a>
<a xlink:href="http://jorgeatgu.com" cursor="pointer"  target="_top">
	<rect x="540" y="250" width="150" height="50" fill="crimson" stroke="navajowhite"  stroke-width="1"/>
	<text x="580" y="280" fill="white">_top</text>
</a>
<a xlink:href="http://jorgeatgu.com" cursor="pointer"  target="_blank">
	<rect x="710" y="250" width="150" height="50" fill="crimson" stroke="navajowhite"  stroke-width="1"/>
	<text x="750" y="280" fill="white">_blank</text>
</a>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/JCqyt/)

####Soporte

![](https://github.com/jorgeatgu/scalable/blob/master/images/soporte/primera.jpg)
