## Selección y ejecución de modelo Zero-Shot en Hugging Face

Para este laboratorio se ingresó a la plataforma **HuggingFace** con el fin de probar un modelo de clasificación *Zero-Shot*.  
Este tipo de modelos permite clasificar textos sin necesidad de entrenamiento adicional, comparando el contenido del texto con una lista de etiquetas proporcionadas por el usuario.

###  Modelo seleccionado
Se seleccionó el modelo: Este modelo pertenece a la familia DeBERTa v3 y está diseñado para clasificar textos sin entrenamiento adicional, comparando el contenido del texto con distintas etiquetas candidatas (Zero-Shot Classification).

<img width="921" height="575" alt="image" src="https://github.com/user-attachments/assets/9e5209d4-ba70-413a-85a5-0b0508469016" />

## Resultados obtenidos 

<img width="921" height="527" alt="image" src="https://github.com/user-attachments/assets/1988561b-0b83-4eb9-93cb-66fcafb89cc9" />

## ⭐ Comparación de eficiencia entre el modelo Zero-Shot y HuggingFace

Para evaluar la eficiencia entre modelos open-source, se comparó el rendimiento del modelo **DeBERTa-v3 Zero-Shot** con el modelo **DistilBERT-SST2**, ambos ejecutados desde la plataforma HuggingFace.

La comparación se realizó midiendo los siguientes criterios:

-  **Tiempo de ejecución (latencia)**
-  **Precisión o coherencia del resultado**
-  **Complejidad del modelo**
-  **Requerimientos de procesamiento**

---

##  Eficiencia del modelo Zero-Shot (DeBERTa-v3-large)

- Es un modelo **grande y complejo** (~0.4B parámetros).
- Capaz de clasificar textos **sin entrenamiento previo**, utilizando *NLI (Natural Language Inference)*.
- La predicción para el texto analizado fue correcta: **“educación”**, con niveles de confianza muy altos.
- Su **tiempo de inferencia es mayor** debido al tamaño de su arquitectura.

### Ventajas
- Funciona para **cualquier conjunto de etiquetas personalizadas**.
- Excelente para tareas donde **no existe un modelo entrenado específicamente**.

### Desventajas
- **Mayor tiempo de ejecución**.
- Requiere más capacidad computacional.

##  Eficiencia del modelo HuggingFace DistilBERT

El segundo modelo probado fue **distilbert-base-uncased-finetuned-sst-2-english**, especializado en análisis de sentimiento.

- Es un modelo **ligero** (~66M parámetros).
- Está extremadamente **optimizado y es rápido**.
- Su tiempo de inferencia es **mucho menor** en comparación con DeBERTa.
- Sin embargo, es **menos flexible**, ya que solo sirve para *sentiment analysis*.

 ## Ventajas
- **Muy rápido** en ejecución.
- Ideal para tareas específicas como sentimiento.

##  Desventajas
- No sirve para **Zero-Shot**.
- No permite usar **etiquetas personalizadas**.


## 📊 Tabla comparativa de eficiencia entre modelos

| Modelo                                      | Tipo de tarea            | Tamaño (parámetros) | Tiempo de inferencia | Flexibilidad | Observaciones |
|---------------------------------------------|---------------------------|----------------------|-----------------------|--------------|----------------|
| DeBERTa-v3-large-ZeroShot                   | Zero-Shot Classification  | ~400M                | (coloca tu tiempo)    | Muy alta     | Clasifica cualquier etiqueta |
| DistilBERT-base-uncased-finetuned-SST2      | Sentiment Analysis        | ~66M                 | (coloca tu tiempo)    | Baja         | Rápido pero limitado a sentimiento |









