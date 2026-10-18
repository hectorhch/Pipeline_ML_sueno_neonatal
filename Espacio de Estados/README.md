<div align="center">

# Espacio de Estados
</div>


## Caso: 
El Sueño en los Primeros Meses de Vida.

## Objetivo: 
Representar formalmente el problema del análisis y la predicción de patrones de sueño en los recién nacidos mediante un modelo conceptual basado en Inteligencia Artificial y Machine Learning, identificando los estados, operadores y restricciones necesarios para transformar los datos iniciales en un modelo predictivo evaluado.

El proyecto se centra en analizar variables relacionadas con el sueño infantil, como la edad del bebé, la duración de los ciclos de sueño, la actividad motora y las horas totales de descanso. Para ello, se plantea un flujo de trabajo que integra GitHub para el control de versiones y Google Colab para el procesamiento de datos y el entrenamiento del modelo.
## Estado Inicial:
Se dispone del problema definido, pero todavía no se han preparado los datos ni entrenado el modelo.
## Estados Intermedios: 
Recopilación y validación de datos, preprocesamiento, selección de variables y entrenamiento.
## Estado Objetivo: 
Obtener un modelo entrenado y evaluado que pueda predecir una característica del sueño, por ejemplo, la duración de un ciclo de sueño en minutos.

---

## Definición Formal del Problema
El espacio de estados se representa mediante la siguiente tupla:
<div align="center">
  
$$
\huge \mathcal{P} = (S, O, S_0, S_g, R)
$$
</div>

Donde:
- S (Estados): conjunto de situaciones por las que pasa el proceso de construcción del modelo predictivo.
- O (Operadores): acciones que permiten pasar de un estado a otro.
- S₀ (Estado inicial): situación en la que el problema está definido, pero los datos aún no han sido procesados.
- Sg (Estado objetivo): situación en la que se dispone de un modelo entrenado, evaluado y documentado.
- R (Restricciones): condiciones que deben cumplirse durante el procesamiento de los datos y la construcción del modelo.

El propósito es encontrar una secuencia de operaciones que permita alcanzar el estado objetivo a partir del estado inicial, respetando las restricciones establecidas.

<div align="center">

$$
MAE = \huge \frac{1}{n}\sum_{i=1}^{n}|y_i-\hat{y}_i|
$$
</div>


