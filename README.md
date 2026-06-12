# ETL Pipeline — Consolidación de datos de monitoreo de campo

Pipeline de ETL en Python que extrae datos operativos de captura manual desde Google Sheets, los limpia y transforma, y los entrega en un formato analítico (tabular) listo para análisis y visualización.

## El problema

Los datos de monitoreo de campo se capturan manualmente en Google Sheets, en un formato pensado para el registro, no para el análisis: _(describe el problema real, por ejemplo: múltiples hojas, encabezados inconsistentes, fechas en distintos formatos, datos sin normalizar)_. Eso hace difícil consolidarlos y analizarlos a tiempo. Este pipeline automatiza esa consolidación y deja los datos listos para usar.

> **Nota:** este proyecto usa datos de ejemplo / simulados. No contiene información confidencial de ninguna organización.

## Qué hace (flujo ETL)

1. **Extracción (Extract):** lee los datos desde Google Sheets _(vía la API de Google Sheets / exportación a CSV)_.
2. **Transformación (Transform):** limpia y normaliza la información — _(maneja valores faltantes, unifica formatos de fecha, consolida varias hojas en una sola tabla, valida tipos de datos)_.
3. **Carga (Load):** entrega un dataset tabular _(en CSV / base de datos)_ listo para Power BI o cualquier herramienta de análisis.

## Tecnologías

- **Python** — _(pandas, gspread / google-api-python-client, etc.)_
- **Google Sheets** — fuente de datos
- _(otras librerías que hayas usado)_

## Estructura del repositorio

```
├── src/            → código del pipeline (etl.py)
├── data/           → datos de ejemplo (entrada y salida)
└── README.md
```

## Cómo ejecutarlo

```bash
pip install -r requirements.txt
python src/etl.py
```

## Ejemplo

**Entrada** 
<img width="958" height="413" alt="image" src="https://github.com/user-attachments/assets/d58bf301-8e29-434c-a8cd-bfbdbd757bd5" />


**Salida** 
<img width="959" height="503" alt="image" src="https://github.com/user-attachments/assets/3125d0d1-ebc4-40c8-9f96-d61ebef717a2" />



## Resultado

_(En una o dos frases: qué se ganó. Ejemplo: "Reduce de X a Y el tiempo de consolidación de los datos y elimina los errores de copiado manual.")_

## Sobre mí

**Emilio Zuluaga Gutiérrez** — Analista de Datos con enfoque financiero. Ingeniero industrial con especialización en finanzas. Construyo pipelines, tableros e indicadores que traducen los datos en decisiones.

- Correo: emzuluaga@unal.edu.co
- LinkedIn: https://linkedin.com/in/emilio-zuluaga
