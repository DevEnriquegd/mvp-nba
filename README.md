# 🏀 MVP NBA — NBA Player Stats Analysis (Jupyter)

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Tech](https://img.shields.io/badge/Tech-Python%20%7C%20pandas%20%7C%20numpy%20%7C%20Jupyter-blue)
![Data](https://img.shields.io/badge/Data-Exploratory%20Analysis-orange)

---

Este repositorio contiene un notebook de análisis exploratorio de estadísticas de jugadores de la NBA (`mvp_nba.ipynb`) y el dataset `all_seasons.csv` usado para calcular líderes por estadística, comparaciones por era y un índice ponderado de "MVP" por temporada.

El notebook realiza: carga de datos, limpieza mínima, identificación de líderes por puntos/rebotes/assists, cálculo de métricas normalizadas, creación de un `MVP_Index` ponderado y reportes por era/posición/equipo.

---

## 🎯 Objetivo del proyecto

Explorar el dataset de temporadas para identificar tendencias en rendimiento individual y de equipo, evaluar eficiencia (TS%), impacto en net rating y proponer un índice objetivo que permita comparar candidatos a "Data MVP" por temporada.

Preguntas principales abordadas:

- ¿Quién lidera cada temporada en puntos, rebotes y asistencias?
- ¿Qué tan eficientes son los líderes (True Shooting %)?
- ¿Cómo cambian tamaño/estilo/producción por era (1990s, 2000s, 2010s, 2020s)?
- ¿Qué jugadores obtienen mayor impacto según `net_rating` y un índice combinado (MVP_Index)?

---

## 📁 Estructura del repositorio

```
├── mvp_nba.ipynb         # Notebook principal (análisis EDA y reportes)
├── all_seasons.csv       # Dataset (puntos, rebotes, asistencias, ts_pct, usg_pct, net_rating, etc.)
├── requirements.txt      # Dependencias Python mínimas
├── create_env.ps1        # Script PowerShell para crear .venv e instalar dependencias
├── .gitignore            # Ignorar .venv y artefactos
└── README.md
```

---

## 📈 Resumen de análisis y resultados (breve)

- Identificación de líderes por temporada en `pts`, `reb`, `ast`.
- Ranking de eficiencia de anotadores usando `ts_pct` (umbral elite/riesgo en notebook).
- Evaluación de impacto defensivo/ofensivo con `net_rating` para rebounders.
- Clasificación de creadores (`ast_pct`) y detección de jugadores de alta creación.
- Segmentación por era basada en la temporada (1990s, 2000s, 2010s, 2020s).
- Cálculo de `MVP_Index` normalizado y selección del `Data MVP` por temporada.

---

## ⚙️ Cómo ejecutar (Windows PowerShell)

```pwsh
# Crear y activar entorno
python -m venv .venv
& '.\.venv\Scripts\Activate.ps1'

# Instalar dependencias
& '.\.venv\Scripts\python.exe' -m pip install -r requirements.txt

# Ejecutar el notebook (desde la carpeta del repo)
jupyter notebook mvp_nba.ipynb
```

Si usas otra plataforma o `conda` puedo generar un `environment.yml` opcional.

---

## 📝 Notas y reproducibilidad

- `requirements.txt` contiene las dependencias mínimas detectadas en el notebook. Para fijar versiones exactas puedes ejecutar `pip freeze > requirements.txt` dentro del entorno y compartir el resultado.
- El notebook carga el CSV desde `all_seasons.csv` (o desde la URL remota si prefieres usar la versión en GitHub). Asegúrate de tener conexión si usas la URL.

---

## ✨ Autor

Proyecto desarrollado por **Enrique**. Para preguntas o mejoras, abre un Issue o PR.
