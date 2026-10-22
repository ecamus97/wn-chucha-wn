# Wn Chucha Wn

Juego para tomar estilo Picolo, hecho para la previa de la despedida de soltero de Exe. By Watacas.

## Modos

- **Individual:** cartas de retos rápidos, “toman los que…”, “yo nunca”, cultura chupística, virus, duelos, votaciones, castigos máximos (terminarse el vaso), brindis y especiales de Exe. Mazo de 55 cartas al azar por partida.
- **2 equipos:** se ingresan los jugadores (mínimo 4), se sortean dos equipos al azar (se les puede cambiar el nombre o volver a sortear) y hay retos de equipo con marcador. Al final, el equipo perdedor toma.

## Cómo jugar

1. Agregar a los jugadores y elegir el modo.
2. Tocar la pantalla para pasar de carta; “Atrás” vuelve a la anterior.
3. En modo equipos, en los retos y duelos se marca qué equipo ganó para sumar al marcador.

Los virus duran entre 5 y 10 cartas y luego aparece su carta de término.

## Estructura

- `index.html`: todo el juego en un solo archivo (cartas, estilos y lógica).
- `manifest.webmanifest`, `sw.js`, `icons/`: para instalarlo como app y jugar sin conexión.

Las cartas están en las constantes `CARDS`, `TEAM_CARDS`, `VIRUS` y `TEAM_VIRUS` dentro del script de `index.html`. `{A}` y `{B}` se reemplazan por jugadores al azar; `{T}` y `{O}` por los equipos.

Los nombres de los jugadores quedan guardados en el `localStorage` del teléfono.

## Publicar con GitHub Pages

Settings → Pages → Deploy from a branch → `main` / `(root)`.

Queda en `https://ecamus97.github.io/wn-chucha-wn/`.

## Instalar como app

- **iPhone (Safari):** botón Compartir → “Agregar a pantalla de inicio”.
- **Android (Chrome):** menú ⋮ → “Instalar app” o “Agregar a la pantalla principal”.

Al cambiar el juego, subir `VERSION` en `sw.js` para que los teléfonos que ya lo instalaron descarguen la versión nueva.
