# 🧠 Proyecto Integrador – Módulo 6  
## Aplicaciones Avanzadas de Machine Learning y Deep Learning

Este proyecto integra **Procesamiento de Lenguaje Natural (PLN)**, **Visión por Computadora** y **Aprendizaje por Refuerzo (RL)** para construir un sistema capaz de **priorizar casos de soporte** en función del sentimiento del mensaje, la emoción facial del cliente y reglas de decisión aprendidas mediante Q-Learning.

El objetivo es apoyar la toma de decisiones sobre **qué caso debe ser atendido primero**, incorporando principios de equidad, privacidad y reducción de sesgos.

---

## 📁 Estructura del Proyecto

Proyecto Integrador/
│
├── cuadernos/
│ ├── 01_eda_visualizacion.ipynb # EDA + modelos PLN y CNN
│ └── 02_integracion_y_rl.ipynb # Integración + Q-Learning
│
├── informes/
│ ├── Informe_Proyecto_Integrador.docx
│ └── img/ # Imágenes (gráficas)
│
├── src/ # Funciones, modelos reutilizables
│
├── data/
│ ├── raw/ # Datos originales (NO se suben)
│ └── processed/
│
├── requirements.txt # Dependencias
└── README.md


---

## 🧩 Componentes del Sistema

### 🔤 1. Procesamiento de Lenguaje Natural (IMDB – LSTM)

Se entrena un modelo **LSTM** para clasificar reseñas de texto en:

- Positivas ✔  
- Negativas ✖  

Este modelo permite estimar el **sentimiento del cliente** basado en su descripción.

---

### 😊 2. Visión por Computadora (FER2013 – CNN)

Se entrena una **Convolutional Neural Network** para reconocer 7 emociones faciales:

- angry  
- disgust  
- fear  
- happy  
- neutral  
- sad  
- surprise  

Este modelo complementa el análisis textual con señales visuales.

---

### 🎯 3. Agente de Aprendizaje por Refuerzo (Q-Learning)

El agente aprende a priorizar casos considerando:

- 🟢🟠🔴 Sentimiento detectado  
- 😡😢😊😱 Emoción facial  
- Estado simulado del sistema  
- Recompensas asociadas a decisiones óptimas  

El resultado es una **política automática de priorización**.

---

## ▶️ ¿Cómo ejecutar el proyecto?

### 1️⃣ Crear y activar entorno virtual

```bash
python -m venv .venv
.\.venv\Scripts\activate

pip install -r requirements.txt

cuadernos/01_eda_visualizacion.ipynb  
cuadernos/02_integracion_y_rl.ipynb

📦 Tecnologías utilizadas

Python 3.12
NumPy / Pandas
TensorFlow / Keras
Matplotlib / Seaborn
Scikit-learn
Q-Learning (RL básico)
Jupyter Notebooks
VS Code