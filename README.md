# 🧠 Clasificación de Sentimientos y Emociones en Español

Este proyecto tiene como propósito desarrollar un modelo de **aprendizaje supervisado** para clasificar automáticamente textos en español. El sistema determina tanto la **polaridad del sentimiento** (positivo, negativo, neutral, no asignado) como la **emoción predominante** (alegría, miedo, tristeza, asco, ira, sorpresa o neutral), utilizando los datasets **InterTASS** y **EmoEvent**.

---

## 🎯 Objetivos

### Objetivo General
Desarrollar un pipeline de NLP que clasifique textos en español según su sentimiento y emoción utilizando modelos de aprendizaje supervisado.

### Objetivos Específicos
- **Aplicar** técnicas de *Procesamiento de Lenguaje Natural (NLP)* para limpiar, normalizar y vectorizar textos.
- **Entrenar** un modelo supervisado con el dataset **InterTASS** para la clasificación de sentimientos.
- **Entrenar** un modelo supervisado con el dataset **EmoEvent** para la clasificación de emociones.
- **Evaluar** el rendimiento mediante métricas estándar (Precisión, Recall, F1-score).
- **Analizar** las palabras y expresiones que más influyen en la predicción de cada categoría.

---

## 📂 Descripción de los Datasets

### 1. InterTASS (Análisis de Sentimientos)
* **Contenido:** Tweets en español (España y Latinoamérica).
* **Tamaño:** ~40,000 tweets.
* **Objetivo:** Identificar la polaridad del sentimiento.
* **Etiquetas:**
    * `P` → Positivo
    * `N` → Negativo
    * `NEU` → Neutral
    * `NONE` → No asignado

### 2. EmoEvent (Análisis de Emociones)
* **Contenido:** Tweets en español clasificados por emociones humanas.
* **Tamaño:** ~21,000 tweets.
* **Objetivo:** Detectar la emoción predominante.
* **Etiquetas:**
    * Alegría, Miedo, Tristeza, Asco, Ira, Sorpresa, Neutral.

---

## ⚙️ Metodología

### Fase 1: Preparación y Exploración de Datos
- [ ] Carga de datasets (CSV/XML).
- [ ] Análisis exploratorio de la distribución de clases.
- [ ] Visualización de ejemplos por categoría.

### Fase 2: Preprocesamiento de Texto
- [ ] Limpieza: Eliminación de URLs, menciones (@) y hashtags (#).
- [ ] Normalización: Conversión a minúsculas y eliminación de signos de puntuación.
- [ ] Filtrado: Tokenización y eliminación de *stopwords*.
- [ ] **Vectorización:**
    - TF-IDF (para modelos clásicos).
    - Embeddings de **BETO** (BERT en español) para Deep Learning.

### Fase 3: Entrenamiento del Modelo

| Modelo | Dataset | Algoritmos Sugeridos | Clases |
| :--- | :--- | :--- | :--- |
| **Sentimientos** | InterTASS | Logistic Regression, Random Forest, BETO | P, N, NEU, NONE |
| **Emociones** | EmoEvent | SVM, LSTM, BETO | Alegría, Miedo, Tristeza, Asco, Ira, Sorpresa, Neutral |

### Fase 4: Evaluación y Comparación
- Cálculo de métricas: **Accuracy, Recall, F1-Score**.
- Generación de **Matriz de Confusión**.
- Identificación de palabras frecuentes por categoría (Feature Importance).

### Fase 5: Implementación Práctica
Creación de una interfaz o script que reciba un texto y devuelva:
1. Clasificación del sentimiento.
2. Clasificación de la emoción.

---

## 📊 Ejemplo de Salida Esperada

| Texto de entrada | Sentimiento | Emoción |
| :--- | :--- | :--- |
| *"Estoy muy feliz con el resultado del partido"* | **Positivo (P)** | Alegría |
| *"Me siento triste por lo ocurrido"* | **Negativo (N)** | Tristeza |
| *"No estuvo mal, pero esperaba más"* | **Neutral (NEU)** | Neutral |
| *"Qué miedo me da esta situación"* | **Negativo (N)** | Miedo |

---

## 📦 Entregables

1.  **Reporte Técnico:** Metodología, descripción de modelos, resultados y conclusiones.
2.  **Código Fuente (Python):** Pipeline completo (entrenamiento, evaluación y predicción).
3.  **Presentación Final:** Visualizaciones de métricas y demos de clasificación.

---

## ❓ Preguntas de Análisis
El proyecto busca responder a las siguientes interrogantes:

* ¿Qué distribución de sentimientos predomina en el dataset InterTASS?
* ¿Qué emociones son más comunes en EmoEvent?
* ¿Cuál modelo tuvo mejor rendimiento: sentimientos o emociones?
* ¿Qué palabras están más asociadas a sentimientos negativos?
* ¿Qué diferencias existen entre clasificar sentimientos vs. emociones?
* ¿Cómo se integraría este modelo en una aplicación real (ej. atención al cliente)?
* ¿Qué ventajas ofrece BETO frente a TF-IDF?
* ¿Cómo mejorar la detección de emociones mixtas?

---

## 📝 Conclusión Esperada

> El proyecto permitirá desarrollar un sistema capaz de **interpretar automáticamente el estado emocional y la polaridad** de mensajes en español. Esto demostrará la eficacia del aprendizaje supervisado y el NLP para el análisis de opiniones, fomentando la comprensión del lenguaje afectivo en áreas como marketing digital y monitoreo social.
