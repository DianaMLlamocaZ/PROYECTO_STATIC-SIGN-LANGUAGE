# Proyecto de Reconocimiento de Señas Estáticas y Señas Dinámicas

Sistema para identificar señas estáticas y dinámicas del lenguaje de señas mediante visión computacional.

## Estado actual

- El proyecto cuenta con un modelo funcional para el reconocimiento de señas estáticas individuales, basado en landmarks extraídos con MediaPipe y procesados mediante un perceptrón multicapa (MLP).

- Se creó un pipeline que permite al usuario tomar screenshots en tiempo real para generar nueva data, junto con funciones de preprocesamiento y un proceso automatizado para entrenar el modelo llamando solo a funciones específicas.

- Para el reconocimiento, se utilizan los **landmarks** extraídos con MediaPipe como input para un modelo de perceptrón multicapa (MLP), que procesa estas coordenadas para clasificar las señas.

- El enfoque principal está en mejorar continuamente el preprocesamiento y el rendimiento del modelo.

- Se aplicó **normalización de keypoints** para mejorar la precisión y la consistencia en el reconocimiento, y el modelo aprenda las distribuciones espaciales de las señas.

- El procesamiento se realiza sobre imágenes estáticas capturadas desde cámara, sin incluir todavía señas dinámicas ni palabras completas.

- Se busca mejorar el sistema a clasificación de señas dinámicas.
  
## Acceso al código

Por el momento, el proyecto no está disponible públicamente, ya que aún está en proceso de mejora continua y optimización.

## Próximos pasos

- Extender el reconocimiento a señas dinámicas.
