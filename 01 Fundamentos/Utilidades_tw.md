# Utilidades en TW

Tailwind CSS es más que colorcitos y hacer que el `html` se vea monstruoso (haha), en este documento haré un repaso por las clases empezando desde la estructura, seguida de diseño, interacción y más:

## `flex` en Tailwind
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

### Ejemplos típicos con `flex`
| Estructura deseada                        | Clases sugeridas                   | Comentario práctico                                 |
| ----------------------------------------- | ---------------------------------- | --------------------------------------------------- |
| Tarjetas verticales                       | `flex flex-col gap-y-4`            | Ideal para apilar elementos con espacio entre ellos |
| Botones uno al lado del otro              | `flex gap-x-2`                     | Mucho más limpio que usar `ml-*` en todos           |
| Centrar cualquier cosa (ambos ejes)       | `flex justify-center items-center` | Muy común en modales, banners, contenedores         |
| Distribuir elementos extremos             | `flex justify-between`             | Ej: logo a la izquierda, menú a la derecha          |
| Diseño que cambia según ancho de pantalla | `flex-col md:flex-row`             | Vertical en móvil, horizontal en desktop            |

## `grid` en Tailwind
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

## Espaciado en Tailwind

🧠 Resumen clave:

* m- y p- = margen y padding
* gap = espacio ENTRE hijos (funciona con flex y grid)
* space-x y space-y = márgenes automáticos ENTRE hijos (solo en flex o inline-flex)
* inset = desplazamiento desde los bordes (cuando hay absolute o relative)
