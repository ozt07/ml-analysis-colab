# 🫀 Análisis de Enfermedad Cardíaca con Machine Learning

## 📋 Descripción del Proyecto
Análisis predictivo de enfermedades cardíacas utilizando **algoritmos de Machine Learning** en **Google Colab (SaaS)**.  
El objetivo principal es **identificar patrones clínicos** y **predecir la presencia de enfermedades cardíacas** a partir de datos médicos estructurados.

---

## 🎯 Objetivos

- Realizar análisis exploratorio completo (EDA)  
- Implementar y comparar modelos de clasificación  
- Identificar factores de riesgo principales  
- Generar insights accionables para diagnóstico temprano  

---

## 📊 Dataset

| Característica | Descripción |
|----------------|-------------|
| **Nombre** | Heart Disease Dataset (Cleveland) |
| **Fuente** | [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+disease) |
| **Muestras** | 303 registros |
| **Variables** | 13 características clínicas + 1 target |
| **Tipo de Problema** | Clasificación binaria *(Presencia de enfermedad cardíaca: Sí/No)* |

---

## 🛠️ Metodología

### 1️⃣ Exploración de Datos (EDA)
- Análisis de distribuciones y correlaciones  
- Detección de valores atípicos y faltantes  
- Visualizaciones exploratorias (mapas de calor, histogramas, boxplots)

### 2️⃣ Preprocesamiento
- Imputación de valores faltantes (moda)  
- Escalado de variables numéricas con `StandardScaler`  
- División **train/test (80/20)** con estratificación  

### 3️⃣ Modelado con Machine Learning
**Algoritmos implementados:**
- Regresión Logística *(modelo base)*  
- Random Forest Classifier *(modelo principal)*  
- Optimización con **GridSearchCV**

### 4️⃣ Evaluación
**Métricas utilizadas:**
- Exactitud (Accuracy)  
- Precisión (Precision)  
- Recall  
- F1-Score  
- Matriz de confusión  
- Importancia de variables  

---

## 📈 Resultados Principales

### 🔹 Rendimiento de Modelos

| Modelo | Exactitud | Precisión | Recall | F1-Score |
|--------|------------|-----------|---------|-----------|
| **Regresión Logística** | 86.9% | 81.2% | 92.9% | 86.7% |
| **Random Forest (Base)** | 90.2% | 84.4% | 96.4% | 90.0% |
| **Random Forest (Optimizado)** | 88.5% | 81.8% | 96.4% | 88.5% |

### 🔹 Variables Más Importantes
1. **thal** (Defecto talasémico) — 14.5%  
2. **cp** (Tipo de dolor de pecho) — 13.6%  
3. **thalach** (Frecuencia cardíaca máxima) — 11.8%  
4. **ca** (Número de vasos principales) — 11.0%  
5. **oldpeak** (Depresión ST) — 10.2%

---

## 💡 Insights Clave

### 🔍 Hallazgos Principales
- La **frecuencia cardíaca máxima** es un predictor fuerte: valores bajos indican mayor riesgo.  
- El **tipo de dolor de pecho** es crítico para el diagnóstico temprano.  
- Los **defectos talasémicos** mostraron la mayor importancia predictiva.  
- El modelo **detecta correctamente la mayoría de casos positivos** (Recall del 96.4%).

### 🩺 Recomendaciones Médicas
- Monitorear la frecuencia cardíaca durante el ejercicio.  
- Evaluar el tipo de dolor de pecho como síntoma clave.  
- Considerar pruebas de talasemia en pacientes de riesgo.  
- Usar angiografía para evaluar vasos afectados.  

---

## 🚀 Cómo Reproducir el Análisis

### 🔧 Prerrequisitos
Instalar dependencias principales:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### ▶️ Ejecución
1. Abrir el notebook `notebooks/data_analysis.ipynb` en **Google Colab**  
2. Ejecutar las celdas secuencialmente  
3. Los datos se descargan automáticamente desde **UCI Repository**

---

## 📁 Estructura del Repositorio

```text
ml-analysis-colab/
├── notebooks/
│   ├── data_analysis.ipynb
│   └── exploratory_analysis.ipynb
├── data/
│   ├── raw/
│   └── processed/
├── results/
│   ├── visualizations/
│   ├── models/
│   └── reports/
├── docs/
└── README.md
```

---

## 🔗 Enlaces Importantes
- 📘 [Notebook en Google Colab](#)  
- 🧩 [Dataset Original - UCI Repository](https://archive.ics.uci.edu/ml/datasets/heart+disease)  
- 🎥 [Video de Sustentación](#)  

---

## ⚠️ Limitaciones
- Dataset pequeño (303 muestras)  
- Algunas variables con valores faltantes  
- Falta validación externa en nuevos conjuntos de datos  

---

## 🛠️ Tecnologías Utilizadas
- **Plataforma:** Google Colab (SaaS)  
- **Lenguaje:** Python 3.x  
- **Librerías:** pandas, numpy, scikit-learn, matplotlib, seaborn  

---

## 👥 Autor
**Óscar Fernando Tovar Prieto**  
📘 *Computación en la Nube - Actividad 5*  
Universidad Los Libertadores  
