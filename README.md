# 📡 Telecom X – Parte 2: Predicción de Churn

Predictivo de cancelación (churn) para Telecom X usando Python y ML.

Abrir en Google Colab: https://colab.research.google.com/github/ladyvifra/telecom-x-churn-ml/blob/main/TelecomX_LATAM_final.ipynb

## 🎯 Objetivo
- Preparar datos (limpieza, codificación, normalización).
- Seleccionar variables (correlación, importancia).
- Entrenar ≥2 modelos (baseline + árbol/boosting).
- Evaluar con métricas (Accuracy, Precision, Recall, F1, ROC-AUC).
- Interpretar resultados y factores clave del churn.

## Descripción del Proyecto
Este proyecto tiene como objetivo principal analizar y predecir la cancelación de clientes (churn) de TelecomX LATAM. Se aplicaron técnicas de limpieza de datos, preprocesamiento, análisis exploratorio y modelado predictivo utilizando algoritmos de Machine Learning. El proyecto permite identificar los factores que más influyen en la cancelación y propone estrategias de retención basadas en los resultados obtenidos.

## Contenido del Repositorio
- `data/` – Carpeta que contiene los datos limpios del proyecto.
- `TelecomX_LATAM_final.ipynb` – Cuaderno de Jupyter donde se desarrolla todo el análisis y modelado.
- `README.md` – Archivo con la descripción del proyecto y detalles del flujo de trabajo.

## Flujo de Trabajo
1. **Carga y limpieza de datos**  
   Se eliminaron columnas irrelevantes, como el `customerID`, y se manejaron valores nulos.

2. **Preprocesamiento**  
   - Codificación de variables categóricas con `One-Hot Encoding`.  
   - Balanceo de clases mediante **undersampling**, **oversampling** y **SMOTE** para corregir el desbalance de churn.  
   - Normalización de variables numéricas para los modelos sensibles a la escala, como Regresión Logística.

3. **Análisis Exploratorio de Datos**  
   - Visualización de la distribución de churn y otras variables.  
   - Análisis de correlación para identificar variables relevantes.  
   - Exploración de relaciones entre tiempo de contrato, gasto mensual y cancelación mediante boxplots y scatter plots.

4. **Modelado Predictivo**  
   - División de datos en entrenamiento (70%) y prueba (30%).  
   - Modelos utilizados:  
     - **Regresión Logística** (requiere normalización).  
     - **Random Forest** (no requiere normalización).  
   - Evaluación mediante exactitud (accuracy), precisión, recall, F1-score y matriz de confusión.

5. **Interpretación de Resultados**  
   - **Regresión Logística**: Variables más relevantes incluyeron `internetservice_fiber optic`, `charges_monthly` y `cuentas_diarias`.  
   - **Random Forest**: Variables más importantes fueron `charges_total`, `tenure` y `charges_monthly`.  
   - Los resultados permitieron identificar clientes con mayor riesgo de churn y priorizar estrategias de retención.

## Conclusiones y Próximos Pasos
El análisis muestra que los factores que más influyen en la cancelación son la duración del contrato, el tipo de servicio de internet, los gastos mensuales y el método de pago electrónico. Se recomienda:  
- Incentivar la renovación de contratos largos.  
- Ofrecer planes de pago flexibles y paquetes personalizados.  
- Implementar campañas de fidelización para clientes nuevos o con baja antigüedad.  
- Explorar modelos de boosting como XGBoost para mejorar la predicción.  
- Crear un sistema de alertas para clientes en riesgo y validar estrategias de retención mediante pruebas A/B.

## Herramientas y Librerías Utilizadas
- Python 3.x  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn (LogisticRegression, RandomForestClassifier, train_test_split, StandardScaler)  
- Imbalanced-learn (SMOTE, RandomOverSampler, RandomUnderSampler)
