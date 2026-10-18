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

## Definición Formal del Problema
El espacio de estados se representa mediante la siguiente tupla:
<div align="center">
  
$$
# \mathcal{P} = (S, O, S_0, S_g, R)
$$
</div>

<div align="center">

$$
MAE = \frac{1}{n}\sum_{i=1}^{n}|y_i-\hat{y}_i|
$$
</div>


