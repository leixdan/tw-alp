# Utilidades en TW

Tailwind CSS es más que colorcitos y hacer que el `html` se vea monstruoso (haha), tiene una gran cantidad de utilidades que en este documento vamos a dividir por clases más usadas y su descripción.

## Apariencia

| **Tipo**                 | **Ejemplos de clases**                                         | **Descripción**                                                               |
| ------------------------ | -------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Colores**              | `bg-blue-500`, `text-red-600`, `border-gray-300`               | Manejo de colores para fondos, texto, bordes, etc.                            |
| **Espaciado**            | `m-4`, `p-2`, `gap-6`, `space-x-4`                             | Margen, padding, separación entre elementos                                   |
| **Tipografía**           | `text-lg`, `font-bold`, `leading-tight`, `tracking-wide`       | Tamaño, peso, interlineado, espaciado de letras                               |
| **Diseño y Layout**      | `grid`, `flex`, `block`, `container`, `col-span-2`             | Control de estructura (grid, flexbox, display, etc.)                          |
| **Tamaño**               | `w-64`, `h-32`, `min-h-screen`, `max-w-sm`                     | Ancho, alto, máximos y mínimos                                                |
| **Posicionamiento**      | `absolute`, `relative`, `top-0`, `z-10`                        | Posición, z-index, offset                                                     |
| **Bordes y formas**      | `rounded-md`, `border`, `border-2`, `border-dashed`            | Bordes, esquinas redondeadas, estilos de borde                                |
| **Sombras y efectos**    | `shadow-lg`, `shadow-inner`, `ring-2`, `backdrop-blur`         | Sombra, efectos de fondo y enfoque                                            |
| **Animaciones**          | `animate-bounce`, `animate-spin`, `transition`, `duration-300` | Animaciones predefinidas, transiciones suaves, duración, tipo                 |
| **Estado (hover/focus)** | `hover:bg-blue-700`, `focus:ring`, `active:scale-95`           | Estilos para interacciones (hover, focus, active, etc.)                       |
| **Responsive**           | `md:flex`, `lg:hidden`, `sm:text-center`                       | Adaptación a distintos tamaños de pantalla                                    |
| **Utilidades avanzadas** | `aspect-video`, `isolate`, `pointer-events-none`               | Utilidades especiales para accesibilidad, comportamiento, relaciones visuales |
| **Interactividad**       | `cursor-pointer`, `select-none`, `touch-auto`                  | Comportamientos interactivos de usuario                                       |
| **Accesibilidad**        | `sr-only`, `not-sr-only`                                       | Mejora de la accesibilidad, por ejemplo, para lectores de pantalla            |

## Propiedades e interactividad

| **Elemento / Propiedad**     | **Tipos de interactividad disponibles**                                                            |
| ---------------------------- | -------------------------------------------------------------------------------------------------- |
| **Texto**                    | `hover:text-*`, `focus:text-*`, `active:text-*`, `group-hover:text-*`, `transition`, `animate-*`   |
| **Fondo**                    | `hover:bg-*`, `focus:bg-*`, `active:bg-*`, `group-hover:bg-*`, `transition-colors`                 |
| **Bordes y sombras**         | `hover:border-*`, `focus:border-*`, `hover:shadow-*`, `focus:shadow-*`, `ring-*`, `focus:ring-*`   |
| **Tamaño / Escala**          | `hover:scale-*`, `active:scale-*`, `transition-transform`, `duration-*`, `ease-*`                  |
| **Rotación**                 | `hover:rotate-*`, `group-hover:rotate-*`, `transition-transform`                                   |
| **Visibilidad**              | `hover:opacity-*`, `group-hover:opacity-*`, `transition-opacity`, `invisible`, `visible`, `hidden` |
| **Posicionamiento**          | `hover:translate-x-*`, `hover:translate-y-*`, `transition-transform`                               |
| **Estado del puntero**       | `cursor-pointer`, `cursor-not-allowed`, `hover:cursor-wait`, etc.                                  |
| **Focus & navegación**       | `focus:outline-none`, `focus:ring-*`, `focus-visible:*`, `focus-within:*`                          |
| **Animaciones**              | `animate-bounce`, `animate-spin`, `hover:animate-ping`, `motion-safe:animate-*`                    |
| **Accesibilidad / Lectores** | `sr-only`, `not-sr-only`, `focus:sr-only`, etc.                                                    |
| **Grupos (padres/hijos)**    | `group-hover:*`, `peer-focus:*`, `peer-checked:*`                                                  |
| **Estados de formulario**    | `checked:*`, `disabled:*`, `invalid:*`, `required:*`, `read-only:*`, etc.                          |

## Estructura

| **Categoría**                | **Clase principal**     | **Ejemplos / Subclases útiles**                                                                   | **Descripción**                                                  |
| ---------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| **Display**                  | `flex`, `grid`, `block` | `inline-flex`, `inline-grid`, `hidden`                                                            | Define el tipo de caja o layout del elemento                     |
| **Flexbox**                  | `flex`                  | `flex-row`, `flex-col`, `flex-wrap`, `flex-nowrap`, `flex-1`, `flex-auto`, `flex-none`            | Dirección, envoltura y crecimiento de elementos flexibles        |
| **Grid**                     | `grid`                  | `grid-cols-2`, `grid-cols-12`, `grid-rows-3`, `col-span-2`, `row-span-1`, `gap-4`, `auto-rows-fr` | Sistema de grillas con filas y columnas, espacios automáticos    |
| **Centrado (flex/grid)**     | `justify-`, `items-`    | `justify-center`, `items-center`, `place-items-center`, `justify-between`, `content-center`       | Centrado y alineación de contenido en ejes horizontal y vertical |
| **Columnas (responsive)**    | `grid-cols-*`           | `grid-cols-1`, `md:grid-cols-2`, `lg:grid-cols-4`                                                 | Distribución de columnas según tamaño de pantalla                |
| **Espaciado entre hijos**    | `gap-*`, `space-x-*`    | `gap-2`, `space-x-4`, `space-y-6`                                                                 | Espacio entre elementos hijos en grid o flex                     |
| **Orden**                    | `order-*`               | `order-1`, `order-2`, `order-last`, `md:order-first`                                              | Cambia el orden visual de los elementos                          |
| **Tamaño de contenedor**     | `container`             | `max-w-screen-lg`, `w-full`, `h-screen`, `min-h-full`                                             | Controla el ancho/alto máximo de elementos contenedores          |
| **Alineación**               | `self-*`, `items-*`     | `self-start`, `items-stretch`, `self-center`, `items-end`                                         | Alineación individual (`self`) o grupal (`items`)                |
| **Posicionamiento**          | `relative`, `absolute`  | `fixed`, `sticky`, `top-0`, `left-1/2`, `z-10`                                                    | Posición en el flujo de la página                                |
| **Overflow y contención**    | `overflow-*`            | `overflow-hidden`, `overflow-auto`, `isolate`, `contain-*`                                        | Manejo de contenido que se desborda y aislamiento visual         |
| **Breakpoints (Responsive)** | `sm:`, `md:`, `lg:`     | `sm:grid-cols-1`, `md:flex`, `lg:hidden`, `xl:container`                                          | Aplica clases de forma condicional según el ancho de pantalla    |

## Por ejemplo:

```html
<!-- Página con header, sidebar, main y footer -->
<div class="min-h-screen flex flex-col">

  <!-- Header -->
  <header class="bg-blue-600 text-white p-4 flex justify-between items-center">
    <h1 class="text-xl font-bold">Mi Sitio</h1>
    <nav class="space-x-4 hidden md:flex">
      <a href="#" class="hover:underline">Inicio</a>
      <a href="#" class="hover:underline">Acerca</a>
      <a href="#" class="hover:underline">Contacto</a>
    </nav>
  </header>

  <!-- Cuerpo principal: sidebar + contenido -->
  <div class="flex flex-1 flex-col md:flex-row">

    <!-- Sidebar -->
    <aside class="bg-gray-100 md:w-1/4 p-4 space-y-2">
      <h2 class="text-lg font-semibold">Menú</h2>
      <ul class="space-y-1">
        <li><a href="#" class="block p-2 rounded hover:bg-blue-100">Dashboard</a></li>
        <li><a href="#" class="block p-2 rounded hover:bg-blue-100">Usuarios</a></li>
        <li><a href="#" class="block p-2 rounded hover:bg-blue-100">Ajustes</a></li>
      </ul>
    </aside>

    <!-- Contenido principal -->
    <main class="flex-1 p-6 bg-white grid grid-cols-1 lg:grid-cols-3 gap-6">
      
      <!-- Tarjeta 1 -->
      <div class="p-4 rounded shadow hover:shadow-lg transition duration-300">
        <h3 class="text-lg font-bold mb-2">Estadísticas</h3>
        <p class="text-gray-600">Visitas recientes, conversión, etc.</p>
      </div>

      <!-- Tarjeta 2 -->
      <div class="p-4 rounded shadow hover:shadow-lg transition duration-300">
        <h3 class="text-lg font-bold mb-2">Tareas</h3>
        <ul class="list-disc list-inside text-gray-700 space-y-1">
          <li>Revisar reportes</li>
          <li>Actualizar usuarios</li>
        </ul>
      </div>

      <!-- Tarjeta 3 -->
      <div class="p-4 rounded shadow hover:shadow-lg transition duration-300">
        <h3 class="text-lg font-bold mb-2">Notificaciones</h3>
        <p class="text-gray-600">No hay nuevas notificaciones.</p>
      </div>

    </main>
  </div>

  <!-- Footer -->
  <footer class="bg-gray-200 text-center p-4 text-sm text-gray-600">
    &copy; 2025 Mi Sitio. Todos los derechos reservados.
  </footer>
</div>

```
### ¿Qué se está usando aquí?

| Categoría                 | Clases usadas                                                      |
| ------------------------- | ------------------------------------------------------------------ |
| **Flexbox**               | `flex`, `flex-col`, `flex-row`, `justify-between`, `items-center`  |
| **Grid**                  | `grid`, `grid-cols-1`, `lg:grid-cols-3`, `gap-6`                   |
| **Responsive**            | `md:flex-row`, `md:w-1/4`, `hidden md:flex`, `lg:grid-cols-3`      |
| **Espaciado**             | `p-4`, `p-6`, `mb-2`, `space-y-*`, `gap-6`, `mx-auto`              |
| **Tamaño**                | `min-h-screen`, `flex-1`, `w-1/4`                                  |
| **Centrado y alineación** | `items-center`, `justify-between`, `text-center`                   |
| **Colores y tipografía**  | `bg-*`, `text-*`, `font-bold`, `text-lg`, `text-sm`                |
| **Interactividad**        | `hover:shadow-lg`, `hover:underline`, `transition`, `duration-300` |
| **Otros**                 | `rounded`, `shadow`, `list-disc`, `list-inside`                    |

