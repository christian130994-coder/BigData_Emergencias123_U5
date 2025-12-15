# Unidad 5 – Big Data Emergencias 123

## Descripción del proyecto
Este proyecto implementa un pipeline de Big Data usando PySpark para el análisis
de llamadas de emergencia 123.  
El pipeline procesa un dataset consolidado de más de 24 meses y genera agregados
optimizados que alimentan un dashboard interactivo en Plotly.

---

## Instrucciones de despliegue

### Requisitos
- Google Colab
- Python 3
- PySpark
- Pandas
- Plotly

### Pasos de ejecución
1. Abrir el notebook `Pipeline_BigData_Emergencias123_U5.ipynb`
2. Montar Google Drive
3. Ejecutar todas las celdas del pipeline
4. Verificar la generación de archivos en la carpeta `U5_output`
5. Abrir el notebook `Visualización emergencias 123.ipynb`
6. Ejecutar el dashboard usando los CSV generados por el pipeline

---

## Justificación técnica de optimizaciones

- Se utiliza **broadcast join** para tablas pequeñas como la dimensión de prioridad,
  reduciendo el costo de los joins.
- El DataFrame principal se **particiona por ANIO_MES** para optimizar agregaciones
  temporales.
- Se aplica **persistencia en memoria y disco** únicamente al DataFrame que se reutiliza
  en múltiples agregaciones.
- Se proyectan únicamente las columnas necesarias para reducir el uso de memoria.

---

## Evidencia de ejecución

El pipeline fue ejecutado correctamente en un entorno Spark.
Se adjunta captura de pantalla donde se evidencia la ejecución del pipeline y los tiempos
de procesamiento obtenidos.

## Evidencia de ejecución

![Pipeline ejecutado]

