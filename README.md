# 🧠 Employee Attrition Prediction

Este proyecto tiene como objetivo predecir si un empleado va a dejar la empresa (attrition) utilizando técnicas de aprendizaje supervisado con Python y scikit-learn.

Es un proyecto introductorio de machine learning que pone en práctica todo el flujo básico de trabajo: análisis exploratorio, preprocesamiento, entrenamiento de varios modelos, evaluación con métricas relevantes y ajuste de hiperparámetros.

---

## 🎯 Objetivo

Desarrollar un modelo de clasificación binaria para anticipar la rotación de empleados, utilizando un dataset real de recursos humanos. El foco está en detectar de forma confiable a los empleados propensos a renunciar, para que una empresa pueda actuar preventivamente.

---

## 📦 Dataset

- **Nombre:** IBM HR Analytics Employee Attrition & Performance
- **Fuente:** [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- **Archivo:** `WA_Fn-UseC_-HR-Employee-Attrition.csv` (renombrado como `employee-attrition-dataset.csv`)
- **Instrucciones:** descargá el archivo desde el link de Kaggle y colocalo en la misma carpeta que el notebook.

---

## 🧪 Flujo de trabajo aplicado

1. **Exploración inicial del dataset**

   - Inspección de tipos de variables, valores faltantes y distribución de la variable objetivo.
   - Visualización con gráficos simples (barras, proporciones).

2. **Preprocesamiento**

   - Codificación de la variable objetivo (`Attrition`) a 0 y 1.
   - Identificación de columnas numéricas y categóricas.
   - Aplicación de `StandardScaler` a columnas numéricas.
   - Aplicación de `OneHotEncoder` a columnas categóricas.
   - División en `train` y `test` **antes de transformar**, evitando data leakage.

3. **Entrenamiento de modelos**

   - `LogisticRegression`
   - `KNeighborsClassifier`
   - `RandomForestClassifier`

4. **Evaluación de desempeño**

   - Matriz de confusión
   - `classification_report` (accuracy, recall, f1)
   - ROC AUC score
   - Curvas ROC comparando modelos

5. **Ajuste de hiperparámetros**
   - `GridSearchCV` sobre `LogisticRegression`, maximizando `recall`

---

## 🧠 Resultados principales

- **Mejor modelo:** `LogisticRegression` con `class_weight='balanced'`
- **Mejores hiperparámetros:** `C=0.0001`, `solver='liblinear'`
- **Recall en test set:** 0.78
- **Principales variables influyentes:** `TotalWorkingYears`, `YearsInCurrentRole`, `Age`, `JobLevel` y `MonthlyIncome`

---

## ⚙️ Cómo correr el proyecto

1. Cloná el repositorio:

   ```bash
   git clone https://github.com/tu_usuario/employee-attrition-prediction.git
   cd employee-attrition-prediction
   ```

2. Instalá las dependencias (si usás pip):

   ```bash
   pip install -r requirements.txt
   ```

3. Descargá el dataset desde Kaggle y guardalo como:

   ```
   employee-attrition-dataset.csv
   ```

4. Abrí y ejecutá el archivo `workflow.ipynb` paso a paso.

---

## 📌 Qué aprendí

- Cómo preparar y transformar un dataset real para modelos de machine learning.
- Cómo comparar modelos con métricas más informativas que el accuracy.
- Cómo usar `GridSearchCV` para mejorar un modelo supervisado.
- Cómo evitar errores comunes como el _data leakage_.

---

## ✅ Estado del proyecto

Este es un **primer proyecto completo**, sin uso de `Pipeline` ni modularización avanzada, pensado para entender en detalle cada etapa del flujo de machine learning. Es una base sólida para proyectos más complejos o para comenzar a construir un portfolio profesional.

---
