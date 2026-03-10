# Telecom X: Análisis de Evasión de Clientes - Alura LATAM - G9

## Descripción del Proyecto
Este repositorio contiene el desarrollo de un flujo ETL (Extract, Transform, Load) y un Análisis Exploratorio de Datos (EDA) aplicado al caso de estudio de la empresa Telecom X.
El objetivo principal es identificar patrones de fuga de clientes (Churn) utilizando herramientas de Data Science.

## Estructura del Trabajo

### 1. Extracción (Extract)
- Consumo de datos crudos en formato JSON desde una API externa mediante la librería `requests`.
- Carga inicial en un DataFrame de Pandas preservando la estructura anidada para su posterior procesamiento.

### 2. Transformación (Transform)
- Normalización de datos anidados con `json_normalize` para desglosar diccionarios de clientes, servicios y cuentas.
- Estandarización de nombres de columnas al español para mejorar la legibilidad.
- Limpieza de tipos de datos: conversión de variables de texto a numéricas y manejo de valores nulos.
- Ingeniería de variables: creación de la métrica `Cuentas_Diarias` basada en la facturación mensual.

### 3. Carga y Análisis (Load & EDA)
- Exportación del dataset procesado a un archivo CSV para asegurar la persistencia de los datos limpios.
- Análisis descriptivo de variables clave como antigüedad y cargos totales.
- Visualización de la distribución de evasión mediante gráficos de barras para identificar puntos críticos de pérdida de clientes.

## Consideraciones Técnicas Aplicadas
- Control de versiones: Uso de Git Flow con ramas específicas (`feature`, `dev`, `main`) para separar cada fase del proyecto.
- Buenas prácticas de programación: Modularización del código en el notebook y documentación técnica de los procesos.
- Enfoque orientado a negocio: Identificación de hallazgos accionables basados en el comportamiento de los contratos y servicios de internet.