# Pruebas

| ID | Requisito | Orden o secuencia | Resultado esperado | Resultado obtenido | OK |
|---|---|---|---|---|---|
| P01 | R1 | `registrar @chasqui` (dos veces) | La segunda vez: `E: No se pudo registrar @chasqui` | `E: No se pudo registrar @chasqui` | OK |
| P02 | R1 | `registrar chasqui` (sin @) | `E: No se pudo registrar chasqui` | `E: No se pudo registrar chasqui` | OK |
| P03 | R2 | `arbol` y `usuarios` | Preorden de 10 nodos, altura 4, hojas 4 y lista en orden alfabético | `Nodos: 10 \| altura: 4 \| hojas: 4` y lista enorden | OK |
| P04 | R3 | `seguir @jazz @jazz` | `E: Una cuenta no puede seguirse a si misma` | `E: Una cuenta no puede seguirse a si misma` | OK |
| P05 | R3 | `seguidores @jazz` y `seguir @pixel @chasqui` (2 veces) | Punto de control `@haiku @misti` y rechazo de arista repetida | `Seguidores de @jazz (2): @haiku @misti` y `E: @pixel ya sigue a @chasqui` | OK |
| P06 | R4 | `mutuos @jazz` y `popular` | Mutuos de `@jazz` (1) y cuenta más seguida (`@misti`) | `Mutuos de @jazz (1): @misti` y `Popular: @misti \| seguidores: 4` | OK |
| P07 | R5 | `alcance @pixel` y `llega @mango @kayak` | Alcanzados desde `@pixel` y verificación de ruta `@mango -> @kayak` | `alcanzados: 7` y `Un post de @mango llega a @kayak: no` | OK |
| P08 | R6 | `guardar`, `cargar`, `reporte` | El mismo preorden, altura 5 y 17 seguimientos tras recargar `nido.txt` | `Cargado: 11 cuentas y 17 seguimientos \| altura 5` | OK |
| P09 | R7 | `hola`, `seguir`, `perfil @nadie`, `salir` | Mensajes de error sin caer y liberación de 11 nodos al salir | Errores controlados y `Nodos liberados: 11. Hasta pronto.` | OK |

Agreguen todas las que necesiten. Incluyan casos con datos invalidos.
