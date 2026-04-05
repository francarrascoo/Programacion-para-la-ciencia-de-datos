# Proyecto: Preparación de Datos para Ciencia de Datos

Repositorio académico orientado al **análisis exploratorio, limpieza, transformación y validación de datos** en un caso realista de clientes, siguiendo buenas prácticas de ingeniería de datos y documentación técnica.

## 1) Objetivo del proyecto

Desarrollar un flujo reproducible de preparación de datos que permita:

- comprender el dataset de clientes,
- detectar y corregir problemas de calidad,
- transformar variables para una etapa posterior de modelado,
- validar integridad, consistencia y procedencia de los datos,
- comunicar hallazgos con visualizaciones y reporte técnico.

## 2) Estructura del repositorio

```text
.
├── README.md
├── data/
│   └── dataset_clientes.csv
├── docs/
├── notebooks/
├── outputs/
└── scripts/
```

Descripción de carpetas:

- `data/`: datos crudos y (opcionalmente) datos procesados.
- `notebooks/`: análisis exploratorio, limpieza y transformación en Jupyter.
- `scripts/`: funciones auxiliares reutilizables (equivalente al `src/` sugerido en pauta).
- `outputs/`: gráficos, tablas y artefactos generados.
- `docs/`: informe técnico final y documentación complementaria.

## 3) Stack tecnológico

- Python 3.10+
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib y/o Seaborn (visualización)

## 4) Reproducibilidad: configuración del entorno

### Opción principal: Google Colab

1. Abrir los notebooks desde `notebooks/` en Colab.
2. Ejecutar una celda inicial de dependencias (solo si falta alguna librería):
   - `!pip install -q pandas numpy matplotlib seaborn`
3. Montar Google Drive si se trabajará con archivos fuera del repositorio.
4. Verificar rutas de lectura/escritura para `data/` y `outputs/`.

### Opción alternativa (local): `venv` o Conda

Si alguien del equipo trabaja localmente, puede usar entorno virtual/Conda para mantener compatibilidad con Colab.

## 5) Flujo de trabajo recomendado

1. **Carga y perfilado inicial** del dataset.
2. **EDA**: estadísticas descriptivas, distribución de variables y relaciones.
3. **Limpieza**:
   - tratamiento de nulos,
   - duplicados,
   - outliers,
   - estandarización de formatos.
4. **Transformación**:
   - codificación de variables,
   - escalamiento/normalización según corresponda,
   - ingeniería de características justificada.
5. **Validación de calidad e integridad**:
   - reglas de consistencia,
   - revisión de tipos y dominios,
   - control de cambios y trazabilidad.
6. **Exportación de resultados** a `outputs/` y/o `data/processed`.
7. **Documentación** en notebooks + informe técnico en `docs/`.

## 6) Entregables esperados

- Enlace del repositorio GitHub del equipo.
- Informe técnico en PDF (8–12 páginas) en `docs/`.
- Notebooks reproducibles en `notebooks/`.
- Resultados visuales y tablas en `outputs/`.

## 7) Contenido mínimo del informe técnico (8–12 páginas)

1. Resumen ejecutivo.
2. Análisis exploratorio inicial.
3. Metodología de transformación (con justificación técnica).
4. Resultados y validación de calidad.
5. Conclusiones, dificultades y recomendaciones.

## 8) Criterios de calidad (checklist rápido)

- [ ] Código legible, modular y con docstrings.
- [ ] Uso correcto de filtros, agrupaciones y joins en Pandas.
- [ ] Visualizaciones pertinentes y bien interpretadas.
- [ ] Transformaciones coherentes con el tipo de variable y objetivo.
- [ ] Flujo de limpieza técnicamente justificado.
- [ ] Entorno reproducible documentado (celda de instalación en Colab y/o `requirements.txt`).
- [ ] Verificación de integridad/procedencia aplicada y documentada.

## 9) Presentación oral: preparación sugerida

Cada integrante debería poder explicar:

- decisiones de limpieza y su impacto,
- transformaciones aplicadas y su fundamento,
- operaciones clave de Pandas implementadas,
- principales hallazgos estadísticos y visuales,
- importancia de validar datos antes del modelado.

## 10) Fechas clave (según pauta)

- **Entrega del encargo:** miércoles 8 de abril (antes del término de clase).
- **Sesión de preguntas individuales:** jueves 9 de abril.

## 11) Notas para el equipo

- Registrar decisiones técnicas en cada notebook (por qué se hizo, no solo qué se hizo).
- Mantener versiones limpias de gráficos/tablas en `outputs/`.
- Evitar celdas con ejecución rota; validar notebooks antes de entregar.
