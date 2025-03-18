# 🗓 Predicción de Ausencias con Redes Neuronales

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.9%2B-orange)](https://www.tensorflow.org/)
[![Optuna](https://img.shields.io/badge/Optuna-Hyperparameter%20Tuning-purple)](https://optuna.org/)
[![Plotly](https://img.shields.io/badge/Plotly-Visualization-success)](https://plotly.com/)

## 📖 Introducción

Este proyecto tiene como objetivo **predecir la cantidad de ausencias** de empleados utilizando un modelo de **red neuronal** optimizado con **Optuna**. Se entrenó la red con datos históricos de Recursos Humanos, ajustando los hiperparámetros para maximizar su rendimiento.

El modelo fue evaluado utilizando métricas como **Mean Squared Error (MSE)**, **Mean Absolute Error (MAE)** y **R² Score**, junto con visualizaciones interactivas para facilitar la interpretación de los resultados.

---

## 🤝 Integrantes del Equipo

- **Carolina Salas (ericka.salas@ulead.ac.cr)**
- **Kristhel Porras (kristhel.porras@ulead.ac.cr)**

---

## 📌 Metodología del Proyecto

### **🔹 1. Preprocesamiento de Datos**
✔️ Conversión de fechas y tratamiento de valores nulos.  
✔️ Normalización de características numéricas.  
✔️ Transformación de variables categóricas con One-Hot Encoding.  
✔️ División en **80% entrenamiento y 20% prueba**.

### **🔹 2. Optimización de Hiperparámetros con Optuna**
✔️ Optimización de:  
   - **Tasa de aprendizaje (`learning_rate`)**  
   - **Tamaño del batch (`batch_size`)**  
   - **Número de épocas (`epochs`)**  
✔️ Se probaron múltiples combinaciones para encontrar la mejor configuración.

### **🔹 3. Entrenamiento de la Red Neuronal**
✔️ **Arquitectura del Modelo:**
   - Capas ocultas: **256 → 128 → 64 neuronas** con activación **ReLU**.
   - Capa de salida: **1 neurona con activación lineal** (problema de regresión).
✔️ **Función de pérdida:** Mean Squared Error (MSE).  
✔️ **Optimizador:** Adam.  
✔️ **Regularización:** Uso de **EarlyStopping** para evitar sobreajuste.  

### **🔹 4. Evaluación del Modelo**
✔️ Cálculo de métricas **MSE, MAE y R² Score**.  
✔️ Visualización de resultados con **gráficos interactivos** en Plotly:
   - **Comparación entre valores reales y predichos** 📊
   - **Distribución de errores** 📉
   - **Curva de residuos** 🔄
   - **Evolución de la pérdida y MAE** 📈

---

## 📊 Reflexión Final del Equipo

### 🔹 **Uso Inteligente de los Recursos Computacionales**
La cantidad de **trials en Optuna** afecta directamente el **tiempo y los recursos computacionales**. En lugar de probar valores arbitrarios, es recomendable utilizar **Grid Search** o incluso **algoritmos genéticos** para encontrar configuraciones óptimas sin desperdiciar capacidad de cómputo.

### 🔹 **Visualizaciones Interactivas Facilitan la Interpretación**
Las gráficas interactivas permiten **comprender mejor los resultados** y detectar posibles problemas en el modelo. Herramientas como **Plotly** facilitan la identificación de patrones y errores de predicción.

### 🔹 **El Overfitting es un Riesgo Constante**
El uso de **EarlyStopping** fue clave para evitar el sobreajuste. Sin embargo, ajustar la arquitectura del modelo y la cantidad de datos de entrenamiento sigue siendo un desafío en redes neuronales.

### 🔹 **Comprender las Métricas es Fundamental**
Las métricas de rendimiento como **MSE, MAE y R² Score** son esenciales para evaluar la calidad del modelo. Entenderlas permite tomar mejores decisiones al ajustar hiperparámetros y mejorar la generalización del modelo.

---
