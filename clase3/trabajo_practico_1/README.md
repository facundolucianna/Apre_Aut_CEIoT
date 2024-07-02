# Trabajo Práctico1 : Análisis de Datos Meteorológicos 

## Introducción:

En este trabajo práctico exploraremos el conjunto de datos ["Rains in Australia"](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package),
el cual contiene información meteorológica recopilada en diversas ubicaciones de Australia. El objetivo 
principal es aplicar técnicas de análisis exploratorio de datos utilizando las bibliotecas Pandas y 
Matplotlib/Seaborn en Python. Este conjunto de herramientas nos permitirá visualizar, analizar y obtener insights 
significativos sobre los patrones climáticos y la distribución de lluvias en diferentes regiones de Australia.

Puntos a Resolver:

### Carga de Datos:

1. Importar el conjunto de datos utilizando Pandas.
2. ¿Cuántas filas y columnas tiene el dataset?
3. ¿Qué atributos presenta el dataset y qué describen? ¿Qué tipos de datos tiene cada atributo?
4. Verifica la consistencia de los tipos de datos y realizar conversiones si es necesario.
5. ¿Existen valores faltantes en algunos atributos? ¿Cuáles son las tres columnas con más valores faltantes y cuál es el porcentaje de valores faltantes en cada una? 
6. Para las columnas numéricas, obtener métricas de estadística descriptiva (media, mediana y cuartiles). Hint: usa el método `.describe()`.

### Limpieza y Preprocesamiento de Datos: 

Existen diversas formas de manejar los datos faltantes. La más sencilla implica eliminar las observaciones con valores 
faltantes, pero esto puede resultar en la pérdida de una cantidad significativa de datos. Otra estrategia consiste en 
completar los valores utilizando estadísticas descriptivas. Sin embargo, dado que estamos trabajando con series de 
tiempo correspondientes a diferentes ciudades y considerando la naturaleza estacional del clima, podemos emplear un 
enfoque más sofisticado. Para aprovechar la estacionalidad del clima, una técnica efectiva es propagar la última 
observación válida hacia la siguiente. Esta metodología asume que las condiciones climáticas cambian gradualmente día 
a día (aunque es cierto que pueden haber cambios abruptos en ciertos días, la premisa es que los días de una misma 
estación son relativamente similares).

1. Ordene el dataset por ciudad y fecha de forma ascendente.
2. Complete los valores faltantes de todas las columnas menos `RainToday`, `RainTomorrow`, `Cloud9am` y `Cloud3pm`
usando [FowardFill](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.ffill.html).
3. Modifique en las columnas `RainToday` y `RainTomorrow` reemplazando `Yes` con `1` y `No` con `0`.
4. Según el dataset, la columna `RainToday` se define como `1` si `Rainfall` supera los 1 mm, sino es 0. Utilice 
esta información para completar los datos faltantes de la columna `RainToday`.
5. Complete los valores faltantes de las columnas `Cloud9am` y `Cloud3pm` usando la mediana de cada una por ciudad.
6. Elimine del dataset la primera fecha de cada ciudad.

### Análisis Exploratorio de Datos:

En esta sección se realizará un análisis exploratorio de los datos para obtener insights sobre el conjunto de datos.
1. Obtenga el top 5 de mayor temperatura media y el top 5 de menor temperatura media. 
2. Repita el proceso para la temperatura a las 3pm. ¿Son las mismas ciudades las que aparecen en ambos tops? 
3. ¿Cuál es la ciudad que registró la mayor cantidad de precipitación en un solo día? ¿Cuánto mm de lluvia se registró?
4. ¿Cuál es la ciudad con la menor cantidad de lluvias registradas? 
5. Para las 10 ciudades obtenidas en el punto 1, calcule la dirección del viento más fuerte que más veces ocurrió.
6. ¿Cuál es la ciudad que experimentó la mayor amplitud térmica en un solo día? ¿Y cuál es la ciudad que, en promedio, 
presenta la mayor amplitud térmica diaria?
7. Calcule la correlación entre `RainTomorrow` y todos los atributos. ¿Cuáles tienen mayor correlación?

### Visualización de Datos:

En esta sección se busca que se realicen visualizaciones que acompañen adecuadamente el análisis de datos, utilizando 
gráficos bien diseñados con colores apropiados, ejes etiquetados, leyendas claras y tamaños adecuados.

1. De las 10 ciudades obtenidas del punto 1 del Análisis Exploratorio de Datos, grafique la temperatura a las 3pm a lo 
largo del tiempo. ¿Se observa estacionalidad?
2. Realice el mismo proceso para la columna `RainToday`. ¿Se observa estacionalidad en la incidencia de lluvia?
3. Para la ciudad de `Sydney`, trace en un mismo gráfico todas las series temporales de temperatura entre los años 2012 
y 2014.
4. Para las ciudades del punto 1 del Análisis Exploratorio de Datos, genere un diagrama de caja comparativo para 
`WindSpeed9am` y otro para `MaxTemp`.
5. Para las ciudades del punto 3 y 4 del Análisis Exploratorio de Datos, cree un diagrama de barras que muestre la 
cantidad de `Rainfall` por año.
6. Realice un gráfico de dispersión entre `WindGustSpeed` y `Pressure9am` para las ciudades del punto 1. Coloree los 
puntos según la variable `RainToday`.
7. Realice un gráfico de dispersión entre `MaxTemp` y `Humidity9am` para las ciudades del punto 1. Coloree los 
puntos según la variable `RainToday`.

### Conclusiones:

1. Resumir los hallazgos más relevantes obtenidos del análisis de datos.
2. Guarde el dataset limpio y ordenado para siguientes TPs en un `csv`, previo al guardado, elimina todas las filas que 
tienen datos incompletos de `RainTomorrow`.

## Entrega del Trabajo:

El entregable consiste en uno o más archivos de notebook `ipynb` con las respuestas (o links a Google Colab). Aunque se 
da libertad para usar otros tipos de entregables, es importante incluir tanto el código de lo resuelto como las 
respuestas. Pueden subir el contenido o proporcionar un enlace a un repositorio público (GitHub o GitLab). 
**No olviden especificar los autores del TP en el entregable**.


### Enlace al formulario de Google para la entrega del TP1:

El informe debe enviarse mediante el siguiente formulario: 
[https://forms.gle/n77poDgHrdthxxyv9](https://forms.gle/n77poDgHrdthxxyv9). La fecha límite de entrega es el 28/07/2024 a 
las 23:59.