# Proyecto: Accidentes Aéreos
## Descripción del proyecto

El objetivo del proyecto es  obtener información relevante que permita desarrollar indicadores clave de rendimiento (KPI) para su posterior visualización en un panel de control utilizando Power BI, para esto se tiene que realizar un Análisis Exploratorio de Datos (EDA) en una base de datos determinada con el fin de identificar patrones y relaciones significativas entre los datos. 

El proceso de EDA involucra la exploración detallada de los diferentes atributos presentes en la base de datos, incluyendo variables numéricas y categóricas. Mediante técnicas estadísticas y visualización de datos, se examinarán distribuciones, correlaciones, tendencias y posibles anomalías. Esto permitirá comprender mejor la naturaleza de los datos y extraer información valiosa para la toma de decisiones.

Una vez completado el EDA, se procederá a definir los KPI relevantes para el proyecto. Estos indicadores se seleccionarán en función de los patrones y relaciones encontrados durante el análisis exploratorio. Se establecerán medidas cuantitativas que reflejen el rendimiento y los resultados deseados en diferentes áreas de interés.

Posteriormente, se desarrollará un panel de control en Power BI para visualizar de manera intuitiva los KPI seleccionados. Este panel proporcionará una visión clara y actualizada del desempeño de los indicadores clave, lo que permitirá tomar decisiones informadas y realizar un seguimiento continuo del progreso hacia los objetivos establecidos.

## Descripción de los archivos

- AccidentesAviones.cv Base de datos en la que se baso el analisis
- EDA.ipynb Jupiter Notebook donde se realizo el Analisis Exploratorio de los datos
- AccidenteAviones_df_mod.cv Base de datos modificada en el EDA, para un mejor analisis
- Dashboard..pbix Panel de control en donde se presentan los KPI en Power BI

## Análisis y la funcionalidad de los KPIs sugeridos.

- KPI: Reducir en 5% la Tasa de Mortalidad a Nivel Anual

La métrica utilizada para este KPI es la Tasa de Mortalidad Anual. Durante el análisis exploratorio de datos, se observó que no existe una tendencia clara en la reducción de la tasa de mortalidad anual. Aunque se registró una ligera disminución en la tasa de mortalidad en comparación con la cantidad de fallecidos anuales, no se encontró una correlación directa entre ambas variables. Esto sugiere que otros factores pueden influir en la cantidad de fallecidos anuales y que se requiere un análisis más detallado para comprender completamente sus determinantes.

Es importante destacar que aunque no se encontró una correlación directa entre la tasa de mortalidad anual y la cantidad de fallecidos, eso no descarta la importancia de reducir la tasa de mortalidad. Aunque no haya una relación clara en el análisis exploratorio, aún se puede establecer como objetivo la reducción de la tasa de mortalidad en un 5% anualmente, ya que cualquier disminución en las muertes es beneficiosa.

- KPI: Reducción del 10% de los Accidentes a Nivel Anual

La métrica utilizada para este KPI es la Cantidad de Accidentes. Durante el análisis, se encontró una relación directa entre la cantidad de accidentes y la cantidad de fallecidos por año. Esto implica que a medida que se logre reducir la cantidad de accidentes en un 10%, se espera una disminución correspondiente en la cantidad de fallecidos.

Se utilizo un gráfico de dispersión entre la suma de cantidad de fallecidos y la reducción de los accidentes por año para definir la relacion de estas dos metricas donde muestra una línea de tendencia horizontal, significa que no hay una relación clara entre estos dos factores. Pero como vemos en el grafico de la relacion entre la cantidad de accidentes y la cantidad de fallecidos, reducir la cantidad de accidentes reduce la cantidad de fallecidos.

Este KPI resalta la importancia de implementar medidas de seguridad y prevención de accidentes para preservar la vida de las personas involucradas en los vuelos.

- KPI: 40% de vuelos con más de 20 pasajeros anualmente

La métrica utilizada para este KPI es la cantidad de vuelos con más de 20 pasajeros. Durante el análisis, se determinó que aproximadamente el 41.58% de los vuelos cumplen con esta condición, mientras que el 58.42% de los vuelos tienen menos de 20 pasajeros. 
Se puede observar una diferencia en la relación entre la cantidad de vuelos con menos de 20 pasajeros y la cantidad de fallecidos, dependiendo del período de tiempo analizado.
En el periodo de 1927 a 2010, se encontró que a mayor cantidad de vuelos con menos de 20 pasajeros, hay una menor cantidad de fallecidos. Esto puede indicar que en ese rango de años, los vuelos con menos pasajeros tuvieron una mejor seguridad y menor incidencia de accidentes mortales.
Sin embargo, cuando se considera la totalidad de la base de datos, la tendencia es opuesta, es decir, a mayor cantidad de vuelos con menos de 20 pasajeros, hay una mayor cantidad de fallecidos. Esta discrepancia puede deberse a factores específicos de la base de datos en su conjunto, como una mayor proporción de vuelos con menos pasajeros involucrados en accidentes particularmente graves o una menor implementación de medidas de seguridad en vuelos con menos ocupación

Este KPI resalta la importancia de asegurar una ocupación adecuada en los vuelos, ya que es un indicador de que se esta utilizando aviones con mayor capacidad y, potencialmente, con más medidas de seguridad implementadas.

- KPI: Tasa de supervivencia mayor del 28% por tipo de avión

La métrica utilizada para este KPI es la Tasa de Supervivencia. Durante el análisis, se encontró que aproximadamente el 25.66% de los tipos de avión superan el umbral del 28% de tasa de supervivencia, mientras que el 74.34% no lo logra. Además, se observó una relación directa entre la cantidad de tipos de avión que superan el umbral y la cantidad de fallecidos por año, siendo que menos aviones superal el umbral de supervivencia, menos fallecidos hay, así como una relación inversa entre la cantidad de tipos de avión que no superan el umbral y la cantidad de fallecidos, siendo que mientras mas aviones no superan el umbral de supervivencia. En un principio uno puede pensar que estos datos deberian ser al revez que mientras mas aviones tengan una mayor tasa de supervivencia deberia haber menos muertes. 

Una posible conclusión que se puede extraer de estos resultados es que, aunque algunos tipos de avión no logran superar el umbral de tasa de supervivencia del 28%, existen otros factores más influyentes en la cantidad de fallecidos por año, como la ocurrencia de accidentes y el número de pasajeros. Es posible que la presencia de una mayor cantidad de aviones con un menor número de pasajeros, aun cuando su tasa de supervivencia sea baja, contribuya a un menor número de fallecidos. Sin embargo, se requiere un análisis adicional para comprender mejor cómo estos factores se relacionan y cómo influyen en la seguridad y los resultados de supervivencia

Por lo que con la ayuda de un grafico de dispersion se enfrento los vuelos con Menos de 20 Pasajeros y Cantidad de Tipos de Avión que NO Superan el Umbral por Año, y se vio que la tendencia es que mientras menos cantidad de tipos de avion que no superan superan el umbral, mayor cantidad de vuelos con menos de 20 pasajero hay. Por lo que se descartar la cantidad de pasajeros como un factor de la anomalia de la relación inversa entre la cantidad de tipos de avión que no superan el umbral y la cantidad de fallecidos.

Esto resalta la importancia de no solo enfocarse en la tasa de supervivencia como único indicador de seguridad, sino también considerar otros aspectos relacionados con la prevención de accidentes y la mitigación de su impacto. Mejorar las condiciones de seguridad y supervivencia en los aviones sigue siendo crucial para reducir la pérdida de vidas en la industria aérea.

Y se recomienda plantear nuevas hipotesis para lograr llegar a la razon de esta anomalia. 


.



En resumen, los KPIs analizados en este proyecto proporcionan una visión integral de la seguridad y el rendimiento de los vuelos. Se destacan la necesidad de implementar medidas para reducir la tasa de mortalidad y la cantidad de accidentes, mejorar la tasa de supervivencia por tipo de avión y garantizar un equilibrio adecuado en la capacidad de los vuelos. Estos KPIs ofrecen información valiosa para la toma de decisiones y la mejora continua de la industria aérea.

