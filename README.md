# Proyecto de Reconocimiento de Señas Estáticas y Señas Dinámicas

Este proyecto realiza el reconocimiento de señas estáticas del alfabeto manual utilizando computer vision y deep learning.


## Demo

El siguiente video muestra el funcionamiento en tiempo real del modelo reconociendo las letras de algunas palabras del alfabeto para los que fue entrenado:
- a, b, c, d, e, f, h

![GIF_Sample](link)

Por el momento, estas letras fueron consideradas para verificar el preprocesamiento de los keypoints (invarianza a escala si el gesto se realiza muy cerca de la cámara) y posteriormente entrenar al modelo.  


## Desarrollo
- Uso de MediaPipe para la extracción de landmarks (keypoints) de la mano, que servirán como inputs del modelo.
- Funciones de preprocesamiento para la invarianza a escala de los keypoints, tanto para entrenamiento como inferencia.
- Implementación de un multilayer perceptron (MLP) para clasificación de señas.


## Pipeline del proyecto
Este proyecto cuenta con un pipeline automatizado para la recolección de datos, limpieza y procesamiento de datos desde cero para entrenar el modelo de reconocimiento de señas.

### Etapas:
#### 1) Recolección de datos
- Implementé un pipeline que permite al usuario tomar screenshots en tiempo real para generar nueva data.
- Los keypoints recolectados en el paso anterior, son almacenados en archivos .csv individuales por clase.
- Creación de funciones específicas para juntar los archivos .csv individuales y dividirlos en train/test sets.

#### 2) Preprocesamiento






## Estado actual

- El proyecto cuenta con un modelo funcional para el reconocimiento de señas estáticas individuales, basado en landmarks extraídos con MediaPipe y procesados mediante un perceptrón multicapa (MLP).

- Se creó un pipeline que permite al usuario tomar screenshots en tiempo real para generar nueva data, junto con funciones de preprocesamiento y un proceso automatizado para entrenar el modelo llamando solo a funciones específicas.

- Para el reconocimiento, se utilizan los **landmarks** extraídos con MediaPipe como input para un modelo de perceptrón multicapa (MLP), que procesa estas coordenadas para clasificar las señas.

- El enfoque principal está en mejorar continuamente el preprocesamiento y el rendimiento del modelo.

- Se aplicó **normalización de keypoints** para mejorar la precisión y la consistencia en el reconocimiento, y el modelo aprenda las distribuciones espaciales de las señas.

- El procesamiento se realiza sobre imágenes estáticas capturadas desde cámara, sin incluir todavía señas dinámicas ni palabras completas.

- Se busca mejorar el sistema a clasificación de señas dinámicas.
  
## Acceso al código

- El código fuente no se encuentra disponible públicamente ya que el proyecto continúa en desarrollo activo y en proceso de mejora técnica.

- El repositorio se mantiene privado mientras se realizan mejoras en el sistema y se optimiza el modelo para lograr resultados más robustos y confiables en señas dinámicas.

## IMPORTANTE

- Actualmente estoy trabajando en la extensión del sistema para reconocer señas dinámicas, utilizando modelos recurrentes para procesar secuencias de movimiento.

