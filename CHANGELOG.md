# Changelog / Cambios

## 0.4.0-alpha

**English**

New:

- NPCs in the packs: characters the player can talk to, made like the
  packs' enemies (`npcs/<name>/npc.txt` and a picture) and placed with
  their letter in the maps. They are harmless. The player talks to them
  with Triangle (a △ appears over them), or they talk when touched (for
  signs). The ones that stand still look at the player.
- Dialogs: what the NPCs say goes in one file per language
  (`dialog_en.txt`, `dialog_es.txt`...), with conversations of several
  lines, the name of who speaks, and answers to choose that lead to other
  parts. A pack can change the dialog box with `textures/dialog.png`.
  `MODDING.txt` explains it with examples. Format 3.
- Two sample packs come with the game, off at first: *Sample: The village*
  (characters and dialogs, 3 levels) and *Sample: Monster gallery* (9 new
  enemies and a boss, 4 levels). Each one changes every picture and sound
  of the game and is played with its own levels. They are made with AI,
  only to show what packs can do: they are not part of the original game.
- `own_levels = yes` in a pack's `pack.txt`: only the packs' levels are
  played, not the game's.
- `MODDING.txt` explains how to make the animations of the enemies and
  NPCs, and how big a pack's enemy must be for the player's bullets to
  hit it (1.5 squares on the ground).
- Up to 24 enemies and NPCs among the active packs (before, 16 enemies).
- △ on the TEXTURE PACKS screen also checks the NPCs and the dialog
  files: a folder without `npc.txt`, a missing conversation, a line it
  doesn't understand, an answer to a section that isn't there, an NPC
  with an enemy's name, and `own_levels` without a `level1.txt`.
- Options for the objects of a level: a flag can hide until the shooting
  enemies are defeated (`hide`), and a shooting enemy (or a pack's enemy
  that shoots) can be told not to shoot (`no_shoot`). They go after the
  object's numbers, e.g. `flag 529 209 2 2 hide`. Packs that use them say
  `format = 3`.
- By default a flag no longer hides: in the packs' levels with shooting,
  the flag is there from the start unless it has `hide`. The original
  level 6 keeps its flag hidden until both shooting enemies are defeated,
  as always, and so do the packs made for 0.3.0 (format 1 or 2).
- A pack's enemy that shoots `around` can say how many bullets each shot
  has: `bullets = 12` (2 to 16, evenly spread; 8 without it, as before).
  Format 3.
- A pack can say what it is in its `pack.txt`: `type = mod` makes it a
  mod, which can only be turned on or off from the main menu (not from
  the pause), even if it only has pictures. `type = textures`, or no
  line, works as before.

Fixed bugs:

- A pack's level named with a 0 in front (`level07.txt`) was shown as
  fine on the TEXTURE PACKS screen, but the game never loaded it. Now △
  says it must be called `level7.txt`.

**Español**

Novedades:

- NPC en los paquetes: personajes con los que el jugador puede hablar,
  hechos como los enemigos de los paquetes (`npcs/<nombre>/npc.txt` y un
  dibujo) y puestos con su letra en los mapas. Son inofensivos. Se les
  habla con Triángulo (les sale un △ encima), o hablan al tocarlos (para
  carteles). Los que están quietos miran al jugador.
- Diálogos: lo que dicen los NPC va en un archivo por idioma
  (`dialog_en.txt`, `dialog_es.txt`...), con conversaciones de varias
  frases, el nombre de quien habla y respuestas para elegir que llevan a
  otras partes. Un paquete puede cambiar el cuadro de diálogo con
  `textures/dialog.png`. `MODDING.txt` lo explica con ejemplos.
  Formato 3.
- Con el juego vienen dos paquetes de ejemplo, desactivados al principio:
  *Ejemplo: El pueblo* (personajes y diálogos, 3 niveles) y *Ejemplo:
  Galería de monstruos* (9 enemigos nuevos y un jefe, 4 niveles). Cada uno
  cambia todos los dibujos y sonidos del juego y se juega con sus propios
  niveles. Están hechos con IA, solo para enseñar lo que pueden hacer los
  paquetes: no son parte del juego original.
- `own_levels = yes` en el `pack.txt` de un paquete: solo se juegan los
  niveles de los paquetes, no los del juego.
- `MODDING.txt` explica cómo hacer las animaciones de los enemigos y los
  NPC, y lo grande que tiene que ser un enemigo de un paquete para que le
  den las balas del jugador (1,5 casillas en el suelo).
- Hasta 24 enemigos y NPC entre los paquetes activos (antes, 16
  enemigos).
- △ en la pantalla PAQUETES DE TEXTURAS también revisa los NPC y los
  archivos de diálogos: una carpeta sin `npc.txt`, una conversación que
  falta, una línea que no se entiende, una respuesta a una sección que no
  está, un NPC con el nombre de un enemigo, y `own_levels` sin un
  `level1.txt`.
- Opciones para los objetos de un nivel: una bandera puede esconderse
  hasta eliminar a los enemigos que disparan (`hide`), y a un enemigo que
  dispara (o a uno del paquete que dispara) se le puede decir que no
  dispare (`no_shoot`). Van después de los números del objeto, por
  ejemplo `flag 529 209 2 2 hide`. Los paquetes que las usan dicen
  `format = 3`.
- Por defecto la bandera ya no se esconde: en los niveles con disparo de
  los paquetes, la bandera está desde el principio si no tiene `hide`. El
  nivel 6 original sigue escondiendo su bandera hasta eliminar a los dos
  enemigos que disparan, como siempre, y también los paquetes hechos
  para la 0.3.0 (formato 1 o 2).
- Un enemigo de un paquete que dispara `around` (alrededor) puede decir
  cuántas balas tiene cada disparo: `bullets = 12` o `balas = 12` (de 2 a
  16, repartidas por igual; sin ponerlo, 8, como antes). Formato 3.
- Un paquete puede decir qué es en su `pack.txt`: `type = mod` (o
  `tipo = mod`) lo hace un mod, que solo se activa o desactiva desde el
  menú principal (no desde la pausa), aunque solo tenga dibujos.
  `type = textures`, o sin la línea, funciona como antes.

Bugs solucionados:

- Un nivel de un paquete con un 0 delante en el nombre (`level07.txt`)
  salía bien en la pantalla PAQUETES DE TEXTURAS, pero el juego nunca lo
  cargaba. Ahora △ avisa de que se tiene que llamar `level7.txt`.

## 0.3.0-alpha

**English**

New:

- Levels drawn as a map: in a pack's level file, after a `map:` line, the
  level is drawn with letters, one per square (20 x 15): `#` walls, `P`
  player, `F` flag, `E` enemy, `S` shooting enemy, `W` wheel, `.` empty.
  No more coordinates; the old way still works, even in the same file.
  `MODDING.txt` explains it with an example, and △ warns about unknown
  letters and maps that are too big.
- Ground, platforms and walls: four pictures instead of one, and in
  tiles (repeated square by square, no longer stretched). The game tells
  them apart: the lowest layer of the level is the ground (`floor.png`,
  with `floor_top.png` on its top row, like grass over dirt), the
  floating blocks are platforms (`platform.png`) and the blocks taller
  than wide are walls (`wall.png`). A pack without the new pictures uses
  its `wall.png`, as before. Each one is one square (HD: 48x37). For now
  the four are the original wall picture; packs can draw them different.
- New enemies in packs, built from pieces: `enemies/<name>/enemy.txt` and
  its picture (with animation frames). Ways to move (still, walk, patrol,
  fly, follow, jump, charge, drop), to shoot (forward, at the player,
  around), life, damage, size, stomp, splitting into others when it dies,
  keeping the exit closed, and up to 3 phases that change all that (for
  bosses). Each one has a letter for the maps. △ warns about every
  mistake with its line, and says how many enemies a pack has.
- The `original` pack is now only the template to copy: it can't be
  turned on (it has the game's own files).
- From the pause menu, packs that change how the game plays (levels,
  enemies or rules) can't be changed, only from the main menu; packs that
  only change pictures, sounds or phrases still can. Levels and rules
  left as in the template don't count as changes.
- Pack format 2: a pack with enemies or levels drawn as a map says
  `format = 2` in its `pack.txt` (△ reminds it), so older versions of the
  game don't load it wrong. `MODDING.txt` explains everything new, with
  examples and tips to design levels.
- In the menus, holding Up or Down keeps moving, like in the PSP menu
  (after a moment, one step every 0.1 seconds).

Optimizations:

- The checks of the TEXTURE PACKS screen are about 10 times faster on a
  PSP-1000: with 5 packs, under 5 seconds (it was about 48).
- Nothing off the screen is drawn.
- The game sorts the ground, platforms and walls of a level once, not in
  every frame.

Fixed bugs:

- On a busy TEXTURE PACKS screen (a slow PSP, big packs) the checks of
  the packs could stay on "Checking..." for ever.

**Español**

Novedades:

- Niveles dibujados como un mapa: en un archivo de nivel de un paquete,
  después de una línea `map:`, el nivel se dibuja con letras, una por
  casilla (20 x 15): `#` paredes, `P` jugador, `F` bandera, `E` enemigo,
  `S` enemigo que dispara, `W` rueda, `.` vacío. Ya no hacen falta
  coordenadas; la forma de antes sigue funcionando, incluso en el mismo
  archivo. `MODDING.txt` lo explica con un ejemplo, y △ avisa de letras
  desconocidas y de mapas demasiado grandes.
- Suelo, plataformas y paredes: cuatro dibujos en vez de uno, y en
  mosaico (repetidos casilla a casilla, ya no se estiran). El juego los
  distingue: la capa más baja del nivel es el suelo (`floor.png`, con
  `floor_top.png` en su fila de arriba, como hierba sobre tierra), los
  bloques que flotan son plataformas (`platform.png`) y los bloques más
  altos que anchos son paredes (`wall.png`). Un paquete sin los dibujos
  nuevos usa su `wall.png`, como antes. Cada uno es una casilla (HD:
  48x37). De momento los cuatro son el dibujo de pared original; los
  paquetes pueden dibujarlos distintos.
- Enemigos nuevos en los paquetes, montados con piezas:
  `enemies/<nombre>/enemy.txt` y su dibujo (con fotogramas de animación).
  Formas de moverse (quieto, andar, patrullar, volar, seguir, saltar,
  embestir, caer desde el techo), de disparar (hacia delante, al jugador,
  alrededor), vida, daño, tamaño, pisotón, dividirse en otros al morir,
  cerrar la salida, y hasta 3 fases que cambian todo eso (para jefes).
  Cada uno tiene una letra para los mapas. △ avisa de cada error con su
  línea, y dice cuántos enemigos tiene un paquete.
- El paquete `original` ahora es solo la plantilla para copiar: no se
  puede activar (tiene los archivos del propio juego).
- Desde el menú de pausa no se pueden cambiar los paquetes que cambian
  cómo se juega (niveles, enemigos o reglas), solo desde el menú
  principal; los que solo cambian dibujos, sonidos o frases, sí. Los
  niveles y reglas que se dejan como en la plantilla no cuentan como
  cambios.
- Formato 2 de los paquetes: un paquete con enemigos o con niveles
  dibujados con mapa dice `format = 2` en su `pack.txt` (△ lo recuerda),
  para que las versiones antiguas del juego no lo carguen mal.
  `MODDING.txt` explica todo lo nuevo, con ejemplos y consejos para
  diseñar niveles.
- En los menús, mantener arriba o abajo sigue moviendo, como en el menú
  de la PSP (tras un momento, un paso cada 0,1 segundos).

Optimizaciones:

- La comprobación de la pantalla de PAQUETES DE TEXTURAS es unas 10 veces
  más rápida en una PSP-1000: con 5 paquetes, menos de 5 segundos (antes
  unos 48).
- No se dibuja lo que queda fuera de la pantalla.
- El juego clasifica el suelo, las plataformas y las paredes de un nivel
  una vez, no en cada imagen.

Bugs solucionados:

- Con la pantalla de PAQUETES DE TEXTURAS muy ocupada (una PSP lenta,
  paquetes grandes) la comprobación de los paquetes podía quedarse en
  "Comprobando..." para siempre.

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

New:

- `MODDING.txt`: clearer first step to make a pack (copy the `original`
  folder inside `resourcepacks`, not the `resourcepacks` folder).

Fixed bugs:

- Touching a shooting enemy now kills, like the walking enemies (before,
  the player went through it).

**Español**

Novedades:

- `MODDING.txt`: el primer paso para crear un paquete está más claro
  (copiar la carpeta `original` dentro de `resourcepacks`, no la carpeta
  `resourcepacks`).

Bugs solucionados:

- Tocar a un enemigo que dispara ahora mata, como los enemigos que andan
  (antes el jugador lo atravesaba).

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
