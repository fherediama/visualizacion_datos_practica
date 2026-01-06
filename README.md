# Práctica – Análisis visual del mercado de fichajes (FC24)

Este proyecto forma parte de la **Práctica de la asignatura M2.859 – Visualización de datos** del Máster en Ciencia de Datos de la UOC.

El objetivo es construir una **narrativa visual interactiva** sobre el mercado de fichajes de fútbol profesional utilizando datos del videojuego EA Sports FC 24. El proyecto combina el procesamiento de datos en **R** con la creación de una historia visual (scrollytelling) en **Flourish**, abordando temáticas como la eficiencia económica, el sesgo posicional y la brecha salarial de género.

---

## Entorno de trabajo y dependencias

| Elemento          | Descripción |
|-------------------|-------------|
| **Lenguaje** | R (Procesamiento de datos) |
| **Herramienta Visual** | Flourish Studio (Visualización interactiva) |
| **Despliegue** | GitHub Pages (`index.html` con embed de Flourish) |
| **Librerías R** | `tidyverse` (dplyr, readr, tidyr) |
| **Fuente de Datos** | EA Sports FC 24 (Kaggle) |
| **Dataset del Repositorio** | `data/all_players.csv` (Dataset unificado y limpio) |
| **Datasets Generados** | 4 archivos CSV procesados para alimentar Flourish |

---

## Técnicas de Visualización

El análisis se estructura en una historia de 4 escenas, cada una respondiendo a una pregunta clave:

| Técnica | Objetivo | Variables Clave |
|---------|----------|-----------|
| **1. Bar Chart** | **Sesgo de goles (Posiciones):** Evidenciar cómo el mercado valora económicamente mucho más los roles ofensivos (delanteros) frente a los defensivos. | `General Position` vs `Avg Value` |
| **2. Europe Map ** | **Mapa de eficiencia:** Identificar ligas infravaloradas (alta calidad, bajo coste) frente a ligas con sobreprecio. | `Avg Overall` (Calidad) vs `Avg Wage` (Coste) |
| **3. Grouped Bar Chart** | **Brecha salarial (Género):** Comparar salarios entre hombres y mujeres controlando por nivel de habilidad (Tier) para mostrar la disparidad real. | `Overall Tier`, `Gender`, `Avg Wage` |
| **4. Line and Bar Chart** | **Ciclo de vida (Edad):** Analizar el ciclo de vida del jugador, mostrando el "cruce" donde el potencial cae y el valor de mercado alcanza su pico. | `Age` vs `Potential` & `Value` |

---

## Estructura del Proyecto

El flujo de trabajo seguido para la realización de la práctica es el siguiente:

1.  **Datos:** Se parte de los datos originales del videojuego FC24. Debido al gran tamaño de los archivos crudos (`male_players.csv` y `female_players.csv`), estos no se incluyen en el repositorio. En su lugar, se proporciona el archivo **`data/all_players.csv`**, que contiene el conjunto de datos ya unificado, filtrado y limpio sobre el que se realiza el análisis.
2.  **Procesamiento (R):** El script `scripts/M2.859_Visualizacion_Practia_Parte_II.rmd` carga el dataset limpio, genera métricas avanzadas (Eficiencia, Gap de Mercado) y exporta los 4 archivos CSV específicos para Flourish.
3.  **Visualización (Flourish):** Los CSV procesados se importan en Flourish para crear las escenas interactivas.
4.  **Publicación:** El resultado final se integra en una web estática alojada en este repositorio (GitHub Pages).

---

## Autor

**Francisco Heredia Mañas**

---