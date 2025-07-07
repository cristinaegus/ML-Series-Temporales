# Proyecto de Series Temporales con Modelos ARIMA

Este proyecto contiene un análisis completo de series temporales desde cero, incluyendo la construcción de series sintéticas y la aplicación de modelos ARIMA para predicción.

## Configuración del Entorno

### Entorno Virtual

Se ha configurado un entorno virtual de Python en `.venv` con todas las dependencias necesarias.

### Activación del Entorno Virtual

**Windows (PowerShell):**

```powershell
.venv\Scripts\Activate.ps1
```

**Windows (CMD):**

```cmd
.venv\Scripts\activate.bat
```

### Instalación de Dependencias

```bash
pip install -r requirements.txt
```

## Contenido del Proyecto

### Archivos Principales

- `Serie_temporal_desde_0_Mod_ARIMA.ipynb`: Notebook principal que contiene:
- `Demanda energía eléctrica.ipynb`: Notebook con análisis real de demanda energética que contiene:
  - Carga y procesamiento de datos reales de demanda eléctrica
  - Análisis exploratorio de datos temporales
  - Variables exógenas (temperatura)
  - Modelos de forecasting con skforecast
  - Backtesting y validación de modelos
  - Optimización de hiperparámetros
  - Visualizaciones interactivas con Plotly

### Componentes de Series Temporales Incluidos

1. **Serie constante**: Base inmutable
2. **Componente cíclico**: Patrones estacionales usando funciones trigonométricas
3. **Tendencia**: Componente lineal ascendente/descendente
4. **Término parabólico**: Aceleración/deceleración en el tiempo
5. **Ruido blanco**: Variaciones aleatorias normales

### Análisis Estadístico

- Pruebas de estacionariedad (ADF, KPSS, Phillips-Perron, DF-GLS)
- Gráficos de autocorrelación (ACF y PACF)
- Descomposición de series temporales
- Test de Ljung-Box para validación de modelos

### Modelos Implementados

1. **ForecasterAutoreg**: Modelo autorregresivo recursivo con regresión Ridge
2. **ARIMA**: Modelo autoregresivo integrado de media móvil

## Librerías Principales Utilizadas

- **pandas**: Manipulación de datos y rangos temporales
- **numpy**: Operaciones numéricas y generación de componentes sintéticos (v1.26.4)
- **matplotlib**: Visualización de gráficos
- **statsmodels**: Análisis estadístico y modelos ARIMA
- **scikit-learn**: Modelos de machine learning
- **skforecast**: Forecasting especializado para series temporales
- **arch**: Pruebas estadísticas adicionales
- **plotly**: Visualizaciones interactivas
- **seaborn**: Visualizaciones estadísticas avanzadas
- **lightgbm**: Modelos de gradient boosting para forecasting
- **optuna**: Optimización de hiperparámetros
- **tqdm**: Barras de progreso para procesos largos
- **numba**: Compilación JIT para acelerar cálculos

## Estructura de Archivos

```
├── Serie_temporal_desde_0_Mod_ARIMA.ipynb  # Notebook principal
├── Series Temporales.pptx                  # Presentación de apoyo
├── requirements.txt                        # Dependencias del proyecto
├── README.md                              # Este archivo
└── .venv/                                 # Entorno virtual (se crea automáticamente)
```

## Notas Técnicas

- **Versión de Python**: 3.12.x
- **Versión de NumPy**: 1.26.4 (fijada para compatibilidad con numba)
- **Frecuencia por defecto**: Diaria ('D')
- **Período de datos**: 2020-01-01 a 2025-12-31

## Uso del Proyecto

1. Activa el entorno virtual
2. Abre el notebook en Jupyter Lab o VS Code
3. Asegúrate de que el kernel del notebook esté configurado para usar el entorno virtual (.venv)
4. **Para el notebook de series sintéticas** (`Serie_temporal_desde_0_Mod_ARIMA.ipynb`):
   - Ejecuta las celdas secuencialmente para construir series temporales sintéticas
   - Analizar propiedades estadísticas
   - Entrenar modelos de predicción
   - Evaluar resultados
5. **Para el notebook de demanda energética** (`Demanda energía eléctrica.ipynb`):
   - Ejecuta las celdas secuencialmente para cargar y procesar datos reales
   - Realizar análisis exploratorio
   - Entrenar modelos de forecasting
   - Ejecutar backtesting y optimización

## Estado del Entorno

✅ **Entorno completamente configurado y funcional**
- Todas las dependencias instaladas y compatibles
- Kernels de notebooks configurados correctamente
- Conflictos de versiones resueltos (numpy/numba)
- Ambos notebooks ejecutándose sin errores

## Notas de Configuración del Kernel

Si experimentas problemas con el kernel en VS Code:
1. Abre la paleta de comandos (Ctrl+Shift+P)
2. Busca "Python: Select Interpreter"
3. Selecciona el intérprete del entorno virtual: `.venv\Scripts\python.exe`
4. En el notebook, asegúrate de seleccionar el kernel correcto (Python 3.12.x (.venv))

Los notebooks están diseñados para ser educativos y mostrar paso a paso la construcción y análisis de series temporales desde los conceptos más básicos hasta modelos avanzados con datos reales.
