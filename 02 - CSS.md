### Presentación Y Objetivos

## 1. Introducción

Tu primer objetivo fue crear la estructura de tu primera página web. Ahora deberás aprender CSS para darle estilos. 


## 2. Objetivos

Al finalizar esta clase podrás:
- Aplicar CSS en un documento HTML.
- Trabajar con selectores CSS y darle estilos a tus páginas.
- Comprender los conceptos de herencia y especificidad en CSS.
- Utilizar el `div` para generar secciones.


+++ 🎶 Inspiración musical

<iframe width="600" height="355" src="https://www.youtube.com/embed/nVrdXUHvsF0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

+++


---

<!-- Contenido -->

### CSS

## 1. Definición

 📚[CSS](https://developer.mozilla.org/es/docs/Web/CSS) (_Cascading Style Sheets_) es un lenguaje de estilo utilizado para describir la apariencia y formato de documentos HTML.

CSS se utiliza para aplicar estilos a elementos HTML, por ejemplo:
- Cambiar el tamaño y el color de texto;
- Establecer fondos y bordes; 
- Ajustar el espacio y la disposición de elementos en la página; 


## 2. Cómo Escribir CSS
 
La sintaxis básica de CSS se compone de estos elementos:
 
![csspartes.png](https://i.imgur.com/tTbemfV.png)
 
 
- **Selector**: Es un comando que selecciona uno o más elementos del documento HTML. Por ejemplo, podemos darle un estilo particular a todo un párrafo dentro de nuestro documento HTML, o solo una palabra dentro de ese mismo párrafo.
- **Declaración**: Es lo que indica **qué cambiaremos** y se escribe dentro de llaves (**{}**). A su vez, se compone de:
  - **La propiedad**: Es el aspecto del elemento que queremos modificar (por ejemplo, el color, el tamaño de la letra, etc.).
  - **Un valor para esa propiedad**: Es lo que define de qué manera modificaremos la propiedad y se separa por dos puntos (**:**).
En el siguiente ejemplo, seleccionaremos los párrafos para darles un color rojo a su tipografía.

⚠️  **Importante:** Si querés modificar al mismo tiempo varias propiedades, podés separarlas con un punto y coma **(;)**. El código se verá de esta forma:

```css
selector { 
  propiedad: valor; 
  otraPropiedad: valor; 
} 
```
Siguiendo el ejemplo anterior, podríamos cambiar la familia tipográfica de los párrafos agregando la propiedad `font-family` y dándole el valor `verdana`:

```css
p { 
  color: red; 
  font-family: verdana; 
} 
```


Para modificar varias propiedades de un mismo elemento, mirá el siguiente ejemplo: 

```css
h1 { 
  font-family: verdana; 
  color: green; 
  background-color: yellow; 
}
```

|||

En este ejemplo, estamos modificando un título dándole una familia tipográfica `verdana`, con color de letra `verde` y un color de fondo `amarillo`. 

- Selector: `h1`
- Propiedad: font-family (tipografía).
- Valor de la propiedad: verdana. 
- Propiedad 1: color (color de la tipografía).
- Valor de la propiedad 1: verde. 
- Propiedad 2: background-color (color de fondo).
- Valor de la propiedad 2: amarillo. 

|||



Para declarar muchas reglas seguidas en un mismo CSS, escribimos una debajo de la otra de esta manera:

```css
h1 { 
  font-family: verdana; 
}

p { 
color: green; 
background-color: yellow; 
}

em {
font-size: 300%;
}
```

⚠️  **Importante:** Estos ejemplos usan selectores de elementos HTML genéricos, es decir, seleccionan todos los `h1`, `p`, `em`, etc. Luego, veremos otros selectores más específicos.




 <!----
+++ Listado De Propiedades CSS

Hay muchísimas propiedades CSS que se pueden modificar. Acá hay una [lista exhaustiva](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) en caso de que quieras investigar. 
Recordá evitar la complejidad y enfocarte en aquellas propiedades que se usen con más frecuencia. 
 
![code_anxiety.jpg](https://pledu-plataforma5.s3.amazonaws.com/5bc731d2-55f7-4462-b8e1-86e32484242e/code_anxiety.jpg)
 
+++

---



### Formas De Aplicar CSS A Un Documento HTML

Hay maneras más (o menos) eficientes de aplicar CSS a un documento HTML. Mirá este video para aprender la diferencia entre ellas:

<iframe width="600" height="355" src="https://www.youtube.com/embed/NNjHbraaV4U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Como viste en el video, hay 3 maneras de aplicar CSS a un documento HTML, según la escala del proyecto:
1. Mediante el atributo `<style>`.
2. Mediante el _tag_ `<style>`.
3. Vincular el código de un archivo `.css` externo (**recomendada**).
 

#### 1. Mediante El Atributo `<style>`

Para incluir CSS de esta forma, directamente le agregamos el **atributo** `<style>` al elemento HTML que queremos modificar. Luego, le asignamos como **valor** un par propiedad-valor (del inglés `key-value pair`), que indique la **propiedad** CSS que queremos cambiar y cuál será su valor.

Por ejemplo, si quisiéramos darle un color de fondo gris al `body` lo escribiríamos así:

```html
<body style="background-color:lightgrey">
```

⚠️ **Importante:** Usar el atributo `<style>` tiene un claro problema de escalabilidad, por lo tanto, no es una práctica recomendable.


+++📚 ¿Qué Quiere Decir Que No Es Escalable?
 


El concepto de **escala** o **escalabilidad** es la propiedad deseable de un sistema, red o proceso, que indica su habilidad para reaccionar o adaptarse sin perder calidad. 

También, para manejar el crecimiento continuo de trabajo de manera fluida. Es decir, estar preparado para hacerse más grande sin perder calidad en los servicios ofrecidos. 

Por ejemplo, si tengo una página con 100 párrafos y quisiera cambiarle el tamaño de la tipografía usando el atributo `style`, tendría que escribir un código por párrafo, repitiendo lo mismo 100 veces. 

 
+++



</div>

#### 2. Mediante El Tag `<style>`

El _tag_ `<style>` se aplica dentro del `<head>` al principio del documento HTML y va a contener las reglas CSS entre su _opening_ y _closing tag_ (`<style>`...`</style>`). 
 
![tag.jpg](https://i.imgur.com/gtAxmbx.jpg)
 
 
⚠️ **Importante:** Esta forma tampoco es recomendable porque carece de **escalabilidad** y porque no respeta la separación entre estructura y contenido. Solo sirve para probar cambios rápidos en una página.
 
#### 3. Vincular El Código De Un Archivo `.css` Externo
 
Para solucionar los problemas que vimos antes, la forma correcta de incorporar CSS en un HTML es hacer un documento `.css` y vincularlo en el HTML usando el _tag_ `<link>` dentro del `<head>`. De esta manera, se aplican las reglas CSS contenidas en un documento externo a una, o más, páginas HTML. 

<div class="editor-recuadro">

Claramente, esta práctica es **mucho más escalable** porque con un solo documento CSS, podés darle estilo a muchos archivos HTML. 
</div>


 
Los 3 atributos clave que deberás escribir en el `<head>` del HTML son:
 
![head](https://i.imgur.com/obdRy3f.jpg)
 
 
1. El **atributo `href`**: Indica la dirección dónde se aloja el archivo con las reglas CSS. Va siempre entre comillas.
2. El **atributo `rel`**: Indica que el archivo que estamos trayendo es una hoja de estilos CSS. Siempre lleva el valor `stylesheet`. 
3. El **atributo `type`**: Indica que el contenido que traemos será texto y reglas CSS. Siempre lleva el valor `text/css`.

## Te toca a vos: creá un archivo `.css`

<iframe width="600" height="355" src="https://www.youtube.com/embed/Drv5gmt0b_o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Para probar estos pasos, hacé lo siguiente: 
1. Dirigite a la carpeta donde hiciste tu blog personal y enlazá tu `index.html` con el nuevo archivo `style.css`.
2. Luego, indicá en este último archivo que todos los `p` tengan un fondo rojo (como en el ejemplo de arriba). 
3. Por último, abrí tu página en el _browser_ y fijate que se haya aplicado el cambio. 



|||
 

![imagen de solución](https://i.imgur.com/PLFruS3.png[/img])
  
|||


📛 Si todo funciona correctamente, avanzá a la siguiente sección.


---

### `class` / `id`

## 1. Definición

Para modificar elementos HTML puntuales podemos usar los atributos `id` y `class`.

Sin embargo, hay algunas diferencias importantes entre ellos que es necesario tener en cuenta:


<iframe width="600" height="355" src="https://www.youtube.com/embed/jCQOuYEi7q4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


El atributo `id` permite seleccionar de manera específica un elemento HTML y darle un estilo único. En cambio, el atributo `class` sirve para dar estilo a varios elementos HTML al mismo tiempo. 
 
Es decir, un elemento HTML puede tener solo un ID que será aplicado únicamente a ese elemento pero se le puede aplicar muchas clases al mismo tiempo. Incluso, puede compartir una `class` con otros elementos. 
 
Imaginemos que hacemos un sitio con los integrantes de mi familia. Mi perro Ron sería una `<p>` en mi HTML. Ron es único y, por lo tanto, tendrá un `id` exclusivo para él.
 
`
id="Ron"
`
 
No obstante, Ron comparte algunas características con otros integrantes. Por ejemplo, es un `perro` y es forma parte de las `mascotas`. 
 
![Ron](https://i.imgur.com/91t04KO.jpg)
 
Si quisiéramos asignar alguna de estas características a otros integrantes de mi familia al mismo tiempo, tendríamos que usar el atributo `class`. Por ejemplo, a mi gato Limón.
 
![Limón](https://i.imgur.com/GOePk48.jpg)
 

+++ Ron y Limón

![coquito-min.jpg](https://i.imgur.com/WtFnK0C.jpg)
 
+++
 
## 2. Sintaxis

####   a. `class`
Como vimos, el atributo `class` sirve para dar estilo a varios elementos HTML al mismo tiempo. 
 
En HTML se asigna usando esta sintaxis:
 
```html
<p class="mascota"> </p>
```
 
Es decir, se agrega el atributo `class` dentro del _tag_ que se quiere modificar.
 
En CSS, deberás seleccionarlo usando el punto (`.`) pegado al **nombre que le diste a esa clase**. Luego, indicarás entre llaves `{}` cuáles son las reglas que le aplicarás. Por ejemplo: 
 
```css
.mascota {
  font-size: 150%;
  color: white;
}
```
 
En este caso, todos los elementos HTML que tengan el atributo `mascotas` tendrán un tamaño tipográfico al `150%` y un color de letra `blanco`.

####   b. `id`

Retomando nuestro ejemplo, si quisiéramos darle un estilo único a mi perro Ron y otro distinto a mi gato Limón, deberíamos:
 
- En el HTML, se debe asignar el ID a la etiqueta de cada uno: 
 
```
<p id="ron"> Mi perro Ron </p>
```
 
```
<p id="limon"> Mi gato Limón </p>
```
- En el CSS, seleccionar ese `id` usando un numeral `#` seguido por el nombre:
 
```css
#ron {
  font-style:italic;
  font-family:impact;
}
```
 
```css
#limon {
  font-style:normal;
}
```
 
Así, “Mi perro Ron“ tendrá una tipografía en itálica, mientras que “Mi gato Limón” tendrá una tipografía por _default_.
 
🛎 **Recordá:** Una misma regla puede incluir muchas características.


## 3. Ejemplos

#### a. `class`

- HTML: 

```html
<!-- Aplicación de la clase "texto-rojo" a un elemento p-->
<p class="texto-rojo">Este texto y otros con esta clase serán rojos </p>
```

- CSS:
```css
/* Definición de la clase "texto-rojo" que aplican a todos los que tengan */
.texto-rojo {
  color: red;
}
```
#### b. `id`

- HTML:
```html
<!-- Aplicación del identificador "titulo-principal" a un elemento h1 en HTML -->
<h1 id="titulo-principal">Este es el título principal</h1>
```
- CSS:
```css
/* Definición del identificador "titulo-principal" ya que hay solo uno*/
#titulo-principal {
  font-size: 24px;
  font-weight: bold;
}
```

## 4. Estilos en `<div>`
Podrás también aplicarle `class` y/o  `id`
a tus `div` para unificar los estilos de determinada sección.

- HTML:

```html
<div class="contenedor">Contenido del div</div>
```
- CSS:
```css
.contenedor {
  color: red;
}
```


<iframe width="600" height="355" src="https://www.youtube.com/embed/woPtxnMBbDc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>



## 5. Herencia

Tené siempre en cuenta el principio de [herencia](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance). 

Este principio  implica que se pueden anidar unos elementos dentro de otros. Esto mismo sucede cuando se aplican reglas de estilo en CSS.
 
Es decir que si le asignamos una regla CSS a un elemento HTML `padre` (o _parent_), también se aplicará a sus elementos `hijos` (_children_). A no ser que alguna de las propiedades de los `hijos` sobreescriban, luego, la regla dada en el inicio (`padre`). 

![DOM](https://i.imgur.com/lDbuOr7.jpg)


Trabajaremos sobre este principio en uno de los ejercicios. Ahora, avanzá a la siguiente sección.

---

### Especificidad En CSS
 
📚 La **especificidad** se refiere al criterio que aplican los navegadores para decidir qué regla CSS aplicar cuando estas son contradictorias entre sí. Es decir, el _browser_ determinará cuál es la más relevante para ese elemento.
 
¿Qué pasaría si creamos una regla que aumenta el tamaño de la letra a los párrafos y otra que los reduce?
 
Teniendo en cuenta el siguiente bloque de código: ¿cuál regla se aplicará? ¿La que aumenta el tamaño tipográfico o la que lo reduce?
1. En tu hoja de estilo del último ejercicio, creá una regla que seleccione los párrafos y le cambie la propiedad `font-size` a `10%`.
2. Inmediatamente después, creá una regla que le cambie el `font-size` a `400%`. 
3. Guardá los cambios, volvé al navegador y refrescá la página. ¿Qué tamaño de tipografía tienen los párrafos?
 
|||

El navegador aplica la regla que está más abajo en el documento CSS.

|||
 
 
⚠️ **Importante:** Cuando CSS encuentra reglas contradictorias, apela al principio de **especificidad** para decidir cuál prevalecerá. Es decir, decide qué es más relevante para ese elemento y, en consecuencia, aplica una regla o la otra. 
 
#### ¿Cómo Se Determina La Especificidad?
 
Cuando creamos un selector, CSS le asigna un valor a su especificidad que varía según el tipo:
 
1. **El selector de `elemento`** (`p {...}`): Cuando seleccionamos elementos HTML genéricos tiene una especificidad de 1 y es el menos específico. 
2. **El selector de `class`** (`.ejemplo {...}`): Es menos genérico que el selector de elemento y, por lo tanto, tiene una especificidad de 10.
3. **El selector de `id`** ( `#ejemplo {...}`): Al ser el menos genérico (o el más específico) tiene una especificidad de 100. 
 
Si en un mismo archivo hubiera reglas contradictorias entre estos tres selectores, se aplicaría el `id`, por ser la de mayor especificidad.

<div class="editor-recuadro">

⚠️ **Importante:** Si hay dos reglas contradictorias con la misma especificidad se aplica la última que fue declarada (es decir, la que está más abajo en el CSS). 
</div>
 

 
Para probarlo, volvé a la hoja de estilo y cambiá el orden de las reglas que modifican el tamaño del párrafo. ¿Cómo lo ves ahora?
 
+++ **¿Cómo Calcular La Especificidad De Distintos Selectores?**
 
Esta [página](https://specificity.keegan.st/) te puede resultar útil para calcular la especificidad de distintos selectores.

🤓 No te detengas en aquellos que aún no conocés; son más complejos y los veremos más adelante.

+++📚

---

### Modelo de Caja 

Hay un concepto fundamental en HTML y CSS que es el del Modelo de Caja o *Box Model*. Mirá este video y aprendé más de este tema: 

<iframe width="600" height="355" src="https://www.youtube.com/embed/IVv2JjgqSxE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

En un documento HTML cada elemento es representado como una *caja rectangular* con 4 capas de profundidad: 

+ **Margen (_margin_):** es el espacio que separa un elemento de los otros. En este caso, es el espacio entre las cajas.
+ **Borde (_border_):** es la línea de la caja que marca su límite. Podemos hacerlo visible con diferentes grosores, estilos y colores.
+ **Padding:** es el espacio que separa el borde de la caja de su contenido. 
+ **Contenido (content):** es todo lo que está contenido en el elemento. Puede ser, por ejemplo, un texto en un `<h1>`, una imagen o cualquier _tag_ anidado.

 ![css_box_model-min.png](https://i.imgur.com/MyUda4S.png)

🎨 Gracias a CSS, podrás manipularlas para tener un diseño más atractivo.

Las propiedades **margin**, **border** y **padding**, tienen 4 lados que se pueden modificar individualmente:
- Top
- Right 
- Bottom
- Left

+++ ¿Qué son las Propiedades Abreviadas?

Para darle diferentes valores a cada uno de los lados, no hace falta escribir:

```css
div {
    margin-top: 5px;
    margin-right: 2px;
    margin-bottom: 10px;
    margin-left: 15px;
}
```

Podemos ser más eficientes y escribir de forma abreviada: 

```css
div {margin: 5px 2px 10px 15px;
}
```
 
Así, le daremos los 4 valores a los distintos lados siguiendo las agujas del reloj: arriba, derecha, abajo e izquierda.



Entrá en este [link](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties#:~:text=When%20three%20values%20are%20specified,in%20that%20order%20(clockwise)) y conocé más acerca de las Propiedades Abreviadas.

+++

<iframe width="600" height="355" src="https://www.youtube.com/embed/Azcyg_6rLU0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>



 
+++ 

![inspector_box_model-min.png](https://i.imgur.com/KQPW6ir.png)

 
 
 
---

### Pseudo-Selectores

📚 Los pseudo-selectores son **palabras clave** que se añaden a los selectores para especificar diferentes estados. Es decir, se **activan** dependiendo de lo que haga el usuario. 

Por lo tanto, si los elementos a los que se aplican estos pseudo-selectores cumplen con estas condiciones o estados, se aplicarán los estilos dados. 

Mirá este video para aprender cómo usar los más frecuentes:

<iframe width="600" height="355" src="https://www.youtube.com/embed/h-27_t_M3OI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**Regla general:** Los pseudo-selectores se escriben en la Hoja de Estilos, seleccionando un elemento HTML seguido por ":" y el nombre del pseudo selector. Por ejemplo:

```css
elemento:hover {color: red}
``` 

#### Los Pseudo-Selectores más frecuentes

+ **Hover (`elemento:hover`):** La regla CSS se aplicará únicamente cuando el usuario pase el *mouse* por encima del elemento indicado. Por ejemplo: 


```css
h1:hover {color:red;}
``` 


En este caso, cada vez que se pase el *mouse* por encima de un `<h1>` se activará regla CSS expresada entre las llaves, haciendo que el color de la letra cambie a rojo.
 
+ **Active (`elemento:active`):** La regla CSS se aplicará cuando el elemento esté siendo activado. Por ejemplo:

```css
#ejemplo:active {background-color: green;}
```

En este caso, cuando se haga click en el elemento con `id="ejemplo"` se activará la regla CSS expresada entre las llaves, haciendo que el color de fondo se ponga verde.

+++ ¿Cómo se activan los elementos?

La **activación**, generalmente, comienza cuando el usuario presiona el botón primario del *mouse* y termina cuando se suelta. `:active` se usa frecuentemente en los elementos `<a>` y `<button>`, pero también se puede aplicar a otros.

**Importante:** Los estilos definidos por `:active` serán anulados por cualquier otro pseudo-selector posterior, relacionado con el enlace, que tenga al menos la misma especificidad (por ejemplo, `:link`, `:hover` o `:visited`). 

**Tip:** Para darle un estilo apropiado a los enlaces, seguí el orden LVHA: `:link`, `:visited`, `:hover` y `:active`. Es decir, `:active` será la última regla que debas definirle a un link. 

+++

+ **Focus (`elemento:focus`):** La regla CSS se aplicará cuando el elemento esté en foco (como el `input` de un formulario que está seleccionado para completar). Por ejemplo:

```css
.formulario:focus {border: 2px solid gold;}
``` 

En este caso, cuando se seleccione un elemento con `class="formulario"` se activará la regla CSS expresada entre las llaves, haciendo que el borde se ponga color dorado.

---

### Propiedades


## 1. `Width` y `Height`

Para cambiar el ancho de un elemento, como el de un `div`, deberás usar la propiedad `width`. Por otro lado, la propiedad `height` define la altura de un elemento.

En estas propiedades, podrás darle al elemento un valor absoluto (una cantidad de píxeles) o relativo a la vista del dispositivo (un porcentaje de la pantalla). 

La diferencia entre uno y el otro es que, usando el relativo te asegurás que el diseño sea *responsive* y se adecue a todos los dispositivos. Más adelante profundizaremos sobre este concepto. 


```css
div {
  width: 20px;
}
```

```css
div {
  width: 50%;
}
```

## 2. Background

Si bien hay más propiedades que podríamos aplicar al background vamos a centrarnos en dos. 

- `background-color`: define el color de fondo de un elemento. 
```css
.caja {
  background-color: blue;
}
```
- `background-image`: define una imagen de fondo para un elemento.

```css
.caja {
  background-image: url("imagen.jpg");
}
```
## ¡Probalo!

- En un archivo HTML vinculado con una hoja de estilos agregá dos `div`.
- Dale a cada `div` un `background-color` diferente para poder diferenciarlos. 
- Hacé que los `div` ocupen sólo la mitad de la pantalla de ancho y toda la panatalla de alto. 
- Achicá la ventana del navegador y confirmá cómo se adapta a cada tamaño. 

<div class="editor-recuadro">

⚠️ **Importante:** usando este criterio podrás notar que miden sólo el 50% del elemento que los contiene. En este caso, los `div` están contenidos dentro del `<body>` que ocupa toda la pantalla. Sin embargo, si estuvieran dentro de otro elemento, el ancho sería un 50% de ese elemento en particular. 
</div>



- Por último, agregá un tercer `div` dentro de uno de los dos y mirá cuanto ocupa.


## Cómo centrar un elemento usando el valor `auto`

El valor `auto` hace que la caja deje el mismo espacio de **margen** de cada lado. Es decir que, eligiendo este valor, la caja quedará centrada. 

Para ver cómo se modifica el posicionamiento de un elemento, seguí estos pasos. Antes de avanzar al siguiente, mirá su posicionamiento usando el Inspector de Chrome.

1. Cambiá el valor de **margin** por `margin: 10px 30px 50px 80px;`.
2. Luego, cambialo por `margin: 0px 100px;`.
3. Por último, dale un `margin: 0px auto;`. Así, tendrá `0px` para arriba y abajo, y `auto` para la derecha y para la izquierda. Es decir, dejará el mismo espacio en cada costado.



<!---->

## 3. Modificando el texto

Para trabajar sobre los textos disponemos de varias propiedades: 
- `color`: define el color del texto de un elemento.
- `font-family`: define el tipo de fuente del texto de un elemento.
- `font-size`: define el tamaño de la fuente del texto de un elemento.

Veamos un ejemplo de cómo utilizar estas propiedades: 
```css
color: blue;
font-family: Arial, sans-serif;
font-size: 16px;
```
- `font-weight`: define el grosor de la fuente del texto de un elemento. Las opciones que tenemos disponibles son: 
```css
font-weight:lighter;
font-weight:normal;
font-weight:bold;
font-weight:bolder;
```

Podemos además colocarle valores que vayan del 100 al 900 considerando que a medida que aumenta el valor aumenta el grosor. Como referencia el valor normal equivale al 400 y el bold a 700. 
Siempre que nos inclinemos por esta opciones debemos tener en cuenta que puede que no todas las fuentes soporten los 9 valores.

- `text-align`: define la alineación horizontal del texto de un elemento. Las opciones son: `left`, `right` o `center`. 
- `text-decoration`: define la decoración del texto (por ejemplo, si está subrayado o tachado). Las opciones son: subrayado (`underline`), suprarrayado (`overline`), tachado (`line-through`) o parpadeo (1). 
- `text-transform`: define la transformación del texto (por ejemplo, si se convierte en mayúsculas o minúsculas).Algunas de las opciones son: 
 
    - `none`: No aplica ninguna transformación al texto. Es el valor predeterminado.

    - `capitalize`: Convierte la primera letra de cada palabra en mayúscula y las demás letras en minúsculas.

    - `uppercase`: Convierte todo el texto a mayúsculas.

    - `lowercase`: Convierte todo el texto a minúsculas.



## ¡Probalo!

Colocá 2 tags `p` en un documento HTML y dales un texto a a cada uno.

* Luego dale al primero un color rojo, font-size de 25px, transformá el texto en mayúsculas y subrayalo.
* Por otro lado, centrá el segundo, tachalo, seleccioná una fuente distinta a la del primero y  dale mayor grosor. 

---

### Unidades 

En CSS existen varias unidades de medida que se utilizan para definir las dimensiones en los elementos de una página web. 
A continuación veremos aquellas más comunes:

 <table >
  <tr>
    <th style="font-size: 10px; font-weight: bold;">Unidad</th>
    <th style="font-size: 10px; font-weight: bold;">Ejemplo</th>
    <th style="font-size: 10px; font-weight: bold;">Descripción</th>
  </tr>
  <tr>
    <td style="text-align: center;">Píxeles</td>
    <td style="text-align: center;"> 200 px</td>
    <td> El píxel es una unidad de medida absoluta y se refiere a un punto físico en la pantalla. 
    Cuando especificamos un tamaño en píxeles, el elemento se renderiza con ese tamaño exacto en todos los dispositivos, independientemente de la resolución de pantalla.
    </td>
  </tr>
  <tr>
    <td style="text-align: center;">Porcentaje</td>
    <td style="text-align: center;">5%</td>
<td>El porcentaje es una unidad de medida relativa que se basa en el tamaño del elemento padre. Por ejemplo, si especificas que el ancho de un elemento es del 50%, significa que ocupará la mitad del ancho de su elemento padre.</td>
  </tr>
   <tr>
    <td style="text-align: center;">Rem</td>
    <td style="text-align: center;">1 rem</td>
<td>La unidad "rem" (root em) es una unidad de medida relativa basada en el tamaño de la fuente del elemento raíz (normalmente el elemento "html" del documento). Por ejemplo, si establecemos el tamaño de fuente del elemento raíz en 16 píxeles, 1rem será igual a 16 píxeles. La ventaja de utilizar "rem" es que cuando cambiamos  el tamaño de fuente en el elemento raíz, todos los elementos que utilicen "rem" como unidad se ajustarán proporcionalmente.</td>
  </tr> 
     <tr>
    <td style="text-align: center;">Em</td>
    <td style="text-align: center;"> 2em</td>
<td> La unidad "em" es similar a "rem" en el sentido de que es relativa al tamaño de fuente del elemento padre. Si establecemos el tamaño de fuente de un elemento en 2em, será el doble del tamaño de fuente del elemento padre. Al igual que "rem", "em" también permite ajustar los tamaños de manera proporcional.</td>
  </tr> 
   <tr>
    <td style="text-align: center;">Viewport units</td>
    <td style="text-align: center;"> 50vw</td>
<td>Las unidades de viewport (unidades de vista) son relativas al tamaño del viewport o ventana gráfica del navegador. Hay cuatro unidades de viewport: vw (1% del ancho del viewport), vh (1% de la altura del viewport), vmin (el mínimo entre vw y vh) y vmax (el máximo entre vw y vh). Estas unidades son útiles para crear diseños responsivos que se adapten al tamaño de la pantalla.</td>
  </tr> 
</table> 

##  Unidades CSS en Acción

Incorporá estas medidas y visualizá los cambios ocurridos con el siguiente ejemplo. Recordá abrir el navegador y analizar si estas modificaciones coinciden con lo que esperabas.

1. En un documento HTML creá un `div` con la clase `box` y, dentro del mismo, colocá un `p`.

2. Vinculá el documento con una hoja de estilos. 

3. Dale un `background-color` para distinguirlo, un `width` y un `height` de 200 px al `div` con la clase `box`. 

4. Utilizá la unidad `vw` para establecer el ancho del `div` en el 50% del ancho del viewport.

5. Utilizá la unidad `vh` para establecer la altura del `div` en el 100% de la altura del viewport.

```css
div{
   width: 50vw;
   background-color: aquamarine;
   height: 100vh;
   font-size: 20px;
}
```
6. Dale al `p` un `background-color` distinto al del `div`, y un padding del 15%. 

7.  Ahora, dale un `font-size` de 20px al `div`. Luego, sumale al `p` un `font-size` de 2em. Posteriormente, cambiá y que sea de 0.5 em. 

🤔 Pregunta: ¿a cuántos píxeles corresponde en cada caso?

---

### Listado de Propiedades

👉 Aquí te dejamos un listado con las más frecuentes:

- `animation`: referencia abreviada para todas las propiedades de animación
- `border`: define el estilo, grosor y color del borde de un elemento.
- `border-radius`: define la curvatura de las esquinas de un borde.
- `box-shadow`: define una sombra alrededor de un elemento.
- `cursor`: define el tipo de cursor que se muestra cuando se coloca el cursor sobre un elemento.
- `display`: define cómo se muestra un elemento en la página (por ejemplo, como bloque o en línea).
- `line-height`: define la altura de línea del texto de un elemento.
- `list-style`: define la apariencia de los elementos de una lista (por ejemplo, si tienen viñetas o números).
- `margin`: define el espacio entre el borde de un elemento y otros elementos cercanos.
- `opacity`: define la opacidad de un elemento.
- `overflow`: define cómo se maneja el contenido de un elemento si es más grande que el espacio disponible.
- `padding`: define el espacio entre el borde y el contenido de un elemento.
- `position`: define cómo se posiciona un elemento en relación con otros elementos en la página. La veremos más adelante.
- `transition`: define la transición suave de un cambio en un elemento.
- `visibility`: define si un elemento es visible o no.
- `z-index`: define el orden de apilamiento de elementos superpuestos.
- `grid-template-columns`: define el número y tamaño de las columnas en una cuadrícula de diseño de rejilla.
- `grid-template-rows`: define el número y tamaño de las filas en una cuadrícula de diseño de rejilla.

<div class="editor-recuadro">

🛎️ Recordá que cuando escribas una propiedad en CSS te aparecerán diferentes alternativas para customizarla.
</div>



## 🔍 Links útiles
- Si querés conocer más propiedades y su utilidad, ingresá a este <a href="https://developer.mozilla.org/es/docs/Web/CSS/Reference" target="_blank">link</a>.
- Para practicar otras propiedades más modernas, accedé a este <a href="https://blog.bitsrc.io/14-awesome-css-properties-you-need-to-know-9cee5b364990" target="_blank">artículo</a>.

---

## Proyecto

### Practicá

Para aplicar lo aprendido en tu proyecto **Plataforma Disco** vas a seguir los siguientes pasos:

- Creá un archivo `styles.css` y vinculalo con tu archivo `index.html`. En este vas a trabajar para comenzar a darle estilo a tu paǵina. 

No te preocupes si no sabés bien qué estética querés darle a tu paǵina, es solo para practicar. En las clases 4 y 5 vamos a profundizar sobre los estilos. 

## Estilado básico

1.  Dale a tu paǵina un color de fondo, también podés usar una imágen si lo deseas, deberás además darle color a cada sección para generar contraste. 

2. Elegí una tipografía, un color y un tamaño de fuente para cada sección. 

3. Utilizá lo visto acerca del modelo de caja para estilar los distintos componentes, dándoles un _padding_ y un _margin_ en caso de ser necesario. 

4. Centrá los títulos y la sección "canciones".

5. Estilá el link para escuchar la canción. Deberá diferecniarse de los títulos de las canciones.

A modo de ejemplo:

![Imgur](https://imgur.com/b8OsdwZ.png)

---

### Conclusión

## 02 - Paint IT, CSS

![fin de clase](https://media.giphy.com/media/d31w24psGYeekCZy/giphy.gif)



En esta clase aprendiste sobre CSS y comprendiste la importancia de la presentación visual de las páginas web. También aprendiste a modificar su estilo para lograr diseños más atractivos.

En ese sentido, avanzaste con los conceptos fundamentales de CSS, tales como modelos de caja, clases e ID, propiedades, entre otros, lo que te permitió crear estilos personalizados para tu página web. 

De la misma forma, pudiste aplicar estos conocimientos en diferentes ejercicios y en tu proyecto, brindándote la oportunidad de experimentar con diferentes estilos y diseños.

<div class="editor-recuadro">

🚀 En el **Bootcamp** podrás ampliar tus conocimientos sobre CSS trabajando con SASS y media queries, por ejemplo. Estas herramientas te ayudarán a personalizar y a adaptar la interfaz de tus sitios, permitiendo estilos y diseños más flexibles y _responsives_.
</div>


#### ¡Excelente trabajo! 🥳
