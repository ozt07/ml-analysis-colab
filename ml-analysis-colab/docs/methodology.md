# Metodología Aplicada

## 1. Recopilación de Datos
- **Fuente**: UCI Machine Learning Repository
- **Dataset**: Heart Disease (Cleveland)
- **Total de registros**: 303
- **Variables**: 14 (13 features + 1 target)

## 2. Preprocesamiento
### Limpieza de Datos
- Identificación de valores faltantes: 6 valores (4 en 'ca', 2 en 'thal')
- Estrategia: Imputación con la moda (valor más frecuente)
- Conversión de target a binario: valores 1-4 → 1 (enfermedad presente)

### Transformación de Variables
- Variables numéricas escaladas: StandardScaler
- Variables categóricas: ya codificadas numéricamente
- División de datos: 80% entrenamiento, 20% prueba (estratificado)

## 3. Análisis Exploratorio (EDA)
- Análisis univariado: distribuciones de cada variable
- Análisis bivariado: correlaciones con target
- Visualizaciones: histogramas, scatter plots, matriz de correlación
- Identificación de outliers y patrones

## 4. Modelado de Machine Learning
### Algoritmos Seleccionados
1. **Regresión Logística**: Modelo interpretable como baseline
2. **Random Forest**: Manejo de relaciones no lineales, robusto

### Proceso de Entrenamiento
- Entrenamiento con datos de entrenamiento (80%)
- Validación cruzada para optimización
- Grid Search para hiperparámetros de Random Forest
- Evaluación en conjunto de prueba (20%)

## 5. Evaluación de Modelos
### Métricas Utilizadas
- Exactitud (Accuracy)
- Precisión (Precision)
- Recall (Sensibilidad)
- F1-Score
- Matrices de confusión

### Criterios de Selección
- Mayor exactitud general
- Alto recall (importante en diagnóstico médico)
- Balance entre precisión y recall
- Interpretabilidad de resultados
