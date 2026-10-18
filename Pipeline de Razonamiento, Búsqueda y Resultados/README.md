<div align="center">

# Pipeline de razonamiento, búsqueda y resultados
</div>

## Objetivo
Construir un notebook en Google Colab que represente el razonamiento computacional necesario para resolver el problema del sueño neonatal, mediante la definición del problema, el espacio de estados, la exploración de alternativas, la búsqueda de una solución y la presentación del resultado.

El pipeline simulará la toma de decisiones de un sistema inteligente que verifica los datos disponibles, selecciona una estrategia de análisis, comprueba las condiciones necesarias y determina si puede avanzar hacia la construcción de un modelo predictivo.

---

## Estrategia de Búsqueda
Se utilizará una búsqueda en anchura (BFS, Breadth-First Search) para recorrer el grafo de estados del proyecto. Este algoritmo explora los estados por niveles y permite encontrar una ruta hacia el objetivo cuando existe una secuencia válida de transiciones.

Los estados representarán las etapas del análisis y los operadores representarán las acciones que permiten avanzar entre ellas.

---

## Resultado Esperado 
Al ejecutar las celdas, el algoritmo BFS encontrará la ruta representada por la secuencia de estados desde S0 hasta Sg, siguiendo las transiciones disponibles.

Este resultado demuestra el funcionamiento de la búsqueda en un espacio de estados. No representa una predicción médica ni evidencia que un modelo real haya alcanzado un desempeño determinado. La aceptación del modelo se deberá comprobar posteriormente con datos de prueba y métricas reales.
