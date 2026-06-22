# Recycling Game 3D

Juego en 3D sobre clasificación de residuos hecho en Godot 4.6. Lo desarrollamos
para el curso de Gráficos por Computadora de la Universidad Nacional.

La idea es sencilla: estás en un hangar rodeado de islas flotantes, la basura aparece
repartida por todo el escenario y hay que ir recogiéndola y echándola en el basurero
que le corresponde antes de que se acabe el tiempo.

## Cómo se juega

Recorrés el mapa, recogés la basura que vas encontrando y la depositás en el basurero
correcto. Cada vez que te equivocás de basurero perdés una vida; con tres errores se
acaba la partida. También hay un cronómetro, así que tampoco podés tardarte demasiado.
Para ganar hay que clasificar toda la basura antes de que el tiempo llegue a cero.

Mientras jugás van saliendo diálogos con voces que te dicen si lo estás haciendo bien
o mal, que fue de las cosas que más nos gustó meterle.

## Controles

- Moverse: W A S D o las flechas
- Correr: Shift
- Saltar: Espacio
- Interactuar: E
- Recoger / depositar: F
- Cambiar de residuo: G

## Las categorías

Manejamos cinco tipos de residuos, cada uno con su basurero:

- Azul: plásticos (botellas, latas, vidrio)
- Gris: papel y cartón (periódico, caja de pizza, tetrabrik)
- Verde: orgánicos (restos de comida, cáscaras)
- Negro: no valorizables (bolsas, residuos contaminados)
- Tapas: tapas plásticas

## Cómo correrlo

1. Instalá Godot 4.6 (la versión normal, no la de .NET): https://godotengine.org/download
2. Clonás el repo:
   ```
   git clone https://github.com/Glend-2003/recycling-game-3d.git
   ```
3. Abrís Godot, le das a Importar y elegís el archivo `project.godot`.
4. Corrés con F5.

La primera vez Godot tarda un rato importando los modelos y generando la carpeta
`.godot`, así que no te asustés si no abre de una.

## Cómo está armado el proyecto

- `main.tscn` / `main.gd`: la escena principal y casi toda la lógica del juego.
- `player.tscn` / `player.gd`: el jugador y su movimiento.
- `pickup_system.gd`: la parte de recoger y depositar la basura.
- `trash_item.gd` / `trash_spawner.gd`: los residuos y cómo se reparten por el mapa.
- `categorias.gd` / `catalogo_basura.gd`: las categorías y el catálogo de modelos.
- `DialogueManager.gd`: los diálogos y las voces.
- `loading.tscn`, `introduction.tscn`, `mainMenu.tscn`: pantallas de carga, intro y menú.
- `audio/`: la música y las locuciones.
- `Game 3D/`: modelos y recursos extra.
- El resto de archivos `.glb`, `.jpg` y `.png` son los modelos, texturas e imágenes
  de la interfaz.

## Detalles técnicos

- Motor: Godot 4.6
- Lenguaje: GDScript
- Física: Jolt Physics
- Renderizado en modo GL Compatibility, para que corra sin problemas en equipos
  no tan potentes.

## Sobre el proyecto

Esto lo hicimos como trabajo del curso de Gráficos por Computadora en la UNA. Varios
de los modelos y sonidos son recursos externos que adaptamos e integramos al juego.
