# Ejercicios Happiness Index Analysis

## Ejercicio 1: País Más Feliz en 2021 🌏

En este ejercicio, se ha realizado un análisis para determinar cuál es el país más "feliz" en el año 2021, según la data disponible.

Primero, se cargó el conjunto de datos "world-happiness-report-2021.csv," que contiene información sobre la felicidad y otros indicadores en diferentes países en el año 2021. Se encontró el país más "feliz" en 2021 al identificar el registro con la puntuación más alta en el índice "Ladder score." Esto se logró mediante la comparación de la columna "Ladder score" con su valor máximo y extrayendo el nombre del país correspondiente.

Finalmente, se muestra el resultado, indicando que ***Finlandia es el país más "feliz" en el año 2021.***



## Ejercicio 2: País Más Feliz por Continente en 2021 🌍

En este ejercicio, se ha realizado un análisis para determinar cuál es el país más "feliz" del año 2021 en cada continente, según la data disponible.

Primero se obtuvieron los valores únicos de la columna "Regional indicator" en la data del año 2021. Estos valores representan las regiones geográficas.

Se crea un diccionario llamado "region_to_country" para mapear las regiones a sus respectivos continentes, y después, una nueva columna llamada "Continent" en la data del año 2021, basada en la columna "Regional indicator". Esto permitió asignar a cada país su continente correspondiente.

Se agruparon la data por continente y se encontró el país más feliz en cada uno. Esto se logró utilizando la función `apply()` y seleccionando el país con la puntuación más alta en el índice "Ladder score." Finalmente, se muestran los resultados en el formato deseado, indicando el país más feliz en cada continente.

***Finlandia es el país más feliz en Europa, Israel en África, Nueva Zelanda en América y Taiwán en Asia.***



## Ejercicio 3: País que más veces ocupó el Primer Lugar de Felicidad 🌏

En este ejercicio, se determinó cuál es el país que más veces ocupó el primer lugar en el índice de felicidad desde 2005 hasta 2021. Se verificó esta información de tres maneras diferentes:

1. Utilizando `idxmax()`: Se agruparon los datos por año y se encontró el país con la puntuación más alta de "Life Ladder" en cada año a través del índice correspondiente.

2. Utilizando `max()`, `lambda`, y `.items()`: Se encontraron los países con la máxima puntuación de "Life Ladder" para cada año, comprobando si el par (año, "Life Ladder") estaba en los valores máximos calculados.

3. Utilizando una columna 'Rank': Se creó una columna 'Rank' para el país más feliz de cada año y se filtró por el rango igual a 1.

En los tres enfoques, se identificó a Dinamarca como el país que más veces ocupó el primer lugar, con un total de 7 apariciones en la posición más alta del índice de felicidad (entre 2005 y 2019).

Finalmente el ejercicio reveló que ***Finlandia y Dinamarca han compartido el primer lugar en siete ocasiones desde 2005 hasta 2021, lo que ha dado lugar a un empate en la posición de liderazgo.***



## Ejercicio 4: Puesto de Felicidad del País con Mayor GDP en 2020 🌍

Se identifica el puesto de felicidad del país con el mayor GDP en 2020. Se utiliza el DataFrame de felicidad que contiene datos de 2020. Se usa Window para agrupar por año y ordenar descendentemente por "Log GDP per capita". Se crean las columnas "GDP Rank" y "Life Ladder Rank" para ver el ranking según el índice GDP y el de felicidad. Luego, se filtra por el año 2020 y GDP Rank=1 para ver el país con el mayor GDP en ese año. Los resultados muestran que Irlanda tiene el mayor GDP en 2020 y ocupa el puesto número 13 entre los países más felices.

En este ejercicio, se ha realizado un análisis para determinar el puesto de felicidad (índice de felicidad) del país con el mayor Producto Interno Bruto (GDP) en el año 2020. 

Primero, se cargó el conjunto de datos "world-happiness-report.csv" y se filtraron los registros correspondientes al año 2020 del conjunto de datos. Se identificó el país con el mayor GDP en 2020. Esto se logró encontrando el registro con el valor máximo en la columna "Log GDP per capita" y extrayendo el nombre del país correspondiente.

Una vez determinado el país con el mayor GDP, se procedió a buscar su puesto de felicidad en 2020. Para ello, se localizó el registro del país en cuestión y se obtuvo el valor de su "Life Ladder" (índice de felicidad). Finalmente, se muestran los resultados.

***El país con el mayor GDP en 2020 resultó ser Irlanda, y su puntaje de felicidad en 2020 fue de 7.035.***



## Ejercicio 5: Variación en el GDP Promedio a nivel mundial entre 2020 y 2021 🌍

Se ha realizado un análisis para determinar la variación porcentual en el GDP promedio a nivel mundial entre los años 2020 y 2021. Primero se cargaron dos conjuntos de datos (datasets): "world-happiness-report.csv" y "world-happiness-report-2021.csv" y se filtraron los registros correspondientes al año 2020 del primer conjunto de datos (data_2020).

Después, se calculó el promedio del GDP per cápita para el año 2020 y el año 2021. El promedio de 2020 se calculó utilizando el campo "Log GDP per capita," y el promedio de 2021 se calculó utilizando el campo "Logged GDP per capita."

Se creó un DataFrame llamado "df_promedios" que contiene los promedios de GDP para ambos años. Además, se calculó la variación porcentual del GDP promedio entre 2020 y 2021 y se agregó como una nueva columna llamada "Variación" en el DataFrame.

Finalmente, se muestran los resultados. La variación porcentual se calculó como `(GDP promedio 2020 - GDP promedio 2021) / GDP promedio 2021 * 100`. En este caso, la ***variación fue positiva***, lo que significa que el ***GDP promedio aumentó en un 3.38% en 2021 en comparación con 2020***. El mensaje de salida indica que el GDP promedio aumentó en un 3.38%.



## Ejercicio 6: País con Mayor Expectativa de Vida y su indicador en 2019 🌏

En este ejercicio se analiza el país con la mayor expectativa de vida en los años 2019, 2020 y 2021. Los resultados muestran que ***Singapur es el país con la mayor expectativa de vida en 2019, 2020 y 2021***.