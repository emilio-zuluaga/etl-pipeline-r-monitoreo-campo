# etl-pipeline-r-monitoreo-campo
Pipeline ETL en python que consolida datos operativos de captura manual en Google Sheets a formato analítico (tabular)


ETL Pipeline — Consolidación de datos de monitoreo de campo

Pipeline de ETL en Python que extrae datos operativos de captura manual desde Google Sheets, los limpia y transforma, y los entrega en un formato analítico (tabular) listo para análisis y visualización.

El problema

Los datos de monitoreo de campo se capturan manualmente en Google Sheets, en un formato pensado para el registro, no para el análisis: (describe el problema real, por ejemplo: múltiples hojas, encabezados inconsistentes, fechas en distintos formatos, datos sin normalizar). Eso hace difícil consolidarlos y analizarlos a tiempo. Este pipeline automatiza esa consolidación y deja los datos listos para usar.


Nota: este proyecto usa datos de ejemplo / simulados. No contiene información confidencial de ninguna organización.



Qué hace (flujo ETL)


Extracción (Extract): lee los datos desde Google Sheets (vía la API de Google Sheets / exportación a CSV).
Transformación (Transform): limpia y normaliza la información — (maneja valores faltantes, unifica formatos de fecha, consolida varias hojas en una sola tabla, valida tipos de datos).
Carga (Load): entrega un dataset tabular (en CSV / base de datos) listo para Power BI o cualquier herramienta de análisis.


Tecnologías


Python — (pandas, gspread / google-api-python-client, etc.)
Google Sheets — fuente de datos
(otras librerías que hayas usado)


Estructura del repositorio

├── src/            → código del pipeline (etl.py)
├── data/           → datos de ejemplo (entrada y salida)
└── README.md

Cómo ejecutarlo

bashpip install -r requirements.txt
python src/etl.py
