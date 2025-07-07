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

### Archivo Principal

- `Serie_temporal_desde_0_Mod_ARIMA.ipynb`: Notebook principal que contiene:
  - Construcción de rangos temporales
  - Creación de series temporales sintéticas con diferentes componentes
  - Análisis de estacionariedad
  - Implementación de modelos autorregresivos
  - Modelos ARIMA completos
  - Evaluación y predicción

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
- **numpy**: Operaciones numéricas y generación de componentes sintéticos
- **matplotlib**: Visualización de gráficos
- **statsmodels**: Análisis estadístico y modelos ARIMA
- **scikit-learn**: Modelos de machine learning
- **skforecast**: Forecasting especializado
- **arch**: Pruebas estadísticas adicionales

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
3. Ejecuta las celdas secuencialmente para:
   - Construir series temporales sintéticas
   - Analizar propiedades estadísticas
   - Entrenar modelos de predicción
   - Evaluar resultados

El notebook está diseñado para ser educativo y mostrar paso a paso la construcción y análisis de series temporales desde los conceptos más básicos hasta modelos avanzados.
