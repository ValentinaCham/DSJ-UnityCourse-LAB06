# A* Pathfinding in Unity - Curso "The A* Algorithm"

Este proyecto implementa el algoritmo de búsqueda A* (A Star) dentro de Unity utilizando visualizaciones 3D para representar el funcionamiento del pathfinding en un entorno tipo laberinto.

> 📌 Proyecto desarrollado como parte del curso **“The A* Algorithm”** disponible en [Unity Learn](https://learn.unity.com/course/a-36369ng?version=2021.3).

---

## 🧩 Descripción General

El código contenido en este repositorio representa paso a paso cómo el algoritmo A* evalúa celdas en un mapa 2D y construye una ruta óptima desde un punto de inicio hasta un destino. Para ello, se utilizan objetos visuales (`prefabs`) en la escena de Unity que marcan:

- El nodo actual en evaluación.
- Los nodos abiertos (en espera).
- Los nodos cerrados (ya visitados).
- La ruta final óptima reconstruida.

---

## 🧠 Algoritmo Implementado: A\*

El A* combina los conceptos de búsqueda de costo uniforme (G) y búsqueda heurística (H) para encontrar el camino más corto en un grafo. En esta implementación se calcula:

- **G**: Costo desde el nodo inicial hasta el nodo actual.
- **H**: Estimación del costo restante hasta el nodo objetivo (usando distancia Euclidiana).
- **F = G + H**: Prioridad para explorar nodos.

---

## 🎮 Controles del Proyecto

Durante la ejecución, puedes interactuar con el sistema presionando las siguientes teclas:

- `P`: Inicia una nueva búsqueda con posiciones aleatorias de inicio y fin.
- `C`: Ejecuta un paso del algoritmo A* (avanza la búsqueda).
- `M`: Muestra la ruta final reconstruida desde el objetivo hasta el inicio.

---

## 🧱 Estructura del Código

El código principal se encuentra en el script `FindPathAStar.cs` y contiene:

### `PathMarker.cs`

- Define una clase para representar cada nodo del grafo.
- Almacena su posición, costos (`G`, `H`, `F`), una referencia a su `GameObject` y al nodo padre.

### `FindPathAStar.cs`

- Controlador principal del algoritmo:
  - `BeginSearch()`: Inicializa la búsqueda.
  - `Search()`: Procesa una iteración del algoritmo.
  - `GetPath()`: Reconstruye el camino óptimo.
- Utiliza listas `open` y `closed` para el control del flujo.
- Instancia marcadores visuales en tiempo real para mostrar resultados.

---

## 📦 Requisitos y Dependencias

- **Versión de Unity**: `2022.3.20f1`
- Se requieren `prefabs` para:
  - Nodo de inicio (`start`)
  - Nodo de fin (`end`)
  - Nodo intermedio o de ruta (`pathP`)
- Clase adicional `Maze` y `MapLocation` necesarias para definir el mapa y las coordenadas.

---

## 🧪 Aprendizaje Adquirido

Este proyecto es una excelente introducción práctica a:

- Algoritmos de búsqueda y heurística.
- Estructuras de datos para AI (listas abiertas/cerradas, árboles de nodos).
- Visualización de procesos algorítmicos.
- Programación orientada a objetos aplicada a videojuegos.
- Uso de Unity para simulaciones educativas.

---

## 📚 Referencia del Curso

- Curso original: [**The A* Algorithm** – Unity Learn](https://learn.unity.com/course/a-36369ng?version=2021.3)

---

## 🚧 Notas Adicionales

Este proyecto **no utiliza librerías externas** ni frameworks como el [A* Pathfinding Project de Aron Granberg](https://arongranberg.com/astar), ya que todo el algoritmo está implementado desde cero como parte del proceso educativo del curso.

---
