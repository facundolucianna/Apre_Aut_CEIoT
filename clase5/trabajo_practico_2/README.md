# Trabajo Práctico 2: Predicción de tormenta en base de Datos Meteorológicos 

## Introducción:

Continuamos con el conjunto de datos ["Rains in Australia"](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package) que exploramos en el TP1. Ahora intentaremos predecir 
si va a llover mañana usando kNN y la regresión logística.

Puntos a resolver:

### Preparación de Datos: 

1. Lea el dataset limpio que se guardó en el TP1 (punto 2 de conclusiones)
2. Realice una codificación adecuada de variables categóricas si es necesario, utilizando técnicas como One-Hot 
Encoding según corresponda. 
3. Separe el dataset en entrenamiento y prueba (70% entrenamiento, 30% prueba). 
4. Normalice o estandarice los atributos numéricos para asegurar que todas las variables tengan la misma escala.

### Modelado y Evaluación:

1. Determine dos métricas de evaluación que considere importante medir para este problema. Justifique su elección.
2. Implemente un modelo de base usando como predicción que determine que llueve mañana si hoy llueve, y si hoy no llueve
mañana no va a llover. 
3. Implemente y entrene un modelo de k Nearest Neighbors (kNN) para predecir si va a llover mañana. Utilice la 
distancia euclidiana como medida de distancia entre vecinos.Ajuste el parámetro k utilizando técnicas como la 
validación cruzada (5 folds) para optimizar el rendimiento del modelo (utilice como función de optimización una de las 
métricas definidas en el punto anterior). 
4. Implemente y entrene un modelo de regresión logística para predecir la misma variable objetivo.
5. Evalúe los dos modelos con las métricas definidas al principio. Discuta las fortalezas y debilidades de cada enfoque 
en el contexto específico de este problema comparándolos con el modelo de base.

### Conclusiones:

1. Resuma los hallazgos más relevantes obtenidos.
2. Guarde los conjuntos de entrenamiento y evaluación para el siguiente TP en archivos `csv`.
3. Guarde en formato pickle el mejor modelo, seleccionado según su criterio.

## Entrega del Trabajo:

El entregable consiste en uno o más archivos de notebook `ipynb` con las respuestas (o links a Google Colab). Aunque se 
da libertad para usar otros tipos de entregables, es importante incluir tanto el código resuelto como las respuestas. 
Pueden subir el contenido o proporcionar un enlace a un repositorio público (GitHub o GitLab). **No olviden especificar 
los autores del TP en el entregable**.

### Enlace al formulario de Google para la entrega del TP2:

El informe debe enviarse mediante el siguiente formulario: 
[https://forms.gle/NfRwRgXxD382YicP6](https://forms.gle/NfRwRgXxD382YicP6). La fecha límite de entrega es el 11/08/2024 
a las 23:59.