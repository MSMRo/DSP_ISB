# Procesamiento Digital de Señales para Ingeniería Biomédica (DSP_ISB)

Serie de códigos educativos para facilitar el aprendizaje y análisis del **procesamiento de señales biomédicas**. Este proyecto incluye notebooks interactivos que cubren conceptos fundamentales de señales, sistemas y filtros digitales, con énfasis en análisis de tiempo y frecuencia.

## 📋 Descripción General

Este repositorio contiene material educativo sobre procesamiento de señales, enfocado en aplicaciones biomédicas. Incluye ejemplos prácticos de:
- **Generación y análisis de señales** en dominio del tiempo y frecuencia
- **Transformadas de Fourier** (FFT y STFT)
- **Sistemas lineales** de primer y segundo orden
- **Filtros analógicos y digitales** con técnicas de diseño clásicas
- **Análisis tiempo-frecuencia** mediante espectrogramas

## 📁 Estructura del Proyecto

```
DSP_ISB/
├── README.md                           # Este archivo
├── environment.yml                     # Dependencias de conda
├── NOTEBOOKS/                          # Cuadernos interactivos Jupyter
│   ├── 1_senales.ipynb                # Creación y análisis de señales
│   └── 2_sistemas.ipynb               # Sistemas y filtros
├── DSP/                               # Código fuente reutilizable
│   ├── main.py
│   ├── pyproject.toml
│   └── README.md
└── _OLD/                              # Archivos antiguos/obsoletos
    └── YOLOv5_Custom_Training.ipynb
```

## 📚 Notebooks

### 1. Creación y Análisis de Señales (`1_senales.ipynb`)

Introduce conceptos fundamentales de generación y análisis de señales:

- **Generación de señales senoidales**: Definición de parámetros como frecuencia, amplitud, fase y frecuencia de muestreo
- **Análisis en el dominio de frecuencia**:
  - Magnitud de espectro (Magnitude Spectrum)
  - Transformada Rápida de Fourier (FFT)
  - Transformada de Fourier de Tiempo Corto (STFT)
  
- **Visualización tiempo-frecuencia**: Espectrogramas para observar cómo cambia el contenido frecuencial a lo largo del tiempo

**Conceptos clave**: Teorema de Nyquist, muestreo, resolución frecuencial, resolución temporal

### 2. Sistemas y Filtros (`2_sistemas.ipynb`)

Análisis de sistemas lineales e invariantes en el tiempo (LTI) y diseño de filtros:

- **Señales de prueba**: Generación de señales CHIRP para análisis de respuesta en frecuencia
- **Filtros paso bajas de 1er orden**:
  - Sistemas RC analógicos continuos
  - Implementación en tiempo discreto mediante transformación bilineal
- **Análisis de respuesta en frecuencia**: Diagramas de Bode
- **Filtros digitales**: Diseño mediante métodos de conversión bilineal

**Conceptos clave**: Función de transferencia, polos y ceros, estabilidad, respuesta impulsiva

## 🔧 Requisitos

### Sistema
- **Python**: 3.12+
- **SO**: Linux, macOS o Windows

### Dependencias principales
- **NumPy**: Álgebra lineal y operaciones numéricas
- **SciPy**: Procesamiento de señales (signal, fft)
- **Matplotlib**: Visualización de gráficas
- **NeuroKit2**: Herramientas para análisis biomédico
- **PyFDA**: Herramienta de diseño de filtros digitales

## 🚀 Instalación y Configuración

### 1. Clonar o descargar el repositorio
```bash
cd /ruta/al/proyecto
```

### 2. Crear el ambiente conda
```bash
conda env create -f environment.yml
conda activate signal-env
```

### 3. Ejecutar los notebooks
```bash
jupyter notebook NOTEBOOKS/
```

## 📖 Uso

1. **Comienza con `1_senales.ipynb`** para entender los conceptos básicos de generación y análisis de señales
2. **Prosigue a `2_sistemas.ipynb`** para aprender sobre filtros y sistemas lineales
3. **Experimenta**: Modifica parámetros (frecuencias, amplitudes, tipo de ventanas) y observa los resultados

## 🔍 Ejemplo Rápido

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy import signal

# Parámetros de la señal
f = 20          # Frecuencia [Hz]
fs = 400        # Frecuencia de muestreo [Hz]
t = np.linspace(0, 1, fs, endpoint=False)

# Generar señal senoidal
x = 10 * np.sin(2*np.pi*f*t)

# Visualizar
plt.plot(t, x)
plt.xlabel('Tiempo (s)')
plt.ylabel('Amplitud')
plt.title(f'Señal Senoidal {f} Hz')
plt.show()

# Análisis de frecuencia
plt.magnitude_spectrum(x, Fs=fs)
plt.show()
```

## 📊 Dependencias del Ambiente

El archivo `environment.yml` especifica:
- **Python 3.12.12**
- Librerías científicas: numpy, scipy, matplotlib
- Herramientas especializadas: neurokit2, pyfda

Ver `environment.yml` para la lista completa de dependencias.

## 🎯 Objetivos de Aprendizaje

Al completar este material, podrás:
- ✅ Generar y manipular señales digitales
- ✅ Analizar señales en dominios de tiempo y frecuencia
- ✅ Entender el muestreo y sus limitaciones (Teorema de Nyquist)
- ✅ Diseñar e implementar filtros digitales simples
- ✅ Analizar sistemas lineales e invariantes en el tiempo
- ✅ Aplicar estas herramientas en problemas biomédicos

## 📝 Notas Importantes

- Los notebooks utilizan métodos clásicos de procesamiento de señales, ideales para aprendizaje
- Todos los ejemplos incluyen visualizaciones para mejor comprensión
- Se recomienda ejecutar los notebooks de forma secuencial
- Los parámetros de las señales pueden modificarse para experimentación

## 📧 Autor

Proyecto educativo para Ingeniería Biomédica

## 📄 Licencia

Uso libre para propósitos educativos

---

**Última actualización**: Marzo 2026

