
PROYECTO: DASHBOARD & ANALISIS DE DATOS

1.  Estructura del repositorio

  La estructura de carpetas es:
  
  03_DashBoard_DataProject
    |  00_DATOS_RAW -- Datos Brutos del proyecto
        |  CSV -- Extracciónes de datos de los años 2021, 2022 y 2023
          |  BCN.csv
          |  MAD.csv
          |  SEV.csv
          |  VLC.csv
          |  ZGZ.csv
    |  Download -- Extracciones en bruto de MeteoSat
          |  Barcelona.csv.gz	
          |  Madrid.csv.gz
          |  Sevilla.csv.gz
          |  Valencia.csv.gz
          |  Zaragoza.csv.gz
      |  Met_Stations_JSON.csv
      |  MeteoSat DATA Only.xlsx
      |  Tablas_Meteosat.xlsx
    |  01_DATOS_ANALISIS -- Informe y Dashboard
      |  03.Informe_EDA_Meteo.docx
      |  DS_ES_MeteoSat.xlsx
    | 03.Requisitos_Proyecto_DB.docx
    | README.md

3.  Objetivo
    Obtención de tendencias estacionales y predicción subjetiva de inclemencias meteorológicas futuras según época y zona geográfica en base a datos históricos.

5.  Descripción del Proyecto:

Transformacion y Limpieza de los Datos

Para la carga y transformación, he utilizado la herramienta Power Query que está integrada en Excel y que, aunque no dispone de todas las funcionalidades de Power BI.
Me ha ayudado a la creación de una automatización para la futura incorporación de cualquier nueva fuente (estación meteorológica), de la misma naturaleza y estructura, y que sea anexada al análisis.
Power Query ha colaborado en la eliminación de columnas vacías, adicción de alguna nueva, cambio del tipo de dato y personalización del orden de presentación. Los títulos de las columnas y tipo de dato están definidos en la página de instrucción técnica de descarga. 
El principal inconveniente de trabajar en Excel para la realización de este Dashboard es que la descarga de los datos, las tablas origen, se deben mantener en el modelo, sobrecargando el archivo para la generación de tablas dinámicas y presentación.

Análisis descriptivo de los datos.

Se han añadido columnas con valores categóricos formulados desde el set de datos que contienen: una baremación de eventos meteorológicos extremos según los datos de temperatura, lluvia y viento; la cardinalidad del viento según los grados de su dirección para la generación de una rosa de los vientos; y la estimación de nieblas según el punto de rocío y temperatura ambiente.
Como tablas para la presentación de los datos apoyo y KPIs se han desarrollado tablas dinámicas filtradas por los siguientes módulos de segmentación:

Principales KPIs:
  1.	Temperatura
    •	Temperatura media anual y mensual
    •	Top 1 de temperaturas máximas y mínimas registradas por estación
  2.	Precipitación:
    •	Precipitación media anual y mensual
    •	Top 1 de precipitaciones máximas registradas por estación relacionadas con presión atmosférica.
  3.	Viento:
    •	Velocidad media del viento
    •	Top 1 de rachas máximas de viento registradas por estación
  4.	Humedad Relativa:
    •	Humedad Relativa media.
  5.	Presión Atmosférica:
    •	Promedio de presión atmosférica.
  6.	Punto de Rocío:
    •	Promedio del punto de rocío.

Indicadores
  1.	Temperatura
    •	Gráfico de temperatura media semanal y mensual
  2.	Precipitación:
    •	Gráfico de precipitación media semanal y acumulada mensual
  3.	Viento:
    •	Dirección del viento en grafico radial (solo disponible su uso en Excel 365 para Windows)
    •	Gráfico de velocidad del viento medio semanal
  4.	Efectos meteorológicos adversos y clima extremo:
    •	Relación de efectos meteorológicos adversos: heladas, frio extremo y olas de calor.
    •	Relación de efectos meteorológicos adversos: lluvias fuertes y tormentas

3.	Conclusiones
  Siguiendo la tendencia de los años analizados podremos predecir:
  Sobre las temperaturas 
    1.	Tendencia a unos meses iniciales del Q1 más fríos: inviernos más extremos con heladas.
    2.	Una subida de temperaturas adelantada al inicio del Q2: primaveras más cálidas lo que desencadenará una floración adelantada.
    3.	Eventuales caídas y heladas a finales de la estación e inicios del verano que perjudicarán a la producción de frutales.
    4.	Veranos más cortos con temperaturas más extremas al inicio del Q3.
    5.	Existencia de una segunda temporada primaveral a finales del Q3 coincidiendo con el inicio del otoño.
    6.	Caída gradual de los termómetros para la temporada de invierno a mediados de Q4.

  Sobre las precipitaciones:
    1.	Tendencia a las lluvias torrenciales coincidiendo con el aumento de las temperaturas en Q1, Q2 e inicio del Q3, coincidiendo con la subida de las temperaturas atípicas comentadas en el punto anterior.
    2.	Menos episodios de lluvias siendo más extremos y con evidencias de desastres mediaoambientales.
    
Sobre el viento:
  1.	No se aprecian grandes cambios respecto a la tendencia habitual.
  2.	Aumento generalizado de las rachas de viento.

Es necesario ver toda esta información contrastada con bases de datos de mayor alcance incluyendo en el informe estaciones meteorológicas globales ya que existen perturbaciones atmosféricas pasajeras que se trasladan de una manera u otra hacia otras latitudes y que afectan al resto de mediciones.
![image](https://github.com/user-attachments/assets/088ff900-ebe7-444f-b3b4-fec6f8205c5b)

6.  Herramientas utilizadas
  * MS Excel

8.  Conjunto de datos usado
  * Origen de los datos: Meteosat (https://dev.meteostat.net/bulk/#quick-start) es una plataforma abierta que proporciona acceso gratuito a datos meteorológicos y climáticos históricos.
  * Obtención del dato: Estaciones meteorológicas de algunas de las principales ciudades españolas identificadas con numero de estación del archivo JSON facilitado por la propia organización para la conexión mediante API desde cualquier web que quiera incluir su codigo.  Para la descarga directa a través del terminal se debe realizar una petición al servidor:
 
10.  Autor
  * Pedro Polo

