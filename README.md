# Proyecto 2 - Inteligencia Artificial
## Sistema de toma de decisiones para una red de logística autónoma


**Integrantes:**
- Vianka Castro (23201)
- Ricardo Godinez (23247)

---

## Descripción del Proyecto

Este proyecto aborda dos problemas fundamentales de la Inteligencia Artificial aplicados a la seguridad de redes: la satisfacción de restricciones (CSP) y la toma de decisiones en entornos adversariales.

El proyecto está dividido en dos tareas principales alojadas en el notebook principal:

### Task 1: Configuración Segura de la Red (CSP y Factor Graphs)
Se modela la asignación de protocolos de seguridad (colores) a los servidores de una red (nodos de un grafo) asegurando que dos nodos conectados no compartan el mismo protocolo para evitar vulnerabilidades. Se implementan y comparan dos enfoques:
- **Backtracking Puro:** Búsqueda exhaustiva tradicional.
- **Backtracking Optimizado:** Incorpora Lookahead (Forward Checking) y la heurística MCV (Minimum Remaining Values), logrando una mejora significativa en el tiempo de ejecución mediante la poda del árbol de búsqueda.

### Task 2: Defensa Adversarial (Juegos de Suma Cero)
Se simula un juego por turnos en la red ya configurada, donde un Defensor (MAX) y un Hacker (MIN) compiten por capturar nodos y maximizar el "Valor de Información" que controlan. Se implementan algoritmos de evaluación de árboles de juego:
- **Minimax Puro:** Evaluación exhaustiva de todos los turnos y decisiones posibles.
- **Poda Alfa-Beta:** Optimización del algoritmo Minimax para podar ramas no prometedoras, reduciendo exponencialmente la cantidad de nodos evaluados sin perder la decisión óptima.

---

## Estructura del Repositorio

- `task_1.ipynb`: Notebook interactivo que contiene toda la lógica, implementaciones de los algoritmos y visualizaciones de los grafos.
- `requirements.txt`: Archivo con las dependencias necesarias para ejecutar el proyecto de forma local.

---

## Requisitos e Instalación

Para ejecutar este proyecto, necesitas Python instalado en tu sistema. Se recomienda utilizar un entorno virtual.

1. Instala las dependencias ejecutando el siguiente comando en tu terminal:
   ```bash
   pip install -r requirements.txt
   ```

2. Las librerías principales utilizadas son:
   - `networkx` (para modelado y manipulación de grafos)
   - `matplotlib` (para visualización)
   - `numpy`
   - `ipykernel` (para ejecutar el notebook)

## Cómo Ejecutar

1. Abre el repositorio en **Visual Studio Code** o Jupyter Notebook.
2. Abre el archivo `task_1.ipynb`.
3. Selecciona tu entorno (Kernel de Python) donde instalaste las dependencias.
4. Ejecuta todas las celdas secuencialmente para observar la generación del grafo, la asignación de protocolos, los esquemas de tiempos y la simulación del juego adversarial.
