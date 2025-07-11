# 🚀 Plantilla Base – Go + Tailwind CSS + Alpine.js

Este proyecto es una **estructura mínima y reutilizable** para iniciar aplicaciones web con Go como backend, Tailwind CSS para el estilo, y Alpine.js para interactividad ligera.

Está pensado para facilitar el trabajo **sin frameworks pesados**, con una separación clara entre frontend y backend.

---

## 📦 Instalación por proyecto

Cada vez que inicies un nuevo proyecto, haz lo siguiente:

```bash
# Crea tu carpeta de proyecto
mkdir mi-proyecto && cd mi-proyecto

# Inicializa Node
npm init -y

# Instala Tailwind como dependencia de desarrollo
npm install -D tailwindcss

# Crea el archivo de configuración de Tailwind
npx tailwindcss init
```

## 🗂️ Estructura de proyecto base

mi-proyecto/

├── assets/

│   ├── input.css          # Instrucciones para Tailwind (@tailwind ...)

│   └── js/

│       └── alpine.js      # Alpine.js (opcional)

├── public/

│   └── output.css         # CSS generado por Tailwind (no lo edites)

├── templates/

│   └── index.tmpl         # Tu plantilla HTML base (renderizada por Go)

├── main.go                # Servidor Go

├── tailwind.config.js     # Configuración de Tailwind

├── package.json           # Configuración de NPM

├── Makefile               # Scripts automáticos (desarrollo y build)

└── README.md              # Esta guía

### 🧾 ¿Qué contiene cada parte?
| Archivo / Carpeta      | Función                                                           |
| ---------------------- | ----------------------------------------------------------------- |
| `assets/input.css`     | Directivas base de Tailwind (`@tailwind base; ...`)               |
| `assets/js/alpine.js`  | Script de Alpine.js (o vía CDN si prefieres)                      |
| `public/output.css`    | CSS generado automáticamente por Tailwind                         |
| `templates/index.tmpl` | Plantilla HTML con clases Tailwind renderizada por Go             |
| `main.go`              | Servidor Go que renderiza plantillas y sirve CSS estático         |
| `tailwind.config.js`   | Define qué archivos escanear para generar clases CSS              |
| `package.json`         | Scripts NPM y dependencias de Tailwind                            |
| `Makefile`             | Comandos para desarrollo (`make dev`) y producción (`make build`) |

### 💻 Visualizar en desarrollo y compilación final de proyecto

| Acción              | Comando                                                                 |
| ------------------- | ----------------------------------------------------------------------- |
| Compilar CSS (dev)  | `npx tailwindcss -i ./assets/input.css -o ./public/output.css --watch`  |
| Compilar CSS (prod) | `npx tailwindcss -i ./assets/input.css -o ./public/output.css --minify` |
| Ejecutar servidor   | `go run main.go`                                                        |
| Compilar binario    | `go build -o mi-app`                                                    |
