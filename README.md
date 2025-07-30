# 🧠 Desafío: Predicción de Attrition en Recursos Humanos

## 🎯 Objetivo

Construir un modelo de machine learning supervisado que prediga si un empleado va a dejar la empresa (`Attrition`). Aplicarás un flujo de trabajo profesional utilizando `scikit-learn`, que incluirá exploración de datos, preprocesamiento, entrenamiento de modelos, evaluación, tuning de hiperparámetros y organización en un `Pipeline`.

---

## 📦 Dataset

Usarás el dataset **IBM HR Analytics Employee Attrition & Performance**, disponible en Kaggle:

🔗 [IBM HR Analytics Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

Este dataset contiene variables demográficas, de desempeño y satisfacción laboral de empleados.

---

## 🧠 Lo que se espera que hagas

### 1. Exploración inicial

- Análisis exploratorio de los datos.
- Identificación de columnas categóricas, numéricas, posibles outliers y proporción de clases (`Attrition`).

### 2. Preprocesamiento

- Imputación de valores faltantes si es necesario.
- Codificación de variables categóricas con `OneHotEncoder`.
- Escalado de variables numéricas con `StandardScaler`.
- Uso de `ColumnTransformer` para combinar transformaciones.
- Implementación de todo en un `Pipeline`.

### 3. Modelado

- Entrenamiento de al menos **tres clasificadores diferentes**, por ejemplo:
  - `LogisticRegression`
  - `KNeighborsClassifier`
  - `RandomForestClassifier`
- Evaluación con `cross_val_score` y métricas como `accuracy`, `roc_auc`.

### 4. Ajuste de hiperparámetros

- Aplicar `GridSearchCV` o `RandomizedSearchCV` a al menos un modelo.

### 5. Evaluación final

- Evaluación sobre conjunto de prueba separado.
- Mostrar:
  - Matriz de confusión
  - Curva ROC + AUC
  - Importancia de variables (si el modelo lo permite)

### 6. Documentación

- Incluir un `README.md` explicando:
  - El problema que resolvés
  - Modelos utilizados y decisiones tomadas
  - Resultados obtenidos
  - Instrucciones para correr el proyecto
  - Reflexiones o aprendizajes

---

## ✅ Bonus (opcional)

- Integrar `Pipeline` con `GridSearchCV`.
- Comparar visualmente modelos.
- Usar `Lasso` para selección de variables.
- Separar correctamente en `train`, `validation`, y `test`.

---
