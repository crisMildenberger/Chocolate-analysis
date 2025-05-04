Proyecto Final
Análisis de distribuidora de chocolates internacional
Para este proyecto, seleccioné un dataset disponible en Kaggle que despertó mi interés:
ventas de un supermercado colombiano. Descargué el archivo en formato .xlsx y lo leí
utilizando Python (Jupyter Notebook).
El objetivo principal de este análisis es responder las siguientes preguntas:
● ¿Cuáles son los productos más vendidos?
● ¿Cuáles son los productos menos vendidos?
● ¿Cómo varían las ventas a lo largo del tiempo (mensualmente)?
● ¿Cuál es el monto promedio de compra por mes?
● ¿Cómo nos fue estos ultimos 4 meses comparados a los primeros 4?
● ¿Como le fue a nuestro nuevo producto lanzado en Junio?
Día 2 – Evaluación de Calidad de Datos
Para asegurarme de que los datos fueran confiables y útiles para el análisis, realicé una
evaluación de calidad basada en los siguientes criterios:
● Precisión: Validé que todos los montos fueran positivos.
● Integridad: Verifiqué la existencia de datos faltantes.
● Validez: No se requería un formato o regla específica para las columnas.
● Coherencia: Comprobé que no hubiera fechas futuras en los registros.
● Unicidad: Revisé que no existieran IDs duplicados.
● Oportunidad: Confirmé que las fechas estuvieran dentro de un rango relevante.
● Aptitud: Me aseguré de que los datos fueran adecuados para el análisis.
Posteriormente, eliminé las columnas booleanas utilizadas en esta evaluación para no
interferir con las siguientes etapas.
Estadísticas Descriptivas
Tras limpiar los datos, analicé la distribución de las variables clave:
Amount Boxes
Shipped
Count 1094 1094
Mean 5652.3 161.8
Min 7.0 1.0
25% 2390.5 70.0
50% (Mediana) 4868.5 135.0
75% 8027.3 228.8
Máx 22050.0 709.0
Desvío Std. 121.5 315.9
La variabilidad es moderada en ambas variables. Además, mediante la prueba de
normalidad de Shapiro-Wilk, se determinó que los datos no siguen una distribución normal:
Estadístico de Shapiro-Wilk: 0.9360
Valor p: 0.0000
Día 3 – Análisis Exploratorio de Datos (EDA)
Rango de fechas: 03/01/2022 al 31/08/2022
Industria: Distribuidora de chocolates
Se eliminaron las filas nulas, especialmente aquellas sin país asignado, ya que uno de los
objetivos era analizar el comportamiento por país. También se eliminaron filas duplicadas.
Productos más vendidos:
● Dark Bites: 9,792 unidades
● Smooth Silky Salty: 8,810 unidades
● Eclairs: 8,757 unidades
Productos menos vendidos:
● Almond Choco: 556 unidades
● Choco Coated Almonds: 455 y 333 unidades
El producto "Choco Coated Almonds" es de los menos vendidos en varios países, aunque
presenta ventas aceptables en UK y buenas en Canadá. En EE.UU., Nueva Zelanda y
Australia es el menos consumido.
Ventas por país (Boxes Shipped):
País Cajas
Vendidas
Australia 32,647
Canadá 31,221
UK 30,265
India 29,470
USA 26,824
New Zealand 26,580
Ventas por país (Amount):
País Monto Total
Australia $1,137,367
UK $1,051,792
India $1,045,800
USA $1,035,349
Canadá $962,899
New Zealand $950,418
Clientes únicos por país:
150 en total (25 por cada país)
Prueba A/B Testing
Se desarrolló una prueba A/B simulada, cuyo objetivo fue comparar el rendimiento del
producto menos vendido ("Choco Coated Almonds") con un nuevo producto alternativo:
"Dark Chocolate Covered Almonds", en los últimos tres meses (junio-agosto).
Para esto:
● Se crearon datos sintéticos con Python, simulando el envío de 250 cajas por país
por mes (total 750).
● Las variables comparadas fueron: Amount y Boxes Shipped.
Tras obtener buenos resultados con el nuevo producto, se procedió a la creación final del
dashboard visual.
Visualización e Indicadores
Los KPIs principales incluidos fueron:
● Promedio de cajas enviadas por grupo
● Total vendido
● Cambio porcentual entre grupo A y B
Además, se utilizaron:
● Gráficos de líneas para analizar la evolución temporal.
● Tablas comparativas por país y producto.
● Tarjetas KPI con indicadores visuales de cambio.
● Segmentaciones dinámicas por fechas y países
