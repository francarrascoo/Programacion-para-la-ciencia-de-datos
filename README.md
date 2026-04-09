# Evaluación 1: Preprocesamiento de Datos de Clientes

**Autores**: Felipe Ahumada Silva - Francisca Carrasco Lozano  
**Fecha**: Abril 2026

---

## 📋 Descripción

Análisis completo de calidad de datos y preprocesamiento de 20,400 registros de clientes. Incluye:

- Diagnóstico de nulos, duplicados, inconsistencias y outliers
- Feature engineering (1 variable numérica derivada y 2 segmentaciones ordinales)
- Pipeline automatizado de transformación
- Análisis de tasas de abandono

---

## 🚀 Instalación Rápida

#### 1. Clonar el repositorio

```bash
git clone https://github.com/francarrascoo/Programacion-para-la-ciencia-de-datos.git
cd Programacion-para-la-ciencia-de-datos
```

#### 2. Abrir en tu IDE y ejecutar en terminal

```bash
pip install -r requirements.txt
jupyter notebook notebooks/notebook.ipynb
```

---

## 📁 Estructura

```
├── README.md
├── requirements.txt                 # Requisitos
├── notebooks/notebook.ipynb          # Notebook
├── data/
│   ├── dataset_clientes.csv         # Original
│   └── dataset_clientes_procesado.csv  # Procesado
└── outputs/visualizaciones/         # Gráficos
```

---

## 📊 Contenido del Notebook

| Sección | Descripción |
|---------|-------------|
| **Diagnóstico** | Nulos, 400 duplicados, valores negativos |
| **Estadísticas** | Descriptivos numéricas y categóricas |
| **Outliers** | Detección IQR en variables financieras |
| **Pipeline** | Winsorize → KNN → Escalado → Codificación |
| **Validación** | Comparativa pre/post transformación |
| **Análisis** | Tasas de abandono y correlaciones |

---

## 🔍 Hallazgos Clave

- **400 duplicados eliminados** → 20,400 → 20,000 registros
- **Valores negativos** en ingreso, gasto y deuda (convertidos a NaN)
- **400+ outliers detectados** por IQR en variables monetarias
- **1 variable numérica derivada** creada: ratio_deuda_ingreso
- **2 variables ordinales de segmentación** creadas: segmento_score, antiguedad_ultima_compra
- **Distribuciones post-pipeline** más normales y sin extremos

---

## 🛠️ Metodología

**IQR para outliers**: Robusto, sin supuestos de normalidad  
**Feature Engineering antes**: Preserva interpretabilidad económica  
**Dos pipelines categóricos**: OneHot (nominales) + Ordinal (ordinales)

---

## ✅ Conclusiones

- Se observa una relación creciente entre el tiempo transcurrido desde la última compra y la tasa de abandono. En los clientes con menor antigüedad desde la última compra, la proporción de abandono es más baja, mientras que en los grupos con mayor antigüedad aumenta de forma marcada. Esto justifica la segmentación, porque sugiere que mientras más tiempo pasa sin comprar el cliente, mayor es la probabilidad observada de fuga.

---

## 📧 Autores

Felipe Ahumada Silva | Francisca Carrasco Lozano  
GitHub: https://github.com/francarrascoo/Programacion-para-la-ciencia-de-datos
