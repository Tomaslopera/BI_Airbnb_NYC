# Análisis de Datos de Airbnb en Nueva York

Este proyecto utiliza el **dataset público de Kaggle [NYC Airbnb Open Data](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data)**, el cual contiene información detallada sobre los listados de Airbnb en la ciudad de Nueva York.  

El análisis se desarrolla siguiendo el marco conceptual **“What? Why? How?”** propuesto por **Tamara Munzner** en su libro *Visualization Analysis & Design* (2014).  

En este proyecto, se parte del análisis exploratorio de los datos de Airbnb en NYC, definiendo las variables del dataset (**What?**), los objetivos analíticos de interés (**Why?**) y finalmente las visualizaciones que se desarrollarán en **Power BI** (**How?**) para mostrar los resultados.

## What?

| # | Nombre | Tipo de Dato |
|---|---|---|
| 0 | id | categórica |
| 1 | name | categórica |
| 2 | host_id | categórica |
| 3 | host_name | categórica |
| 4 | neighbourhood_group | categórica |
| 5 | neighbourhood | categórica |
| 6 | latitude | cuantitativa secuencial |
| 7 | longitude | cuantitativa secuencial |
| 8 | room_type | categórica |
| 9 | price | cuantitativa secuencial |
| 10 | minimum_nights | cuantitativa secuencial |
| 11 | number_of_reviews | cuantitativa secuencial |
| 12 | last_review | ordinal secuencial |
| 13 | reviews_per_month | cuantitativa secuencial |
| 14 | calculated_host_listings_count | cuantitativa secuencial |
| 15 | availability_365 | cuantitativa secuencial |

## Why?

1. Detectar precios atípicos por `room_type` y `neighbourhood_group` {identify, outliers}  
2. Comparar la distribución de `price` entre `neighbourhood_group` y `room_type` {compare, distribution}  
3. Evaluar diferencias de `price` entre `neighbourhood` dentro de cada `neighbourhood_group` {compare, distribution}  
4. Analizar la dependencia entre `availability_365` y `price` {compare, dependency}  
5. Analizar la relación de `number_of_reviews` y `reviews_per_month` con `price` {compare, dependency}  
6. Localizar *hotspots* espaciales de oferta y de precios elevados (`latitude`, `longitude`, `price`) {explore/locate, spatial}  
7. Identificar umbrales problemáticos en `minimum_nights` y `availability_365` {identify, thresholds}  
8. Resumir la recencia de reseñas por zona y tipo (a partir de `last_review`) {summarize, temporal}  
9. Comparar la accesibilidad de precio (mediana) entre `neighbourhood_group` para `room_type` = Private vs Entire {compare, aggregates}  
10. Evaluar el impacto de `calculated_host_listings_count` en `price` e identificar extremos {compare, dependency}  
11. Identificar `neighbourhood` con alta `availability_365` y baja `number_of_reviews` {identify, joint-conditions}  
12. Habilitar búsqueda dirigida por rango de `price` en un `neighbourhood` y `room_type` específicos {lookup, target-known}
