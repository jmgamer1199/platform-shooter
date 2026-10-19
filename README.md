# platform-shooter for PSP

**English** | [Español](#español)

Native PlayStation Portable port of **platform-shooter**, a platform game
by **jmgamer1199**, first made with GameMaker in 2017. Written in C for the
PSP, it does not emulate anything. It works on the **PSP-1000, PSP-2000
and PSP-3000** and on the PPSSPP emulator, at 60 FPS.

> **Bugs and ideas.** If you find a bug or a problem, or you have an idea
> for the game, write it in [Issues](../../issues) > *New issue*, and
> choose **Bug** (the title starts with [bug]), **Idea** ([idea]) or
> **Other** ([other]). The form asks for what is needed, like your PSP
> model (or emulator) and the version of the game.

> **Alpha version.** The icon and background shown in the PSP menu and the
> button symbols are provisional. This repository only has the files to
> play (no source code).

> **Homebrew.** platform-shooter is unofficial homebrew: a free game, not
> made, licensed or endorsed by Sony. PlayStation and PSP are trademarks of
> Sony Interactive Entertainment. On a real PSP it needs custom firmware
> (CFW).

## Download

Go to [Releases](../../releases) and download `platform-shooter-<version>.zip`.

## Install

**PPSSPP emulator** (free, Windows, Android, Mac, Linux, iOS):
[ppsspp.org/download](https://www.ppsspp.org/download/)

1. Unzip the file. You get a folder named `platform-shooter`.
2. In PPSSPP, open the Memory Stick folder (Windows: *File > Open Memory
   Stick*; other systems: *Settings > System*).
3. Copy the whole `platform-shooter` folder into `PSP/GAME/` (create it if
   it is not there). It must end up as `PSP/GAME/platform-shooter/EBOOT.PBP`.
4. Open PPSSPP: the game is in the *Games* tab (or *Homebrew & Demos*).

**Real PSP** (PSP-1000, 2000 or 3000 with custom firmware): copy the
`platform-shooter` folder to `PSP/GAME/` on the Memory Stick and open it
from *Game > Memory Stick*.

## Controls

| Button | In the game | In the menus |
|---|---|---|
| D-pad / stick | move | choose (hold to keep moving) |
| X | jump | accept |
| R | shoot (from level 6, hold for 3 shots per second) | lower a pack's priority |
| L | | raise a pack's priority |
| Triangle | | details and warnings of a pack |
| O | | back |
| Start | pause | |
| Select | debug mode (FPS, memory, collision boxes) | debug mode |

## What's in it

- The 5 original levels and a new level 6 with enemies that shoot.
- English and Spanish (more languages can be added as text files).
- **Resource packs**, like Minecraft's: change any picture (PNG) or sound
  (WAV) of the game, change the levels or add new ones (simple text files),
  several packs at once with priorities. Packs use the same format on every
  port of the game, and the game tells you what is wrong in a pack.
- In the packs, **levels drawn as a map** with letters (no coordinates),
  **new enemies** built from pieces (how they move, shoot, split, phases
  for bosses...) and separate pictures for the ground, the platforms and
  the walls. The game itself doesn't come with new levels or enemies:
  these are for the packs.
- **Rules** in the packs: change the life, the jump, the gravity, the
  speeds and the fire rate to make an easy mode, a moon mode...
- Language and packs are remembered.

How to make packs, levels and rules, add languages or change the font:
`MODDING.txt` inside the game folder.

## The original game and what was made with AI

**From the original game**, made by jmgamer1199 in 2017 with GameMaker:
all the pictures (the player, the enemies, the wheel, the flag, the walls,
the bullets and the backgrounds, including the drawings of the player
shooting, which the original didn't use), the sounds, levels 1 to 5, and
how the game plays: movement, jumps, enemies, collisions and menus. The
ground and the platforms use, for now, the original wall picture.

**Made with AI for the PSP port**, directed by jmgamer1199:
- all the code of the port: the game rewritten in C for the PSP from the
  original GameMaker code, plus its tools and tests;
- level 6 and the shooting;
- the texture packs, the levels in files and drawn as maps, the enemies
  of the packs (built from pieces), the rules and the warnings;
- the languages and their texts (menus, tutorials and title screen
  phrases), the debug mode and the 60 FPS drawing;
- the provisional pictures: the icon and background of the PSP menu, the
  button symbols, the icon of the template pack and the new buttons drawn
  on the menus (the gear and TEXTURE PACKS). The menu backgrounds are the
  original ones, with their painted text removed;
- these documents.

**From others**: the Lilita One font (Juan Montoreano, SIL Open Font
License) and the free software in `THIRD_PARTY_LICENSES.txt`.

## License

platform-shooter © 2017-2026 jmgamer1199, licensed under
[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) (see
`LICENSE`): you can play it, share it and change it (packs, levels,
translations...), as long as you give credit to jmgamer1199 and say what
you changed, and you can't sell it or use it for commercial purposes.

The third party software and the font keep their own licenses:
`THIRD_PARTY_LICENSES.txt` and `font/LICENSE.txt` inside the game folder.

---

## Español

Port nativo para PlayStation Portable de **platform-shooter**, un juego de
plataformas de **jmgamer1199**, hecho originalmente con GameMaker en 2017.
Está escrito en C para la PSP y no emula nada. Funciona en **PSP-1000,
PSP-2000 y PSP-3000** y en el emulador PPSSPP, a 60 FPS.

> **Fallos e ideas.** Si encuentras un fallo o un problema, o tienes una
> idea para el juego, escríbelo en [Issues](../../issues) > *New issue*, y
> elige **Bug** (el título empieza por [bug]), **Idea** ([idea]) u
> **Other** ([other]). El formulario pide lo necesario, como tu modelo de
> PSP (o emulador) y la versión del juego.

> **Versión alfa.** El icono y el fondo del menú de la PSP y los símbolos
> de los botones son provisionales. Este repositorio solo tiene los
> archivos para jugar (no el código fuente).

> **Homebrew.** platform-shooter es homebrew no oficial: un juego gratuito,
> que no está hecho, licenciado ni respaldado por Sony. PlayStation y PSP
> son marcas de Sony Interactive Entertainment. En una PSP real necesita
> firmware personalizado (CFW).

### Descargar

Entra en [Releases](../../releases) y descarga `platform-shooter-<versión>.zip`.

### Instalar

**Emulador PPSSPP** (gratis, Windows, Android, Mac, Linux, iOS):
[ppsspp.org/download](https://www.ppsspp.org/download/)

1. Descomprime el archivo. Sale una carpeta llamada `platform-shooter`.
2. En PPSSPP, abre la carpeta de la Memory Stick (Windows: *Archivo > Abrir
   Memory Stick*; otros sistemas: *Ajustes > Sistema*).
3. Copia la carpeta `platform-shooter` entera dentro de `PSP/GAME/` (créala
   si no existe). Debe quedar `PSP/GAME/platform-shooter/EBOOT.PBP`.
4. Abre PPSSPP: el juego está en la pestaña *Juegos* (o *Homebrew y demos*).

**PSP real** (PSP-1000, 2000 o 3000 con firmware personalizado): copia la
carpeta `platform-shooter` en `PSP/GAME/` de la Memory Stick y ábrelo desde
*Juego > Memory Stick*.

### Controles

| Botón | En el juego | En los menús |
|---|---|---|
| Cruceta / stick | moverse | elegir (mantén para seguir moviendo) |
| X | saltar | aceptar |
| R | disparar (desde el nivel 6; mantenlo para 3 disparos por segundo) | bajar la prioridad de un paquete |
| L | | subir la prioridad de un paquete |
| Triángulo | | detalles y avisos de un paquete |
| O | | atrás |
| Start | pausa | |
| Select | modo debug (FPS, memoria, cajas de colisión) | modo debug |

### Qué trae

- Los 5 niveles originales y un nivel 6 nuevo con enemigos que disparan.
- Inglés y español (se pueden añadir más idiomas con archivos de texto).
- **Paquetes de recursos**, como los de Minecraft: cambia cualquier dibujo
  (PNG) o sonido (WAV) del juego, cambia los niveles o añade otros nuevos
  (archivos de texto sencillos), varios paquetes a la vez con prioridades.
  Los paquetes usan el mismo formato en todos los ports del juego, y el
  juego te dice qué tiene mal un paquete.
- En los paquetes, **niveles dibujados como un mapa** con letras (sin
  coordenadas), **enemigos nuevos** montados con piezas (cómo se mueven,
  disparan, se dividen, fases para jefes...) y dibujos distintos para el
  suelo, las plataformas y las paredes. El juego en sí no trae niveles ni
  enemigos nuevos: son para los paquetes.
- **Reglas** en los paquetes: cambia la vida, el salto, la gravedad, las
  velocidades y la cadencia de disparo para hacer un modo fácil, un modo
  luna...
- El idioma y los paquetes se recuerdan.

Cómo hacer paquetes, niveles y reglas, añadir idiomas o cambiar la fuente:
`MODDING.txt` en la carpeta del juego.

### El juego original y lo que se ha hecho con IA

**Del juego original**, hecho por jmgamer1199 en 2017 con GameMaker: todos
los dibujos (el jugador, los enemigos, la rueda, la bandera, las paredes,
las balas y los fondos, también los del jugador disparando, que el
original no usaba), los sonidos, los niveles 1 a 5, y cómo se juega:
movimiento, saltos, enemigos, colisiones y menús. El suelo y las
plataformas usan, de momento, el dibujo de pared original.

**Hecho con IA para el port de PSP**, bajo la dirección de jmgamer1199:
- todo el código del port: el juego reescrito en C para la PSP a partir
  del código original de GameMaker, y sus herramientas y pruebas;
- el nivel 6 y el disparo;
- los paquetes de texturas, los niveles en archivos y dibujados como
  mapa, los enemigos de los paquetes (montados con piezas), las reglas y
  los avisos;
- los idiomas y sus textos (menús, tutoriales y frases de la pantalla de
  inicio), el modo debug y el dibujado a 60 FPS;
- los dibujos provisionales: el icono y el fondo del menú de la PSP, los
  símbolos de los botones, el icono del paquete plantilla y los botones
  nuevos dibujados en los menús (el engranaje y PAQUETES DE TEXTURAS). Los
  fondos de los menús son los originales, con su texto pintado borrado;
- estos documentos.

**De otros**: la fuente Lilita One (Juan Montoreano, SIL Open Font
License) y el software libre de `THIRD_PARTY_LICENSES.txt`.

### Licencia

platform-shooter © 2017-2026 jmgamer1199, con licencia
[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.es) (ver
`LICENSE`): puedes jugarlo, compartirlo y cambiarlo (paquetes, niveles,
traducciones...), siempre que digas que es de jmgamer1199 y qué cambiaste,
y no puedes venderlo ni usarlo con fines comerciales.

El software de terceros y la fuente mantienen sus propias licencias:
`THIRD_PARTY_LICENSES.txt` y `font/LICENSE.txt` dentro de la carpeta del
juego.
