# Wn Chucha Wn

Juego para tomar estilo Picolo, hecho para la previa de la despedida de soltero de Exe. By Watacas.

## Modos

- **Individual:** 52 cartas al azar (retos, “toman los que…”, “yo nunca”, cultura chupística, duelos, votaciones, over/under, ¡a buscar!, castigos máximos y especiales de Exe), más los brindis, 5 virus y una bomba.
- **2 equipos:** cartas propias, distintas a las del modo individual: retos con marcador (cultura por equipos, flip the cup, beer pong, pirámide del ciego, Wordle, over/under, trivias…), cartas de equipo, brindis, virus de equipos y una bomba. Al final, el equipo perdedor toma.

## Cómo jugar

1. Agregar a los jugadores y elegir el modo.
2. Tocar la pantalla para pasar de carta; “Atrás” vuelve a la anterior.
3. En las trivias y over/under con respuesta, el primer toque muestra la respuesta y el segundo pasa de carta.
4. En modo equipos, en los retos se marca qué equipo ganó para sumar al marcador.

Los virus terminan entre 3 y 14 cartas después de aparecer. En la bomba, el jugador que sale pone una alarma secreta en su celular; cuando suena, el que aparezca en la carta en pantalla se toma el vaso.

## Estructura

- `index.html`: todo el juego en un solo archivo (cartas, estilos y lógica).
- `manifest.webmanifest`, `sw.js`, `icons/`: para instalarlo como app y jugar sin conexión.

Las cartas están en las constantes `CARDS` (individual), `TEAM_CARDS` (equipos), `SHARED` (ambos), `VIRUS` y `TEAM_VIRUS` dentro del script de `index.html`. `{A}` y `{B}` se reemplazan por jugadores al azar; `{T}` y `{O}` por los equipos.

Los nombres de los jugadores quedan guardados en el `localStorage` del teléfono.

## Publicar con GitHub Pages

Settings → Pages → Deploy from a branch → `main` / `(root)`.

Queda en `https://ecamus97.github.io/wn-chucha-wn/`.

## Instalar como app

- **iPhone (Safari):** botón Compartir → “Agregar a pantalla de inicio”.
- **Android (Chrome):** menú ⋮ → “Instalar app” o “Agregar a la pantalla principal”.

Al cambiar el juego, subir `VERSION` en `sw.js` para que los teléfonos que ya lo instalaron descarguen la versión nueva.
