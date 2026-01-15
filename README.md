# 📊 Análisis de Datos – Tienda Inglesa

Proyecto de **Análisis Exploratorio de Datos (EDA)** basado en un dataset de tipo *Sample Superstore*, enfocado en el estudio del comportamiento de ventas, estacionalidad y rendimiento por categoría.  
El análisis está orientado a la **preparación de datos y visualizaciones para Power BI**, combinando trabajo en **Python** y **Jupyter Notebook**.

Este repositorio forma parte de mi portfolio como **Analista de Datos Junior**, con foco en visualización, análisis y comunicación de insights.

---

## 📌 Resumen del Proyecto

- **Dataset:** `TiendaInglesa:PowerBi/train 2.csv`  
  (~9.800 filas, 22 columnas)
- **Análisis principal:**  
  `TiendaInglesa:PowerBi/BBDD.eda.ipynb` (EDA completo con gráficos)
- **Imagen de apoyo:**  
  `TiendaInglesa:PowerBi/Sin título-2025-11-24-2120.png`

El dataset contiene información de pedidos y ventas (clientes, productos, fechas, regiones y segmentos), lo que permite analizar patrones comerciales y preparar dashboards orientados a negocio.

---

## 🧠 Objetivos del Análisis

- Comprender la estructura y calidad del dataset.
- Analizar el comportamiento de ventas a lo largo del tiempo.
- Evaluar el rendimiento por **categoría**, **subcategoría** y **región**.
- Detectar patrones de estacionalidad.
- Preparar datos limpios y estructurados para su uso en **Power BI**.
- Generar visualizaciones claras y accionables.

---

## 🧰 Tecnologías y herramientas utilizadas

- **Python**
  - pandas (manipulación y limpieza de datos)
  - matplotlib & seaborn (visualización)
- **Jupyter Notebook**
  - Análisis exploratorio paso a paso
- **Power BI**
  - Preparación de datos para dashboards y reporting
- **Git / GitHub**
  - Versionado y documentación del proyecto

---

## 📁 Estructura del Proyecto

Primeros pasos (rápido)
1. Clona el repo y navega a la carpeta raíz.
2. Crea un entorno Python e instala las dependencias básicas:

```bash
python -m venv .venv
source .venv/bin/activate  # zsh / bash
pip install --upgrade pip
pip install pandas matplotlib seaborn jupyterlab
```

3. Abre el notebook para explorar el EDA:

```bash
jupyter lab "TiendaInglesa:PowerBi/BBDD.eda.ipynb"
```

Tips técnicos específicos
- Al leer fechas con pandas especifica dayfirst:

```py
import pandas as pd
df = pd.read_csv('TiendaInglesa:PowerBi/train 2.csv', parse_dates=['Order Date','Ship Date'], dayfirst=True)
```

- Si hay problemas con caracteres, prueba `encoding='latin-1'`.
- Observación: la carpeta contiene dos puntos (`:`) en su nombre; esto puede provocar problemas en Windows o al exportar. Recomendado renombrarla a `TiendaInglesa-PowerBi` si se comparte fuera de macOS.


📊 Ejemplos de análisis realizados

Ventas por año/mes y por `Region`.
Top productos y categorías por ventas y margen (si se añade columna de coste).
Comparativa de ventas por región.
Análisis de rendimiento por categoría y subcategoría.
Identificación de productos con mayor volumen de ventas.

---



Lucía Tejera
 
Analista de Datos Junior
 
LinkedIn: https://linkedin.com/in/lucia-tejera

## 📊 Power BI Dashboard

[![View Power BI Dashboard](https://img.shields.io/badge/View%20Dashboard-Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://app.powerbi.com/groups/71eddc4f-25bd-4d3f-a741-229717deea63/reports/0cfec1fc-1696-4e80-a6f7-825c4ae84e2c/01d379cfb5a220e75723?experience=power-bi)

