# Análisis de Uso de Servicios de Telecomunicaciones

## Descripción General

Este proyecto tiene como objetivo analizar los patrones de uso de los servicios ofrecidos por una empresa de telecomunicaciones a partir de la información de sus clientes suscritos. El análisis considera variables demográficas, el nivel de suscripción contratado y la interacción de los usuarios con los servicios de llamadas y mensajería durante un período determinado.

A partir de este estudio se busca identificar segmentos de clientes, patrones de consumo y oportunidades de mejora que permitan optimizar la oferta de servicios y fortalecer las estrategias de captación y fidelización de usuarios.

## Objetivos del Proyecto

### Objetivo General

Analizar la distribución y los patrones de uso de los servicios ofrecidos por la empresa considerando la edad de los clientes, el nivel de suscripción contratado y el uso registrado de los servicios de llamadas y mensajería.

### Objetivos Específicos
1- Evaluar la calidad de los datos proporcionados.
2- Identificar y tratar valores faltantes, valores centinela y registros fuera de rango.
3- Caracterizar el comportamiento de los usuarios mediante estadísticas descriptivas y visualizaciones.
4- Segmentar a los clientes según criterios demográficos y de uso.
5- Analizar las diferencias entre los planes de suscripción.
6- Generar recomendaciones de negocio basadas en los resultados obtenidos.

## Conjuntos de Datos Utilizados

### users.csv

Contiene información relacionada con los clientes suscritos a la plataforma, incluyendo:

1- Identificador único del cliente.
2- Ciudad asociada al usuario.
3- Plan de suscripción contratado.
4- Información demográfica como la edad.

### usage.csv

Contiene información sobre el uso de los servicios ofrecidos por la empresa:

1- Cantidad de mensajes enviados.
2- Servicio efectuado
3- Cantidad de llamadas realizadas.
4- Duración de las llamadas.
5- Fecha de utilización del servicio.

La relación entre los registros de uso y los clientes se establece mediante el identificador único de cada usuario.

### plans.csv

Contiene información sobre los planes de suscripción disponibles y las características asociadas a cada uno de ellos.

## Tecnologías Utilizadas
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook

## Metodología de Trabajo
### 1. Carga de Datos

Se realizó la importación de los conjuntos de datos proporcionados para su posterior procesamiento.

### 2. Limpieza y Preparación de Datos

Durante esta etapa se identificaron:

Valores faltantes.
Valores centinela.
Registros fuera del rango temporal de estudio.
Valores atípicos.

Las acciones realizadas incluyeron:

Sustitución del valor centinela -999 en la variable edad mediante la mediana de la distribución.
Reemplazo del valor centinela ? en la variable ciudad por valores nulos.
Exclusión de registros con fechas fuera del período de análisis.
Evaluación de valores atípicos presentes en las variables de uso.

### 3. Análisis Exploratorio de Datos (EDA)

Se analizaron las siguientes variables:

Edad de los usuarios.
Cantidad de mensajes enviados.
Cantidad de llamadas realizadas.
Minutos acumulados de llamadas.

Se emplearon:

Estadísticas descriptivas.
Histogramas.
Diagramas de caja (Boxplots).
Distribuciones por tipo de plan.

### 4. Segmentación de Clientes
Segmentación por Edad
Jóvenes: menores de 30 años.
Adultos: entre 30 y 60 años.
Adultos mayores: mayores de 60 años.
Segmentación por Uso
Bajo uso.
Uso medio.
Alto uso.

La clasificación se realizó utilizando la cantidad de mensajes enviados y llamadas realizadas por cada usuario.

### 5. Generación de Recomendaciones

A partir de los hallazgos obtenidos se formularon recomendaciones orientadas a:

Incrementar la captación de usuarios jóvenes.
Mejorar la propuesta de valor del plan Premium.
Identificar oportunidades de crecimiento comercial.

## Principales Hallazgos
### Distribución de Clientes
El plan Básico concentra la mayor cantidad de suscriptores.
Los adultos representan el segmento predominante dentro de la base de clientes.
Los jóvenes constituyen el segmento menos representado.
### Uso de los Servicios
La mayoría de los usuarios presenta un nivel de uso medio.
No se observan diferencias significativas en los patrones de uso entre los planes Básico y Premium.
Los usuarios de alto uso representan una proporción reducida de la muestra.
### Valores Atípicos
Se identificaron valores atípicos en llamadas, mensajes y minutos acumulados.
Los valores atípicos asociados a minutos acumulados presentan una separación considerable respecto al comportamiento general de la muestra y fueron evaluados de forma independiente.

### Recomendaciones
Diseñar estrategias de captación orientadas al segmento joven.
Desarrollar promociones y servicios específicos para usuarios con alta interacción.
Evaluar la estructura de precios y beneficios del plan Premium para incrementar su atractivo.
Analizar de forma independiente los usuarios con patrones de consumo atípicos.

## Ejecución del Proyecto
### Google Colab
1- Abrir Google Colab.
2- Cargar el archivo .ipynb alojado en el repositorio de Github.
3- Subir los archivos users.csv, usage.csv y plans.csv.
4- Ejecutar todas las celdas del notebook.

## Guía de Reproducción
1- Cargar los conjuntos de datos.
2- Ejecutar la limpieza y depuración de datos.
3- Crear las variables derivadas y segmentos de clientes.
4- Generar las estadísticas descriptivas.
5- Ejecutar las visualizaciones.
6- Revisar las conclusiones y recomendaciones obtenidas.

## Autor
Ernesto Molina Santana
