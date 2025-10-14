# Proyecto de Reconocimiento de Señas Estáticas y Señas Dinámicas

Este proyecto realiza el reconocimiento de lenguaje de señas estáticas del alfabeto manual utilizando computer vision y deep learning.


## Demo

El siguiente video muestra el funcionamiento en tiempo real del modelo reconociendo las letras de algunas letras para las que fue entrenado:
- a, b, c, d, e, f, h
  
![]()

Estas letras se utilizaron para validar el preprocesamiento de los keypoints (invarianza a escala, por ejemplo cuando el gesto está muy cerca de la cámara) y para entrenar el modelo inicial.


## Desarrollo
- Uso de MediaPipe para la extracción de landmarks (keypoints) de la mano, que sirven como inputs para el modelo.
- Funciones de preprocesamiento para lograr invarianza a escala en los keypoints, aplicadas tanto en entrenamiento como en inferencia.
- Implementación de un perceptrón multicapa (MLP) para clasificación de señas.



## Pipeline del proyecto
Este proyecto cuenta con un pipeline automatizado para la recolección, limpieza y preprocesamiento de datos desde cero para entrenar el modelo de reconocimiento de señas, facilitando la escalabilidad del proyecto.


### Etapas:
#### 1) Recolección de datos
  - Pipeline que permite al usuario tomar screenshots en tiempo real para generar nueva data.
  - Los keypoints recolectados se almacenan en archivos .csv individuales por clase.
  - Funciones para unir los archivos .csv y dividir los datos en sets de entrenamiento y prueba.



#### 2) Preprocesamiento
  - Normalización y escalamiento de keypoints para invarianza a escala.
  - Conversión a tensores para entrenamiento, y uso de DataLoaders para batches.


#### 3) Entrenamiento
- Función automatizada para entrenar el modelo con los datos procesados.



## Estado actual
Modelo funcional para reconocimiento de señas estáticas individuales, basado en landmarks extraídos con MediaPipe y procesados mediante un MLP.
  - Pipeline de recolección y preprocesamiento que facilita la ampliación y mejora continua.
  - Normalización aplicada para mejorar precisión y consistencia.
  - Procesamiento basado en imágenes estáticas, sin soporte para señas dinámicas todavía.
  - **Próximo objetivo**: extender reconocimiento a señas dinámicas mediante modelos recurrentes.

  
## Acceso al código

- El código fuente no se encuentra disponible públicamente ya que el proyecto continúa en desarrollo activo y en proceso de mejora técnica.

- El repositorio se mantiene privado mientras se realizan mejoras en el sistema y se optimiza el modelo para lograr resultados más robustos y confiables en señas dinámicas.

## IMPORTANTE

- Actualmente estoy trabajando en la extensión del sistema para reconocer señas dinámicas, utilizando modelos recurrentes para procesar secuencias de movimiento.

