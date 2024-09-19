# Sistema de Recomendación de Productos - CMQ

## Descripción General

Este proyecto implementa un sistema de recomendación de productos para comercios locales, basado en el análisis de datos de transacciones y atributos de productos. El objetivo principal es sugerir productos relevantes a los clientes basándose en su historial de compras y en la popularidad de los productos dentro de la misma área geográfica.

## Estructura del Repositorio

El repositorio contiene los siguientes archivos:

- **README.md**: Documento de introducción y guía del proyecto.
- **RECOM_CMQ_SYSTEM.ipynb**: Notebook de Jupyter que contiene todo el análisis, preprocesamiento de datos, generación de características, modelado y evaluación.
- **Test-CMQ-Algosselling.docx**: Documento de pruebas y especificaciones del algoritmo.
- **atributos.csv**: Archivo que contiene los atributos de los productos.
- **transacciones.csv**: Archivo que contiene el historial de transacciones de los clientes.

## Requisitos

Para ejecutar este proyecto es necesario contar con las siguientes herramientas y bibliotecas:

- Python 3.8 o superior
- Jupyter Notebook
- Librerías necesarias: 

  - Pandas
  - Numpy
  - Matplotlib
  - Scikit-learn
  - **Plotly** (para visualizaciones interactivas)
  - **Surprise** (para el modelado de sistemas de recomendación)

Puedes instalar todas las dependencias con el siguiente comando:

```bash
pip install -r requirements.txt
```

Si no cuentas con el archivo `requirements.txt`, puedes instalar las librerías manualmente con el siguiente comando:

```bash
pip install pandas numpy matplotlib scikit-learn plotly surprise
```

## Ejecución del Proyecto

1. **Preprocesamiento de Datos**: Asegúrate de que los archivos `atributos.csv` y `transacciones.csv` estén ubicados en el mismo directorio donde ejecutarás los scripts.
   
2. **Entrenamiento del Modelo**: El notebook contiene todo el flujo de trabajo para el entrenamiento del modelo de recomendación. Puedes ejecutar cada celda secuencialmente para generar las recomendaciones.

   ```bash
   jupyter notebook RECOM_CMQ_SYSTEM.ipynb
   ```

3. **Evaluación del Modelo**: Se han implementado métricas de precisión y recall para evaluar la calidad de las recomendaciones generadas. Los resultados se muestran directamente en el notebook al final de la ejecución.

## Ejemplo de Salida

Un ejemplo de las recomendaciones generadas por el modelo:

| ACCOUNT_ID | SKU_ID | SCORE | FECHA_DE_RECOMENDACION |
|------------|--------|-------|------------------------|
| 456111     | 7651   | 5     | 2024-09-18             |
| 456111     | 6582   | 5     | 2024-09-18             |
| 456111     | 23902  | 5     | 2024-09-18             |

## Evaluación del Clustering

También se realizó un análisis de clustering para segmentar a los clientes en grupos basados en su comportamiento de compra. Los resultados agrupan a los clientes en los siguientes segmentos:

- **Clúster 0**: Compradores Ocasionales.
- **Clúster 1**: Clientes Fieles y Activos.
- **Clúster 2**: Compradores Moderados.
- **Clúster 3**: Compradores de Bajo Volumen.

## Visualizaciones

Se generaron gráficos comparativos para evaluar el rendimiento del clustering y la efectividad de las recomendaciones.
