# Descripción General

Esta API desarrollada con Flask en Chromebook proporciona una interfaz para interactuar con modelos de Machine Learning (Regresión Logística, SVM, Árbol de Decisión y Random Forest) pre-entrenados para clasificar flores del dataset Iris. Permite enviar las características de una flor (longitud y ancho del sépalo y del pétalo) y recibir una predicción sobre su especie.

# Requisitos

Antes de comenzar, asegúrate de tener instalado lo siguiente en tu sistema:

* **Python 3.x**
* **pip** (el gestor de paquetes de Python)

# Instalación

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

# Uso

### Activar el Entorno Virtual

Si has cerrado la terminal o el entorno virtual no está activo, asegúrate de activarlo antes de continuar:

**En Chromebook:** `source flask/bin/activate`

Deberías ver `(flask)` al principio de tu línea de comandos, indicando que el entorno virtual está activo.

### Ejecutar la API de Flask

Una vez que el entorno virtual esté activo y las dependencias instaladas, ejecuta la aplicación Flask con el siguiente comando:

```bash
python3 app.py
```

La API se iniciará y mostrará información sobre el servidor en tu terminal, incluyendo la dirección en la que está corriendo (normalmente http://127.0.0.1:5001).

### Realizar Peticiones de Predicción

Puedes interactuar con la API enviando peticiones HTTP POST a los endpoints de predicción con datos en formato JSON. 

# Ejemplo con Postman
1. **Abre la aplicación Postman**
   
2.  **Crea una nueva solicitud**

3. **Selecciona el método POST**

4. **Ingresa la URL del endpoint (http://127.0.0.1:5001)**

5. **Ve a la pestaña "Headers" y añade una clave Content-Type con el valor application/json**

6. **Ve a la pestaña "Body", selecciona la opción "raw" y elige el formato "JSON"**

7. **Ingresa los datos JSON en el cuerpo:**

 JSON
      
    {
    "sepal_length": 6.3,
    "sepal_width": 2.9,
    "petal_length": 5.6,
    "petal_width": 1.8
    }


8. **Haz clic en "Send". La respuesta de la API se mostrará en la sección de resultados**


# Endpoints de la API
### La API ofrece los siguientes endpoints para la predicción:

**/predict/logistic**

**/predict/svm**

**/predict/decisiontree** 

**/predict/randomforest**

### Todos los endpoints de predicción esperan una solicitud POST con un cuerpo JSON que contenga las siguientes claves:

sepal_length

sepal_width

petal_length

petal_width

# Modelos Disponibles

### Esta API actualmente soporta los siguientes modelos de Machine Learning para la clasificación de flores Iris:

Regresión Logística

SVM

Árbol de Decisión

Random Forest

**Nota:** Los modelos fueron pre-entrenados y están listos para realizar predicciones.


