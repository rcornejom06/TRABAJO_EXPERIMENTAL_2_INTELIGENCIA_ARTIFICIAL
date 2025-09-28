# S6-TRABAJO PRÁCTICO EXPERIMENTAL_2
## Algoritmos de Búsqueda y Caminos Mínimos en Inteligencia Artificial

### 📋 Descripción del Repositorio

Este repositorio contiene la implementación de tres algoritmos fundamentales para la búsqueda de caminos y resolución de problemas en grafos, comúnmente utilizados en Inteligencia Artificial:

- **BFS (Breadth-First Search)** - Búsqueda en Anchura
- **Algoritmo de Dijkstra** - Caminos más cortos desde un nodo origen
- **Algoritmo de Floyd-Warshall** - Caminos más cortos entre todos los pares de nodos

---

## 🔎 Algoritmos Implementados

### 1. BFS (Breadth-First Search)
**Archivo:** `bfs.py`

#### Descripción
La búsqueda en anchura es un algoritmo de recorrido de grafos que explora todos los nodos a una distancia dada antes de explorar nodos a una mayor distancia del nodo de inicio.

#### Características
- **Complejidad temporal:** O(V + E) donde V = vértices, E = aristas
- **Complejidad espacial:** O(V)
- **Garantiza:** Encontrar el camino con menor número de aristas
- **Uso:** Grafos no ponderados, encontrar el camino más corto

#### Funcionamiento
1. Utiliza una cola (FIFO) para mantener los nodos por visitar
2. Marca los nodos como visitados para evitar ciclos
3. Explora todos los vecinos del nodo actual antes de avanzar al siguiente nivel

### 2. Algoritmo de Dijkstra
**Archivo:** `dijkstra.py`

#### Descripción
Algoritmo que encuentra los caminos más cortos desde un nodo origen a todos los demás nodos en un grafo ponderado con pesos no negativos.

#### Características
- **Complejidad temporal:** O((V + E) log V) con heap binario
- **Complejidad espacial:** O(V)
- **Garantiza:** Camino óptimo desde un origen a todos los destinos
- **Uso:** Grafos ponderados con pesos no negativos

#### Funcionamiento
1. Inicializa distancias a infinito excepto el nodo origen (distancia 0)
2. Utiliza una cola de prioridad para seleccionar el nodo no visitado más cercano
3. Actualiza las distancias de los vecinos si se encuentra un camino más corto
4. Repite hasta procesar todos los nodos

### 3. Algoritmo de Floyd-Warshall
**Archivo:** `floyd_warshall.py`
### Prerrequisitos
- Python 3.x instalado
- Ninguna librería externa requerida (solo librerías estándar de Python)

### Ejecución Individual

```bash
# Ejecutar BFS
python bfs.py

# Ejecutar Dijkstra
python dijkstra.py

# Ejecutar Floyd-Warshall
python floyd_warshall.py
```

### Ejemplos de Salida

**BFS:**
```
Camino BFS de A a F: ['A', 'C', 'F']
```

**Dijkstra:**
```
Distancias mínimas desde A:
A → A: 0
A → B: 2
A → C: 5
A → D: 3
A → E: 4
```

**Floyd-Warshall:**
```
Matriz de distancias mínimas:
[0, 3, 5, 6]
[5, 0, 2, 3]
[3, 6, 0, 1]
[2, 5, 7, 0]
```

## 🎯 Aplicaciones en Inteligencia Artificial

### BFS
- Resolución de puzzles (8-puzzle, 15-puzzle)
- Búsqueda en espacios de estados
- Análisis de redes sociales
- Detección de componentes conectados

### Dijkstra
- Sistemas de navegación GPS
- Routing en redes de computadoras
- Planificación de rutas en robótica
- Optimización de costos en logística

### Floyd-Warshall
- Análisis de centralidad en grafos
- Detección de arbitraje en mercados financieros
- Planificación multi-objetivo
- Análisis de transitividad en relaciones

---

