# Recycling Game 3D

Juego educativo en 3D sobre clasificación de residuos, desarrollado en **Godot 4.6**.
El jugador recorre un hangar rodeado de islas flotantes, recoge basura repartida por
el escenario y la deposita en el basurero correcto antes de que se acabe el tiempo.

> Proyecto del curso de **Gráficos por Computadora** — Universidad Nacional (UNA).

---

## 🎮 Sobre el juego

El objetivo es **clasificar correctamente todos los residuos** del escenario antes de
que el cronómetro llegue a cero. Cada depósito equivocado cuesta una vida; al perder las
tres, la partida termina. Un sistema de diálogos con locuciones acompaña la acción dando
retroalimentación al jugador en cada acierto y cada error.

### Características

- Escenario 3D completo: hangar central, anillos de islas flotantes y vehículos decorativos.
- Generación y dispersión procedural de la basura por el mapa en cada partida.
- Sistema de recogida y depósito con detección de la categoría correcta.
- Cronómetro, marcador de puntaje y sistema de vidas (3 por partida).
- Pantallas de carga, victoria y derrota.
- Retroalimentación por voz mediante el gestor de diálogos.
- Renderizado en modo *GL Compatibility* (compatible con equipos modestos y exportación web).

---

## ♻️ Categorías de reciclaje

El juego clasifica los residuos en cinco categorías, cada una asociada a un basurero:

| Color del basurero | Categoría            | Ejemplos                                   |
| ------------------ | -------------------- | ------------------------------------------ |
| 🔵 Azul            | Plásticos            | Botellas, latas, vidrio reciclable         |
| ⚪ Gris            | Papel y cartón       | Periódico, caja de pizza, tetrabrik        |
| 🟢 Verde           | Orgánicos            | Restos de comida, cáscaras                 |
| ⚫ Negro           | No valorizables      | Bolsas, residuos contaminados              |
| 🟠 Tapas           | Tapas plásticas      | Tapas de botella                           |

---

## ⌨️ Controles

| Acción              | Tecla            |
| ------------------- | ---------------- |
| Mover               | `W` `A` `S` `D` / Flechas |
| Correr              | `Shift`          |
| Saltar              | `Espacio`        |
| Interactuar         | `E`              |
| Recoger / depositar | `F`              |
| Cambiar de residuo  | `G`              |

---

## 🛠️ Tecnologías

- **Motor:** Godot Engine 4.6
- **Lenguaje:** GDScript
- **Física:** Jolt Physics
- **Renderizado:** GL Compatibility

---

## 🚀 Cómo ejecutar

1. Instalar [Godot 4.6](https://godotengine.org/download) (versión estándar, no .NET).
2. Clonar el repositorio:
   ```bash
   git clone https://github.com/Glend-2003/recycling-game-3d.git
   ```
3. Abrir Godot, pulsar **Importar** y seleccionar el archivo `project.godot` del proyecto.
4. Ejecutar con **F5** o el botón ▶ de reproducción.

> En el primer arranque Godot regenerará la carpeta de caché `.godot/` e importará los
> recursos; el proceso puede tardar un poco por el tamaño de los modelos 3D.

---

## 📁 Estructura del proyecto

```
recycling-game-3d/
├── project.godot          # Configuración del proyecto Godot
├── main.tscn / main.gd    # Escena principal y lógica de juego
├── player.tscn / player.gd        # Jugador y movimiento
├── pickup_system.gd               # Sistema de recoger y depositar basura
├── trash_item.gd / trash_spawner.gd   # Residuos y su generación
├── categorias.gd / catalogo_basura.gd # Categorías y catálogo de modelos
├── DialogueManager.gd             # Gestor de diálogos y locuciones
├── loading.tscn / introduction.tscn   # Pantallas de carga e introducción
├── mainMenu.tscn                  # Menú principal
├── audio/                 # Música y locuciones
├── Game 3D/               # Recursos gráficos adicionales
└── *.glb / *.jpg / *.png  # Modelos 3D, texturas e imágenes de interfaz
```

---

## 👥 Créditos

Desarrollado como proyecto académico para el curso de Gráficos por Computadora de la
Universidad Nacional (UNA). Modelos y assets 3D integrados y adaptados para el juego.
