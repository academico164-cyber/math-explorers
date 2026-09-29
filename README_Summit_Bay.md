# Summit Bay — Math Explorers, Módulo 4 (README técnico)

Módulo interactivo bilingüe (CLIL) de matemáticas, dividido en 7 archivos HTML independientes: un índice y una página por estación. Todo funciona abierto directamente en el navegador, sin internet para el contenido principal y sin instalar nada.

## Archivos

| Archivo | Qué es | Tamaño aprox. |
|---|---|---|
| `summit-bay-index.html` | Página de entrada: mapa de Summit Bay con Milo y una tarjeta por estación | 0,15 MB |
| `operation-outpost.html` | Operaciones combinadas y problemas de palabras (+, −, ×, ÷) | 1,0 MB |
| `compass-cove.html` | Plano cartesiano y coordenadas | 1,0 MB |
| `twist-temple.html` | Transformaciones: trasladar, girar y reflejar figuras | 0,25 MB |
| `graph-meadow.html` | Lectura de gráficos de barras y pictogramas | 1,1 MB |
| `chance-falls.html` | Probabilidad: seguro, probable, poco probable, imposible | 0,26 MB |
| `code-cave.html` | Pensamiento computacional (referencia + Matific + juegos) | 0,24 MB |

Los archivos más pesados son los que incluyen páginas reales del Math Booklet incrustadas como imagen.

## Contenido por estación

| Estación | Retos | Videos | Juegos gratuitos | Páginas del Math Booklet | Taller |
|---|---|---|---|---|---|
| Operation Outpost | 10 | 3 | 3 | Págs. 20, 36 | Reinforcement Test (SharePoint) |
| Compass Cove | 8 | 3 | 3 | Págs. 74, 75, 76 | Workshop (SharePoint) |
| Twist Temple | 8 | 1 | — | No existe en la cartilla (se usan ejemplos originales) | Workshop (SharePoint) |
| Graph Meadow | 5 | 3 | 3 | Págs. 80, 81, 82 | Workshop (SharePoint) |
| Chance Falls | 8 | 3 | 3 | No existe en la cartilla (se usan ejemplos originales) | Workshop (SharePoint) |
| Code Cave | — (referencia) | — | 3 (nuevos) | No existe en la cartilla | — (usa Matific) |

Estructura de cada estación: Learning Outcome → Concept block (What is it? + Parts of…) → Strategies → ejemplo de metodología activa (CSS/SVG) → videos → juegos → Math Booklet → Practice (portada + Matific) → retos con retroalimentación inmediata, pista y barra de progreso → celebración con confeti.

## Navegación y links editables

Todos los links internos están marcados en el código con un comentario `<!-- 🔗 LINK ... -->` justo encima. Para cambiarlos, abre el archivo en un editor de texto (Bloc de notas, VS Code), busca `🔗 LINK` y reemplaza el valor de `href="..."`.

| Dónde | Link por defecto | Cuándo cambiarlo |
|---|---|---|
| Índice → botón "← Atlas" | `Math_Explorers_Atlas.html` | Si el Atlas queda en SharePoint/AVA |
| Índice → cada tarjeta de estación | `operation-outpost.html`, etc. | Si cada estación se sube por separado |
| Cada estación → "← Summit Bay" y "Back to Summit Bay" | `summit-bay-index.html` | Si el índice queda en SharePoint/AVA |

Con los links por defecto, todo funciona si los 7 archivos están en la misma carpeta (por ejemplo, descargados juntos en un .zip).

## Estándar de seguridad (verificado)

Verificado con navegador real (Chromium/Playwright) el 29 sept. 2026: 0 errores de JavaScript y 0 conexiones de red al abrir cualquiera de los 7 archivos.

- Sin `fetch`, `XMLHttpRequest`, formularios, analítica ni tracking.
- Fuentes tipográficas incrustadas en base64 (sin Google Fonts ni CDN).
- Imágenes incrustadas en el propio archivo; sonidos generados con Web Audio (sin archivos externos).
- Links externos solo de salida y voluntarios (YouTube, juegos, SharePoint, Matific), con `target="_blank" rel="noopener"`.
- No guarda datos: el progreso se reinicia al cerrar la página.

## Cambios frente al `module4.html` original

- Separado en índice + 6 estaciones; el menú interno se reemplazó por links reales.
- Botón "← Atlas" agregado al índice (antes no existía).
- Botón "Play again 🔁" en la celebración de cada estación con retos.
- Tarjeta "🎮 Free games" nueva en Code Cave: Code.org Classic Maze, Blockly Games Maze y Blockly Games Puzzle.
- Las estrellas de progreso del mapa se retiraron: al estar en archivos separados, el índice no puede saber qué estación se completó.

## Pendientes conocidos

- Twist Temple tiene 1 solo video y no tiene tarjeta de juegos gratuitos en este archivo.
- Operation Outpost y Code Cave no tienen tarjeta de taller propia en el mismo formato que las demás (Operation Outpost usa un Reinforcement Test).
- Si se edita el contenido de una estación, hay que volver a subir solo ese archivo; los demás no cambian.
