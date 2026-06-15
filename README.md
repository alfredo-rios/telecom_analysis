# Proyecto: Análisis de Clientes de Telecomunicaciones - ConnectaTel

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones con operaciones en México y Colombia.

A través de técnicas de limpieza, exploración y análisis de datos, se estudian los patrones de uso de llamadas y mensajes de los usuarios para identificar segmentos de clientes, detectar comportamientos atípicos y generar recomendaciones que ayuden a optimizar la oferta comercial y mejorar la experiencia del cliente.

---

## Objetivos del Análisis

* Evaluar la calidad de los datos y corregir inconsistencias.
* Analizar el comportamiento de uso de llamadas y mensajes.
* Detectar valores atípicos (outliers) que puedan representar usuarios de alto consumo o posibles errores de captura.
* Segmentar clientes según edad y nivel de uso.
* Identificar oportunidades para mejorar los planes actuales y diseñar nuevas estrategias comerciales.

---

## Datasets Utilizados

### 1. plans.csv

Contiene información sobre los planes de telefonía disponibles:

* Nombre del plan
* Precio mensual
* Minutos incluidos
* Datos incluidos
* Costos por excedente

### 2. users_latam.csv

Contiene información demográfica y contractual de los clientes:

* user_id
* first_name
* last_name
* age
* city
* reg_date
* plan
* churn_date

### 3. usage.csv

Contiene el historial de actividad de los usuarios:

* user_id
* type (call o text)
* duration
* length
* date

---

## Etapas del Análisis

### 1. Exploración Inicial de los Datos

* Revisión de estructura y tipos de datos.
* Identificación de valores nulos.
* Detección de posibles errores de captura.

### 2. Limpieza y Preparación de Datos

* Corrección de valores centinela (-999).
* Tratamiento de valores inválidos en ciudades.
* Conversión de columnas de fecha.
* Identificación y corrección de fechas fuera de rango.
* Validación de valores nulos dependientes del tipo de actividad.

### 3. Análisis Estadístico

* Resumen estadístico de variables numéricas.
* Distribución de variables categóricas.
* Análisis descriptivo del comportamiento de los usuarios.

### 4. Agregación de Métricas por Usuario

Creación de indicadores de comportamiento:

* Cantidad de mensajes enviados.
* Cantidad de llamadas realizadas.
* Minutos totales de llamadas.

### 5. Visualización de Datos

* Histogramas.
* Boxplots.
* Análisis de distribuciones.
* Comparación entre planes.

### 6. Detección de Outliers

Aplicación del método IQR para identificar valores extremos en:

* Cantidad de mensajes.
* Cantidad de llamadas.
* Minutos totales de llamadas.

### 7. Segmentación de Clientes

Segmentación por:

#### Nivel de Uso

* Bajo uso
* Uso medio
* Alto uso

#### Edad

* Joven
* Adulto
* Adulto Mayor

### 8. Generación de Insights de Negocio

Interpretación de resultados y elaboración de recomendaciones para ConnectaTel.

---

## Principales Hallazgos

* La mayoría de los usuarios pertenece al segmento de uso medio.
* Los adultos representan el grupo de edad más numeroso.
* Se identificaron usuarios con consumos significativamente superiores al promedio.
* Los valores atípicos observados corresponden a comportamientos reales de uso y no a errores de captura.
* Existen oportunidades para diseñar planes dirigidos a usuarios de alto consumo.

---

## Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Cómo Ejecutar el Proyecto

### Google Colab

1. Descarga el archivo `.ipynb` del repositorio.
2. Ingresa a Google Colab.
3. Selecciona **Archivo > Subir notebook**.
4. Carga el notebook.
5. Sube los archivos:

   * plans.csv
   * users_latam.csv
   * usage.csv
6. Ejecuta las celdas en orden.


## Guía de Reproducción

Para reproducir completamente el análisis:

1. Colocar los tres datasets dentro de la carpeta correspondiente del proyecto.
2. Ejecutar las secciones del notebook en el siguiente orden:

   * Carga de datos
   * Exploración inicial
   * Limpieza de datos
   * Análisis descriptivo
   * Agregación por usuario
   * Visualizaciones
   * Detección de outliers
   * Segmentación de clientes
   * Conclusiones e insights
3. Verificar que todas las bibliotecas estén instaladas antes de ejecutar el notebook.

---

## Autor del Análisis
Alfredo Rios

Proyecto desarrollado como parte de un ejercicio de análisis de datos enfocado en limpieza, exploración, visualización, segmentación de clientes y generación de insights de negocio utilizando Python.
