# 🌤️ WeatherLocal Copiapó

[![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

**Aplicación de meteorología hiperlocalizada con inteligencia artificial para la región de Atacama**

---

## 📋 Descripción

WeatherLocal Copiapó es una aplicación completa de análisis meteorológico que proporciona información precisa y personalizada para Copiapó y sus alrededores. Implementa tecnologías modernas de:

- 📍 **Datos Hiperlocalizado**: 12 estaciones distribuidas en la región
- 🤖 **Machine Learning**: Predicción de contaminación atmosférica
- 🗺️ **Mapas Interactivos**: Visualización en tiempo real con Folium
- 📊 **Análisis Gráfico**: Visualizaciones meteorológicas completas
- 📅 **Pronósticos**: Predicciones de temperatura para 3 días

---

## 🚀 Características Principales

✅ **Mapa Interactivo Folium**
- 12 estaciones meteorológicas geolocalizadas
- Popups con información completa al hacer clic
- Códigos de color según calidad del aire (ICA)

✅ **4 Gráficos Matplotlib**
- Temperatura por estación
- Humedad relativa por estación
- Velocidad del viento por estación
- Índice de Calidad del Aire (ICA)

✅ **Tablas de Datos Completas**
- Datos meteorológicos en tiempo real
- Pronósticos de temperatura (3 días)
- Predicciones de contaminación (Machine Learning)

✅ **Modelo de Machine Learning**
- Algoritmo: Random Forest Classifier
- Variables: Temperatura, Humedad, Velocidad del viento
- Precisión: ~84%
- Predicción: Eventos de contaminación atmosférica (48 horas)

✅ **Interfaz Web Responsiva**
- Diseño profesional con gradientes morados
- Tablas interactivas con efectos hover
- Leyenda de colores para ICA
- Compatible con dispositivos móviles

---

## 📁 Estructura del Proyecto

```
WeatherLocal-Copiapó/
│
├── README.md                          # Este archivo
├── LICENSE                            # Licencia MIT
├── requirements.txt                   # Dependencias Python
│
├── weatherlocal_completo.html         # HTML con mapa, gráficos y tablas
├── weatherlocal_notebook.ipynb        # Jupyter Notebook completo
│
├── Ejercicio2/                        # Páginas HTML básicas (Lección 2)
│   ├── index.html                     # Página principal
│   ├── pronostico.html                # Página de pronósticos
│   ├── estaciones.html                # Página de estaciones
│   └── contaminacion.html             # Página de contaminación
│
└── Ejercicio3/                        # Página informativa (Lección 3)
    ├── index.html                     # Página informativa
    └── assets/
        ├── img/                       # Carpeta de imágenes
        └── css/
            └── estilos.css            # Hoja de estilos
```

---

## 🛠️ Tecnología Utilizada

| Tecnología | Versión | Propósito |
|-----------|---------|----------|
| **Python** | 3.8+ | Lenguaje principal |
| **Jupyter Notebook** | 1.0+ | Entorno interactivo |
| **Folium** | 0.14+ | Mapas interactivos |
| **Pandas** | 1.5+ | Análisis de datos |
| **NumPy** | 1.22+ | Computación numérica |
| **Scikit-learn** | 1.0+ | Machine Learning |
| **Matplotlib** | 3.5+ | Gráficos |
| **HTML5/CSS3** | - | Interfaz web |

---

## 📦 Instalación

### Requisitos Previos

- Python 3.8 o superior
- Anaconda (recomendado) o pip
- Git

### Pasos de Instalación

#### Opción 1: Clonar desde GitHub

```bash
# Clonar el repositorio
git clone https://github.com/migellucero123/WeatherLocal-Copiapó.git
cd WeatherLocal-Copiapó

# Crear entorno virtual
conda create -n weatherlocal python=3.11 -y
conda activate weatherlocal

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar Jupyter
jupyter notebook weatherlocal_notebook.ipynb
```

#### Opción 2: Instalación Manual

```bash
# Crear entorno
conda create -n weatherlocal python=3.11 -y
conda activate weatherlocal

# Instalar librerías
conda install folium pandas numpy scikit-learn matplotlib jupyter -y

# Instalar librerías adicionales
pip install requests beautifulsoup4
```

---

## 🚀 Uso

### Ejecutar el Notebook

1. Abre Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

2. Haz clic en `weatherlocal_notebook.ipynb`

3. Ejecuta las celdas en orden (Shift + Enter)

4. Se generarán automáticamente:
   - Mapa interactivo Folium
   - 4 gráficos meteorológicos
   - Archivo HTML con análisis completo

### Ver el Análisis HTML

1. Abre `weatherlocal_completo.html` en tu navegador

2. Explora:
   - 📍 Mapa interactivo con 12 estaciones
   - 📊 Estadísticas resumen
   - 📈 Gráficos meteorológicos
   - 🌡️ Tabla de datos en tiempo real
   - 📅 Tabla de pronósticos (3 días)
   - 🤖 Tabla de predicciones ML

---

## 📍 Estaciones Monitoreadas

La región cuenta con 12 estaciones estratégicamente ubicadas:

| # | Estación | Tipo |
|---|----------|------|
| 1 | Copiapó Centro | Urbana |
| 2 | Caldera Puerto | Costera |
| 3 | Tierra Amarilla | Interior |
| 4 | Cerro Empeñada | Transicional |
| 5 | Punta de Choros | Costera |
| 6 | La Higuera | Interior |
| 7 | Nantoco | Interior |
| 8 | Zona Industrial | Urbana |
| 9 | Pajonales | Transicional |
| 10 | Atacama Sur | Interior |
| 11 | Chañaral | Costera |
| 12 | Los Loros | Transicional |

---

## 🤖 Modelo Machine Learning

### Algoritmo
- **Tipo**: Random Forest Classifier
- **Número de árboles**: 10
- **Características**: 3 (Temperatura, Humedad, Velocidad del viento)

### Predicción
- **Variable objetivo**: Contaminación atmosférica (ICA > 100)
- **Horizonte**: 48 horas
- **Precisión**: ~84%

### Variables de Entrada
```python
X = [temperatura, humedad, viento_intensidad]
y = (ica > 100)  # 1 = Contaminación, 0 = Normal
```

---

## 📊 Índice de Calidad del Aire (ICA)

| Rango | Estado | Color | Recomendación |
|-------|--------|-------|---------------|
| 0-50 | Buena | 🟢 Verde | Actividades normales |
| 51-100 | Moderada | 🟡 Amarillo | Personas sensibles cuidado |
| 101-200 | Mala | 🔴 Rojo | Evitar actividades al aire libre |
| 201+ | Muy Mala | 🔴🔴 Rojo Oscuro | Permanecer en interiores |

---

## 📈 Análisis de Datos

El proyecto realiza:

1. **Análisis Estadístico**
   - Máximos, mínimos y promedios
   - Desviación estándar
   - Distribuciones

2. **Análisis Gráfico**
   - Gráficos de barras comparativas
   - Series temporales
   - Distribuciones de frecuencia

3. **Predicción ML**
   - Clasificación de eventos de contaminación
   - Probabilidades de ocurrencia
   - Recomendaciones por estación

---

## 📞 Contacto

- **Email**: info@weatherlocal.cl
- **Teléfono**: +56 52 2345678
- **Ubicación**: Copiapó, Región de Atacama, Chile
- **GitHub**: https://github.com/migellucero123/WeatherLocal-Copiapó

---

## 👩‍💻 Autores

- **Alicia Piero**
- Bootcamp DEV - AIEP

---

## 📄 Licencia

Este proyecto está bajo licencia **MIT**. Ver archivo `LICENSE` para más detalles.

---

## 🙏 Agradecimientos

- Datos meteorológicos simulados para fines educativos
- **Folium** por los mapas interactivos
- **OpenStreetMap** por los datos de cartografía
- **Scikit-learn** por las herramientas de Machine Learning
- **Jupyter** por el entorno interactivo

---

## 🔗 Enlaces Útiles

- [Documentación Folium](https://python-visualization.github.io/folium/)
- [Documentación Pandas](https://pandas.pydata.org/docs/)
- [Documentación Scikit-learn](https://scikit-learn.org/stable/)
- [Tutorial Jupyter](https://jupyter.org/try)

---

## 📝 Notas

- Este proyecto utiliza datos meteorológicos simulados para fines educativos
- El modelo ML se entrena con datos históricos de la región
- Las predicciones son estimaciones basadas en patrones históricos
- Para producción, se requeriría integración con APIs reales de meteorología

---

## 🚀 Mejoras Futuras

- [ ] Integración con API de datos meteorológicos reales
- [ ] Panel de control interactivo (Dash/Streamlit)
- [ ] Modelo LSTM para series temporales
- [ ] Alertas automáticas por email/SMS
- [ ] App móvil nativa
- [ ] Base de datos PostgreSQL
- [ ] Despliegue en cloud (AWS/Google Cloud)

---

**Última actualización**: Octubre 2025

---

<div align="center">

**Hecho con ❤️ en Copiapó, Región de Atacama, Chile**

⭐ Si te gustó este proyecto, ¡déjanos una estrella en GitHub!

</div>