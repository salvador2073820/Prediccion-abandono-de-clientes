# 📉 Predicción de Abandono de Clientes (Customer Churn)

> Modelo de Machine Learning para identificar clientes en riesgo de abandono en una empresa de telecomunicaciones, utilizando Regresión Logística y Random Forest.

---

## 📋 Tabla de Contenidos

- [Descripción del Proyecto](#descripción-del-proyecto)
- [Dataset](#dataset)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Pipeline de Análisis](#pipeline-de-análisis)
- [Modelos Implementados](#modelos-implementados)
- [Resultados](#resultados)
- [Segmentación de Riesgo](#segmentación-de-riesgo)
- [Cómo Ejecutar el Proyecto](#cómo-ejecutar-el-proyecto)
- [Autor](#autor)

---

## Descripción del Proyecto

El **churn** (abandono de clientes) es uno de los problemas más críticos en la industria de telecomunicaciones. Perder un cliente existente cuesta entre 5 y 25 veces más que retenerlo, por lo que anticipar su salida permite actuar de forma proactiva.

Este proyecto construye un pipeline completo de Machine Learning que:

- Analiza el comportamiento de clientes a través de exploración de datos (EDA)
- Entrena y compara dos modelos de clasificación
- Genera una **segmentación de riesgo** (Alto / Medio / Bajo) para cada cliente del conjunto de prueba

---

## 📂 Dataset

**Fuente:** `telecom_churn.csv` — Dataset clásico de telecomunicaciones con información de 7,043 clientes.

| Característica | Detalle |
|---|---|
| Registros | 7,043 clientes |
| Variables | 21 columnas |
| Variable objetivo | `Churn` (Yes / No) |
| Distribución de clases | ~74% No Churn / ~26% Churn |

### Variables principales

| Variable | Descripción |
|---|---|
| `tenure` | Meses que el cliente lleva con la empresa |
| `Contract` | Tipo de contrato (mes a mes, 1 año, 2 años) |
| `MonthlyCharges` | Cargo mensual del cliente |
| `TotalCharges` | Cargo total acumulado |
| `InternetService` | Tipo de servicio de internet (DSL, Fibra óptica, Ninguno) |
| `PaymentMethod` | Método de pago |
| `Churn` | Si el cliente abandonó la empresa (variable objetivo) |

---

## 🛠 Tecnologías Utilizadas

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-F7931E?logo=scikit-learn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557c)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

```
pandas        → Manipulación y limpieza de datos
numpy         → Operaciones numéricas
matplotlib    → Visualizaciones
scikit-learn  → Modelos de ML, preprocesamiento y métricas
```

---

## 📁 Estructura del Proyecto

```
Prediccion-abandono-de-clientes/
│
├── ML.ipynb                  # Notebook principal con todo el análisis
├── telecom_churn.csv         # Dataset de clientes
└── README.md                 # Este archivo
```

---

## Pipeline de Análisis

```
1. Carga de datos
       ↓
2. Exploración (EDA)
   - Distribución de Churn
   - Churn por tipo de contrato
   - Churn por método de pago
   - Distribución de tenure y cargos mensuales
       ↓
3. Limpieza y preprocesamiento
   - Eliminación de columna ID
   - Conversión de TotalCharges a numérico
   - Imputación de valores nulos (mediana / moda)
   - One-Hot Encoding de variables categóricas
       ↓
4. División Train / Test (80% / 20%, stratify=y)
       ↓
5. Escalado de variables (StandardScaler)
       ↓
6. Entrenamiento de modelos
   - Regresión Logística
   - Random Forest
       ↓
7. Evaluación y comparación
       ↓
8. Segmentación de riesgo por cliente
```

---

## Modelos Implementados

### Regresión Logística

```python
LogisticRegression(max_iter=1000, random_state=42)
```

Modelo base, interpretable y eficiente. Entrenado sobre datos escalados con `StandardScaler`. Permite analizar el coeficiente de cada variable para identificar los factores más influyentes en el abandono.

### Random Forest

```python
RandomForestClassifier(
    n_estimators=200,
    random_state=42,
    class_weight="balanced"
)
```

Modelo de ensamble que maneja el desbalance de clases automáticamente con `class_weight="balanced"`. Proporciona la importancia de cada variable como resultado adicional.

---

## 📊 Resultados

Los modelos fueron evaluados con las siguientes métricas sobre el conjunto de prueba (20% del dataset):

| Métrica | Regresión Logística | Random Forest |
|---|---|---|
| Accuracy | — | — |
| Precision | — | — |
| Recall | — | — |
| F1-Score | — | — |

> Los valores exactos se encuentran en la salida del notebook `ML.ipynb`.

### Variables más importantes (Random Forest)

El modelo identificó las siguientes variables como las más predictivas de abandono:

1. `tenure` — Tiempo de permanencia del cliente
2. `MonthlyCharges` — Cargo mensual
3. `TotalCharges` — Cargo total acumulado
4. `Contract_Two year` — Contrato de dos años (reduce el riesgo)
5. `InternetService_Fiber optic` — Servicio de fibra óptica

---

## Segmentación de Riesgo

A partir de la probabilidad de churn estimada por Random Forest, cada cliente del conjunto de prueba es clasificado en uno de tres niveles:

| Nivel | Probabilidad de Churn | Clientes (test set) |
|---|---|---|
| 🟢 Bajo | 0% – 40% | 911 |
| 🟡 Medio | 40% – 70% | 257 |
| 🔴 Alto | 70% – 100% | 136 |

Esta segmentación permite priorizar acciones de retención enfocadas en los clientes de riesgo **Alto** y **Medio**.

---

## ▶️ Cómo Ejecutar el Proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/SalvadorHernandezJuarez/Prediccion-abandono-de-clientes.git
cd Prediccion-abandono-de-clientes
```

### 2. Instalar dependencias

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### 3. Ejecutar el notebook

```bash
jupyter notebook ML.ipynb
```

> Asegúrate de que el archivo `telecom_churn.csv` esté en la misma carpeta que el notebook antes de ejecutarlo.

---

## 👤 Autor

**Salvador Hernández Juárez**

[![GitHub](https://img.shields.io/badge/GitHub-SalvadorHernandezJuarez-181717?logo=github)](https://github.com/SalvadorHernandezJuarez)

---

*Proyecto de Machine Learning — Predicción de Abandono de Clientes en Telecomunicaciones*
