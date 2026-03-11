# 📡 TelecomX: Predicción de Churn de Clientes

Este repositorio contiene un análisis completo y un modelo de **Machine Learning** desarrollado para predecir la fuga de clientes (**Churn**) en la empresa TelecomX. El objetivo es identificar usuarios con alta probabilidad de cancelar su servicio para aplicar estrategias de retención oportunas.

## 📊 Resumen del Proyecto
En la industria de las telecomunicaciones, retener a un cliente existente es mucho más rentable que adquirir uno nuevo. Este proyecto utiliza datos históricos de clientes (servicios contratados, facturación, demografía) para construir un clasificador capaz de anticipar renuncias.

## 🛠️ Tecnologías y Librerías
- **Python 3.x**
- **Pandas & NumPy**: Procesamiento y limpieza de datos JSON.
- **Scikit-Learn**: Entrenamiento de modelos y métricas de evaluación.
- **Imbalanced-learn (SMOTE)**: Manejo de clases desbalanceadas.
- **Matplotlib & Seaborn**: Visualización de datos y análisis exploratorio (EDA).
- **Requests**: Extracción de datos desde API externa.

## 🚀 Pipeline de Datos
1. **Extracción**: Consumo de datos desde fuente externa en formato JSON.
2. **Transformación**: 
   - Normalización de estructuras anidadas.
   - Tratamiento de nulos en la columna `TotalCharges`.
   - Conversión de variables categóricas a numéricas (One-Hot & Label Encoding).
3. **Ingeniería de Características**: Creación de nuevas métricas basadas en el uso de servicios y antigüedad (`tenure`).
4. **Modelado**: Implementación de **Random Forest Regressor/Classifier** con optimización de hiperparámetros mediante `GridSearchCV`.
5. **Evaluación**: Análisis mediante Matriz de Confusión y reporte de clasificación (Precision, Recall, F1-Score).

## 📈 Hallazgos e Impacto
- **Indicadores Críticos**: Se identificó que el tipo de contrato "Month-to-month" y el método de pago "Electronic Check" son los factores con mayor correlación con la fuga.
- **Fidelización**: El modelo permite segmentar a los clientes en riesgo, sugiriendo acciones específicas para usuarios de Fibra Óptica y contratos de corto plazo.

## 📋 Cómo utilizar este Notebook
1. Clonar el repositorio.
2. Instalar las dependencias necesarias:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn requests
