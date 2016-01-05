
#Degradados
Los degradados son una transición lineal o radial entre dos o más colores. Tenemos dos tipos, el degradado lineal que obtenemos con la etiqueta `<linearGradient>` y el radial con la etiqueta `<radialGradient>`. Hay que dar un ***ID*** a los degradados para usarlos posteriormente sobre los elementos a los que queremos aplicar el degradado, esto lo haremos con `fill=”url(#nombreDelDegradado)”` también es recomendable declarar los degradados dentro de las etiquetas `<defs>`.

##linearGradient
Con este degradado conseguimos cambios de color de forma lineal. Lo podemos utilizar de forma horizontal, vertical, diagonal, también podemos hacer que el relleno sólo afecte a una parte del objeto donde se aplica.

Los atributos que tenemos disponibles para `linearGradient` son los siguientes:

Para posicionar el degradado tenemos las ***x1*** e ***y1*** que definen el punto inicial que marcará la dirección del degradado, también tenemos ***x2*** e ***y2*** que marcarán el punto final del degradado. La unidad de valor por defecto es el porcentaje. En caso de no definir las coordenadas estos serán sus valores por defecto: `x1="0%" y1="0%" x2="100%" y2="0%"`

Con el atributo ***gradientUnits*** definimos el sistema de coordenadas del degradado a través de los valores ***userSpaceOnUse*** con el cual las coordenada ***x1 y1 x2 y2*** tomarán como referencia las medidas del documento, con el atributo ***objectBoundingBox*** las coordenadas ***x1 y1 x2 y2*** tomarán como referencia las medidas del objeto al que vamos a aplicar el degradado.

Una vez definidas las propiedades de nuestro degradado vamos a pasar a definir que colores y que posiciones van a tener a lo largo del degradado. Para ello tenemos que utilizar la etiqueta stop, esta etiqueta tiene dos atributos, el primero de ellos `stop-color=””` lo utilizamos para definir el color que queremos en esa franja del degradado, el segundo es ***offset*** y lo utilizaremos para indicar la posición que queremos que ocupe este color en el degradado, admite números del 0 al 1, y porcentajes del 0% al 100%, quizás nos sea más fácil utilizar los porcentajes como unidad. Por último podemos controlar la opacidad de los colores a través de `stop-opacity=””`, los valores que admite van desde el 0 al 1.

Vamos a utilizar el mismo degradado para los tres rectángulos, sólo voy a poner una vez el código del degradado ya que ocupa demasiado y no tiene sentido repetirlo continuamente.

{lang="html", linenos="off"}
~~~~~~~
<stop offset="0%" stop-color="khaki"/>
<stop offset="10%" stop-color="khaki"/>
<stop offset="10%" stop-color="crimson"/>
<stop offset="20%" stop-color="crimson"/>
<stop offset="20%" stop-color="khaki"/>
<stop offset="30%" stop-color="khaki"/>
<stop offset="30%" stop-color="crimson"/>
<stop offset="40%" stop-color="crimson"/>
<stop offset="40%" stop-color="khaki"/>
<stop offset="50%" stop-color="khaki"/>
<stop offset="50%" stop-color="crimson"/>
<stop offset="60%" stop-color="crimson"/>
<stop offset="60%" stop-color="khaki"/>
<stop offset="70%" stop-color="khaki"/>
<stop offset="70%" stop-color="crimson"/>
<stop offset="80%" stop-color="crimson"/>
<stop offset="80%" stop-color="khaki"/>
<stop offset="90%" stop-color="khaki"/>
<stop offset="90%" stop-color="crimson"/>
<stop offset="100%" stop-color="crimson"/>
~~~~~~~

Ahora vamos a ver las diferentes opciones, recordad que sólo vamos a ver las etiquetas principales y que dentro de ellas debería de ir el código que acabamos de ver.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-8/Capitulo-8-linearGradient.jpg)

{lang="html", linenos="off"}
~~~~~~~
<defs>
	<linearGradient id="userspace" gradientUnits="userSpaceOnUse">
	</linearGradient>
	<linearGradient id="objectBounding" gradientUnits="objectBoundingBox">
	</linearGradient>
	<linearGradient id="objectBounding2" gradientUnits="objectBoundingBox" x1="50%" y1="20%" x2="10%" y2="10%">
	</linearGradient>
</defs>

<rect x="500" y="20" fill="url(#userspace)" stroke="black" stroke-width=".5px" width="300" height="100"/>
<rect x="500" y="180" fill="url(#objectBounding)" stroke="black" stroke-width=".5px" width="300" height="100"/>
<rect x="500" y="320" fill="url(#objectBounding2)" stroke="black" stroke-width=".5px" width="300" height="100"/>

~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/iboLr/)

Al primer rectángulo le aplicamos el degradado ***#userspace*** el cual tiene el atributo ***gradientUnits*** con ***userSpaceOnUse***, el degradado ocupará todo el documento.

Al segundo rectángulo le aplicamos el degradado ***#objectBounding*** el cual tiene el atributo ***gradientUnits*** con ***objectBoundingbox*** así que el degradado se aplica solamente al elemento, en este caso al rectángulo.

Al tercer rectángulo le aplicamos el degradado ***#objectBounding2*** el cual tiene el atributo ***gradientUnits*** con ***objectBoundingbox*** pero le hemos indicado unas coordenadas que modifican el inicio y el fin del degradado.

####Soporte

![](images/soporte/primera.jpg)

En **iOS5.1.1** las líneas que separan los colores de `linearGradient` se ven borrosas.

##radialGradient

Con este degradado conseguimos cambios de color de forma circular. Los atributos que tenemos disponibles para ***radialGradient*** son también utilizados en ***linearGradient***.

Para posicionar el degradado radial tenemos tres coordenadas, estás son ***cx cy*** que formarán el centro del degradado y ***r*** que determinará el tamaño, si ninguna de estas coordenadas están definidas su valor por defecto será del 50%. Las coordenadas ***fx fy*** definirán el punto focal del degradado. Con el atributo ***gradientUnits*** definimos el sistema de coordenadas del degradado a través de los valores ***userSpaceOnUse*** con el cual las coordenada ***cx cy r fx fy*** tomarán como referencia las medidas del documento, también tenemos el atributo ***objectBoundingBox*** con el cual las coordenadas ***cx cy r fx fy*** tomarán como referencia las medidas del objeto al que vamos a aplicar el degradado.

Una vez definidas las propiedades de nuestro degradado vamos a pasar a definir que colores y que posiciones van a tener a lo largo del degradado. Para ello tenemos que utilizar la etiqueta stop, esta etiqueta tiene dos atributos, el primero de ellos `stop-color=””` lo utilizamos para definir el color que queremos en esa franja del degradado, el segundo es ***offset*** y lo utilizaremos para indicar la posición que queremos que ocupe este color en el degradado, admite números del 0 al 1, y porcentajes del 0% al 100%, quizás nos sea más fácil utilizar los porcentajes como unidad.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-8/Capitulo-8-radialGradient.jpg)

{lang="html", linenos="off"}
~~~~~~~
<defs>
	<radialGradient id="primero" gradientUnits="objectBoundingBox">
		<stop offset="0%" stop-color="khaki"/>
		<stop offset="100%" stop-color="crimson"/>
	</radialGradient>
	<radialGradient id="segundo" gradientUnits="objectBoundingBox" cx="50%" cy="50%" r="50%" fx="70%" fy="70%">
		<stop offset="0%" stop-color="khaki"/>
		<stop offset="100%" stop-color="crimson"/>
	</radialGradient>
	<radialGradient id="tercero" gradientUnits="objectBoundingBox" cx="50%" cy="50%" r="50%" fx="20%" fy="20%">
		<stop offset="0%" stop-color="khaki"/>
		<stop offset="100%" stop-color="crimson"/>
	</radialGradient>
</defs>
<rect x="550" y="15" fill="url(#primero)" stroke="black" stroke-width=".5px" width="150" height="150" rx="20"/>
<rect x="550" y="185" fill="url(#segundo)" stroke="black" stroke-width=".5px" width="150" height="150" rx="20"/>
<rect x="550" y="370" fill="url(#tercero)" stroke="black" stroke-width=".5px" width="150" height="150" rx="20"/>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/fzmHi/)

####Soporte

![](images/soporte/primera.jpg)

##spreadMethod

Este atributo sirve para ***linearGradient*** y ***radialGradient***, se utiliza para definir el relleno del degradado a lo largo del objeto, y sólo es efectivo cuando el degradado no consiga rellenar todo el objeto. Disponemos de tres valores ***pad*** que es el valor por defecto y con el que el degradado es extendido a lo largo del objeto, ***repeat***, el degradado se repite a lo largo del objeto,  y por último ***reflect*** con el cual conseguimos que el degradado se refleje en el objeto.

Vamos a ver un ejemplo utilizando todos los valores con este orden ***pad repeat reflect***.

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-8/Capitulo-8-spreadMethod.jpg)

{lang="html", linenos="off"}
~~~~~~~
<defs>
	<linearGradient id="uno"spreadMethod="pad" x1="87" y1="206" x2="259" y2="206" gradientUnits="userSpaceOnUse">
		<stop offset="0" stop-color="khaki"/>
		<stop offset="1" stop-color="crimson"/>
	</linearGradient>

	<linearGradient id="dos" spreadMethod="repeat" x1="87" y1="206" x2="259" y2="206" gradientUnits="userSpaceOnUse">
		<stop offset="0" stop-color="khaki"/>
		<stop offset="1" stop-color="crimson"/>
	</linearGradient>

	<linearGradient id="tres" spreadMethod="reflect" gradientUnits="userSpaceOnUse" x1="87" y1="206" x2="259" y2="206">
		<stop offset="0" stop-color="khaki"/>
		<stop offset="1" stop-color="crimson"/>
	</linearGradient>
</defs>

<rect x="500" y="20" fill="url(#uno)" stroke="black" width="300" height="100"/>
<rect x="500" y="180" fill="url(#dos)" stroke="black" width="300" height="100"/>
<rect x="500" y="320" fill="url(#tres)" stroke="black" width="300" height="100"/>
~~~~~~~
[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/kmsGi/)

####Soporte

![](images/soporte/sexta.jpg)


##gradientTransform

Por último vamos a ver ***gradientTransform***, este atributo sirve para añadir transformaciones como ***matrix***, ***translate***, ***scale***, ***rotate***, ***skewX***, ***skewY*** a nuestros degradados.

Las transformaciones se añaden a las etiquetas `<linearGradient>` y `<radialGradient>` con `gradientTransform=""` y entre las comillas el nombre de la transformación con el valor que le queramos dar.

En el ejemplo que vamos a ver a continuación he aplicado al mismo degradado un `gradientTransform="rotate(25)"` y un `gradientTransform="translate(45)"`

![](https://github.com/jorgeatgu/scalable/blob/master/images/Capitulo-8/Capitulo-8-gradientTransform.jpg)

[![](https://github.com/jorgeatgu/scalable/blob/master/images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/nxyHE/)

{lang="html", linenos="off"}
~~~~~~~
<linearGradient id="rotate" gradientUnits="userSpaceOnUse" gradientTransform="rotate(25)">
<linearGradient id="translate" gradientUnits="userSpaceOnUse" gradientTransform="translate(45)">
~~~~~~~

####Soporte

![](images/soporte/primera.jpg)


