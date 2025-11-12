# 🏦 Bank Churn Analysis

El objetivo del proyecto es **predecir si un cliente abandonará el banco**, analizando variables demográficas, financieras y de comportamiento.

---

## 📊 Dataset

📦 Fuente: [Bank Customer Churn Dataset](https://www.kaggle.com)  
El dataset contiene información de más de **10 000 clientes** de un banco europeo, con variables relacionadas a su edad, país, actividad y productos contratados.

**Variables principales:**
- `Age`
- `Gender`
- `Geography`
- `Tenure`
- `Balance`
- `NumOfProducts`
- `HasCrCard`
- `IsActiveMember`
- `EstimatedSalary`
- `Exited` *(variable objetivo: 1 = cliente se fue, 0 = cliente permaneció)*

---

## 🧹 Limpieza de datos

- ✅ **Sin valores faltantes (NAs)**  
- ⚠️ **Algunos outliers** detectados en `Balance` y `EstimatedSalary`, pero sin impacto significativo  
- Variables categóricas (`Gender`, `Geography`) fueron codificadas para el modelado  
- Escalado de variables numéricas antes del entrenamiento

---

## 🔍 Insights Principales

### 👥 Perfil del cliente
- La variable más influyente es la **actividad del cliente** (`IsActiveMember`).
- Los **clientes activos**  y **Hombres** muestran **menor tasa de churn**.  
- Los **clientes de Alemania** son los más propensos a dejar el banco.
<img width="1363" height="691" alt="Captura de pantalla 2025-11-12 113009" src="https://github.com/user-attachments/assets/dadfb628-d902-4e12-a86d-0cc4d810b323" />

### 💰 Variables numéricas
- Los clientes que abandonan el banco suelen ser mayores de 40 años, mientras que los que siguen son menores de 40 años y mayores de 70.
- No existen grandes diferencias de medias de **Creditscore**, de **EstimatedSalary** y **Tenure** entre aquellos clientes que permanecen en el banco y los que no.
- Clientes con mayor dinero en cuenta tienden a irse.
  
---
<img width="1355" height="691" alt="Captura de pantalla 2025-11-12 123430" src="https://github.com/user-attachments/assets/45617ed0-3062-4756-b186-d59e01868e26" />

## 🤖 Modelado Predictivo

Se entrenaron modelos de clasificación para predecir la variable `Exited`.

**Mejor modelo:** `XGBoost`

| Modelo | Accuracy | Precision | Recall | F1 Score |
|---------|-----------|-----------|---------|-----------|
| XGBoost | 0.86 | 0.75 | **0.73** | 0.74 |

Otros modelos probados: Logistic Regression, Random Forest, LightGBM.

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** R
- **Bibliotecas:** 
- **Técnicas:**  
  - Feature encoding y escalado  
  - EDA y visualización de churn  
  - Balanceo de clases  
  - Optimización de hiperparámetros  
  - Validación cruzada  

---



