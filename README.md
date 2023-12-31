Paso 1: 
Se inició importando las librerías necesarias y cargando el conjunto de datos, revelando 878 entradas con información de reseñas ('Review') y puntuaciones ('Rating'). 
Se identificaron 8 valores nulos en la columna de puntuación ('Rating').
La distribución de las puntuaciones destacó una tendencia hacia valores altos, siendo 8, 9 y 10 las calificaciones más comunes, siendo 10 la puntuación predominante.

Paso 2:
Se realizó un procesamiento de texto, eliminando stopwords, lematizando y normalizando las reseñas y títulos. 
El analizador de sentimientos se utilizó para medir la positividad en estos textos. Los resultados se almacenaron en las columnas 'ReviewSentiment' y 'TitleSentiment'.

Paso 3
Se eliminaron las filas con valores nulos para entrenar modelos (KNN, SVM y RandomForest) usando las columnas 'ReviewSentiment' y 'TitleSentiment' como variables predictoras y 'Rating' como variable objetivo. La precisión vario, KNN tuvo una precisión del 49.6%, mientras que SVM y RandomForest alcanzaron alrededor del 49.6%. 
El RMSE fue de aproximadamente 2.68 para KNN y 2.68 para SVM y RandomForest.
Los resultados son iguales haciendo que cuaquier modelo sea util.

los modelos mostraron un rendimiento limitado en la predicción de puntuaciones de reseñas, con precisiones modestas. Los 3 modelos capturaron mejor las reseñas altamente positivas.