### Presentación y Objetivos

## 1. Introducción

En esta clase aprenderemos mucho sobre los formularios, piezas clave en la construcción de una página web. 

Adicionalmente, profundizaremos sobre el tag `a`, visto en la primer clase y conoceremos los `iframes`, que nos permitirán mostrar el contenido de páginas externas. 


## 2. Objetivos

Al finalizar esta clase podrás:

- Crear formularios para recibir _inputs_ de los usuarios.
- Enviar esa información por correo electrónico.
- Aplicar `iframes` para mostrar contenido de otras páginas.
- Dirigir al usuario a secciones dentro de una misma página _web_.


+++ 🎶 Inspiración musical

<iframe width="600" height="355" src="https://www.youtube.com/embed/JGwWNGJdvx8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

+++ 

---

### Formularios

## 0. Presentación

Los formularios HTML se usan para recoger información que nos da el usuario. Seguramente, a lo largo de tu vida, completaste algun formulario web (por ejemplo, los de registro/login). 

+++ Ejemplos De Formularios
![formularios_google-min.png](https://i.imgur.com/xMxVMbQ.png)

---

![formularios_facebook2-min.png](https://i.imgur.com/NZm6nX6.png)

---

![formularios_facebook1-min.png](https://i.imgur.com/JNWmVuF.png)

+++


#### 1. Características De Los Formularios

Los formularios que existen en la _web_ son modulares, es decir, se construyen a partir de distintos tipos de módulos o _inputs_.

<div class="editor-recuadro">

📚 Un _input_ es un campo de datos que permite que el usuario ingrese o elija un valor. Es decir, es una de las maneras que tenemos de recolectar su información. 

</div>

Hay muchos tipos de _input_, desde espacios vacíos para que el usuario complete con letras o números, listas desplegables, campos para escribir una contraseña, etc. Lo veremos en la sección siguiente.



## 2. Estructura De Los Formularios

#### a. Etiqueta `<form>`

La etiqueta `<form>` define el comienzo y el fin de un formulario HTML. Este _tag_ se abre y se cierra normalmente.

Tiene dos atributos principales: `action` y `method`. 
  - `action`: Define a dónde debe mandar la información del formulario. Puede ser una URL o carpeta dentro de un servidor. 
  - `method`: Define qué método HTTP usará. Puede ser `get` si pide información o `post` si la envía.

####  b. Etiqueta `<input>`

Dentro de `<form>` se escriben los _tags_ `<input>` que crean los campos donde el usuario ingresa la información. Tienen el atributo `type` que define el tipo de información que recibe. Por ejemplo:
  - `type="text"`: Define un campo donde el usuario puede escribir cualquier texto. 
  - `type="password"`: Oculta la información al momento de escribirla. Generalmente, reemplaza los caracteres ingresados por asteriscos o puntos. 
  - `type="email"`: Define un campo donde el usuario debe escribir una dirección de correo electrónico. 
  - `type="submit"`: Genera un `botón` que envía la información del formulario. 

<div class="editor-recuadro">

⚠️ **Importante:** Los _tags_ `<input>` son autocontenidos, es decir, no se cierran. 
</div>


Veamos cómo se ve en el código:


```html
<form method="POST" action="login">
  <input type="text">
  <input type="password">
  <input type="email">
  <input type="submit">
</form>
```

|||
<form>
  <input type="text">
  <input type="password">
  <input type="email">
  <input type="submit">
</form>

|||



Cuando apretamos `submit`, el formulario envía la información ingresada en forma de **_key-value pairs_**. Es decir, genera una variable para guardar el contenido de cada `<input>`. Por lo tanto, cada `<input>` deberá tener un atributo `name` que indique a qué campo corresponde la información ingresada.


Por ejemplo, si queremos enviar la edad de una persona, el servidor recibirá un campo `edad` y el valor numérico que ingresó el usuario. 
El siguiente código enviará un campo con el `nombre` del usuario, otro con su `edad` y otro con su `contraseña`:


```html
<form>
  <input type="text" name="nombre">
  <input type="number" name="edad">
  <input type="password" name="contraseña">
  <input type="submit">
</form>
```

Para ver cómo funciona, pegá el código de arriba en un nuevo documento HTML, completalo y apretá `submit`.

Si te fijás en la URL verás que ahora contiene un signo de pregunta (`?`) seguido por la información de cada campo, separado por un signo _et_ (`&`). A esta parte de la URL se la llama _Query String_.

![formulario_query_string-min.png](https://i.imgur.com/n51MTne.png)

⚠️ **Importante**: Los _tags_ `<input>` pueden ponerse por separado en el HTML, fuera del _tag_ `<form>`. Pero, si queremos que la información que ingresa el usuario **esté relacionada y se envíe toda junta**, tiene que estar contenida dentro de un _tag_ `<form>`.

##### 3. Placeholders Y Labels

El atributo `placeholder` y el _tag_ `<label>` sirven para indicar al usuario qué debe poner en cada campo. Mirá el siguiente video y aprendé más acerca de ellos:


<iframe width="600" height="355" src="https://www.youtube.com/embed/MvAFpoeaEok" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!----
@vimeo=186373129
!---->

#### 4. El Atributo `placeholder`

El atributo `placeholder` se agrega dentro del _tag_ `<input>` y sirve como referencia visual para el usuario. 


Es decir, es el texto que se muestra en el `<input>` y que indicará al usuario qué debe escribir ahí. 

Así se ve en el código:

```html
<input type="text" name="nombre" placeholder="Nombre y Apellido">
```

Esto es lo que ve el usuario:

![imagen](https://i.imgur.com/tnDALqz.jpg)

Antes de continuar, volvé al formulario anterior y agregale a cada `<input>` un atributo `placeholder` con su respectivo valor.

<!----
<div style="border:3px; border-style:solid; border-color:grey; padding: 1em;"> 

👩‍🏫👨‍🏫 El _placeholder_ no genera un valor dentro del campo; es decir, la información nunca se envía porque es solo una referencia visual para el usuario. Para comprobarlo, hacé _click_ en `submit` en el formulario vacío y mirá la _Query String_.

</div>
<!---->

#### 5. El Tag `<label>`

El _tag_ `<label>`, en cambio, es la etiqueta que lleva el nombre del `<input>`. 

![imagen](https://i.imgur.com/G7kUEB6.jpg)

Hay dos formas de usarlo:

1. Escribiendo el nombre del campo y el _tag_ `<input>` dentro de `<label>`:

```html
<label>Nombre: <input type="text" name="username" placeholder="nombre y apellido"> </label>
```

2. Escribiendo dentro del _tag_ `<label>` un atributo `for` que, a su vez, tome el valor del `id` que le daremos al `input`. 


```html
<label for="nombre_usuario">Nombre:</label> <input type="text" id="nombre_usuario" name="username" placeholder="nombre y apellido">
```


+++ ¿Por Qué Usar El _Tag_ `<label>` En Vez Del `<p>`?

Si bien podrías usar un _tag_ `<p>` para escribir el nombre de ese campo, es una buena práctica usar `<label>` ya que:
- Vincula los elementos en el código.
- Es de ayuda a los usuarios no-videntes porque el _software_ que les lee las páginas busca los _tags_ `<label>` para decirles qué tienen que poner en el campo de un formulario. 
- Se alinea con la tendencia en HTML de ir hacia la web semántica. Es decir, que el código HTML esté escrito con significado para que ayude a las máquinas a entender mejor _internet_ y a resolver muchos de nuestros problemas de forma más eficiente. 
- _Google_ beneficia a los sitios escritos semánticamente ya que sus buscadores pueden catalogarlos y posicionarlos mejor.
- 
+++

#### 6. Demostración 

Vamos a ver una breve demostración de todo lo aprendido. Mirá este video para aprender cómo usar los formularios: 

<iframe width="600" height="355" src="https://www.youtube.com/embed/35OjWLoOYAY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---

### Tipos de inputs 

 Los elementos `<input>` pueden tener diferentes tipos. Algunos de los más comunes son:

- `text`: Campo de texto de una sola línea.
- `password`: Campo de texto para contraseñas (los caracteres se ocultan).
- `email`: Campo de texto para direcciones de correo electrónico.
- `number`: Campo de texto para números.
- `checkbox`: Casilla de verificación.
- `radio`: Botón de opción.
- `submit`: Botón de envío del formulario.
- `file`: Campo de carga de archivos.

Veamos algunos de ellos en mayor profundidad. 

#### 1. ***Input Password***

El `<input type="password">` oculta la información que ingresa el usuario usando asteriscos o puntos.

Si bien cuando escribimos en el campo con `type="password"` el texto aparece oculto, al apretar `submit`, la información se envía sin encriptar. Esto, por ahora, nos sirve para generar una mejor experiencia del usuario. 

Sin embargo, no es la forma más segura ya que alguien con conocimientos en programación podría verla.

<div class="editor-recuadro">

⚠️ **Importante:** Para mantener segura la información y enviarla encriptada, se usan sistemas complejos que veremos más adelante en este curso. 
</div>



Antes de avanzar, hacé esta prueba: 

1. Entrá a la página de algún banco. Por ejemplo, hacé _click_ [acá](https://onlinebanking.bancogalicia.com.ar/login?_ga=2.23523898.1412064939.1598274949-2054595263.1598274949).
2. Escribí algo en el campo contraseña.
3. Hacé _click_ derecho y entrá al Inspector de _Chrome_. 
4. Seleccioná el campo de la contraseña.

![input_password_banco-min.png](https://i.imgur.com/wtQizah.png)



5. Modificá el `type` de ese `input` y cambialo a `text` para ver cómo se hace visible la contraseña.


<div class="editor-recuadro">

👮‍♀️**Conclusión**: Nunca dejes contraseñas escritas porque alguien con conocimientos como los tuyos las podría ver.
</div>



#### 2. ***Dropdowns***

Un `dropdown` es una lista desplegable. Es decir, es un tipo de `input` que te muestra las opciones disponibles dentro de un menú. Mirá este video y conocé más acerca de ellos:

<iframe width="600" height="355" src="https://www.youtube.com/embed/E7FQb1gW_bg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!----
@vimeo=186373083
<!---->

#### Sintaxis De Los ***Dropdowns***

Para agregar un `dropdown` en tu formulario, seguí estos pasos:

1. Escribí un _tag_ `<select>` con su _opening_ y _closing tag_. Ellos contendrán las opciones disponibles.
2. Escribí un atributo `name` que indique en tu *Query String* a qué campo corresponde la opción elegida. 
3. Ingresá los valores disponibles usando un _tag_ `<option>` para cada una de ellos. 
4. Agregale un atributo `value` que indique cómo querés que aparezca en la *Query String* la opción elegida por el usuario.

⚠️ **Importante:** Puede tener el mismo valor que la `option`, una abreviación o cualquier otra nomenclatura. En caso de que no agregues este atributo, aparecerá en la *Query String* el valor dado en la `option`.  

Mirá cómo queda este código, siguiendo el ejemplo anterior:

```html
  <label for="sede">Elegí La Sede Donde Querés Estudiar:</label>
      <select name="sede" id="sede">
          <option value="atr">Online A Tu Ritmo</option>
          <option value="pal">Palermo</option>
          <option value="itu">Ituzaingó</option>
          <option value="chi">Santiago De Chile</option>
      </select>
```   

Así se verá la opción seleccionada en la _Query String_.

![imagen](https://i.imgur.com/3n19piO.jpg)

🤓 **Tip:** Si tenemos cuatro opciones o menos, es mejor usar `radio button`. Si ya son más de cinco, recomendamos usar _dropdown_.


##### c ***Radio Buttons***

Los `radio buttons` son botones que nos permiten seleccionar una opción entre dos o más dadas. La idea de este tipo de `input` es que no se puedan seleccionar ambos en simultáneo. 

<iframe width="600" height="355" src="https://www.youtube.com/embed/mdSy2csGRxE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!----
@vimeo=186373135
!---->


Para crearlos deberás escribir:
- Un _tag_ `<label>` que indique el nombre que aparecerá antes del `radio button`.
- Un _tag_ `<input>` que tenga estos 3 atributos:
  - `name`: Indicará a qué variable refiere el valor del `input` al momento de enviar la información. Es decir, en la *Query String*, el campo `"name"` tendrá el valor de la opción que haya elegido el usuario. 
  - `type`: Indicará qué tipo de botón es, en este caso, `radio`.
  - `value`: Indicará cómo querés que aparezca en la *Query String* la opción elegida por el usuario (puede tener el mismo valor que la `label`, una abreviación o cualquier otra nomenclatura). 

+++ ¿Cómo Hacer Para Que Los `radio button` Sean Excluyentes Entre Sí?

Si el nombre dado al atributo `name` es el mismo, los `radio buttons` serán excluyentes entre sí. Es decir, los usuarios solo podrán elegir una de las opciones dadas.

En el ejemplo que sigue, le daremos a todos los `input` el `name="Turno"` para que elijan a qué curso asistir.

+++

Veamos un ejemplo de un `radio button` para elegir el turno del Curso Introductorio de Programación.

El código se verá así:

```html
<label> Mañana:
  <input name="Turno" type="radio" value="tm"> 
</label>

<label> Tarde:
  <input name="Turno" type="radio" value="tt"> 
</label>

<label> Sábado:
  <input name="Turno" type="radio" value="ts"> 
</label>

<label> A Tu Ritmo:
  <input name="Turno" type="radio" value="atr"> 
</label>
```

⚠️ **Importante:** Debés escribir un `input` por cada opción.

|||
<label> Mañana:
  <input name="Turno" type="radio" value="tm"> 
</label>

<label> Tarde:
  <input name="Turno" type="radio" value="tt"> 
</label>

<label> Sábado:
  <input name="Turno" type="radio" value="ts"> 
</label>

<label> A Tu Ritmo:
  <input name="Turno" type="radio" value="atr"> 
</label>

|||

Así se verá la opción seleccionada en la _Query String_.

![imagen](https://i.imgur.com/BzpIphx.jpg)

##### d. ***Checkbox***

Los `checkbox` permiten seleccionar y deseleccionar la opción en un formulario. Por ejemplo, el `checkbox` de "Acepto Bases y Condiciones".



<div class="editor-recuadro">

⚠️ **Importante:** No es un _tag_ `<input>` con un `type="textarea"`, sino una etiqueta diferente, que se abre y se cierra. 

</div>



El `checkbox` tiene un _tag_ `<label>` que indica el nombre que aparecerá antes. Además, tiene un _tag_ `<input>` con 3 atributos:
1. `name`: Indicará a qué `variable` refiere el valor del `input` al momento de enviar la información. Es decir, en la *Query String*, el campo `"name"` tendrá el valor de la opción que haya elegido el usuario. 
2. `type`: Indicará qué tipo de botón es, en este caso, `checkbox`.
3. `value`: Indicará cómo aparecerá en la *Query String* la opción elegida por el usuario.

<div class="editor-recuadro">
  
  ⚠️ **Importante:** Puede tener el mismo valor que la `label`, una abreviación o cualquier otra nomenclatura. 
  
</div>



Siguiendo el ejemplo anterior, quedaría así:

Código del `checkbox`:

```html
<label for="checkbox">Acepto recibir información sobre el curso: </label>
        <input id="checkbox" name="mailing" type="checkbox" value="consent"> 
```

|||

<label for="checkbox">Acepto recibir información sobre el curso: </label>
        <input id="checkbox" name="mailing" type="checkbox" value="consent"> 

|||

#### e. Etiqueta `<textarea>`

Un _tag_ `<textarea>` es un campo para ingresar texto. Es similar a un `<input>` `type="text"` solo que el espacio dado al usuario es mayor. 

La etiqueta `<textarea>` tiene un _opening_ y _closing tag_ y los siguientes atributos:
  - `rows` (filas): Es un valor numérico que indica el alto de la caja de texto. Por ejemplo, "20".
  - `cols` (columnas): Es un valor numérico que indica el ancho de la caja de texto. Por ejemplo, "40".

⚠️ **Importante:** Si querés, podés agregarle un atributo `placeholder` para que sea más claro para el usuario.


Mirá cómo queda este código, siguiendo el ejemplo anterior:

```html
<label for="consultas">¿Tenés alguna otra duda?</label>
    <br>
    <textarea id="consultas" rows="20" cols="40" placeholder="Dejanos tu consulta"></textarea>
```

|||

<label for="consultas">¿Tenés alguna otra duda?</label>
    <br>
    <textarea id="consultas" rows="20" cols="40" placeholder="Dejanos tu consulta"></textarea> </textarea>

|||

---

### Cómo Enviar La Información Por ***Mail***

Para enviar por _mail_ la información cargada por el usuario, podemos usar varios prestadores. Hoy, aprenderás a usar [_Formspree_](https://formspree.io/), un servicio que nos permite procesar el envío de formularios de forma gratuita. 

Mirá este video para aprender a usarlo:

<iframe width="600" height="355" src="https://www.youtube.com/embed/Sta2bZdemsg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---

### Más Acerca Del ***Tag*** `<a>`

En nuestra primer clase vimos la anatomía del _tag_ `<a>` (_Anchor_). Esta etiqueta es muy versátil. 
<!----
Mirá este video y aprendé todo lo que podés hacer con él:

<iframe width="600" height="355" src="https://www.youtube.com/embed/ybsvjGS4Zqk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!----
<iframe src="https://player.vimeo.com/video/186373066" width="640" height="564" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
!---->

El _tag_ `<a>` puede usarse para:

- Generar _links_ a páginas externas.
- Direccionar al usuario a las secciones dentro de una página.
- Hacer que se abra un _mail_ cuando se _clickea_ el link.
- Hacer que la página objetivo se abra en una pestaña nueva.

## 1. Cómo Direccionar A Secciones Dentro De Una Página.

1. Dale un ID a la sección a la que quieras direccionar al usuario.
2. Creá un _link_ en otra parte de la misma página poniendo el nombre del ID con un `#` dentro del atributo `href`. Por ejemplo: 

```html
<a href="#seccion1"> Link a la sección1 <a>
```

  - Ese _link_ te llevará a la `sección1` dentro de la misma página.
  - Si querés redireccionar a esta sección desde otra página, deberás agregar el ID al final de la dirección. Por ejemplo: 
  
```html
<a href="http://www.ejemplo.com/#seccion1"> Link a la sección1 desde una página externa<a>
```


## 2. Cómo Abrir Un Mail En Blanco

Es muy común que, al hacer _click_ sobre "Contacto", se abra un _mail_ en blanco en nuestra casilla de correo. Para configurarlo, poné como valor del atributo `href`: 

 `href="mailto:ejemplo@tumail.com"`

## 3. Cómo Hacer Que La Página Objetivo Se Abra En Una Pestaña Nueva

🔍 Seguí ejercitando esta habilidad **clave** de los programadores y [googleá](https://google.com) cómo hacer que la página objetivo se abra en una pestaña nueva.

---

### Proyecto

## 1. Registro

En esta primera sección vas a construir el esqueleto de la vista de registro para tu página. No hace falta que te enfoques en los estilos aún, ya lo veremos más adelante.

1. Creá un archivo `signUp.html`.

2. Agregá un tag `h3` con el título "Registro". 

3. Agregá un `form` que: 
    * Tenga un mínimo de 4 campos: nombre, apellido, mail y contraseña. Todos ellos deberán ser requeridos.
    * Tenga un botón que el usuario presione cuando esté listo para registrar sus datos. 
    * No pueda leerse en texto plano la contraseña.

<div class="editor-recuadro">
 En todos los casos coloca el placeholder , label y type correspondientes.
</div>

---

### Proyecto

## 2. Login

 Ahora, construiremos el esqueleto de la vista de login para tu página. Seguí las siguientes instrucciones:  

1. Creá un archivo `login.html`.

2. Agregá un tag `h3 `con el título "log in". 

3. Agregá un `form` que: 
   * Tenga un mínimo de 2 campos: mail y contraseña.
    * Incluya un botón que el usuario presione cuando esté   listo para loguearse. 
    * El campo contraseña no debe poder leerse en texto plano.

4. Incluí un `div` luego del `form`. El mismo deberá tener: 

    * Un tag `p` con el contenido: "¿Aún no sos miembro?""
    * Un tag `a` que redirija al ususario al formulario de registro, cuyo contendio deberá leer Registrate.
    
Te dejamos el ejemplo de Linkedin como inspiración: 

![log-in](https://imgur.com/yX0iXfA.png)

---

### Proyecto

## 3. Agregar albums

Por último, vas a construir el esqueleto de la vista que necesitaremos para agregar un nuevo album.

1. Creá un archivo `addAlbum.html`.

2. Agregá un `div` para el título con el nombre de "Nuevo Album".

3. Agregá un `form` donde el usuario deba completar:
    * Título.
   * Año de lanzamiento del album.
    * Descripción.
    * Y un campo para agregar una imagen. 
    El mismo deberá tener un `placeholder` que indique que el usuario debe completar este campo con una url. 


<div class="editor-recuadro">

🤓 Pensá bien qué tipo de input deberías usar en cada caso.
</div>


---

### Ejercicio

#### Envío De Formulario

En este ejercicio, deberás lograr que la información de tu formulario InstaPet te llegue por _mail_. 

Para eso, seguí este paso a paso:

1. Entrá a [formspree.io](https://formspree.io/) y registrate gratuitamente.
2. Verificá tu dirección de correo electrónico. 
3. Luego, creá un nuevo formulario en Formspree y copiá la URL que te proporciona.
3. En el atributo action del formulario HTML, pegá la URL que copiaste en el paso anterior.
4. Asegurate de que los nombres de los campos del formulario HTML coincidan con los nombres de los campos que quieras recopilar en Formspree. 
5. Prueba el formulario completando los campos y enviando la información. Verifica que recibas la información en tu dirección de correo electrónico.
6. Subí la carpeta con el ejercicio de InstaPet completo a [_Netlify Drop_](https://app.netlify.com/drop).
7. Entrá a la URL que te dio _Netlify_ y asegurate de que todo funcione.


👮‍♀️ Si tenés un problema con el `<textarea>`, inspeccioná tu código y descubrí qué te falta.


---

### Conclusión

## Form Of You


![fin de clase](https://media.giphy.com/media/3orif3HlX3i4fDdqCY/giphy.gif)

En esta clase te sumergiste en el mundo de los formularios HTML, aprendiendo a crear campos de entrada, botones, inputs y validar la información ingresada por los usuarios. También conociste los iframes y la funcionalidad que le aportan a tus páginas.

Como siempre, aprovechaste los ejercicios y los desafíos en el proyecto, aplicando lo aprendido de manera creativa. 

<div class="editor-recuadro">

La programación es un proceso de aprendizaje constante, y cada desafío te brinda la oportunidad de crecer y mejorar. No olvides practicar lo aprendido, experimentar y resolver problemas por tu cuenta. ¡Eso es lo que te hará destacar como _developer_!

</div>



+++ 🚨 Reportá un error
 

 🛎️ **Recordá**: Si algún aspecto de PLEDU no funciona como esperabas o algún contenido merece revisión podés avisar por [acá](https://forms.gle/okCETdVFsbg9S9kX7).
 

 
+++

## ¡Nos vemos en la próxima clase! 


