# Tienda Inglesa

Proyecto sobre Tienda Inglesa EDA y visualizaciones listos para Power BI y trabajo en Python.

Resumen rápido
- Dataset: `TiendaInglesa:PowerBi/train 2.csv` (~9.800 filas, 22 columnas).
- Análisis: `TiendaInglesa:PowerBi/BBDD.eda.ipynb` (notebook Jupyter con análisis exploratorio y gráficos).
- Imagen de apoyo: `TiendaInglesa:PowerBi/Sin título-2025-11-24-2120.png`.


Este proyecto recopila un dataset tipo "Sample - Superstore" (pedidos y ventas) para explorar comportamiento de ventas, estacionalidad, rendimiento por categoría y preparación de dashboards en Power BI.

Qué encontrarás (ejemplos de columnas)
- `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`
- `Customer ID`, `Customer Name`, `Segment`, `Region`
- `Product ID`, `Category`, `Sub-Category`, `Product Name`, `Sales`

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

Ideas rápidas para análisis (valor inmediato)
- Ventas por año/mes y por `Region`.
- Top productos y categorías por ventas y margen (si se añade columna de coste).
- Tiempo entre `Order Date` y `Ship Date` (lead time) y su impacto en satisfacción/segmento.

