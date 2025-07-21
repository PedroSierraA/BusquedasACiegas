# Búsqueda a Ciegas - Problema de las Jarras

Este proyecto implementa algoritmos clásicos de búsqueda a ciegas y heurística para resolver el problema de las jarras de agua, utilizando Python y visualización de árboles con `pydot`.

## Descripción

El problema consiste en dos jarras (una de 3L y otra de 4L) y el objetivo es obtener exactamente 2 litros en la jarra de 4L, usando operaciones de llenado, vaciado y trasvase entre jarras.

Se implementan los siguientes algoritmos de búsqueda:
- Búsqueda primero en anchura (Breadth-First Search)
- Búsqueda primero en profundidad (Depth-First Search)
- Búsqueda Best-First (Greedy)
- Búsqueda A* (A-Star)

El código incluye una clase base `Node` y una clase específica `Jarra` que modela el problema.

## Estructura

- **Node**: Clase base para nodos del árbol de búsqueda.
- **Jarra**: Hereda de Node, implementa las operaciones del problema de las jarras.
- **Algoritmos**: Implementaciones de BFS, DFS, Best-First y A*.
- **Visualización**: Funciones para dibujar el árbol de búsqueda usando `pydot`.

## Requisitos

- Python 3.x
- pydot
- numpy
- IPython (para notebooks)
- graphviz (para visualizar los árboles)

Instala las dependencias con:

```sh
pip install pydot numpy ipython
```
## Ejemplo de uso 

```python
jarra = Jarra(value="inicio", state=[0,0], operators=operators)
(tree, objective) = breadthFirst(jarra, [0,2])
path = objective.pathObjective()
objective.printPath()
graph = draw(tree, path)
tree_image = Image(graph.create_png(), width=900, height=700)
display(tree_image)
