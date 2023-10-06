# **Análisis de Accidentes Mortales de Tráfico en la Ciudad de Buenos Aires (2016-2021)**
## Proyecto Individual #2 

## **Introducción**

Este proyecto, realizado en el rol de Analista de Datos para una consultora, tiene como objetivo analizar datos solicitados por el Observatorio de Movilidad y Seguridad Vial (OMSV) bajo la Secretaría de Transporte de la Ciudad Autónoma de Buenos Aires (CABA). El objetivo principal es proporcionar información basada en datos para informar a los tomadores de decisiones y mejorar la seguridad vial mientras se reducen los accidentes mortales de tráfico en la ciudad.

## **Contexto**

En Argentina, se registra una cifra alarmante de aproximadamente 4,000 personas que fallecen anualmente debido a siniestros viales. Esta triste realidad sitúa a los accidentes de tráfico como la principal causa de muertes violentas en el país. Los datos provienen del Sistema Nacional de Información Criminal (SNIC) del Ministerio de Seguridad de la Nación y revelan que, en el período comprendido entre 2018 y 2022, se documentaron un total de 19,630 fallecimientos en accidentes de tránsito en todo el territorio argentino. Esto equivale a un promedio de 11 personas por día que lamentablemente perdieron la vida en incidentes viales.

Resulta igualmente impactante observar que únicamente en el año 2022 se registraron 3,828 muertes fatales en este tipo de sucesos. Los expertos en la materia señalan que en Argentina la probabilidad de fallecer en un siniestro vial es de dos a tres veces mayor que la de sufrir un hecho de inseguridad delictiva. Estas estadísticas reflejan la urgente necesidad de abordar y mejorar la seguridad vial en el país.

## **Desarrollo**

### Datos

En relación a los datos utilizados en este proyecto:

- Se emplearon los conjuntos de datos sobre víctimas fatales en siniestros viales, los cuales se presentan en formato Excel y constan de dos hojas de datos:

    - "HECHOS": Esta hoja contiene un registro único por cada incidente, junto con las variables temporales, espaciales y los detalles de los involucrados en cada incidente.

    - "VICTIMAS": En esta hoja de datos se registra a cada víctima de los incidentes, incluyendo información sobre edad, género y método de desplazamiento. Estos datos están vinculados a los incidentes a través de identificadores únicos. El documento proporciona definiciones detalladas de las variables utilizadas en el análisis.

- Se llevó a cabo un proceso de **ETL (Extracción, Transformación y Carga de Datos)** para preparar los datos. Este proceso involucró la extracción y limpieza de los datos de las dos hojas de datos, "HECHOS" y "VICTIMAS", utilizando bibliotecas como Pandas y Jupyter Notebook. Durante la limpieza de los datos, se eliminaron valores nulos, duplicados y se realizaron transformaciones necesarias, como cambios en los tipos de datos. Además, se unieron las tablas relacionadas para crear un archivo llamado "siniestros_limpio.csv".

- Posteriormente, se realizó un proceso de **Análisis Exploratorio de Datos (EDA)**. Una vez que los datos estuvieron limpios, se llevaron a cabo análisis para explorar las relaciones entre las variables numéricas y categóricas en los conjuntos de datos. Este proceso incluyó la identificación de valores atípicos o anomalías (que no necesariamente son errores) y la búsqueda de patrones o conocimientos que pudieran ser útiles en análisis posteriores.

### Análisis de Datos

- **Análisis de Distribución del Número de Víctimas por Mes**
Se analizó la distribución del número de víctimas en función de los meses utilizando un diagrama de caja (boxplot). Este tipo de visualización nos permite identificar puntos atípicos que indican eventos excepcionales en nuestros datos. A continuación, se presentan las principales conclusiones derivadas de este análisis:

![Distribución del Número de Víctimas Por Mes]/Distribución_de_Edad_de_Víctimas_por_Género.png


Meses con Puntos Atípicos (2, 3, 4 y del 8 al 12):** Hemos identificado puntos atípicos en varios meses, específicamente en los meses 2, 3, 4 y en los meses del 8 al 12. Estos puntos atípicos sugieren que en estos períodos se produjeron eventos inusuales con un número inusualmente alto de víctimas en comparación con otros meses.

   - Mes 3 (Marzo) con 3 Víctimas:** El mes de marzo se destaca con un punto atípico que registra 3 víctimas en un solo evento. Este hallazgo señala un suceso singular que merece una atención especial y un análisis detallado para comprender sus causas y tomar medidas adecuadas.

   - Meses con 2 Víctimas (2, 3, 4 y del 8 al 12):** Además, hemos observado la presencia de puntos atípicos en varios meses que muestran 2 víctimas en eventos particulares. Estos meses también requieren un análisis adicional para investigar los eventos excepcionales que podrían haber contribuido a estos resultados.

En resumen, la identificación de puntos atípicos en la distribución del número de víctimas por mes resalta la existencia de eventos inusuales con un alto número de víctimas en momentos específicos del año. Este análisis puede ser fundamental para comprender patrones y tendencias en la seguridad vial y orientar decisiones y acciones en materia de prevención de accidentes.

- **Análisis de Distribución de Edad de Víctimas por Género**
Observamos un gráfico que representa dos histogramas superpuestos en un mismo eje. Esto se hace para facilitar la comparación visual entre las edades de las víctimas de ambos sexos.

![Distribución de Edad de Víctimas por Género](/Distribución_de_Edad_de_Víctimas_por_Género.png)

   - Los resultados del gráfico revelan que las víctimas de sexo masculino tienden a tener edades comprendidas principalmente entre los 20 y los 40 años. Por otro lado, las víctimas de sexo femenino presentan una distribución más dispersa, con edades que se concentran en los grupos de 40, 60 y 80 años.

En resumen, el análisis de edades de las víctimas sugiere diferencias significativas entre los sexos, con los hombres siendo más jóvenes en promedio y las mujeres abarcando un rango de edades más amplio en los incidentes viales.

### Indicadores Clave de Rendimiento (KPIs)

Tras el análisis exploratorio, se calcularon los KPIs en Power BI utilizando el conjunto de datos "Siniestros" y los datos del sitio web oficial de la Ciudad de Buenos Aires ("Comunas"). Se creó un panel para presentar el informe y la visualización de datos de manera interactiva.

### **KPIs Propuestos**

Puedes agregar una sección en tu archivo README para describir los KPIs que has calculado y explicar por qué son relevantes en el contexto de tu análisis de seguridad vial. Aquí tienes un ejemplo de cómo podrías estructurar esa sección:

## KPIs de Seguridad Vial

En este proyecto de análisis de seguridad vial, se han calculado una serie de Indicadores Clave de Desempeño (KPIs) para evaluar y comprender la situación de seguridad vial en nuestra región. A continuación, se presentan los KPIs y se proporciona una breve explicación de por qué son importantes:

### Tasa de Accidentes Viales

   **Tasa de Accidentes Viales:** Este KPI nos permite evaluar la frecuencia de accidentes en relación con la cantidad de vehículos en circulación o la longitud de las carreteras. Es esencial para comprender la densidad de accidentes en nuestras carreteras y su variación a lo largo del tiempo.

   **Tasa de Víctimas en Accidentes Viales:** Similar a la tasa de accidentes, esta métrica nos ayuda a evaluar la seguridad vial en función de las víctimas involucradas. Puede arrojar luz sobre la gravedad de los accidentes y la eficacia de las medidas de seguridad.

### KPIs de Gravedad de Incidentes

   **Tasa de Mortalidad Vial:** Este indicador nos permite evaluar el número de fallecimientos en accidentes viales en relación con la población o la cantidad de accidentes. Es crucial para comprender la gravedad de la seguridad vial en nuestra región.

   **Tasa de Lesiones Graves:** Al igual que la tasa de mortalidad, esta métrica se enfoca en evaluar las lesiones graves en accidentes viales. Proporciona información valiosa sobre el impacto de los accidentes en la salud de las personas.

### KPIs de Edades de Víctimas

   **Distribución de Edades de Víctimas:** Este KPI nos ayuda a identificar grupos de edad particularmente afectados por los accidentes viales. Puede guiar estrategias de prevención dirigidas a grupos vulnerables.

   **Tasa de Mortalidad por Grupos de Edad:** Desglosar la tasa de mortalidad por grupos de edad nos permite comprender mejor los patrones de riesgo y adaptar las medidas de seguridad a grupos específicos.

### KPIs de Tipos de Vehículos

   **Tasa de Accidentes de Motocicletas:** Dado el aumento de motocicletas en nuestras carreteras, esta métrica evalúa la seguridad de este grupo de vehículos en particular.

   **Tasa de Accidentes de Vehículos Pesados:** Los vehículos pesados pueden representar un riesgo adicional en carreteras. Este KPI evalúa la frecuencia de accidentes con estos vehículos.

### KPIs de Días y Horarios de Mayor Riesgo

   **Tasa de Accidentes en Días de Fin de Semana:** Identificar los días de mayor riesgo nos permite enfocar la aplicación de medidas preventivas en momentos específicos de la semana.

   **Tasa de Accidentes en Horas Pico:** Evaluar las horas de mayor tráfico es crucial para comprender los momentos de mayor riesgo en nuestras carreteras.

Cada uno de estos KPIs proporciona información valiosa sobre la seguridad vial en nuestra región y puede guiar estrategias y políticas para reducir accidentes y mejorar la seguridad en nuestras carreteras.

## Uso

- Puedes utilizar el conjunto de datos proporcionado, "siniestros_clean.csv", para análisis o visualización adicionales.
- El panel de Power BI está disponible para exploración interactiva de datos.

## Agradecimientos

- Fuente de datos: [Gobierno de la Ciudad de Buenos Aires](https://www.buenosaires.gob.ar/movilidad/observatorio-de-movilidad-y-seguridad-vial/datos-oficiales)

## Contacto

Para consultas, por favor contacta a [María García](mailto:data.mariagarcia@gmail.com) [Perfíl LinkedIn](https://www.linkedin.com/in/mariagarciarubio/).
