# Práctica – Análisis visual del mercado de fichajes

Este proyecto forma parte de la Práctica de la asignatura M2.859 – Visualización de datos del Máster en Ciencia de Datos de la UOC.

El objetivo es construir una narrativa visual interactiva sobre el mercado de fichajes de fútbol profesional utilizando datos del videojuego EA Sports FC 24. El proyecto combina el procesamiento de datos en R con la creación de una historia visual en Flourish, abordando temáticas como el el sesgo posicional, la eficiencia económica, el sesgo posicional, la brecha salarial de género y el ciclo de edad.

---

## Entorno de trabajo y dependencias

| Elemento          | Descripción |
|-------------------|-------------|
| **Lenguaje** | R (Procesamiento de datos) |
| **Herramienta Visual** | Flourish Studio (Visualización interactiva) |
| **Despliegue** | GitHub Pages (`index.html` con embed de Flourish) |
| **Fuente de datos** | EA Sports FC 24 (Kaggle) |
| **Dataset utilizado** | `data/all_players.csv` (Unificado y limpio) |
| **Datasets generados** | `data/` 4 archivos CSV procesados para alimentar Flourish |

---

## Técnicas de visualización

El análisis se estructura en una historia de 4 escenas, cada una respondiendo a una pregunta clave:

| Técnica | Objetivo | Variables Clave |
|---------|----------|-----------|
| **1. Column chart (Grouped)** | **Sesgo de goles (Posiciones):** Evidenciar cómo el mercado valora económicamente mucho más los roles ofensivos frente a los defensivos. | `Posición` vs `Valor de mercado`/`Salario semanal` |
| **2. Braun Stereographic (Europe)**  | **Mapa de la eficiencia:** Identificar ligas infravaloradas (alta calidad, bajo coste) frente a ligas con sobreprecio. | `Eficiencia` vs `Salario semanal` |
| **3. Bar Chart (Grouped)** | **Brecha salarial (Género):** Comparar salarios entre hombres y mujeres controlando por nivel de habilidad para mostrar la disparidad real. | `Nivel de habilidad`, `Genero`, `Salario semanal` |
| **4. Line and Bar Chart (Stacked)** | **Ciclo de vida (Edad):** Analizar el ciclo de vida del jugador, mostrando el cruce donde el potencial cae y el valor de mercado alcanza su pico. | `Edad` vs `Potencial` & `Valor de mercado` |

---

## Estructura del Proyecto

El flujo de trabajo seguido para la realización de la práctica es el siguiente:

1.  **Datos:** Se parte de los datos originales del videojuego FC24. Debido al gran tamaño de los archivos crudos (`male_players.csv` y `female_players.csv`), estos no se incluyen en el repositorio. En su lugar, se proporciona el archivo **`data/all_players.csv`**, que contiene el conjunto de datos ya unificado, filtrado y limpio sobre el que se realiza el análisis.
2.  **Procesamiento (R):** El script `scripts/M2.859_Visualizacion_Practia_Parte_II.rmd` carga el dataset limpio, genera métricas avanzadas y exporta los 4 archivos CSV específicos para Flourish.
3.  **Visualización (Flourish):** Los CSV procesados se importan en Flourish para crear las escenas interactivas.
4.  **Publicación:** El resultado final se integra en una web estática alojada en este repositorio (GitHub Pages).

---

## Autor

Francisco Heredia Mañas

---