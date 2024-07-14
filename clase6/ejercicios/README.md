# Ejercicios para prácticar

1. Sos un data scientist que trabaja para una empresa de publicidad que lanzo una campaña de publicidad en una red social. 
Se registró cada usuario al que se le mostró la publicidad, y se pudo obtener datos de la persona tales como 
`genero`, `edad` y `salario estimado`. Además, se registró si el usuario luego compró el producto que la publicidad 
hacía referencia. Los datos están en `Social_Network_Ads.csv`. Se busca poder predecir dado un usuario con datos 
socioeconómicos si va a comprar o no el producto.
   1. Realice un estudio de variables y de limpieza de datos. Analice las clases, están balanceadas, o no? ¿Qué clase 
   nos parece más importante de las dos?
   2. Separe el dataset en entrenamiento y validación.
   3. Elija un modelo SVC dejando las opciones por defecto que nos indica Scikit-Learn. Elija los atributos de entrada 
   basándonos en el análisis del punto 1.
   4. Obtenga dos o más metrica de evaluación. Discuta los resultados.
   5. Utilizando alguna técnica de búsqueda de hiper-parámetros, busque los mejores parámetros. 
   6. Obtenga las mismas métricas del punto 4 y compare con el modelo anterior. Discuta los resultados.
   7. Cree una curva ROC para evaluar el mejor modelo para ver la calidad del modelo, sin depender 
   del valor umbral. Elija un valor umbral que considere más óptimo y vuelva a clasificar usando ese valor. ¿Cómo 
   cambiaron las métricas usadas en el punto 6 con este valor umbral?

2. Usando el dataset `winequality-red.csv`, el cual consiste en datos de vinos rojos basados en datos físico-químicos y 
una métrica de calidad de vino. Más info en [Kaggle](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009). 
Queremos predecir la calidad del vino usando los atributos físico-químicos del mismo.
   1. Lea el dataset como un DataFrame de Pandas. Realice un estudio de variables. Como se llaman y que están midiendo 
   exactamente (vea la documentación del dataset). Además, analice que tipo de variables (incluido el target) son, 
   cuál es el rango de estas variables y cómo se distribuyen (histograma). Además, realice una matriz de correlación, 
   ¿cuáles variables parecen estar correlacionadas? ¿Y con respectos a la calidad del vino?
   2. Realice si es necesaria la limpieza de datos y corrección de errores.
   3. Construya usando un SVM un modelo de regresión o clasificación (multi-clase), según lo que considere más 
   apropiado, el cual se intente predecir la calidad del vino usando el nivel de alcohol.
      1. Realiza la separación entre el dataset de entrenamiento y testeo. Utilice 80%-20%.
      2. Determine que métrica se va a usar para evaluar la calidad del modelo (MSE, MAE, etc.)
      3. Entrene el modelo con el set de entrenamiento.
      4. Evalúe el modelo con la métrica de evaluación.
