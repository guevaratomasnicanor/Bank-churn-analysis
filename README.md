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
- Los **clientes activos** y quienes poseen **2 o más productos** muestran **menor tasa de churn**.  
- Los **clientes jóvenes (≤ 40 años)** presentan mayor probabilidad de abandonar el banco.  
- Clientes **mayores de 40 años** tienden a mantenerse más tiempo.  
- Los **clientes de Alemania** son los más propensos a dejar el banco.

### 💰 Variables numéricas
- No hay correlación directa entre **saldo o salario estimado** y la salida del cliente.  
- La variable más influyente es la **actividad del cliente** (`IsActiveMember`).

---

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



