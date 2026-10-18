<div align="center">

# Espacio de Estados
</div>


## Caso: El Sueño en los Primeros Meses de Vida

## Objetivo: 
Representar formalmente el problema del análisis y la predicción de patrones de sueño en los recién nacidos mediante un modelo conceptual basado en Inteligencia Artificial y Machine Learning, identificando los estados, operadores y restricciones necesarios para transformar los datos iniciales en un modelo predictivo evaluado.

El proyecto se centra en analizar variables relacionadas con el sueño infantil, como la edad del bebé, la duración de los ciclos de sueño, la actividad motora y las horas totales de descanso. Para ello, se plantea un flujo de trabajo que integra GitHub para el control de versiones y Google Colab para el procesamiento de datos y el entrenamiento del modelo.

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

---

## Definición de los Estados
Se establecen los siguientes estados para representar el flujo de aprendizaje del proyecto:

| Código | Estado | Descripción | 
|--------|--------|-------------|
| **S₀** | Problema definido | Se establece la necesidad de analizar y predecir características del sueño neonatal. |
| **S₁** | Datos recopilados | Se dispone de un conjunto de datos con registros de sueño infantil. |
| **S₂** | Datos validados | Se comprueba la estructura, integridad y calidad de los registros. | 
| **S₃** | Datos preprocesados | Se tratan valores faltantes, registros duplicados e inconsistencias. |
| **S₄** | Variables seleccionadas | Se determinan las variables de entrada y la variable objetivo. |
| **S₅** | Datos divididos | Se separan los datos en conjuntos de entrenamiento y prueba. |
| **S₆** | Modelo entrenado | Se entrena un algoritmo de regresión con los datos correspondientes. |
| **S₇** | Modelo evaluado | Se comparan las predicciones con los valores reales mediante métricas de error. |
| **Sg** | Objetivo alcanzado | Se obtiene un modelo que cumple los criterios de evaluación y cuyos resultados están documentados. |

En este caso, la variable objetivo será la duración de un ciclo de sueño, expresada en minutos. Las variables de entrada podrán incluir la edad del bebé y otras características disponibles en el conjunto de datos.

---

## Definición de los Operadores
Los operadores representan las acciones que transforman un estado en el siguiente.

| Código | Acción | Transición | 
|--------|--------|------------|
| **O₁** | Recopilar o cargar el conjunto de datos. | **S₀ → S₁** |
| **O₂** | Validar la estructura y calidad de los registros. | **S₁ → S₂** |
| **O₃** | Limpiar y transformar los datos. | **S₂ → S₃** | 
| **O₄** | Seleccionar las variables predictoras y la variable objetivo. | **S₃ → S₄** |
| **O₅** | Dividir los datos en entrenamiento y prueba. | **S₄ → S₅** |
| **O₆** | Entrenar el modelo de regresión. | **S₅ → S₆** |
| **O₇** | Evaluar las predicciones con datos de prueba. | **S₆ → S₇** |
| **O₈** | Verificar los criterios de aceptación y documentar los resultados. | **S₇ → Sg**, si se cumplen los criterios |

Si el modelo no alcanza el desempeño esperado, se ejecuta un operador de ajuste que permite regresar a las etapas de preprocesamiento, selección de variables o entrenamiento. Posteriormente, se vuelve a evaluar el modelo.

---

## Definición de las Restricciones
Las restricciones establecen las condiciones necesarias para garantizar que el proceso sea válido y que las predicciones tengan una base de evaluación confiable.

| Código | Restricción | Aplicación | 
|--------|-------------|------------|
| **R₁** | Disponibilidad de datos | El conjunto de datos debe contener registros pertinentes sobre el sueño infantil. |
| **R₂** | Calidad de los datos | Se deben identificar valores faltantes, duplicados e inconsistencias. |
| **R₃** | Variable objetivo válida | La duración del ciclo de sueño debe estar registrada mediante valores numéricos válidos. | 
| **R₄** | Relevancia de las variables | Las características seleccionadas deben tener sentido para la tarea predictiva. |
| **R₅** | Separación de datos | Los datos de prueba no deben utilizarse para entrenar el modelo. |
| **R₆** | Evaluación objetiva | El modelo debe evaluarse mediante métricas como MAE y RMSE. |
| **R₇** | Privacidad | Los datos personales o clínicos identificables de los bebés deben protegerse. |
| **R₈** | Reproducibilidad | El código, los procedimientos y los resultados deben documentarse en el repositorio de GitHub. |

Para determinar si se alcanza el estado objetivo, se establece como criterio que el modelo obtenga un error de predicción aceptable, definido antes de la evaluación y justificado según las características del conjunto de datos. No se presupone que el modelo cumplirá este criterio antes de entrenarlo y probarlo.

---

## Representación Visual del Espacio de Estados
El siguiente diagrama muestra la secuencia de estados, los operadores que permiten avanzar y la ruta de retroceso cuando los resultados no son satisfactorios.

<div align="center">

<img src="/Recursos/espacio_estados.png" width="500"/>
</div>
<div align="center">
  
<em>Figura 1. Representación del espacio de estados para el desarrollo de un modelo predictivo del sueño neonatal.</em>
</div>

El diagrama muestra que el proceso no es necesariamente lineal: si el modelo presenta errores elevados o incumple los criterios establecidos, es posible regresar a una etapa anterior para corregir problemas y realizar nuevas pruebas.

---

## Representación del Estado Inicial y el Estado Objetivo

Estado inicial (S₀): el problema de predicción está definido, pero todavía no se ha completado la preparación de los datos ni el entrenamiento del algoritmo. Se requiere un conjunto de datos adecuado para iniciar el procesamiento.

Estado objetivo (Sg): se dispone de un modelo de regresión entrenado y evaluado con datos independientes, con métricas registradas, código reproducible y documentación almacenada en GitHub.

El estado objetivo no implica que el modelo sea apto para realizar diagnósticos médicos. Su finalidad es académica y consiste en estudiar la capacidad predictiva de los datos disponibles.

---

## Formulación Matemática de la Transición 
Cada operador transforma un estado actual en un nuevo estado:
<div align="center">
  
$$
O_i : S_i \huge \rightarrow S_{i+1}
$$
</div>

La secuencia completa del proceso se expresa como:
<div align="center">
  
$$
S_0 \huge \xrightarrow{O_1} S_1 \xrightarrow{O_2} S_2
\xrightarrow{O_3} \cdots \xrightarrow{O_8} S_g
$$
</div>

El modelo de regresión se evaluará mediante el error absoluto medio (MAE), definido como:
<div align="center">

$$
MAE = \huge \frac{1}{n}\sum_{i=1}^{n}|y_i-\hat{y}_i|
$$
</div>


Donde:
- \(n\): número de observaciones utilizadas en la evaluación.
- \(y_i\): duración real del ciclo de sueño.
- \(\hat{y}_i\): duración estimada por el modelo.

Un valor menor de MAE representa un menor error absoluto promedio en las predicciones. El modelo podrá alcanzar el estado objetivo si el error obtenido satisface el umbral de aceptación establecido para el proyecto.


