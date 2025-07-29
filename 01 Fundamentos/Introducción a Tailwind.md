# Introducción a Tailwind CSS 🌬️🍃

Tailwind CSS es un framework de CSS de utilidad que te permite construir interfaces modernas y responsivas rápidamente, directamente en tu HTML. A diferencia de frameworks como Bootstrap, Tailwind no ofrece componentes prehechos, sino clases utilitarias para construir tus propios diseños desde cero.

Super importante: instalar la extensión oficial de tailwind: ![IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)

## Pros y contras ✅❗

Pros 😎
1. Modularidad: Se construyen componentes con alta personalización sin necesidad de sobrescribir estilos.
2. Sin archivos CSS personalizados: No es necesario escribir casi nada de CSS de forma manual.
3. Muy rápido en conjunto con JIT (Just-in-time): Genera solo CSS que usas.
4. Compatible con Apline.js: Se vuelve ideal para UI reactivas con el usuario sin frameworks grandes y buen manejo de espacio.

Contras 🤨
1. Curva de aprendizaje: El uso de clases que sustituyen el código CSS puede ser abrumador al inicio.
2. HTML cargado: Se pueden sumar varias clases en el código HTML.
3. Sin componentes viuales: Se deben crear desde cero, esto puede llevar tiempo.

Para producción en curso y si no se tiene instalado directamente tailwind, se puede usar el método CDN mientras se aprende.

```html
<script src="https://cdn.tailwindcss.com"></script>
```

Limitaciones:
El CSS cargado es completo (sin purga), por lo que es pesado

No puedes personalizar (colores, fuentes, plugins) fácilmente

No recomendado para apps grandes en producción

## Clases y Ejemplos comunes 📚
Las clases en Tailwind CSS son utilidades CSS predefinidas que puedes usar directamente en el HTML para aplicar estilos. En lugar de escribir CSS personalizado, Tailwind ofrece muchas clases pequeñas que hacen cosas específicas, como:

* text-center → para centrar el texto
* bg-blue-500 → para poner un fondo azul con intensidad 500
* p-4 → para aplicar padding (relleno) de 1 rem (espaciado)
* flex → para aplicar display: flex;
* y muchas más...

| Clase Tailwind     | Ejemplo en código                                    | Uso común                                                         |
| ------------------ | ---------------------------------------------------- | ----------------------------------------------------------------- |
| `text-center`      | `<p class="text-center">Texto</p>`                   | Centrar el texto                                                  |
| `bg-blue-500`      | `<div class="bg-blue-500 p-4"></div>`                | Fondo azul con intensidad 500                                     |
| `p-4`              | `<div class="p-4">Contenido</div>`                   | Padding (relleno) de 1 rem en todos lados                         |
| `m-2`              | `<div class="m-2">Caja</div>`                        | Margin (margen) de 0.5 rem en todos lados                         |
| `flex`             | `<div class="flex"><div>1</div><div>2</div></div>`   | Aplica `display: flex` para layout flexible                       |
| `justify-center`   | `<div class="flex justify-center">...</div>`         | Centra elementos en el eje horizontal dentro de un flex container |
| `items-center`     | `<div class="flex items-center">...</div>`           | Centra elementos verticalmente en flex container                  |
| `rounded`          | `<button class="rounded bg-gray-200">Botón</button>` | Bordes redondeados                                                |
| `hover:bg-red-500` | `<button class="hover:bg-red-500">Hover me</button>` | Cambia fondo al pasar el mouse (hover)                            |
| `w-full`           | `<input class="w-full" />`                           | Ancho completo del contenedor padre                               |
| `text-xl`          | `<h1 class="text-xl">Título</h1>`                    | Tamaño de texto extra grande                                      |
| `font-bold`        | `<span class="font-bold">Negrita</span>`             | Texto en negrita                                                  |
| `overflow-hidden`  | `<div class="overflow-hidden">...</div>`             | Oculta contenido que se sale del contenedor                       |
| `grid`             | `<div class="grid grid-cols-3 gap-4">...</div>`      | Layout en grilla con 3 columnas y espacio entre elementos         |


Estos son sólo algunas de las clases y ejemplos, pero el ideal sería investigar y conocer otras opciones en la documentación oficial:

### 📚 Sitio oficial de la documentación:

👉 https://tailwindcss.com/docs

