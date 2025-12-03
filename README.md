# 📈 Bitcoin Price Prediction using Machine Learning

> **Trabajo Práctico - Machine Learning**

Este proyecto, realizado para la Materia Machine Learning, aborda el desafío de predecir el precio futuro de Bitcoin en un horizonte de 7 días. Se implementó un flujo de trabajo completo de Ciencia de Datos, desde la ingeniería de características con indicadores técnicos hasta la optimización de hiperparámetros y evaluación en datos no vistos (Test Set).

## Key Features

* **Ingeniería de Características:** Generación de indicadores técnicos (RSI, MACD, Bandas de Bollinger, ATR) y variables de lag utilizando `pandas-ta`.
* **Análisis Exploratorio (EDA):** Estudio de correlaciones con mercados tradicionales (S&P 500, Nasdaq), estacionalidad semanal y análisis de sentimiento (Fear & Greed Index).
* **Modelos Implementados:**
    * **K-Nearest Neighbors (KNN):** Regresión basada en instancias.
    * **Random Forest:** Ensemble learning con optimización de profundidad y estimadores.
    * **Regresión Ridge:** Modelo lineal con regularización L2.
    * **Redes Neuronales (Deep Learning):** Arquitectura densa optimizada con **Keras Tuner**.
* **Metodología Rigurosa:** Separación estricta de datos en *Train* (Entrenamiento), *Validation* (Ajuste de Hiperparámetros) y *Test* (Evaluación Final) respetando el orden temporal.

## Tech Stack
* **Lenguaje:** Python 3.13
* **Librerías Principales:**
    * `pandas` & `numpy`: Manipulación de datos.
    * `scikit-learn`: Modelado y preprocesamiento (Pipelines, ColumnTransformer).
    * `tensorflow` / `keras`: Redes Neuronales.
    * `keras-tuner`: Búsqueda de hiperparámetros para la red neuronal.
    * `pandas_ta`: Cálculo de indicadores técnicos financieros.
    * `yfinance`: Extracción de datos históricos.
    * `matplotlib` & `seaborn`: Visualización de datos.

## Estructura del Proyecto

El análisis se divide en notebooks específicos para cada etapa y modelo:

1.  `analisis_exploratorios`: Carga de datos, limpieza, cálculo de indicadores y EDA.
2.  `modelo_RL`: Implementación y optimización de Regresión Lineal (Ridge).
3.  `modelo_KNN`: Implementación de KNN con escalado de variables.
4.  `modelo_Random_Forest`: Entrenamiento de Random Forest con búsqueda de grilla (GridSearch).
5.  `modelo_RN`: Diseño y tuning de Red Neuronal Artificial (ANN).

## Resultados y Metodología

Para garantizar una evaluación honesta, se utilizaron las siguientes métricas sobre el conjunto de **Test** (datos nunca vistos por el modelo durante el ajuste):

* **RMSE (Root Mean Squared Error):** Para penalizar grandes errores.
* **MAPE (Mean Absolute Percentage Error):** Para interpretabilidad del error en porcentaje.

*Se observó que los modelos de ensamble (Random Forest) y la Regresion Lineal obtuvieron los mejores resultados en distintos horizontes de tiempo, +1 dia para Regresion Lineal y +2 a +7 dias para Random Forest.*

---
