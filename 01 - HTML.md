### 01- Presentación Y Objetivos 

## 1. Introducción

<iframe width="600" height="355" src="https://www.youtube.com/embed/o37WIcOp2-4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## 2. Objetivos

Al finalizar esta clase podrás:
- Hacer una wiki de tu banda o artista preferido.
- Conocer los primeros elementos de HTML.
- Trabajar correctamente en el Visual Studio Code.


+++ 🎶 Inspiración musical

Cada nombre de clase vincula su nombre con una canción y con el tópico a trabajar. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/2cZ_EFAmj08" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


+++

---

<!-- Contenidos -->

### Desarrollo Web

## 1. Internet

La carrera de todo _developer_ está íntimamente relacionada con la evolución de _internet_. Por eso, es muy importante entender cómo funciona esta maravilla tecnológica. 

@youtube=ewrBalT_eBM





## ¿Qué sucede cuando navegamos en Internet?

Cuando navegamos en internet, estamos usando un navegador web para acceder a diferentes sitios. Esto nos permite ver contenido, interactuar con aplicaciones y utilizar diferentes servicios en línea. 




![internet y servidores](https://i.imgur.com/Zp5EvCW.gif)



Cuando ingresás una dirección web (**URL**) en el navegador y apretás enter, se genera un pedido (_request_) de la web que estás buscando al proveedor de internet (**ISP**). 

Al recibir el pedido, transforma el nombre de la web en una dirección IP (a través del DNS).

![request](https://i.imgur.com/qtZcQVF.gif)


+++DNS
 
El Sistema de Nombres de Dominio (DNS, por sus siglas en inglés) es un sistema fundamental para el funcionamiento de Internet. Su principal función es traducir los nombres de dominio legibles para los humanos, como "www.ejemplo.com", en direcciones IP numéricas, que son las que los dispositivos utilizan para comunicarse entre sí en la red.
 
+++


## 2. Desarrollo Web 

 Se refiere al proceso de creación de sitios web y aplicaciones web. Se involucran diferentes disciplinas y habilidades, incluyendo diseño gráfico, programación, alojamiento web, seguridad de la información y estrategia de contenido.

<div class="editor-recuadro">

 👩🏻‍💻👨‍💻Un desarrollador web es un profesional que se especializa en el desarrollo de sitios web y aplicaciones. Pueden trabajar en una variedad de roles, desde la programación back-end hasta el diseño front-end. 
</div>
 

👉 Veamos en la siguiente sección de qué se trata HTML y qué tiene que ver con todo esto.


---

### HTML

## 1. Definición

📚 HTML (_HyperText Markup Language_) es un lenguaje de marcado (que se utiliza para crear páginas web. 

+++ ¿Qué Es Hyper Text Markup Language?

- _Hyper Text_ (Hipertexto): Quiere decir [texto con links](https://es.wikipedia.org/wiki/Hipertexto) a otros textos.
- _Markup Language_ (Lenguajes de Marcado): Es una forma de codificar un documento para darle estructura e información  acerca de cómo se presentará su contenido. 

+++

Es uno de los lenguajes más básicos y fáciles de aprender, y se utiliza junto con otros lenguajes como CSS y JavaScript para dar forma y estilo a las páginas web.


+++Aclaración importante
 
HTML es considerado un lenguaje de marcado pero no de programación, ya que no puede crear funcionalidades dinámicas. 


En su lugar, con HTML, los usuarios web pueden crear y estructurar secciones, párrafos y enlaces mediante elementos, etiquetas y atributos.

Más adelante, comprenderás mejor la diferencia. 
 
+++

## 2. Tags / Elemento `Block` y Elemento `Inline`

👩🏻‍💻👨‍💻 Para utilizar HTML, se escriben **etiquetas** (_tags_ ) en un archivo de texto que luego se abre en un navegador web. Las etiquetas se utilizan para definir diferentes elementos de la página web, como el texto, las imágenes y los enlaces. 

<div class="editor-recuadro">

En HTML, existen dos tipos de elementos: los elementos de bloque (_block elements_) y los elementos en línea (_inline elements_).

</div>

 
Los elementos de bloque ocupan todo el ancho disponible en su contenedor y generan un salto de línea antes y después de ellos. Algunos ejemplos comunes de elementos de bloque son los encabezados (`<h1>` a `<h6>`), los párrafos (`<p>`), las listas (`<ul>`, `<ol>`) y los divs (`<div>`).

+++ Ejemplo De _Tag_ Tipo _Block_

![ejemplo_block-min.png](https://i.imgur.com/1sFc7qU.png)

+++



Por otro lado, los elementos en línea no generan saltos de línea y ocupan solo el espacio necesario para mostrar su contenido. Algunos ejemplos de elementos en línea son los enlaces (`<a>`), las imágenes (`<img>`), los span (`<span>`) y los elementos de texto, como `<strong>` o `<em>`.

+++ Ejemplos De _Tags_ Tipo _Inline_ 

![ejemplo_inline-min.png](https://i.imgur.com/MxQkdyy.png)

+++

Cada uno de ellos los iremos trabajando a lo largo de la clase.





## 3. ¿Cómo escribir código en HTML?

🤓 Para escribir código en HTML, primero necesitás un editor de texto básico. En este curso utilizaremos el Visual Studio Code.

Seguí este video para configurar tu entorno de trabajo:

<iframe width="600" height="355" src="https://www.youtube.com/embed/AgmRBsVw--Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Una vez que tengas el editor de texto abierto, y configurado tu archivo `index.html`, podés empezar a escribir código en HTML.
 
📛 Probá todo esto en tu archivo y avanzá cuando hayas terminado.

---

### Estructura HTML Y Etiquetas `<h1>` y `<p>`

## 1. Estructura HTML

Empezá por este video:

<iframe width="600" height="355" src="https://www.youtube.com/embed/HMHbOUk4zKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Para crear una página web básica en HTML necesitarás al menos las siguientes etiquetas:

```html
<html>
  <head>
   <title>Título de la página</title>
  </head>
  <body>
   <h1>Esto es un título</h1>
   <p>Esto es un párrafo</p>
  </body>
</html>
```

Al leer el código, el _browser_ interpreta: 

- La declaración `DOCTYPE` le avisa al navegador que el documento que va a leer es HTML.
- El texto entre `<html>` y `</html>` define dónde empieza y dónde termina el documento.
- El texto entre `<head>` y `</head>` provee información (**meta data**) sobre el documento. Si bien no forma parte del contenido visible de la página, aporta información adicional que es muy útil para el navegador.
   <!--Un ejemplo no informático de meta data puede ser el género de un libro. Si un libro es de aventura, el lector podrá anticipar algunas situaciones asociadas a ese género, aunque no conozca el contenido particular de esa publicación. -->
- El texto entre `<title>` y `</title>` provee un título para el documento: lo que aparece escrito en la pestaña del navegador. Este contenido será mostrado por los motores de búsqueda en sus resultados.
  - Por ejemplo, _Google_ usa esta meta data para entender el contenido de una página y decidir cómo posicionarla.
- El texto entre `<body>` y `</body>` describe el contenido visible del documento; es decir, lo que el navegador le mostrará al usuario.
- El texto entre `<h1>` y `</h1>` describe un encabezado. El _tag_ `<h1>` ('_Heading_ 1') agranda la letra que contiene y la pone como título o encabezado.
- El texto entre `<p>` y `</p>` describe un párrafo. El _tag_ `<p>` genera un salto de línea al final, dándole forma de párrafo al texto que contiene.


+++ 📚 Glosario

- _Browser_: Se refiere a los navegadores _web_ (por ejemplo: Chrome, IE, Firefox, Safari). 

Según las reglas prescritas de HTML, un _browser_ lee el código de una página y entiende qué contenido tiene que mostrar al usuario y de qué forma.

+++









🛎️ **Recordá**: utilizá el atajo de `html:5` en el VSC para que te aparezca esta estructura automáticamente.


## 2. Etiquetas `<h1>` y `<p>`

Para agregar contenido a la página, como texto o imágenes, podés utilizar etiquetas adicionales de HTML. 

Para profundizar sobre este tema, mirá el siguiente video:
<iframe width="560" height="315" src="https://www.youtube.com/embed/qJfNv9RYrVI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Resumiendo: 
- La etiqueta `<h>` se utiliza para definir un encabezado. Pueden ser de nivel 1 a 6 (`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`,`<h6>`).
- La etiqueta `<p>` se utiliza para definir un párrafo de texto.



+++ _Autosave_
 
⚠️ **Importante:** recordá activar la función “Autosave” en el VSC para que tus cambios se guarden automáticamente. 

![autoguardado](https://i.imgur.com/SDV8kog.jpg)

También el VSC te permite retrodcer con los cambios.

+++



 Una vez que hayas escrito el código HTML y lo hayas guardado en un archivo con la extensión `.html`, podrás abrir el archivo en un navegador web para ver la página que has creado.
 
 
+++ Cómo Escribir Los Nombres De Los Archivos
 
Te recomendamos alguno de estos tres formatos:

🐍 **snake\_case**: Escribe las palabras en minúsculas, separadas con guiones bajos (_underscores_). 
   - Por ejemplo: palabras\_en\_minuscula\_separadas\_por_underscores 

🥙 **kebab-case**: Escribe las palabras en minúsculas y las separa con guiones medios.
   
  - Por ejemplo: 
  palabras-en-minuscula-separadas-por-guiones

🐪 **camelCase**: Escribe la primera palabra en minúscula y las siguientes con su inicial en mayúscula, pero sin usar espacios.

  Por ejemplo: 
  
  laPrimeraPalabraEnMinusculaYLasSiguientesConMayusculaSinUsarEspacios
 
+++

 
  📛 Probá todo esto en tu archivo y avanzá cuando hayas terminado.

---

### Listas, ***Buttons*** y Favicon




## 1. Listas

Una lista se utiliza para presentar información en forma de elementos ordenados o desordenados. 

Para crear una lista, se utiliza la etiqueta `<ul>` para una lista desordenada o `<ol>` para una lista ordenada, y se agregan los elementos de la lista utilizando la etiqueta `<li>`.


<iframe width="600" height="355" src="https://www.youtube.com/embed/XNMsJ5bzqFs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Por ejemplo, una lista desordenada de frutas se puede crear de la siguiente manera:

```html
<ul>
  <li>Manzana</li>
  <li>Naranja</li>
  <li>Pera</li>
</ul>
```
En cambio, una lista ordenada se escribe así:

```html
<ol>
  <li>Primer elemento</li>
  <li>Segundo elemento</li>
  <li>Tercer elemento</li>
</ol>
```

## 2. Buttons

La etiqueta `<button>` en HTML es una herramienta para crear botones en una página web. Suele utilizarse para diferentes casos: enviar formularios, activar eventos o simplemente crear un enlace visualmente atractivo.

Por ejemplo, para este botón:


<button type="button">Haz click aquí</button>

La sintaxis correcta sería:

```html
<button type="button">Haz click aquí</button>
```

Al hacer click en él, por el momento, no ocurre nada, esto lo aprenderemos más adelante, junto a darle estilos.


+++ Botones modernos
 
Podés revisar estos [botones prediseñados](https://uiverse.io/buttons) para optimizar tus HTML. Luego, cuando veamos CSS entenderás las diferentes propiedades que se incluyen.
 
+++

## 3. Favicon

Un favicon es el ícono que se muestra en la pestaña del navegador web cuando se carga una página. 

<iframe width="600" height="355" src="https://www.youtube.com/embed/1mugUzxhWoM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Para agregar un favicon a un sitio web, se debe crear una imagen con un tamaño de 16x16 píxeles o 32x32 píxeles, guardarla en formato **.png** preferentemente, y agregarla al código HTML utilizando la etiqueta `<link>` en la sección `<head>` del documento.

Por ejemplo, para agregar un favicon llamado "favicon.png" se utilizaría el siguiente código:

```html
<head>
  <link rel="icon" type="image/x-icon" href="favicon.png">
</head>
```
+++ Cómo Convertir Una Imagen En Favicon

Muchos sitios convierten imágenes con distintos tamaños y extensiones a imágenes pequeñas para tu página. 

Tres de estos son:

* [Ionos](https://www.ionos.com/tools/favicon-generator#tool) (.png)
* [Favicon Generator](https://www.favicongenerator.com/) (.ico)
* [Gen Favicon](http://www.genfavicon.com/) (.jpg)

+++

📛 Antes de avanzar, asegurate de haber comprendido todo y haberlo probado en tu archivo.


---

### Etiquetas `<img>` Y `<a>` 

Como vimos, las etiquetas en HTML son elementos que se utilizan para definir diferentes partes de una página web. 

Las etiquetas se escriben entre corchetes angulares `<>`, y suelen tener una versión de apertura y una de cierre, como `<p>` y `</p>`. 

Además de las ya vistas (`<head>`, `<body>`,`<h1>`,`<h2>`, `<p>`, etc.), te resultarán muy útiles aprender las siguientes:

- `<img>`: inserta una imagen en la página.
- `<a>`: define un enlace que te lleva a otra página web.
- `<button>`: crea botones interactivos en tu página web.

Los _tags_ (tag quiere decir etiqueta en inglés, usaremos los términos de forma intercambiable) pueden tener atributos que proveen información adicional sobre un elemento. Están **siempre** en el _opening tag_ y se componen por dos partes: un **nombre** y un **valor**, separados por un signo igual (=). Un elemento puede tener muchos atributos que hagan diferentes cosas. Veamoslo más en profundidad con el caso del tag `<img>`.


## 1. Etiqueta `<img>`

<iframe width="600" height="355" src="https://www.youtube.com/embed/vAxvDuxR6oU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


#### 1a. Anatomía

![tag-image.gif](https://i.imgur.com/TYMuxdI.gif)

- Un atributo `src`: indica al _browser_ cual es la fuente de la imagen (source = fuente en inglés), osea el lugar donde se aloja la imagen. Puede ser un link a un sitio web externo o una ruta a un archivo en nuestro propio directorio local.
- La propiedad `alt`: Indica al navegador el nombre que debe mostrar en caso de que la imagen no se cargue o que el usuario sea una persona con discapacidad visual.

<div class="editor-recuadro">

⚠️  **Importante**: El _tag_ `<img>` **no tiene _closing tag_**, ya que solo le indica al _browser_ que ahí debe ir una imagen. Es decir, la misma imagen es el contenido del _tag_. 
</div>




🛎️ **Recordá**: podés agregar el link de la imagen o descargarla para incluirla en tu HTML. 

## 2. Etiqueta `<a>`

<iframe width="600" height="355" src="https://www.youtube.com/embed/jR7PZ97-ncE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

#### 2a. Anatomía

![anchor-tag-anatomia.gif](https://i.imgur.com/oUgjMR2.png)



- Tiene un _tag_ de apertura `<a>` y uno de cierre `</a>`.
- El _opening_ y _closing tag_ contienen al texto (en este caso "Texto que contiene el hipervínculo"), transformándolo en un _link_ visible para el usuario. Este contenido puede ser tanto un texto como otros elementos de HTML: por ejemplo, una imagen.
- El atributo `href` indica dónde llevará el _link_ cuando el usuario haga _click_. En este caso, el valor es "URL", una página externa.

#### 2b. Hipervínculos A Archivos Locales O A Páginas Externas
 
1. En el caso de que el archivo esté alojado en la computadora (**local**), 
deberás escribir su nombre y extensión. 

    - Si el archivo está en **la misma carpeta** que la página que tiene el _link_, solo deberás escribir su nombre. Por ejemplo: `hope.html`. 

2. Si está en **otro directorio**, deberás indicar la ruta completa, desde la página en la que estás hasta la página de destino. Por ejemplo: `secundarias/hope.html`.

En caso de vincular a una **página externa**, el valor del atributo tiene que incluir `"http://"`. 
Por ejemplo, para dirigir el enlace a <a href="http://www.google.com"> Google</a>, el valor de `href` será:

```html
<a href="http://www.google.com"> Texto que dirige el usuario a Google </a>
``` 
 



 📛 Probá todo esto en tu archivo y avanzá cuando hayas terminado.

 ---

 ### Contenedores: `<div>` Y `<span>`



📚Un `<div>` es un elemento HTML que se utiliza para crear una sección o contenedor en una página web. 

Específicamente, se pueden incluir para una amplia variedad de propósitos, como agrupar elementos relacionados, crear diseños de página, dividir secciones de contenido, etc.

Es importante saber que un `<div>` **es un elemento de bloque**, lo que significa que ocupa todo el ancho disponible en su contenedor y se muestra en una nueva línea después de cualquier elemento anterior.



<iframe width="600" height="355" src="https://www.youtube.com/embed/7Uu1lvni38k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


```html
<!-- Un div con listas de ejemplo -->

<div>
  <h2>Mis tareas</h2>
  <ul>
    <li>Tarea 1</li>
    <li>Tarea 2</li>
    <li>Tarea 3</li>
  </ul>
  
  <h2>Mis metas</h2>
  <ol>
    <li>Meta 1</li>
    <li>Meta 2</li>
    <li>Meta 3</li>
  </ol>
</div>
```

📚 Los `<span>`, en cambio, son _tags_ de tipo _inline_. Es decir, afectan únicamente el espacio que ocupa su contenido. Generalmente se usan para seleccionar partes específicas de un documento, como una frase de un párrafo, una palabra o una imagen.

A modo de ejemplo:

![imagen](https://i.imgur.com/HXAduzd.jpg[/img])


<div class="editor-recuadro">

⚠️ **Importante:** Con CSS se pueden aplicar estilos y formatos específicos a los _divs_ y a los _spans_, lo que permite crear diseños atractivos y personalizados. Esto lo veremos en la próxima clase

</div>


---

### Otras Etiquetas

Estas etiquetas, que se utilizan con frecuencia, se relacionan directamente con el texto del contenido. Probalas en tu editor de texto:

## 1. `<br>`

Esta etiqueta sirve para hacer un salto de línea en el texto. No necesita etiqueta de cierre.

```html
<p> hola </p>
<br>
<p> hola, de nuevo </p>
```


## 2. `<em>`

Esta etiqueta sirve para poner tu texto en _itálica_.
```html
<p> hola </p>
<br>
<p><em> hola, de nuevo </em></p>
```

## 3. `<strong>`

Esta etiqueta sirve para poner tu texto en **negrita**.

```html
<p> hola </p>
<br>
<p><strong> hola, de nuevo </strong></p>
```


## 4. `<hr>`

Esta etiqueta sirve para trazar una línea separadora en tu texto. No necesita etiqueta de cierre. 

```html
<p> hola </p>
<hr>
<p><strong> hola, de nuevo </strong></p>
```


## 5. `<u>`
Esta etiqueta sirve para subrayar tu texto.

```html
<p> Texto normal y <u>Texto subrayado</u></p>
```


## 6. Código comentado/oculto
 
Para comentar tu código, y que no interrumpa la lectura del editor, debés usar los siguientes comandos:

- En HTML: 

```html
<!--Este es un comentario en HTML-->
```
- En JavaScript: 

```js
// Este es un comentario en JavaScript
```

⚠️ **Importante**: nunca incluyas información sensible en tu código comentado ya que se puede acceder desde el navegador con la inspección del código fuente.

## 7. Más etiquetas

Si querés conocer más etiquetas de HTML podés acceder a esta  [tabla periódica](https://lenguajehtml.com/html/introduccion/tabla-periodica-html5/) sumamente útil y didáctica.


---

## Proyecto

### Práctica 1

## La elección

Vas a comenzar con el proyecto transversal del curso. Para eso, deberás configurar tu espacio de trabajo y elegir a tu artista o a tu banda musical.

<div class="editor-recuadro">

⚠️ **Importante**: trabajarás con este artista o banda durante todo el Curso. No tomes a la ligera tu elección.
</div>


Luego, seguí con este paso a paso:

- Creá una carpeta en tu escritorio con el nombre de **Plataforma Disco** con _Camel Case_:
  - Ejemplo: plataformaDisco

- Abri esta carpeta vacía en el VSC. 
- Agregá en esta carpeta un archivo `index.html`.
- Dentro de este archivo desplegá la estructura base del `<!DOCTYPE>`.
- No te olvides de tener activado el _autosave_. 
- Agregá el nombre del artista o banda en el `<title>` y en un `<h1>`.
- Abrí el archivo en el _browser_ y fijate que todo esté funcionado correctamente.
- Luego, avanzá a la siguiente sección.

---

### Práctica 2

## La Wiki

La página que deberás realizar es una de las bases de tu proyecto **Plataforma Disco**. Comenzarás por construir la vista de un album en particular.

Primero, observá detenidamente y pensá qué elementos deberías incluir en tu código.


![Imgur](https://imgur.com/fBgSHA5.png)


👉 Luego, aplicalos de forma ordenada con la información de tu artista. 
  - En esta parte no te guiaremos mucho porque queremos que empieces a ganar autonomía. Podés revisar el contenido si tenés dudas o preguntar por Discord si te trabaste con algo. 

<div class="editor-recuadro">

⚠️ **Importante**: no te olvides de incluir el Favicon, ni de probar todos los elementos que viste en esta clase. 

</div>

---

### Práctica 3

## Netlify

Subí tu wiki a Netlify. 

### Guía Para Crear Tu Cuenta En ***Netlify***

Para crear tu cuenta en _Netlify_, seguí este paso a paso.

1. Accedé a este [link](https://app.netlify.com/drop ) y hacé _click_ en `Sign up`.

![acceder-netlify.png](https://i.imgur.com/eMlfXV8.png)

2. Hacé _click_ en `email`.

![welcome-netlify.png](https://i.imgur.com/MbUuTy8.png)

3. Cargá tu e-mail y contraseña (debe contener más de 10 caracteres).

![email-netlify.png](https://i.imgur.com/Kh8hiSO.png)

4. Revisá tu bandeja de entrada y activá tu cuenta. 

![activar-netlify.png](https://i.imgur.com/TfoMloe.png)

5. Hacé _click_ en `Verify email` para verificar tu cuenta.

![verify-netlify.png](https://i.imgur.com/NlVDFKI.png)

6. Colocá tu nombre y, en `type`, elegí `Personal blog or portfolio`.

![portfolio-netlify.png](https://i.imgur.com/tltbc6q.png)

7. Hacé _click_ en `Get Started`.

<p style="border:3px; border-style:solid; border-color:grey; padding: 1em;">👩🏻‍💻👨‍💻 ¡Felicidades! Ya podés subir tu página <em>web</em> y tus futuros proyectos.<br></p>
Ya sabés como hacerlo. Esta vez, **no** hace falta compartir el link por Discord.


![alt](https://media.giphy.com/media/m5B4JzuoIrrcbibbnc/giphy.gif)

📛 Corroborá que todo funcione correctamente y avanzá a la última parte de la clase.

---