# Shin Megami Tensei if... — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/playstation/shin-megami-tensei-if)**.

Traducción al **español de España** de *Shin Megami Tensei if...* (真・女神転生if..., PlayStation,
2002), la versión de PlayStation del RPG de Atlus en el que un instituto entero acaba arrastrado
al mundo demoníaco. Nunca salió de Japón.

La traducción se distribuye como **parche**. No incluye el juego: necesitas tu propia copia
japonesa para aplicarlo.

## Estado

Última versión: **[v1.0](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Guion de eventos y mazmorras | 4.292 mensajes traducidos |
| Negociación y sucesos con demonios | 6.058 textos traducidos |
| Demonios, razas, objetos y magias | Traducidos (glosario de 780 nombres) |
| Combate | Traducido |
| Menús, ayudas, avisos y tarjeta de memoria | Traducidos |
| Pantalla de nombre | Teclado en castellano con tildes y ñ |
| Vídeos de introducción y de los cuatro finales | Texto en castellano |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »** |
| Revisión durante una partida | Parcial (ver abajo) |

Detalles técnicos:

- Fuente proporcional nueva para diálogos, menús y combate, con el mismo color y sombra que
  la original.
- Los nombres del grupo se ven en el panel con una fuente redibujada.
- La narración de los vídeos se ha vuelto a componer en castellano, con el mismo ritmo que el
  original.

Se quedan como en el original:

- El logotipo y los rótulos gráficos en inglés que forman parte de la imagen del juego
  («NEW GAME», «COMP», «FIGHT», los encabezados de la pantalla de estado…).
- Los términos que el original escribe en inglés, como LAW, CHAOS o NEUTRAL.
- El himno del instituto que abre dos de los finales.

### Comprobaciones y trabajo pendiente

Se ha jugado en emulador desde una partida nueva por el instituto. Se han comprobado:

- La pantalla de título, la adivina Nova, el cuestionario y la pantalla de nombre.
- El prólogo, la llegada de Yumi y los diálogos del instituto (alumnos, enfermería, dirección).
- Los menús del campo (COMP, magia, objetos, equipo, estado y formación).
- Combates: órdenes, mensajes de ataque, daño, magia enemiga y huida.
- La muerte del protagonista y la escena de Caronte.
- El vídeo de introducción.

El parche se ha aplicado sobre el BIN japonés original y el resultado se ha comparado byte a
byte con la imagen probada.

**No se ha jugado una partida completa de principio a fin** ni se ha probado en consola real.
La negociación con demonios, las tiendas, la Catedral de las Sombras, las mazmorras y los
finales no se han recorrido dentro de una partida: sus textos se han revisado en los datos del
disco y los vídeos de los finales se han comprobado decodificándolos. La traducción y su
revisión se han hecho con asistencia de IA, sin revisores humanos independientes. Si
encuentras un error, abre una incidencia con una captura.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia de **Shin Megami Tensei if... (Japón)**, SLPM-87154, en formato BIN/CUE de
   una sola pista.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Shin Megami Tensei If... (Japan).bin` |
   | Tamaño | 256.417.392 bytes |
   | MD5 | `9f6348150071dc0a2aa9be07250c8806` |

   ```bash
   md5sum "Shin Megami Tensei If... (Japan).bin"                 # Linux
   md5 "Shin Megami Tensei If... (Japan).bin"                    # macOS
   CertUtil -hashfile "Shin Megami Tensei If... (Japan).bin" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Shin Megami Tensei If... (Japan).bin" parche.xdelta "Shin Megami Tensei if (ES).bin"`
5. Comprueba que el BIN resultante tiene el MD5 **`d99aa3c294d54bd39804094cb309b86c`** (v1.0).
6. Crea un CUE para el nuevo BIN, por ejemplo `Shin Megami Tensei if (ES).cue`:

   ```
   FILE "Shin Megami Tensei if (ES).bin" BINARY
     TRACK 01 MODE2/2352
       INDEX 01 00:00:00
   ```

7. Carga el CUE en tu emulador y empieza una partida nueva.

Aplica cada versión sobre el **BIN japonés original**, no sobre una copia ya traducida.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna con
Atlus ni Sega. Aquí no se distribuye el juego ni ninguna parte de él: solo un parche que
modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
