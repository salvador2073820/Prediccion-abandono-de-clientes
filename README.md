
# Predicción de Churn de Clientes con Machine Learning

## 📌 Descripción del Proyecto
El churn de clientes (cancelación de servicios) es un problema crítico para empresas basadas en suscripciones, ya que retener clientes existentes suele ser más rentable que adquirir nuevos.  
Este proyecto tiene como objetivo desarrollar un **modelo de Machine Learning** capaz de predecir si un cliente abandonará el servicio, utilizando datos históricos y de comportamiento.

El proyecto sigue un **flujo completo de ciencia de datos**, desde la exploración y limpieza de datos hasta el entrenamiento de modelos, evaluación y segmentación de clientes según su nivel de riesgo.

---

## 🎯 Objetivo
Los objetivos principales de este proyecto son:
- Predecir el churn de clientes mediante modelos de clasificación supervisada
- Estimar la probabilidad de cancelación de cada cliente
- Segmentar a los clientes por nivel de riesgo para apoyar estrategias de retención

---

## 📊 Dataset
- **Fuente:** Dataset de Telecomunicaciones (Customer Churn)
- **Tipo:** Datos estructurados
- **Variable objetivo:** `Churn` (Yes / No)

El dataset incluye información demográfica, detalles de la cuenta y uso de servicios por parte de los clientes.

---

## 🛠️ Tecnologías y Herramientas
- Python
- Pandas y NumPy
- Matplotlib y Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 🔍 Flujo del Proyecto

1. **Carga y Exploración de Datos**
   - Revisión de dimensiones del dataset
   - Análisis de tipos de datos y valores nulos
   - Estadísticas descriptivas básicas

2. **Limpieza y Preprocesamiento**
   - Tratamiento de valores faltantes
   - Codificación de variables categóricas
   - Escalado de variables numéricas
   - Eliminación de columnas irrelevantes

3. **Análisis Exploratorio de Datos (EDA)**
   - Distribución del churn
   - Relación entre churn y variables clave
   - Visualización de patrones relevantes para el negocio

4. **Entrenamiento de Modelos**
   - Regresión Logística
   - Random Forest Classifier (con balanceo de clases)

5. **Evaluación del Modelo**
   - Comparación de desempeño entre modelos
   - Evaluación sobre conjunto de prueba

6. **Segmentación de Riesgo**
   - Clasificación de clientes en:
     - Riesgo Bajo
     - Riesgo Medio
     - Riesgo Alto
   - Basada en la probabilidad estimada de churn

---

## 🤖 Modelos Utilizados

- **Regresión Logística**
  - Modelo base interpretable para clasificación binaria

- **Random Forest**
  - Modelo de ensamble no lineal
  - Mejor desempeño general
  - Manejo del desbalance de clases mediante pesos

---

## 📈 Resultados
El modelo de **Random Forest** obtuvo un mejor desempeño en comparación con la Regresión Logística, permitiendo:
- Calcular probabilidades de churn por cliente
- Identificar clientes con alto riesgo de cancelación
- Apoyar la toma de decisiones en estrategias de retención

---

## 🚀 Posibles Mejoras
- Implementar validación cruzada
- Agregar métricas adicionales (ROC-AUC, F1-score, matriz de confusión)
- Analizar la importancia de las variables
- Optimizar hiperparámetros con GridSearch o RandomizedSearch

---

## 📁 Estructura del Repositorio
# Predicción de Churn de Clientes con Machine Learning

## 📌 Descripción del Proyecto
El churn de clientes (cancelación de servicios) es un problema crítico para empresas basadas en suscripciones, ya que retener clientes existentes suele ser más rentable que adquirir nuevos.  
Este proyecto tiene como objetivo desarrollar un **modelo de Machine Learning** capaz de predecir si un cliente abandonará el servicio, utilizando datos históricos y de comportamiento.

El proyecto sigue un **flujo completo de ciencia de datos**, desde la exploración y limpieza de datos hasta el entrenamiento de modelos, evaluación y segmentación de clientes según su nivel de riesgo.

---

## 🎯 Objetivo
Los objetivos principales de este proyecto son:
- Predecir el churn de clientes mediante modelos de clasificación supervisada
- Estimar la probabilidad de cancelación de cada cliente
- Segmentar a los clientes por nivel de riesgo para apoyar estrategias de retención

---

## 📊 Dataset
- **Fuente:** Dataset de Telecomunicaciones (Customer Churn)
- **Tipo:** Datos estructurados
- **Variable objetivo:** `Churn` (Yes / No)

El dataset incluye información demográfica, detalles de la cuenta y uso de servicios por parte de los clientes.

---

## 🛠️ Tecnologías y Herramientas
- Python
- Pandas y NumPy
- Matplotlib y Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 🔍 Flujo del Proyecto

1. **Carga y Exploración de Datos**
   - Revisión de dimensiones del dataset
   - Análisis de tipos de datos y valores nulos
   - Estadísticas descriptivas básicas

2. **Limpieza y Preprocesamiento**
   - Tratamiento de valores faltantes
   - Codificación de variables categóricas
   - Escalado de variables numéricas
   - Eliminación de columnas irrelevantes

3. **Análisis Exploratorio de Datos (EDA)**
   - Distribución del churn
   - Relación entre churn y variables clave
   - Visualización de patrones relevantes para el negocio

4. **Entrenamiento de Modelos**
   - Regresión Logística
   - Random Forest Classifier (con balanceo de clases)

5. **Evaluación del Modelo**
   - Comparación de desempeño entre modelos
   - Evaluación sobre conjunto de prueba

6. **Segmentación de Riesgo**
   - Clasificación de clientes en:
     - Riesgo Bajo
     - Riesgo Medio
     - Riesgo Alto
   - Basada en la probabilidad estimada de churn

---

## 🤖 Modelos Utilizados

- **Regresión Logística**
  - Modelo base interpretable para clasificación binaria

- **Random Forest**
  - Modelo de ensamble no lineal
  - Mejor desempeño general
  - Manejo del desbalance de clases mediante pesos

---

## 📈 Resultados
El modelo de **Random Forest** obtuvo un mejor desempeño en comparación con la Regresión Logística, permitiendo:
- Calcular probabilidades de churn por cliente
- Identificar clientes con alto riesgo de cancelación
- Apoyar la toma de decisiones en estrategias de retención

---

## 🚀 Posibles Mejoras
- Implementar validación cruzada
- Agregar métricas adicionales (ROC-AUC, F1-score, matriz de confusión)
- Analizar la importancia de las variables
- Optimizar hiperparámetros con GridSearch o RandomizedSearch

---

## 📁 Estructura del Repositorio
