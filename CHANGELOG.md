# Changelog / Cambios

## 0.2.0-alpha

**English**

- Pack info: `pack.txt` can say the author of the pack (`author`), its
  version (`version`, raise it with each update) and the version of the
  game it was made with (`game_version`). OPTIONS > TEXTURE PACKS shows
  the version next to the name, and △ shows all three.
- Splashes like Minecraft's: the title screen phrases are now the same in
  every language, in `splashes.txt` of the `original` pack (one phrase per
  line). A pack can change them with its own `splashes.txt`; △ shows how
  many phrases it has. The language files no longer have phrases.
- Faster TEXTURE PACKS screen: it shows at once and checks the packs in
  the background ("Checking..." until each one is done), opening each
  file once at most (half the files of before), and it remembers the
  checks until the game is restarted. Before, it could take about 13
  seconds on a PSP-3000 with 3 packs.
- Up to 8 packs can be on at once; turning on one more says so.
- Up to 16 packs are listed (it was 32). With more, the game keeps the
  active ones and `original`, then the rest by name, and says how many
  are left out (before, which ones were left out was random).
- Tested on a PSP-1000.

**Español**

- Datos de los paquetes: `pack.txt` puede decir el autor del paquete
  (`author`), su versión (`version`, súbela con cada actualización) y la
  versión del juego con la que se hizo (`game_version`). OPCIONES >
  PAQUETES DE TEXTURAS muestra la versión junto al nombre, y △ muestra las
  tres.
- Frases como las de Minecraft: las frases de la pantalla de inicio ahora
  son las mismas en todos los idiomas, en el `splashes.txt` del paquete
  `original` (una frase por línea). Un paquete puede cambiarlas con su
  propio `splashes.txt`; △ muestra cuántas frases tiene. Los archivos de
  idioma ya no tienen frases.
- Pantalla de PAQUETES DE TEXTURAS más rápida: sale al momento y revisa
  los paquetes en segundo plano ("Comprobando..." hasta que acaba cada
  uno), abriendo cada archivo una vez como mucho (la mitad de archivos que
  antes), y recuerda las revisiones hasta que se reinicia el juego. Antes
  podía tardar unos 13 segundos en una PSP-3000 con 3 paquetes.
- Puede haber hasta 8 paquetes activados a la vez; al activar uno más, lo
  avisa.
- Se muestran hasta 16 paquetes (antes 32). Si hay más, el juego se queda
  con los activos y con `original`, luego con el resto por nombre, y dice
  cuántos quedan fuera (antes, cuáles se quedaban fuera era al azar).
- Probado en una PSP-1000.

## 0.1.1-alpha

**English**

- Fixed: touching a shooting enemy now kills, like the walking enemies
  (before, the player went through it).
- `MODDING.txt`: clearer first step to make a pack (copy the `original`
  folder inside `resourcepacks`, not the `resourcepacks` folder).

**Español**

- Arreglado: tocar a un enemigo que dispara ahora mata, como los enemigos
  que andan (antes el jugador lo atravesaba).
- `MODDING.txt`: el primer paso para crear un paquete está más claro
  (copiar la carpeta `original` dentro de `resourcepacks`, no la carpeta
  `resourcepacks`).

## 0.1.0-alpha

**English**

First public version of the native PSP port of platform-shooter, by
jmgamer1199.

- The 5 levels of the original game, with the same physics and collisions.
- 60 FPS: the game runs 30 steps per second like the original and draws a
  smooth frame between each two.
- New level 6: two enemies that shoot. From this level on, R shoots.
- Pause menu with a gear button for the options.
- English and Spanish; languages are text files (`languages/`), and the
  title screen phrases (splash) too.
- Resource packs (`resourcepacks/`): pictures (PNG, HD up to twice the
  screen size) and sounds (WAV). Several at once, with priorities. Shared
  format for all future ports (`format = 1`), with optional per-console
  folders (`textures_psp/`, `sounds_psp/`, `levels_psp/`).
- Language and packs are saved in `config.txt`.
- Pack warnings: a pack with files the game can't use shows WARNINGS, and
  Triangle lists each file with what is wrong in it.
- PSP button symbols (△ ○ □ ✕) in the texts, with their own pictures
  (`button_*.png`, provisional ones for now).
- Levels in packs: `levels/levelN.txt` text files replace levels or add
  new ones after the 6th, with their own background, texts and shooting.
  The template pack has the 6 original levels in this format.
- Rules in packs: `rules.txt` changes the life, jump, gravity, speeds,
  enemy life and fire rate, within safe limits. The packs list marks the
  packs that change the rules.
- `MODDING.txt`: the guide to make packs, levels, rules, languages and
  fonts.
- Debug mode with Select: FPS, frame time, memory, room, player data and
  collision boxes.
- The version is shown in the PSP menu (in the title and in Information).
- Works on PSP-1000, PSP-2000 and PSP-3000 with custom firmware (tested
  on a PSP-1000 and a PSP-3000), and on PPSSPP (CPU at 333 MHz, about
  13 MB of memory at most with a large pack).
- Licensed under CC BY-NC 4.0.

Known: the icon and background in the PSP menu and the button symbols are
provisional.

**Español**

Primera versión pública del port nativo para PSP de platform-shooter, de
jmgamer1199.

- Los 5 niveles del juego original, con la misma física y colisiones.
- 60 FPS: el juego da 30 pasos por segundo como el original y dibuja un
  frame suave entre cada dos.
- Nivel 6 nuevo: dos enemigos que disparan. Desde este nivel, R dispara.
- Menú de pausa con un engranaje para las opciones.
- Inglés y español; los idiomas son archivos de texto (`languages/`), y las
  frases de la pantalla de inicio (splash) también.
- Paquetes de recursos (`resourcepacks/`): dibujos (PNG, HD hasta el doble
  del tamaño en pantalla) y sonidos (WAV). Varios a la vez, con
  prioridades. Formato común para todos los futuros ports (`format = 1`),
  con carpetas opcionales por consola (`textures_psp/`, `sounds_psp/`,
  `levels_psp/`).
- El idioma y los paquetes se guardan en `config.txt`.
- Avisos de los paquetes: un paquete con archivos que el juego no puede
  usar muestra AVISOS, y Triángulo lista cada archivo con lo que tiene mal.
- Símbolos de los botones de la PSP (△ ○ □ ✕) en los textos, con sus
  propios dibujos (`button_*.png`, de momento provisionales).
- Niveles en los paquetes: archivos de texto `levels/levelN.txt` cambian
  niveles o añaden otros después del 6, con su fondo, textos y disparo. La
  plantilla trae los 6 niveles originales en este formato.
- Reglas en los paquetes: `rules.txt` cambia la vida, el salto, la
  gravedad, las velocidades, la vida de los enemigos y la cadencia, dentro
  de unos límites seguros. La lista de paquetes marca los que cambian las
  reglas.
- `MODDING.txt`: la guía para hacer paquetes, niveles, reglas, idiomas y
  fuentes.
- Modo debug con Select: FPS, tiempo por frame, memoria, sala, datos del
  jugador y cajas de colisión.
- La versión sale en el menú de la PSP (en el título y en Información).
- Funciona en PSP-1000, PSP-2000 y PSP-3000 con firmware personalizado
  (probado en una PSP-1000 y una PSP-3000), y en PPSSPP (CPU a 333 MHz,
  unos 13 MB de memoria como máximo con un paquete grande).
- Licencia CC BY-NC 4.0.

Pendiente: el icono y el fondo del menú de la PSP y los símbolos de los
botones son provisionales.
