# los_simpson
### 1. Corrección en la carga de datos de prueba
- Se eliminó un filtro incorrecto que estaba incluido en la función de carga de datos de prueba.
- Ese filtro venía del modelo anterior de bounding box y alteraba los canales de color de las imágenes, convirtiéndolos de RGB a BGR, lo que provocaba errores sistemáticos de predicción, especialmente clasificando muchas imágenes como Milhouse y Krusty que tenian en comun el pelo azul, incluso cuando no aparecían.
### 2. Mejora del modelo CNN
- Aprovechando tiempo extra disponible, se decidió mejorar el modelo y construir una arquitectura más robusta y profunda.
- El nuevo modelo tiene mayor capacidad de representación y mejora significativamente el `accuracy`, haciéndolo **más presentable y competitivo**.
- Se mantuvo el uso de técnicas de regularización (`Dropout`, `BatchNormalization`) y se entrenó con mayor resolución (128x128).
### 3. Predicción por imagen individual
- Agrega una nueva funcionalidad para mostrar **predicciones con imágenes individuales del conjunto de prueba**, mostrando tanto la clase real como la predicha.
- Las imágenes se visualizan junto a la predicción del modelo, marcadas en verde si son correctas y rojo si son incorrectas, lo cual **facilita el análisis visual del rendimiento**.
### 4. Matriz de confusión (heatmap) sobre los datos de prueba
- La matriz de confusión ya estaba implementada previamente, pero no fue mencionada en la presentacion porque se nos fue ya que estabamos al 100% con el tema del gradio y la prediccion.
