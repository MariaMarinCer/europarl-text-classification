# europarl-text-classification
Detección de idiomas utilizando Europarl Parallel Corpus con modelos de aprendizaje automático y procesamiento de lenguaje natural.

## Autoría: María Marín Cerdá
# Detección Automática de Idiomas con Europarl Parallel Corpus

Este proyecto tiene como objetivo la detección automática del idioma en textos del **Europarl Parallel Corpus**, aplicando técnicas de procesamiento de lenguaje natural (PLN) y modelos de clasificación supervisados. El trabajo se centra en distinguir entre siete idiomas europeos: español, portugués, francés, inglés, alemán, lituano y polaco.

## Índice

- [Introducción](#introducción)
- [Origen de los Datos](#origen-de-los-datos)
- [Limpieza y Preprocesamiento](#limpieza-y-preprocesamiento)
- [Análisis Exploratorio de Datos (EDA)](#análisis-exploratorio-de-datos-eda)
- [Modelado Automático y Evaluación](#modelado-automático-y-evaluación)
- [RNN](#rnn)
- [Conclusiones](#conclusiones)

## Introducción

La detección de idioma es una tarea fundamental en el procesamiento de lenguaje natural, especialmente en entornos multilingües como la Unión Europea. Este proyecto implementa diferentes técnicas de PLN y modelos de clasificación supervisados para identificar el idioma de origen de un texto, partiendo de discursos parlamentarios multilingües.

## Origen de los Datos

Los textos utilizados provienen del **Europarl Parallel Corpus**, un corpus paralelo multilingüe que contiene transcripciones de debates del Parlamento Europeo en varios idiomas. Se han seleccionado los siguientes idiomas para el estudio:

- Español  
- Portugués  
- Francés  
- Inglés  
- Alemán  
- Lituano  
- Polaco

## Limpieza y Preprocesamiento

Se aplicaron técnicas de limpieza y normalización de texto, entre ellas:

- Conversión a minúsculas  
- Eliminación de caracteres puntuación similar en las diversas lenguas
- Tokenización  
- Eliminación de cifras numéricas

Además, se equilibró el número de muestras por idioma para evitar sesgos en el entrenamiento.

## Análisis Exploratorio de Datos (EDA)

Durante esta etapa se analizaron:

- Frecuencias de palabras por idioma  
- Longitud media de los textos  
- Distribución de clases  
- Nubes de palabras para cada idioma

Esto permitió identificar patrones lingüísticos útiles para la clasificación.

## Modelado Automático y Evaluación
Para representar los textos, se probaron distintas técnicas de vectorización:

- **TF-IDF por palabra**  
- **TF-IDF por carácter**  
- **Vectorización mediante hashing (HashingVectorizer)**

Se entrenaron diversos modelos de clasificación supervisada, entre ellos:

- Regresión Logística  
- Multinomial Naive Bayes  


Para cada modelo se calcularon métricas como *accuracy*, *precision*, *recall* y *F1-score*. Se utilizó conjunto de entrenamiento, validación y test para asegurar la estabilidad de los resultados.

## RNN 
Tras una secuenciación del texto mediante tokenización, se implementaron modelos basados en redes neuronales recurrentes para la detección de idiomas. En concreto, se utilizaron dos arquitecturas:
- Red Neuronal Recurrente (RNN) simple 
- LSTM Bidireccional


## Conclusiones

El modelo que obtuvo el mejor rendimiento fue el de **Regresión Logística**, destacándose por su mayor *accuracy* y facilidad de implementación. Esto lo convierte en la opción más eficaz y práctica para la tarea de detección de idioma en textos multilingües del Europarl Parallel Corpus.

