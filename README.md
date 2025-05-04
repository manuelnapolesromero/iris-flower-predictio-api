# iris-flower-prediction-api

# API de Predicción de la Flor de Iris con Modelos de Machine Learning

Este repositorio contiene el código para una API REST que utiliza modelos de Machine Learning preentrenados para predecir la especie de una flor de iris basándose en sus cuatro características: largo y ancho del sépalo y largo y ancho del pétalo.

**Se han entrenado cuatro modelos distintos:** Regresión Logística, Árbol de Decisión, Máquina de Vectores de Soporte (SVM) y Bosque Aleatorio (Random Forest). Cada modelo está disponible a través de un endpoint diferente de la API.

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

## Descripción General de la API:

Esta API, desarrollada utilizando el framework Flask en Python, tiene como propósito fundamental ofrecer funcionalidades de predicción basadas en modelos de Machine Learning. En el ejemplo proporcionado, la API se centra en la clasificación de datos del dataset Iris.

## ¿Qué hace?

La API realiza las siguientes acciones principales:

**Expone modelos de Machine Learning:** A través de diferentes rutas o "endpoints", la API permite interactuar con modelos pre-entrenados. En este caso, se han entrenado y cargado modelos de Regresión Logística, Bosque Aleatorio, Maquinas de Soporte Vectorial y Arból de decisión.

**Recibe solicitudes de predicción:** Los usuarios o aplicaciones pueden enviar datos a la API a través de peticiones HTTP POST a endpoints específicos (como /predict/logistic, /predict/randomforest, /predict/svm, /predict/tree_decision).

**Procesa los datos de entrada:** La API espera recibir datos en un formato específico (aunque no se detalla en la información proporcionada) para poder alimentar los modelos de Machine Learning.

**Realiza predicciones:** Utilizando los modelos cargados, la API procesa los datos de entrada y genera una predicción sobre la clase a la que pertenece la muestra.

**Devuelve resultados:** La API responde a las solicitudes con los resultados de la predicción, probablemente en un formato como JSON, para que la aplicación cliente pueda interpretarlos.

**Sirve una interfaz web básica (opcional):** La presencia de una petición GET a la ruta / sugiere que la API podría ofrecer una página web básica, aunque su funcionalidad específica no se describe.

## ¿Cuál es su propósito?

El propósito principal de esta API es democratizar el acceso a los modelos de Machine Learning entrenados. En lugar de requerir que otras aplicaciones o usuarios implementen los modelos directamente, la API actúa como un intermediario, permitiendo:

**Reutilización de modelos:** Los modelos entrenados pueden ser utilizados por múltiples aplicaciones sin necesidad de re-entrenamiento.

**Abstracción de la complejidad:** Las aplicaciones cliente no necesitan conocer los detalles internos de los modelos de Machine Learning ni las bibliotecas utilizadas para su implementación. Solo necesitan saber cómo comunicarse con la API.

**Integración sencilla:** Permite integrar capacidades de Machine Learning en diversas aplicaciones web o sistemas a través de solicitudes HTTP estándar.

**Escalabilidad:** Al desacoplar los modelos de las aplicaciones cliente, se facilita la escalabilidad y el mantenimiento de la infraestructura de Machine Learning.

**Nota:** Esta API de Machine Learning para la clasificación del dataset Iris busca ofrecer una forma sencilla y eficiente de obtener predicciones a partir de modelos pre-entrenados a través de una interfaz web.
