# Introducción a HTML moderno 📄️
HyperText Markup Lenguage o Lenguaje de Marcado de Hipertexto, es el código estándar para crear páginas web, se maneja a través de etiquetas que dan estructura y formato al contenido de una pagina web.

Dado que se usan etiquetas, es importante tener un sentido coherente y semántico, la semántica en HTML5 significa usar las etiquetas correctas según el contenido, esto nos ayuda a:

- El navegador entenderá mejor el contenido.
- Mejora la accesibilidad.
- Hace el código más fácil de mantener a futuro.

Las etiquetas semánticas se diferencían de las demás ya que son exclusivamente para dar esa estructura y organización, existen muchas otras etiquetas, ya sea para agregar texto, scripts, etc. El conocimiento y uso correcto de estas etiquetas hacen la diferencia entre un programador y un profesional con buenas prácticas:

| Etiqueta       | Propósito                                                                                                  | Ejemplo en uso                                                             |
| -------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `<header>`     | Contenido introductorio o navegación principal. Puede ir en `<body>` o dentro de `<section>`, `<article>`. | `<header><h1>Mi Blog</h1></header>`                                        |
| `<nav>`        | Contenedor de enlaces de navegación.                                                                       | `<nav><a href="/">Inicio</a></nav>`                                        |
| `<main>`       | Contenido principal único de la página. Solo debe haber uno por página.                                    | `<main><h2>Contenido</h2></main>`                                          |
| `<section>`    | Agrupación temática de contenido.                                                                          | `<section><h2>Artículos recientes</h2></section>`                          |
| `<article>`    | Contenido independiente y reutilizable (como un post o noticia).                                           | `<article><h2>Post</h2><p>Texto</p></article>`                             |
| `<aside>`      | Contenido complementario o contextual (como una barra lateral).                                            | `<aside><p>Publicidad</p></aside>`                                         |
| `<footer>`     | Información de pie de página. Puede ir en la página o dentro de secciones.                                 | `<footer><p>&copy; 2025 Mi Sitio</p></footer>`                             |
| `<figure>`     | Contenedor para contenido gráfico (imágenes, diagramas).                                                   | `<figure><img src="img.png"><figcaption>Descripción</figcaption></figure>` |
| `<figcaption>` | Título o descripción de una figura.                                                                        | `<figcaption>Esta es una imagen del logo</figcaption>`                     |
| `<time>`       | Representa una hora o fecha.                                                                               | `<time datetime="2025-07-06">6 de julio de 2025</time>`                    |
| `<mark>`       | Resalta texto como si fuera un marcador.                                                                   | `<p>Este es un <mark>dato importante</mark>.</p>`                          |
| `<address>`    | Información de contacto (autor, empresa...).                                                               | `<address>contacto@ejemplo.com</address>`                                  |

Si no las usamos, a ojo humano podría no haber una diferencia, pero a nivel de funcionamiento y entendimiento de la página por parte del navegador podrían haber problemas, por ejemplo:

```html
<!-- NO semántico -->
<div class="header">
  <div class="titulo">Mi Blog</div>
</div>

<!-- Semántico -->
<header>
  <h1>Mi Blog</h1>
</header>
```
## Etiquetas más comunes en HTML y su función 🏷️
Las hay de varios tipos, intentaré separarlas por categorías indicando su funcionalidad:

* Estructura básica 🏗️

| Etiqueta  | Descripción                          | Ejemplo                                 |
| --------- | ------------------------------------ | --------------------------------------- |
| `<html>`  | Contenedor raíz de un documento HTML | `<html>...</html>`                      |
| `<head>`  | Contiene metadatos                   | `<head><title>Mi página</title></head>` |
| `<title>` | Título de la página                  | `<title>Inicio</title>`                 |
| `<body>`  | Contiene el contenido visible        | `<body><p>Hola</p></body>`              |


* Texto y formato ✏️

| Etiqueta        | Descripción                | Ejemplo                               |
| --------------- | -------------------------- | ------------------------------------- |
| `<h1>` a `<h6>` | Encabezados de nivel 1 a 6 | `<h1>Encabezado</h1>`                 |
| `<p>`           | Párrafo                    | `<p>Este es un párrafo.</p>`          |
| `<br>`          | Salto de línea             | `Línea 1<br>Línea 2`                  |
| `<strong>`      | Negrita semántica          | `<strong>Importante</strong>`         |
| `<b>`           | Negrita (solo visual)      | `<b>Texto</b>`                        |
| `<em>`          | Cursiva semántica          | `<em>Énfasis</em>`                    |
| `<i>`           | Cursiva (solo visual)      | `<i>Texto</i>`                        |
| `<u>`           | Subrayado                  | `<u>Texto subrayado</u>`              |
| `<span>`        | Contenedor en línea        | `<span style="color:red">Rojo</span>` |
| `<div>`         | Contenedor en bloque       | `<div>Bloque de contenido</div>`      |

* Enlaces e Imágenes 🔗️

| Etiqueta       | Descripción           | Ejemplo                                                              |
| -------------- | --------------------- | -------------------------------------------------------------------- |
| `<a>`          | Enlace (hipervínculo) | `<a href="https://example.com">Ir</a>`                               |
| `<img>`        | Imagen                | `<img src="logo.png" alt="Logo">`                                    |
| `<figure>`     | Contenedor visual     | `<figure><img src="foto.jpg"><figcaption>Foto</figcaption></figure>` |
| `<figcaption>` | Título de figura      | `<figcaption>Descripción</figcaption>`                               |

* Listas 📋

| Etiqueta | Descripción                     | Ejemplo                      |
| -------- | ------------------------------- | ---------------------------- |
| `<ul>`   | Lista no ordenada (con viñetas) | `<ul><li>Elemento</li></ul>` |
| `<ol>`   | Lista ordenada (con números)    | `<ol><li>Primero</li></ol>`  |
| `<li>`   | Elemento de una lista           | `<li>Ítem</li>`              |

* Tablas 🧮️

| Etiqueta  | Descripción         | Ejemplo                                   |
| --------- | ------------------- | ----------------------------------------- |
| `<table>` | Crea una tabla      | `<table><tr><td>Dato</td></tr></table>`   |
| `<tr>`    | Fila de tabla       | `<tr><td>Fila</td></tr>`                  |
| `<td>`    | Celda de datos      | `<td>Celda</td>`                          |
| `<th>`    | Celda de encabezado | `<th>Encabezado</th>`                     |
| `<thead>` | Encabezado de tabla | `<thead><tr><th>Nombre</th></tr></thead>` |
| `<tbody>` | Cuerpo de tabla     | `<tbody><tr><td>Juan</td></tr></tbody>`   |
| `<tfoot>` | Pie de tabla        | `<tfoot><tr><td>Total</td></tr></tfoot>`  |

* Formularios 📋️

| Etiqueta     | Descripción                 | Ejemplo                                    |
| ------------ | --------------------------- | ------------------------------------------ |
| `<form>`     | Formulario HTML             | `<form action="/envio"></form>`            |
| `<input>`    | Campo de entrada            | `<input type="text">`                      |
| `<label>`    | Etiqueta para un campo      | `<label for="nombre">Nombre:</label>`      |
| `<textarea>` | Área de texto               | `<textarea></textarea>`                    |
| `<button>`   | Botón de envío u otro uso   | `<button>Enviar</button>`                  |
| `<select>`   | Menú desplegable            | `<select><option>Opción</option></select>` |
| `<option>`   | Opción dentro de `<select>` | `<option value="1">Uno</option>`           |

* Multimedia 📹️

| Etiqueta   | Descripción          | Ejemplo                                            |
| ---------- | -------------------- | -------------------------------------------------- |
| `<video>`  | Reproductor de video | `<video controls><source src="video.mp4"></video>` |
| `<audio>`  | Reproductor de audio | `<audio controls><source src="audio.mp3"></audio>` |
| `<source>` | Fuente multimedia    | `<source src="archivo.mp4" type="video/mp4">`      |


***
# CSS 🏞️
Cascading Style Sheets, es el lenguaje utilizado para describir la presentación de un documento HTML o XML, se encarga de darle el estilo a una página web controlando aspectos como colores, fuente, formas y disposición de los elementos, es el "cómo" se ve la estructura y datos de la página web.

## Box model (CSS) 📦️
Para CSS, cada elemento HTML se comporta como una "caja", y esta caja tiene 4 capas vistas desde dentro hacia afuera:

| Parte     | Descripción                                                     |
| --------- | --------------------------------------------------------------- |
| `content` | El contenido real (texto, imagen, botón, etc.)                  |
| `padding` | Espacio **dentro** de la caja, entre el borde y el contenido    |
| `border`  | El borde visible de la caja                                     |
| `margin`  | Espacio **afuera** de la caja, que la separa de otros elementos |

Visto de otra manera, podemos imaginar una caja de texto en power point, tiene un texto (`content`), un espacio dentro de la caja de texto (`padding`), un borde de la caja (`border`) y un márgen exterior, espacio entre otras cajas (`margin`).

## Flexbox 📏️
Flexbox es un sistema de diseño que organiza elementos en línea o en columnas, de forma responsiva y adaptable.

Ideal para:

    - Menús horizontales

    - Alinear cosas verticalmente

    - Distribuir espacio

## Grid 📐️
CSS Grid es un sistema más potente que Flexbox, pensado para distribuir elementos en filas y columnas. Es ideal cuando:

    - Quieres una estructura tipo “rejilla” (como una galería de imágenes)

    - Necesitas más control en 2 dimensiones (horizontal + vertical)

¿Cómo funciona?

* Se aplica al contenedor con la clase `grid`
* Se define cuántas columnas o filas tendrá (`grid-cols-*`, `grid-rows-*`)
* Se usa `gap-*` para espaciar elementos

| Clase Tailwind                | ¿Qué hace?                                 |
| ----------------------------- | ------------------------------------------ |
| `grid`                        | Activa Grid en el contenedor               |
| `grid-cols-*`                 | Define cuántas columnas hay                |
| `grid-rows-*`                 | Define cuántas filas hay (menos usado)     |
| `gap-*`, `gap-x-*`, `gap-y-*` | Espacios entre filas y columnas            |
| `col-span-*`                  | Hace que un elemento ocupe varias columnas |
| `row-span-*`                  | Lo mismo pero en filas                     |

***
# Accesibilidad y buenas prácticas 📖️

1. Usar etiquetas semánticas como estructura del documento HTML.
2. Usar `alt` en imágenes: `<img src="logo.png" alt="Logo de la empresa"`, habrán momentos que la liga falle.
3. Usar botones reales `<button>` en vez de `<div>` clickeable.
4. Usar `label` para formularios:
```html
<label for="nombre">Nombre</label>
<input id="nombre" name="nombre" type="text" />
 ```
5. Usar `aria-*` si se están construyendo componentes personalizados.

***
# Código de ejemplo 👀️

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Interfaz Semántica</title>
    <script defer src="https://unpkg.com/alpinejs"></script>
    <script src="https://cdn.tailwindcss.com"></script>
  </head>
  <body class="font-sans bg-gray-100 text-gray-900">

    <header class="bg-white shadow p-4">
      <h1 class="text-2xl font-bold">Panel de Usuario</h1>
    </header>

    <main class="p-6 grid grid-cols-2 gap-6">
      <section>
        <article class="bg-white p-4 rounded shadow">
          <h2 class="text-xl font-semibold">Perfil</h2>
          <p>Información del usuario...</p>
        </article>
      </section>

      <section x-data="{ abierto: false }">
        <button @click="abierto = !abierto" class="bg-blue-500 text-white px-4 py-2 rounded">
          Mostrar detalles
        </button>
        <div x-show="abierto" class="mt-2 bg-white p-4 rounded shadow">
          <p>Más información del usuario...</p>
        </div>
      </section>
    </main>

    <footer class="bg-white shadow p-4 text-center">
      <p>&copy; 2025 Panel de Usuario</p>
    </footer>

  </body>
</html>

```