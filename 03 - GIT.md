### Git Y GitHub

<!-- El objetivo de este modulo es lograr instalar y ejecutar Git para el segumiento de versiones y vincularlo a un repositorio remoto -->

**Git**  es un sistema de control de versiones distribuido de código abierto que se utiliza para gestionar cambios en el código fuente. Git permite a los desarrolladores realizar un seguimiento de las versiones antiguas del código, trabajar en paralelo en diferentes ramas y fusionar los cambios en una única línea principal.


**GitHub**, por su parte, proporciona una interfaz web fácil de usar que se integra con Git, lo que hace que sea más fácil para los desarrolladores colaborar en proyectos y compartir el código con otros.

Además, nos proporciona una variedad de herramientas para la gestión de versiones, la colaboración, el seguimiento de errores, la automatización y la integración continua.


<iframe width="600" height="355" src="https://www.youtube.com/embed/IJmk4kR64LE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## Comandos de git 
Git ofrece una variedad de comandos que se utilizan para interactuar con el sistema de control de versiones y gestionar los repositorios. Veamos algunos que deberemos utilizar en el curso: 

```js
git add index.js // se utiliza para indicar qué archivos debemos incluir en el próximo commit 
```
+++ **Y si quiero agregar todos los archivos modificados...**
 
También podemos utilizar el comodín `.` para agregar todos los archivos modificados en el directorio actual:

```js
git add .
```

 
+++

Una vez que agregamos los archivos debemos commitear los cambios : 
```
git commit -m 'mensaje del commit' //
```


 📸 Un commit es como una foto  de los cambios realizados en el proyecto en un momento determinado. Al crear un commit, se deben proporcionar un mensaje que explique brevemente los cambios realizados

Y luego vamos a enviar los cambios realizados en el repositorio local a un repositorio remoto, como GitHub. Lo que, de tratarse de un equipo de devs, permitiría que otros miembros del equipo vean los cambios y trabajen en ellos.

Para esto debemos "pushear" nuestros cambios con el comando : 
```
git push 
```

<div class="editor-recuadro">

✅ **Buenas prácticas para escribir commits**

* Usa un verbo que describa la acción : agregar, cambiar, remover
 
* Sé corto y conciso, tu commit debe cumplir la función de explicar qué cambios haz realizado. Pero no hace falta que sea largo, lo ideal es que si necesitas explicar muchas acciones lo hagas en distintos commits.

* Agrega un prefijo a tus commits: Nosotros vamos a usar dos por ahora: 
  - **chore**: para hacer referecia a la realización de una nueva tarea.
  - **fix**: para arreglar bugs.

**Ejemplo:**
```bash
git commit -m 'chore: remover search bar de la navbar'
```


</div>


+++ 💡 Comandos De Git
 
Vistiá este [sitio](https://gitexplorer.com/) que cuenta con una hoja de trucos con todos los comandos.

+++

