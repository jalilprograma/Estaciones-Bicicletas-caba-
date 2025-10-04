#  Dashboard de Estaciones de Bicicletas Públicas - CABA

Este proyecto forma parte del **Trabajo Práctico – Segundo Módulo** de Programación Avanzada en Ciencia de Datos.

---

##  Dataset
- **Fuente:** [Gobierno de la Ciudad de Buenos Aires - Nuevas estaciones de bicicletas públicas](https://data.buenosaires.gob.ar)
- **Archivo:** `nuevas-estaciones-bicicletas-publicas.csv`

---

##  Motor de base de datos
- Se utiliza **SQLite**, que no requiere instalación adicional.
- La base se genera en Google Colab directamente a partir del CSV.
- Nombre del archivo de base: `bicicletas.db`.

Para recrearla manualmente, ejecutar:

```python
import pandas as pd
import sqlite3

df = pd.read_csv("data/nuevas-estaciones-bicicletas-publicas.csv")
conn = sqlite3.connect("bicicletas.db")
df.to_sql("estaciones", conn, if_exists="replace", index=False)

La notebook dashboard_bicicletas.ipynb incluye:

 -  Carga del dataset en un DataFrame de Pandas.
 -  Creación de la base SQLite.
 -  Consultas SQL básicas.
 -  Visualizaciones interactivas con Plotly:
    -  Mapa de estaciones.
    -  Cantidad de estaciones por emplazamiento.
    -  Top de estaciones más frecuentes.
    -  Distribución de estaciones por dirección.

---------- Pasos para ejecutar--------------

Clonar este repositorio:

git clone https://github.com/usuario/bicicletas-dashboard.git
cd bicicletas-dashboard


Instalar dependencias:

pip install -r requirements.txt


Abrir la notebook en Google Colab o Jupyter:

jupyter notebook notebooks/dashboard_bicicletas.ipynb


Ejecutar todas las celdas para recrear la base de datos y generar las visualizaciones.

--------------Dependencias----------

Listado en requirements.txt:

pandas

plotly

sqlite3 (incluido en Python)

jupyter


Participantes:
Guillermo German jalil
Sabrina Ianni lucio


