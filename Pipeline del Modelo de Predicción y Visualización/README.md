<div align="center">
  
# Pipeline del Modelo de Predicción y Visualización  
</div>

## Objetivo
Desarrollar un modelo predictivo de Machine Learning para estimar la duración de los ciclos de sueño en los recién nacidos, a partir de variables relacionadas con el descanso infantil. El pipeline incluirá la generación de datos sintéticos, el análisis exploratorio, el preprocesamiento, el entrenamiento, la evaluación y la visualización de resultados.

La consigna permite utilizar datos sintéticos o un conjunto de datos referencial. Para este desarrollo se utilizarán datos sintéticos, generados con fines académicos. Por tanto, los resultados permitirán demostrar el funcionamiento del pipeline, pero no establecer conclusiones clínicas sobre bebés reales.

---

## Tipo de Aprendizaje y Tarea

| Elemento | Definición |
|----------|------------|
| Tipo de aprendizaje | Aprendizaje supervisado |
| Tarea de aprendizaje | Regresión | 
| Variable objetivo | Duración del ciclo de sueño, en minutos | 
| Variables predictoras | Edad en meses, horas de sueño diarias y actividad motora |  
| Modelo seleccionado | Random Forest Regressor | 
| Métricas de evaluación | MAE, RMSE y coeficiente de determinación R² |
| Herramientas | Python, Google Colab, pandas, scikit-learn y Matplotlib |

Se selecciona Random Forest Regressor porque combina múltiples árboles de decisión y puede representar relaciones no lineales entre las variables. Además, permite obtener una medida de importancia de las características utilizadas por el modelo.
