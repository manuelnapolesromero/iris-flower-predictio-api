# iris-flower-prediction-api

# API de Predicción de la Flor de Iris con Modelos de Machine Learning

Este repositorio contiene el código para una API REST que utiliza modelos de Machine Learning preentrenados para predecir la especie de una flor de iris basándose en sus cuatro características: largo y ancho del sépalo, y largo y ancho del pétalo.

Se han entrenado cuatro modelos distintos: Regresión Logística, Árbol de Decisión, Máquina de Vectores de Soporte (SVM) y Bosque Aleatorio (Random Forest). Cada modelo está disponible a través de un endpoint diferente de la API.

## Estructura del Proyecto
iris-flower-prediction-api/

├── models/

│   ├── model_logistic.h5

│   ├── model_forest.h5

│   ├── model_svm.h5

│   └── model_tree.h5

├── app.py          # Código principal de la API Flask

├── iris_models.py  # Script para entrenar y guardar los modelos

└── requirements.txt # Lista de dependencias de Python

<img src="blob:chrome-untrusted://media-app/cc818e29-8865-4427-ac8f-7941d206d7e2" alt="Screenshot 2025-05-04 11.48.28.png"/>![image](https://github.com/user-attachments/assets/e6953eb2-0a6e-43f0-9ff1-0fffcea5ace7)
