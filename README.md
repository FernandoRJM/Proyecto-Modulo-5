# Detector de Noticias Falsas con Redes Neuronales (NLP)

## 📝 Descripción
Este proyecto desarrolla un modelo de Deep Learning diseñado para clasificar noticias como "reales" o "falsas" (fake news). Utilizando técnicas de Procesamiento de Lenguaje Natural (NLP) y redes neuronales secuenciales, el modelo analiza el contenido textual para identificar patrones de desinformación, un problema crítico exacerbado desde la pandemia de COVID-19.

## 🛠️ Herramientas y Tecnologías
• Lenguaje: Python 3.x. 
• Librerías principales: TensorFlow/Keras, Pandas, NumPy, Scikit-Learn, NLTK. 
• Técnicas de NLP: * Tokenización y limpieza de texto (remoción de stopwords). * Secuenciación y Padding de texto. * Capas de Embedding para representación vectorial de palabras. • Arquitectura del Modelo: Red Neuronal Secuencial (Sequential) con capas densas y funciones de activación personalizadas.

## 📊 Dashboard / Resultados
El modelo de red neuronal secuencial fue diseñado y entrenado para la detección de noticias falsas utilizando el dataset WELFake. Los resultados clave fueron:

1. Desempeño del Modelo

- Accuracy: El modelo alcanzó una precisión del 94.5% en el conjunto de validación tras el entrenamiento.
- Loss: Se logró reducir la pérdida hasta un valor de 0.12, lo que indica una alta capacidad de generalización del modelo frente a nuevos textos.
- Optimización de Épocas: Se determinó que 5 épocas de entrenamiento eran el punto óptimo. Más allá de esto, se observó el inicio de un ligero overfitting donde la precisión de entrenamiento seguía subiendo pero la de validación se estabilizaba.

2. Pruebas de Validación Externa
El modelo fue sometido a pruebas con artículos reales fuera del dataset original:

- Noticia Falsa (Breitbart): El modelo clasificó correctamente el artículo sobre James Comey como "FAKE" con un alto nivel de confianza.
- Noticia Verdadera (Washington Post): El modelo identificó correctamente el artículo sobre la árbitra Kathryn Nesbitt como "REAL".

3. Arquitectura y Preprocesamiento
Se implementó una capa de Embedding para convertir las palabras en vectores densos, seguida de capas Flatten y Dense con activación ReLU y Sigmoid.
El preprocesamiento incluyó la eliminación de stopwords y la tokenización de las 10,000 palabras más frecuentes, asegurando que el modelo se centrara en el contenido semántico relevante.
