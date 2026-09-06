# sprint7-final-project
telecom-analysis
Objetivo del proyecto

El objetivo de este proyecto es analizar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones, para identificar patrones de uso, segmentos de clientes y oportunidades de negocio.
El análisis busca ayudar a ConnectaTel a tomar decisiones sobre la oferta de planes, mejorar la segmentación de clientes y detectar usuarios con comportamientos de consumo relevantes.

Datasets utilizados

Para el análisis se utilizaron dos datasets principales:

users

Contiene información de los clientes de ConnectaTel, incluyendo variables como:

user_id: identificador del cliente.
age: edad del cliente.
city: ciudad.
plan: plan contratado.
reg_date: fecha de registro.
usage

Contiene información sobre el uso de los servicios:

user_id: identificador del cliente.
type: tipo de uso, como llamadas o mensajes de texto.
duration: duración de las llamadas.
length: longitud de los mensajes.
date: fecha de uso.

Etapas del análisis

El proyecto se desarrolló en varias etapas:

1. Exploración inicial

Se revisó la estructura de los datasets, tipos de datos, valores únicos y posibles valores faltantes o inválidos.

2. Limpieza de datos

Se identificaron y trataron diferentes problemas de calidad:

Valores sentinel -999 en age.
Valores ? en city.
Fechas inválidas en reg_date.
Valores faltantes en las variables de uso.
Se identificaron valores faltantes estructurales en duration y length, relacionados con el tipo de servicio.
3. Revisión y estandarización de fechas

Las columnas de fechas fueron convertidas a formato datetime y se revisaron los años para detectar fechas fuera del rango esperado.

4. Agregación de información

Se agregaron los datos de usage por cliente para obtener:

Cantidad de mensajes.
Cantidad de llamadas.
Cantidad de minutos de llamadas.

Posteriormente, esta información se combinó con los datos de users.

5. Análisis estadístico

Se calcularon medidas como:

Media.
Mediana.
Desviación estándar.
Cuartiles.
Valores mínimos y máximos.

También se analizaron las distribuciones mediante histogramas y boxplots.

6. Detección de outliers

Se utilizó el método del rango intercuartílico (IQR) para identificar valores extremos.

Se encontraron valores elevados principalmente en:

Cantidad de mensajes.
Cantidad de llamadas.
Minutos de llamadas.

Estos valores fueron conservados porque pueden representar clientes reales con un nivel de consumo elevado y no necesariamente errores en los datos.

7. Segmentación de clientes

Se crearon segmentos según dos criterios:

Por nivel de uso
Bajo uso: menos de 5 llamadas y menos de 5 mensajes.
Uso medio: menos de 10 llamadas y menos de 10 mensajes.
Alto uso: 10 o más llamadas o mensajes.
Por edad
Joven: menores de 30 años.
Adulto: entre 30 y 59 años.
Adulto Mayor: 60 años o más.
8. Visualización

Se utilizaron gráficos para analizar:

Distribución de edades.
Cantidad de llamadas.
Cantidad de mensajes.
Minutos de llamadas.
Distribución de clientes por grupo de uso.
Distribución de clientes por grupo de edad.
9. Insight ejecutivo

Finalmente, los resultados fueron traducidos en conclusiones y recomendaciones para ConnectaTel, enfocadas en:

Segmentación de clientes.
Identificación de usuarios de alto consumo.
Diferenciación de planes.
Oportunidades de fidelización y migración hacia planes Premium.
