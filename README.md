# machine_learning_api

Una API sencilla para la clasificación de flores Iris utilizando modelos de Machine Learning (Regresión Logística, SVM, Árbol de Decisión y Random Forest) desarrollada con Flask en Chromebook.

## Descripción General

Esta API proporciona una interfaz para interactuar con modelos de Machine Learning pre-entrenados para clasificar flores del dataset Iris. Permite enviar las características de una flor (longitud y ancho del sépalo y del pétalo) y recibir una predicción sobre su especie.

## Requisitos

Antes de comenzar, asegúrate de tener instalado lo siguiente en tu sistema:

* **Python 3.x**
* **pip** (el gestor de paquetes de Python)

## Instalación

Sigue estos pasos para configurar el entorno y ejecutar la API:

1.  **Clonar el repositorio (si aún no lo has hecho):**

    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd machine_learning_api
    ```

2.  **Crear un entorno virtual:**

    ```bash
    python3 -m venv flask
    ```

3.  **Activar el entorno virtual:**

    * **En Chromebook:**
        ```bash
        source flask/bin/activate
        ```

4.  **Instalar las dependencias:**

    ```bash
    pip3 install -r requirements.txt
    ```

## Uso

### Activar el Entorno Virtual

Si has cerrado la terminal o el entorno virtual no está activo, asegúrate de activarlo antes de continuar:

* **En Chromebook:** `source flask/bin/activate`

Deberías ver `(flask)` al principio de tu línea de comandos, indicando que el entorno virtual está activo.

### Ejecutar la API de Flask

Una vez que el entorno virtual esté activo y las dependencias instaladas, ejecuta la aplicación Flask con el siguiente comando:

```bash
python3 app.py
```

La API se iniciará y mostrará información sobre el servidor en tu terminal, incluyendo la dirección en la que está corriendo (normalmente http://127.0.0.1:5001).

## Realizar Peticiones de Predicción

Puedes interactuar con la API enviando peticiones HTTP POST a los endpoints de predicción con datos en formato JSON. 

# Ejemplo con Postman
Abre la aplicación Postman.


Crea una nueva solicitud.


Selecciona el método POST.


Ingresa la URL del endpoint (por ejemplo, http://127.0.0.1:5001).


Ve a la pestaña "Headers" y añade una clave Content-Type con el valor application/json.


Ve a la pestaña "Body", selecciona la opción "raw" y elige el formato "JSON".


Ingresa los datos JSON en el cuerpo:

 JSON
{
    "sepal_length": 6.3,
    "sepal_width": 2.9,
    "petal_length": 5.6,
    "petal_width": 1.8
}
Haz clic en "Send". La respuesta de la API se mostrará en la sección de resultados.


## Endpoints de la API
Actualmente, la API ofrece los siguientes endpoints para la predicción:

**/predict/logistic:** Utiliza el modelo de Regresión Logística para predecir la especie de la flor.

**/predict/svm:** Utiliza el modelo SVM para la predicción.

**/predict/decisiontree:** Utiliza el modelo de Árbol de Decisión para la predicción.

**/predict/randomforest:** Utiliza el modelo de Random Forest para predecir la especie de la flor.

**Todos los endpoints de predicción esperan una solicitud POST con un cuerpo JSON que contenga las siguientes claves:**

sepal_length (float)

sepal_width (float)

petal_length (float)

petal_width (float)

## Modelos Disponibles
**Esta API actualmente soporta los siguientes modelos de Machine Learning para la clasificación de flores Iris:**

Regresión Logística

SVM

Árbol de Decisión

Random Forest

**Nota:** Los modelos fueron pre-entrenados y están listos para realizar predicciones.


