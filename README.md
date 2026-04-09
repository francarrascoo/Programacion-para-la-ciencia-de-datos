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

> Flujo estandar para todos: mismos pasos en Windows, macOS y Linux.
> Versiones recomendadas de Python: 3.10 a 3.14.

#### 1. Clonar el repositorio

```bash
git clone https://github.com/francarrascoo/Programacion-para-la-ciencia-de-datos.git
cd Programacion-para-la-ciencia-de-datos
```

#### 2. Verificar Python

```bash
python --version
```

> Si en Windows `python` no funciona, usa `py` en los mismos comandos.

#### 3. Instalar dependencias (sin entorno virtual)

```bash
python -m pip install --upgrade pip setuptools wheel
python -m pip install -r requirements.txt
```

#### 4. Ejecutar el notebook

```bash
python -m jupyter notebook notebooks/notebook.ipynb
```

> Si ya estás dentro de la carpeta `notebooks`, usa:
> `python -m jupyter notebook notebook.ipynb`

#### 5. Ejecutar directamente en VS Code (sin comando jupyter)

1. Instalar las extensiones **Python** y **Jupyter** desde el Marketplace de VS Code.
2. Abrir `notebooks/notebook.ipynb` desde el explorador de archivos de VS Code.
3. En la esquina superior derecha del notebook, seleccionar un kernel de Python.
4. Si VS Code lo solicita, instalar `ipykernel`.
5. Ejecutar celdas con **Run Cell** o todo el notebook con **Run All**.

> Recomendado para este proyecto: ejecutar el notebook dentro de VS Code y usar terminal solo para instalar dependencias.

---

## 📁 Estructura

```
├── README.md
├── requirements.txt                 # Requisitos
├── data/
│   ├── dataset_clientes.csv         # Original
│   └── dataset_clientes_procesado.csv  # Procesado
├── docs/
├── notebooks/
│   └── notebook.ipynb               # Notebook principal
├── outputs/
│   ├── reportes_generados/          # Reportes PNG
│   └── visualizaciones/             # Gráficos
└── scripts/
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

## 📧 Autores

Felipe Ahumada Silva | Francisca Carrasco Lozano  
GitHub: https://github.com/francarrascoo/Programacion-para-la-ciencia-de-datos
