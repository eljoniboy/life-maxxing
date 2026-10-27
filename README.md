# Life Maxxing

Programa de 365 días: hábitos, briefing diario del coach, campaña semanal/mensual y celebraciones.
App 100 % estática y offline: no hay servidor, cuentas ni analítica. **Tus datos viven solo en tu dispositivo** (localStorage del navegador).

## Contenido
| Archivo | Para qué |
|---|---|
| `index.html` | La app completa (HTML+CSS+JS, fuentes y sonidos generados en el propio archivo) |
| `manifest.webmanifest` | Datos para "Añadir a pantalla de inicio" (nombre, colores, iconos) |
| `icon-180.png`, `icon-192.png`, `icon-512.png` | Iconos (iPhone / Android / instalación) |
| `sw.js` | Service worker: abre sin conexión; con red siempre carga la última versión |
| `.nojekyll` | Evita que GitHub Pages procese el sitio con Jekyll |

Todas las rutas son relativas: funciona en `https://usuario.github.io/` o en una subcarpeta como `https://usuario.github.io/life-maxxing/`.

## Publicar en GitHub Pages
1. Crea un repositorio (p. ej. `life-maxxing`) y sube **el contenido de esta carpeta** a la raíz de la rama `main`.
2. En el repo: **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`** → Save.
3. En 1–2 minutos estará en `https://<tu-usuario>.github.io/life-maxxing/`.

## Instalar en iPhone
Abre la URL en **Safari** → botón Compartir → **Añadir a pantalla de inicio**. Se abre a pantalla completa y funciona sin conexión.

## Respaldo de datos
Ajustes → **Guardar archivo** descarga `life-maxxing-save-AAAA-MM-DD.json`; **Cargar archivo** lo restaura. Los datos de Safari y los de la app instalada en la pantalla de inicio pueden estar separados: usa el archivo para moverlos. Borrar los datos del sitio en el navegador borra el progreso.

## Actualizar
Reemplaza los archivos y haz push. El service worker usa red primero, así que la nueva versión se carga en la siguiente apertura con conexión.
