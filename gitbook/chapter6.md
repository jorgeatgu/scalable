# Transformaciones

En este capítulo vamos a ver como podemos aplicar una serie de transformaciones a los siguientes elementos, `<a>` `<clippath>` `<defs>` `<foreignobject>` `<g>` `<switch>` `<circle>` `<ellipse>` `<image>` `<line>` `<path>` `<polygon>` `<polyline>` `<rect>` `<text>` `<use>`

Tenemos a nuestra disposición las siguientes transformaciones:

- Translate
- Rotate
- Scale
- SkewX
- SkewY
- Matrix

## Translate

Con esta transformación vamos a desplazar el objeto horizontal y verticalmente a lo largo del documento, para ello contamos con dos valores, el primero de ellos para la coordenada ***x*** y el segundo para la coordenada ***y***. Si tan sólo le pasamos un valor este solamente se aplicará a la coordenada ***x***.

En el código que vamos a ver a continuación los dos rectángulos están posicionados en las mismas coordenadas, el primer rectángulo no sufre ninguna transformación, en cambio al segundo le aplicamos la siguiente transformación `transform="translate(60 100)"` la cual desplaza 60 ***pixels*** hacia la derecha el rectángulo y 100 ***pixels*** hacia abajo.

![](images/capitulo-6/Capitulo-6-translate.jpg)


~~~~~~~
<rect x="500" y="100" width="150" height="150" fill="crimson"/>
<rect x="500" y="100" width="150" height="150" fill="blue" transform="translate(60 100)"/>
~~~~~~~

[![](images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/xbrwe/)


## Rotate

Con esta transformación vamos a rotar el objeto, para ello contamos con tres valores, el primero de ellos es obligatorio y con el determinamos los grados de rotación que le vamos a aplicar al objeto, los cuáles son de 0 a 360 grados. El sentido de la rotación es el mismo que el de las agujas del reloj.

En el código que vamos a ver a continuación los cuatro rectángulos están posicionados en las mismas coordenadas.

El primer rectángulo de color rosa no recibe ninguna transformación.

Al segundo rectángulo de color rojo le vamos a aplicar un `transform="rotate(20)"` esta rotación se hace desde la esquina superior izquierda, es decir desde la coordenada 0,0.

Al tercer rectángulo de color azul le damos los dos valores opcionales `transform="rotate(20 150 150)"` el efecto que vamos a conseguir va a ser distinto, el motivo es que primero aplica un `transform=”translate(150 150)”` donde traslada el elemento 150pixels a lo largo de su coordenada horizontal y vertical, a continuación aplica un `transform=”rotate(20)”`, y por último vuelve a trasladar el elemento -150pixels a lo largo de su coordenada horizontal y vertical con `transform=”translate(-150 -150)”`

Al cuarto rectángulo de color cyan lo vamos a rotar desde su centro con `transform="rotate(20 575 175)"` para rotarlo desde su centro el primer valor lo obtenemos de sumar su posición en la coordenada horizontal `x="500"` más la mitad de su anchura `width="150"` así 500+75 = 575. El segundo valor lo obtenemos de sumar su posición en la coordenada vertical `y=100` más la mitad de su altura `height="150"` así 100+75 = 175.

![](images/capitulo-6/Capitulo-6-rotate.jpg)


~~~~~~~
<rect x="500" y="100" width="150" height="150" fill="pink"/>
<rect x="500" y="100" width="150" height="150" fill="crimson" transform="rotate(20)"/>
<rect x="500" y="100" width="150" height="150" fill="blue" transform="rotate(20 150 150)"/>
<rect x="500" y="100" width="150" height="150" fill="cyan" transform="rotate(20 625 175)"/>
~~~~~~~

[![](images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/hcksx/)

## Scale

Con esta transformación vamos a escalar el objeto, para ello contamos con dos valores, uno para la coordenada horizontal con ***x*** y el otro para la coordenada vertical con ***y***. Si tan sólo pasamos el primer valor la transformación se aplicará a los dos valores.

![](images/capitulo-6/Capitulo-6-scale.jpg)


~~~~~~~
<rect x="500" y="100" width="150" height="150" fill="crimson" transform="scale(.5)"/>
<rect x="500" y="100" width="150" height="150" fill="blue" transform="scale(2 3)"/>
~~~~~~~

[![](images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/osfiE/)

## SkewX

Con esta transformación vamos a sesgar el objeto a lo largo de su coordenada ***x***, vamos a inclinar la posición del objeto a lo largo de su coordenada ***x***, el valor que vamos a pasarle representa los grados del ángulo.

En el ejemplo que vamos a ver a continuación se puede apreciar como el rectángulo se estira horizontalmente hacia su derecha.

![](images/capitulo-6/Capitulo-6-skewX.jpg)


~~~~~~~
<rect x="500" y="100" width="150" height="150" fill="crimson" transform="skewX(5)"/>
<rect x="500" y="300" width="150" height="150" fill="blue" transform="skewX(20)"/>
~~~~~~~

[![](images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/jtHlv/)

## SkewY

Como su nombre indica esta transformación es hermana de ***skewX*** pero en esta ocasión vamos a sesgar el objeto a lo largo de su coordenada ***y***, estiramos la posición del objeto a lo largo de su coordenada ***y***, el valor que vamos a pasarle representa los grados del ángulo.

En el ejemplo que vamos a ver a continuación se puede apreciar como el rectángulo se estira verticalmente hacia abajo.

![](images/capitulo-6/Capitulo-6-skewY.jpg)


~~~~~~~
<rect x="500" y="100" width="150" height="150" fill="crimson" transform="skewY(5)"/>
<rect x="500" y="300" width="150" height="150" fill="blue" transform="skewY(10)"/>
~~~~~~~

[![](images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/yeICs/)

## Matrix

Para esta transformación necesitamos seis valores(a,b,c,d,e,f), con estos valores se realizan una serie de sumas y multiplicaciones que van modificar la posición de las coordenadas del elemento en cuestión.
Los valores se reparten de la siguiente manera:

- ace
- bdf
- 001

Vamos a ver detalladamente todas las operaciones que se realizan con `transform="matrix(1,2,1,4,5,1)"`

Valores que vamos a utilizar del elemento línea:

- x1 = 5
- y1 = 25
- x2 = 20
- y2 = 40

Valores de `transform=”matrix”`:

- a = 1
- b = 2
- c = 1
- d = 4
- e = 5
- f = 1

Primera operación:

- a × x1 + c × y1 + e =
- 1 × 5 + 1 × 25 + 5 = 35

Este primer resultado sustituirá al valor que tenemos en ***x1***

Segunda operación:

- b × x1 + d × y1 + f
- 2 × 5 + 4 × 25 + 1 = 111

Esta segunda operación sustituirá al valor que tenemos en ***y1***

Tercera operación:

- a × x2 + c × y2 + e
- 1 × 20 + 1 × 40 + 5 = 65

Este tercer resultado sustituirá al valor que tenemos en ***x2***

Cuarta operación:

- b × x2 + d × y2 + f
- 2 × 20 + 4 × 40 + 1 = 201

Este cuarto resultado sustituirá al valor que tenemos en ***y2***

Así que después de todas las operaciones el resultado que se aplicará al elemento `<line>` es el siguiente:

![](images/capitulo-6/Capitulo-6-matrix.jpg)


~~~~~~~
<line x1="35" y1="111" x2="65" y2="201"/>
<line x1="5" y1="25" x2="20" y2="40" stroke-width="40px" stroke="crimson"/>
<line x1="5" y1="25" x2="20" y2="40" stroke-width="40px" stroke="blue" transform="matrix(1,2,1,4,5,1)"/>
~~~~~~~

[![](images/logo-codepen.jpg)](http://codepen.io/jorgeatgu/details/biEhe/)

####Soporte

![](images/soporte/primera.jpg)

La única diferencia notable es que en la transformacion scale en **IE10 y IE11** generan un espacio a la derecha del objeto que recibe la transformación.
