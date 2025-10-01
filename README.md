# Proyecto de Reconocimiento de Señas Estáticas

Sistema en desarrollo para identificar señas estáticas del lenguaje de señas mediante visión computacional.

## Estado actual

Este proyecto está en una fase inicial de desarrollo.
- Actualmente, el sistema puede detectar señas estáticas individuales y asociarlas con letras del alfabeto.

- Se creó un pipeline que permite al usuario tomar screenshots en tiempo real para generar nueva data, junto con funciones de preprocesamiento y un proceso automatizado para entrenar el modelo llamando solo a funciones específicas.

- Para el reconocimiento, se utilizan los **landmarks** extraídos con MediaPipe como input para un modelo de perceptrón multicapa (MLP), que procesa estas coordenadas para clasificar las señas.

- El enfoque principal está en mejorar continuamente el preprocesamiento y el rendimiento del modelo.

- Se aplicó **normalización de keypoints** para mejorar la precisión y la consistencia en el reconocimiento, y el modelo aprenda las distribuciones espaciales de las señas.

- El procesamiento se realiza sobre imágenes estáticas capturadas desde cámara, sin incluir todavía señas dinámicas ni palabras completas.

## Acceso al código

Por el momento, el proyecto no está disponible públicamente, ya que aún está en proceso de mejora continua y optimización.

## Próximos pasos

- Extender el reconocimiento a señas dinámicas.
