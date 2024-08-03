# Trabajo Práctico 3: Predicción de tormenta en base de Datos Meteorológicos usando modelo más avanzados

## Introducción:

Continuamos con el conjunto de datos ["Rains in Australia"](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package) que exploramos en el TP1, e implementamos modelos en 
el TP2. Ahora intentaremos predecir si va a llover mañana usando SVC, Árboles de decision o XGBoost.

Puntos a resolver:

### Modelado y Evaluación:

Utilizaremos el mismo dataset que en el TP2, manteniendo el mismo conjunto de entrenamiento y de evaluación, así como 
las métricas de evaluación definidas anteriormente. Seleccionar uno de los siguientes clasificadores vistos en las 
clases 6 y 7:
- SVC
- Árbol de clasificación
- Bosques aleatorios
- XGBoost

1. Evalúe el modelo con las métricas definidas. 
2. Discuta las fortalezas y debilidades del modelo elegido en el contexto específico de este problema.

Se tiene la libertad de realizar búsqueda de hiperparámetros o utilizar los valores por defecto. En caso de usar SVC, 
se recomienda encarecidamente realizar una búsqueda de hiperparámetros.

### Conclusiones:

1. Construya una tabla comparativa con los resultados de los diferentes modelos y el modelo base. 
¿Cuál fue el mejor modelo y por qué?
2. Resuma los hallazgos más relevantes obtenidos durante todo el proceso desde el TP1 al TP3.
3. Guarde en formato pickle el mejor modelo, seleccionado según su criterio.

## Entrega del Trabajo:

El entregable consiste en uno o más archivos de notebook `ipynb` con las respuestas (o links a Google Colab). Aunque se 
da libertad para usar otros tipos de entregables, es importante incluir tanto el código resuelto como las respuestas. 
Pueden subir el contenido o proporcionar un enlace a un repositorio público (GitHub o GitLab). **No olviden especificar 
los autores del TP en el entregable**.

### Enlace al formulario de Google para la entrega del TP3:

El informe debe enviarse mediante el siguiente formulario: 
[https://forms.gle/UNY3wk7axqBFvaGA9](https://forms.gle/UNY3wk7axqBFvaGA9). La fecha límite de entrega es el 25/08/2024 
a las 23:59.