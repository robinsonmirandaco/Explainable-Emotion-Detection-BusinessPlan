# Explainable Emotion Detection in Business Plans

Este repositorio contiene un prototipo funcional de análisis emocional aplicado a business plans escritos en español, con un enfoque en explicabilidad utilizando técnicas de NLP y XAI.

## Descripción

El objetivo principal es detectar la emoción predominante presente en un texto complejo (como un business plan) y explicar por qué el modelo tomó esa decisión, identificando las palabras que más contribuyeron a dicha emoción.

Para lograrlo, se traduce el texto original al inglés, se analiza con un modelo robusto de clasificación emocional (`j-hartmann/emotion-english-distilroberta-base`) y se aplica *Integrated Gradients* desde Captum para obtener interpretabilidad palabra por palabra.

## Características del proyecto

- Procesamiento de texto completo desde archivo PDF
- Traducción automática de español a inglés
- Detección de emociones con modelo de Hugging Face
- Aplicación de técnicas de explicabilidad (XAI) con Captum
- Reconstrucción y visualización de palabras clave que justifican la emoción
- Refuerzo del resultado ajustando la narrativa para activar emociones específicas

## Estructura
- Explainable_Emotion_Detection_BusinessPlan.ipynb: notebook principal con todo el flujo implementado

- business_plan.pdf: archivo de entrada que contiene el texto a analizar


## Resultados
- Emoción detectada: fear

- Palabras clave explicables detectadas: distrust, insecurity, losing, gap, etc.

- Visualizaciones integradas en el notebook

- Reflexión final sobre ajustes narrativos y rendimiento del modelo

## Referencias
- Hugging Face: j-hartmann/emotion-english-distilroberta-base

- Captum (Meta AI): https://captum.ai

- Paper base: Axiomatic Attribution for Deep Networks (Sundararajan et al., 2017)

- deep-translator: traducción simple desde Python



## Requisitos

- Python 3.8+
- Google Colab o Jupyter Notebook
- Dependencias:

```bash
pip install transformers captum deep-translator matplotlib

