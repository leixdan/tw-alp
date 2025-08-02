# Utilidades en TW

Tailwind CSS es más que colorcitos y hacer que el `html` se vea monstruoso (haha), en este documento haré un repaso por las clases empezando desde la estructura, seguida de diseño, interacción y más:

## **Estructura y organización**
### Estructura de la página

| Clase base         | Se usa para                                  | Ejemplo             | Valores disponibles                                                          |
| ------------------ | -------------------------------------------- | ------------------- | ---------------------------------------------------------------------------- |
| `h-`               | Altura                                       | `h-20`              | `0` a `96`, `px`, `full`, `screen`, `min`, `max`, `fit`, etc.                |
| `w-`               | Anchura                                      | `w-1/2`             | `0` a `96`, `px`, `1/2`, `1/3`, `full`, `screen`, `min`, `max`, `fit`, etc.  |
| `min-h-`           | Altura mínima                                | `min-h-screen`      | `0`, `full`, `screen`, etc.                                                  |
| `max-h-`           | Altura máxima                                | `max-h-96`          | `0` a `96`, `full`, `screen`                                                 |
| `min-w-`           | Ancho mínimo                                 | `min-w-full`        | `0`, `full`, `min`, `max`, etc.                                              |
| `max-w-`           | Ancho máximo                                 | `max-w-xl`          | `xs`, `sm`, `md`, `lg`, `xl`, `2xl`, `3xl`, etc.                             |
| `m-`               | Margen general                               | `m-4`               | `0` a `96`, `px`, `auto`, negativos: `-m-4`                                  |
| `mt-`, `mb-`, etc. | Margen en un solo lado                       | `mt-8`, `ml-2`      | Igual que `m-`                                                               |
| `mx-`, `my-`       | Margen horizontal / vertical                 | `mx-auto`, `my-2`   | Igual que `m-`, incluye `auto`                                               |
| `p-`               | Padding general                              | `p-6`               | `0` a `96`, `px`                                                             |
| `pt-`, `pb-`, etc. | Padding en un solo lado                      | `pt-4`, `pl-1`      | Igual que `p-`                                                               |
| `px-`, `py-`       | Padding horizontal / vertical                | `px-4`, `py-2`      | Igual que `p-`                                                               |
| `container`        | Contenedor centrado con max-width automática | `container mx-auto` | Comportamiento predeterminado por Tailwind                                   |
| `box-border`       | Modelo de caja incluye padding y border      | `box-border`        | `box-border`, `content-box`                                                  |
| `overflow-`        | Manejo de desbordamiento                     | `overflow-hidden`   | `auto`, `hidden`, `visible`, `scroll`                                        |
| `aspect-`          | Mantener proporciones de ancho/alto          | `aspect-square`     | `aspect-square`, `aspect-video`, proporciones personalizadas si se habilitan |



### `flex` en Tailwind
Flexbox está diseñado para la disposición unidimensional (filas o columnas):

Clase              | Se usa para...                                       | Comentario explicativo / Ejemplo de uso
------------------ |------------------------------------------------------|-------------------------------------------------------------
flex               | Activa el modo flexbox                               | Convierte al contenedor en un "alineador" de sus hijos en fila (horizontal por defecto)
flex-row           | Organiza los hijos en fila (izquierda a derecha)     | Es el valor por defecto, pero se puede poner explícitamente
flex-col           | Organiza los hijos en columna (de arriba a abajo)    | Muy útil para listas verticales, formularios o menús laterales
flex-wrap          | Permite que los hijos "salten" de línea si no caben  | Esencial en layouts responsivos; hijos se acomodan abajo
justify-start      | Alinea los hijos al inicio del eje principal         | Horizontal si `flex-row`, vertical si `flex-col`
justify-center     | Centra los hijos en el eje principal                 | Ej: centrar horizontalmente en una fila
justify-end        | Alinea los hijos al final del eje principal          | Ej: alinear a la derecha
justify-between    | Espacia a los hijos entre sí, sin margen en extremos | Ej: menú con elementos en los extremos
justify-around     | Deja espacio igual alrededor de cada hijo            | Similar a `between` pero con márgenes laterales
items-start        | Alinea los hijos al inicio del eje cruzado           | Vertical si `flex-row`; horizontal si `flex-col`
items-center       | Centra los hijos en el eje cruzado                   | Ej: centrar verticalmente una fila
items-end          | Alinea los hijos al final del eje cruzado            | Ej: alinearlos abajo
gap-x-4            | Deja espacio horizontal entre los hijos              | Solo afecta el eje X, útil en `flex-row`
gap-y-4            | Deja espacio vertical entre los hijos                | Solo eje Y, útil en `flex-col`
gap-4              | Aplica espacio en ambos ejes (x e y)                 | Se puede usar como atajo si no necesitas separar por eje

#### Ejemplos típicos con `flex`
| Estructura deseada                        | Clases sugeridas                   | Comentario práctico                                 |
| ----------------------------------------- | ---------------------------------- | --------------------------------------------------- |
| Tarjetas verticales                       | `flex flex-col gap-y-4`            | Ideal para apilar elementos con espacio entre ellos |
| Botones uno al lado del otro              | `flex gap-x-2`                     | Mucho más limpio que usar `ml-*` en todos           |
| Centrar cualquier cosa (ambos ejes)       | `flex justify-center items-center` | Muy común en modales, banners, contenedores         |
| Distribuir elementos extremos             | `flex justify-between`             | Ej: logo a la izquierda, menú a la derecha          |
| Diseño que cambia según ancho de pantalla | `flex-col md:flex-row`             | Vertical en móvil, horizontal en desktop            |

### `grid` en Tailwind
Grid está optimizado para diseños bidimensionales (filas y columnas simultáneamente):

Clase              | Se usa para...                               | Comentario explicativo / Ejemplo de uso
------------------ |--------------------------------------------- |----------------------------------------------------------
grid               | Activa CSS Grid                              | El contenedor se comporta como una cuadrícula (como una tabla visual)
grid-cols-2        | Crea 2 columnas iguales                      | Se pueden definir de 1 a 12 columnas (`grid-cols-3`, etc.)
grid-rows-3        | Crea 3 filas iguales                         | Igual que columnas; útil para tableros o layouts complejos
gap-4              | Espacio entre filas y columnas               | Aplica separación en ambos ejes; útil para que los hijos no estén pegados
gap-x-4            | Espacio horizontal entre columnas            | Se usa cuando solo quieres separar horizontalmente
gap-y-4            | Espacio vertical entre filas                 | Ideal si solo quieres separación vertical (por ejemplo, listas en grid)
col-span-2         | Hace que un hijo ocupe 2 columnas            | Similar a `colspan` en tablas HTML. Útil para crear elementos más grandes
row-span-2         | Hace que un hijo ocupe 2 filas               | Para tarjetas que se extienden hacia abajo más que las otras
place-items-center | Centra TODOS los hijos en ambos ejes        | Equivale a `justify-items-center` + `items-center` (horizontal + vertical)
justify-items-start| Alinea hijos horizontalmente al inicio      | Aplica dentro de cada celda del grid, no al grid entero
items-start        | Alinea hijos verticalmente arriba            | Similar a `align-items` en CSS; útil para alinear contenido en celdas

### Espaciado en Tailwind
Resumen clave:
* m- y p- = margen y padding
* gap = espacio ENTRE hijos (funciona con flex y grid)
* space-x y space-y = márgenes automáticos ENTRE hijos (solo en flex o inline-flex)
* inset = desplazamiento desde los bordes (cuando hay absolute o relative)

Clase              | Se usa para...                                      | Comentario explicativo / Ejemplo de uso
------------------ |-----------------------------------------------------|-------------------------------------------------------------
m-4                | Margen exterior en los 4 lados                      | Equivale a `margin: 1rem;` (espaciado base de Tailwind)
mt-4 / mb-2        | Margen superior o inferior                         | `t = top`, `b = bottom`, `l = left`, `r = right`
mx-2 / my-6        | Margen en eje horizontal o vertical                 | `x = left & right`, `y = top & bottom`
p-4                | Padding interior en los 4 lados                    | Equivale a `padding: 1rem;`
pt-1 / pl-2        | Padding específico en un lado                      | `pt = padding-top`, `pl = padding-left`, etc.
px-6 / py-2        | Padding en eje horizontal o vertical               | Muy usado en botones y tarjetas para equilibrar espacios
gap-4              | Espacio entre hijos en `grid` o `flex`             | Separa a todos los elementos hijos sin usar `m-*`
gap-x-4            | Solo deja espacio horizontal entre hijos           | Útil en `flex-row`
gap-y-4            | Solo deja espacio vertical entre hijos             | Útil en `flex-col`
space-x-4          | Margen automático horizontal ENTRE hijos           | Funciona SOLO en contenedor `flex` o `inline-flex`
space-y-2          | Margen automático vertical ENTRE hijos             | No afecta al primer ni último hijo, ideal para listas
inset-0            | Posiciona en los 4 bordes (top, bottom, etc.)      | Requiere que el padre tenga `relative` y el hijo `absolute`
inset-x-0 / y-0    | Posiciona en eje horizontal o vertical             | Ej: `inset-x-0` = izquierda y derecha en 0
top-4 / left-2     | Posiciona solo desde ese lado                      | Funciona con `absolute` o `fixed`


### Posición en Tailwind
La posición define cómo se ubica un elemento dentro de su contenedor padre, especialmente cuando quieres que un botón, tooltip, menú o modal se "despegue" de su flujo normal (por ejemplo, que flote, se quede fijo o se posicione respecto a un punto):

Clase              | Se usa para...                                         | Comentario explicativo / Ejemplo de uso
------------------ |--------------------------------------------------------|-------------------------------------------------------------
relative           | Define al elemento como "referencia de posición"       | Necesario para que los elementos hijos `absolute` se ubiquen respecto a él
absolute           | Saca al elemento del flujo normal y lo posiciona      | Se posiciona respecto al padre más cercano con `relative`
fixed              | Lo posiciona respecto a la ventana del navegador      | No se mueve al hacer scroll (ej: menú fijo arriba)
sticky             | Se comporta como relativa hasta que se hace scroll    | Ej: títulos que se quedan pegados al llegar arriba
top-0              | Coloca el elemento en el borde superior                | Requiere que sea `absolute`, `fixed` o `sticky`
right-0            | Borde derecho                                           | Lo empuja hasta la derecha
bottom-4           | 4 unidades desde el fondo del contenedor               | Ideal para botones flotantes o banners
left-1/2           | Mitad del ancho desde la izquierda                     | Útil para centrar elementos con transform
inset-0            | Aplica `top-0 right-0 bottom-0 left-0` al mismo tiempo| El elemento se estira o posiciona en las 4 esquinas
inset-x-0          | Aplica `left-0` y `right-0`                             | Se estira horizontalmente
inset-y-4          | Aplica `top-4` y `bottom-4`                             | Despega el elemento del borde superior e inferior
z-10               | Controla el nivel “frontal” del elemento               | Mayor `z` = más arriba; útil para tooltips, modales

#### Casos comunes:
| Lo que quieres hacer                            | Clases típicas                        | Notas                                     |
| ----------------------------------------------- | ------------------------------------- | ----------------------------------------- |
| Colocar un botón flotante abajo a la derecha    | `absolute bottom-4 right-4`           | Requiere que el padre tenga `relative`    |
| Fijar una barra superior que no desaparezca     | `fixed top-0 left-0 right-0 z-50`     | Útil para navbars que se quedan en scroll |
| Poner un tooltip encima de un ícono             | `absolute -top-2 left-full ml-2 z-20` | Combina desplazamientos para colocar bien |
| Que un título se quede "pegado" al hacer scroll | `sticky top-0 bg-white z-10`          | Se usa con scroll dentro de un div        |

### Alineación de texto y contenido en Tailwind
Clase               | Se usa para...                                       | Comentario explicativo / Ejemplo de uso
--------------------|------------------------------------------------------|---------------------------------------------------------------
text-left           | Alinea el texto a la izquierda (por defecto)         | Equivale a `text-align: left;`
text-center         | Centra el texto horizontalmente                      | Muy común en títulos, botones y alertas
text-right          | Alinea el texto a la derecha                         | Útil para totales, montos o idiomas RTL
text-justify        | Justifica el texto (como en libros o periódicos)     | Crea bordes rectos a ambos lados
align-top           | Alinea un elemento al inicio del eje vertical        | Funciona dentro de un contenedor `flex` o celda de `table`
align-middle        | Centra verticalmente dentro del contenedor           | Útil en celdas de tabla o contenedores pequeños
align-bottom        | Alinea al fondo del contenedor                       | Ideal para botones o íconos en línea
vertical-align-top  | Igual que `align-top` pero en elementos `inline`     | Ej: `<span>`, `<img>`, etc.
place-content-center| Centra TODO el contenido (en `grid`)                 | Centra horizontal y verticalmente los hijos
justify-self-center | Centra el hijo horizontal individualmente en `grid`  | Funciona solo dentro de celdas `grid`
text-base / text-sm | Cambia el tamaño del texto                           | No es alineación, pero ayuda a distribuir mejor visualmente
leading-tight       | Ajusta el interlineado (espacio entre líneas)        | Mejora la legibilidad del texto

#### Usos comunes:

| Situación común                               | Clase recomendada           | Comentario                                                     |
| --------------------------------------------- | --------------------------- | -------------------------------------------------------------- |
| Centrar título o botón                        | `text-center`               | Clásico y muy legible                                          |
| Texto en tabla centrado vertical y horizontal | `text-center align-middle`  | En `<td>` o `div.table-cell`                                   |
| Diseños tipo tabla                            | `inline-block align-middle` | Elementos como íconos, imágenes o inputs alineados visualmente |
| Centrar el contenido de una tarjeta (grid)    | `place-content-center`      | En combinación con `grid`                                      |
| Texto alineado a la derecha                   | `text-right`                | Ideal para totales o firmas                                    |

## **Visualización e interacción**
### Colores
Clase                  | Se usa para...                              | Comentario / Ejemplo
---------------------- |---------------------------------------------|-------------------------------------------------------------
bg-blue-500            | Fondo azul tono medio                       | Los colores tienen 100 a 900, mientras más alto, más oscuro
bg-red-100             | Fondo rojo claro                            | Ideal para fondos suaves de alertas o badges
text-white             | Texto blanco                                | También puedes usar `text-gray-700`, `text-blue-800`, etc.
text-black/gray-900    | Texto negro o gris oscuro                   | `gray-900` es un negro más suave (más usado que `text-black`)
border-blue-500        | Borde con color azul                        | Se usa con `border` para que se vea
hover:bg-blue-600      | Cambia el fondo al pasar el mouse           | Usado para botones interactivos
focus:border-blue-500  | Cambia borde al hacer foco (inputs)         | Mejora la accesibilidad visual
placeholder-gray-400   | Color del texto de placeholder              | Útil en inputs

### Estados (interacción: hover, focus, active, etc.)
Clase                         | Se usa para...                             | Comentario / Ejemplo
----------------------------- |--------------------------------------------|-------------------------------------------------------------
hover:bg-blue-600             | Cambia color al pasar el mouse             | Ideal en botones o tarjetas
hover:scale-105               | Aumenta tamaño ligeramente al pasar cursor | Requiere `transform` o `transition`
focus:outline-none            | Quita el borde predeterminado del foco     | En inputs, buttons
focus:ring-2 ring-blue-300   | Crea un halo suave al enfocar              | Mejora la visibilidad para accesibilidad
active:bg-blue-700           | Cambia color cuando se hace clic           | Estado `presionado`
disabled:opacity-50          | Hace que un botón deshabilitado se vea gris| Visual y accesible
group-hover:bg-gray-200      | Cambia elementos hijos si el padre es hovered| Usa `group` en el padre

### Responsividad
Clase               | Se usa para...                                     | Comentario / Ejemplo
------------------- |----------------------------------------------------|-------------------------------------------------------------
sm:                | A partir de 640px (móviles grandes)                | Ej: `sm:text-lg`
md:                | Desde 768px (tablets y más)                        | Ej: `md:flex-row`
lg:                | Desde 1024px (laptops)                             | Ej: `lg:grid-cols-4`
xl:                | Desde 1280px (pantallas grandes)                   | Ej: `xl:text-2xl`
2xl:               | Desde 1536px (monitores muy grandes)               | Ej: `2xl:container`
responsive override| Puedes cambiar estilos según tamaño                | Ej: `text-sm md:text-base lg:text-xl`
hidden sm:block    | Oculta en móvil, muestra en tablet                 | Combinación muy común en menús

### Animaciones y transiciones
Clase                      | Se usa para...                                  | Comentario / Ejemplo
-------------------------- |--------------------------------------------------|-------------------------------------------------------------
transition                 | Activa transiciones (por defecto all)           | Necesario para que los `hover:` o `focus:` se animen
transition-colors          | Solo transiciona colores                        | Mejor rendimiento que `transition` general
duration-300               | Duración de la transición en ms (300ms aquí)    | Muy usada para efectos suaves
ease-in / ease-out         | Curva de animación                              | `ease-in-out` es muy equilibrada
delay-150                  | Retardo antes de empezar la animación           | Útil en tooltips o loaders
animate-bounce             | Aplica una animación predefinida                | Otros: `pulse`, `spin`, `ping`, `fade-in-down` (con plugins)
hover:scale-110            | Escala al pasar el mouse                        | Usado junto con `transform transition`

### Extras visuales (bordes, sombras, opacidad, blur…)
Clase               | Se usa para...                                   | Comentario / Ejemplo
------------------- |--------------------------------------------------|-------------------------------------------------------------
rounded             | Borde redondeado general                         | Hay variantes como `rounded-md`, `rounded-lg`, etc.
rounded-full        | Círculo perfecto                                 | Ideal para avatares, botones circulares
shadow              | Sombra suave                                     | También: `shadow-md`, `shadow-xl`, `shadow-inner`, etc.
opacity-50          | Reduce opacidad                                  | Útil para elementos secundarios o deshabilitados
backdrop-blur-sm    | Aplica desenfoque al fondo                       | Funciona en overlays (requires `backdrop-filter`)
border              | Aplica borde básico (1px gris claro)             | Puedes combinar con `border-color` y `border-*`
ring-2 ring-blue-300| Halo o anillo exterior                           | Visualmente más suave que un `border`
