# Vertex Tarea M.H



**Descripción**: Implementación de red neuronal para predicción de precio de casa, mediante la generación de pipeline en Vertex IA de Google Cloud.

**Requisitos**

1.  Cuenta GCP
2.  Cuenta de servicio con permisos para Google Storage y Vertex IA
3.  Python 3.10

Dependencias - PIP:

-   google-cloud-aiplatform==1.18.1
-   tensorflow==2.16.1
-   kfp==1.8.22

> Es importante que reemplace el valor de las variables de entorno para
> la ejecución del notebook.

**Componentes**

A continuación, una breve explicación de los componentes:

 - **LOAD DATA**: El primer componente obtiene datos de Cloud Storage para
   generar un DataFrame de pandas.
   
   **SPLIT DATA AND TRAIN MODEL**: Este componente realiza el split de la
   data para el entrenamiento y test para posteriormente hacer la
   implementación de la red neuronal.
   
   **UPLOAD MODEL**: Se encarga de subir el modelo de red neuronal a Vertex
   AI.
   
   **ENDPOINT CREATE**: Despliega el modelo, generando una URL para el
   endpoint para ser consumido.

Finalmente, se crea el pipeline que contiene los componentes ya mencionados.

A continuación, se realiza la ejecución del pipeline en GCP.

> El código se encuentra en el notebook Tarea.ipynb.

**Consideraciones**: En el proceso completo se consideraba la ejecución de un pipeline en Vertex, el cual daba como resultado un modelo que debería desplegarse en un endpoint para ser consumido.
