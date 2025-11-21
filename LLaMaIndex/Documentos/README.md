## Descripcion 

LLaMaIndex es un framework especializado para construir sistemas de Recuperación Aumentada por Generación (RAG). Permite crear asistentes que responden con precisión utilizando información proveniente de documentos propios, como PDFs, bases de datos, APIs, páginas web y archivos locales. El framework gestiona la ingestión, indexación y consulta del conocimiento, garantizando respuestas basadas en evidencia y sustentadas en fuentes verificables.

## Creacion con cinco documentos 
 <img width="425" height="426" alt="image" src="https://github.com/user-attachments/assets/ac2e671f-0ad9-4470-9f94-4f6352b848ab" />

 ## Configuracion 


### 2.9.1 Ingestión de documentos

Para la fase de ingestión se creó una carpeta llamada `Documentos/` que contiene 5 archivos PDF propios (actividades, resúmenes y guías de la asignatura).  
Desde el notebook de Google Colab se cargaron todos los documentos usando el lector de directorios de LLaMaIndex:

<img width="921" height="572" alt="image" src="https://github.com/user-attachments/assets/5148b432-1335-4030-8a05-94c9e0042917" />

## Capturas de consultas 

<img width="1785" height="487" alt="image" src="https://github.com/user-attachments/assets/09ac40de-0055-4617-a2b4-ae2f4d7bc916" />

## Arquitectura RAG con LLaMaIndex

##  1. ¿Qué es la arquitectura RAG?

1. **Recuperación de información (Retrieval)** → busca documentos relevantes.
2. **Generación de texto (Generation)** → produce respuestas basadas en evidencia.

El objetivo es generar respuestas precisas, evitando alucinaciones, y usando documentos reales como fuente de verdad.
---

Usuario → Pregunta
          ↓
     Embedding de la pregunta
          ↓
   Búsqueda en índice vectorial
          ↓
Fragmentos relevantes obtenidos
          ↓
  Motor de generación (LLM)
          ↓
Respuesta basada en evidencia


## Ventajas del enfoque RAG

- Reduce significativamente las alucinaciones del modelo.
- Permite integrar información propia sin necesidad de reentrenar modelos.
- Facilita la búsqueda semántica avanzada mediante embeddings.
- Ideal para investigación, educación y análisis técnico.
- Compatible con múltiples tipos de documentos (PDF, texto, web, APIs).
- Se puede combinar con cualquier LLM o motor generativo.

##  Limitaciones del enfoque RAG

- Los resultados dependen de la calidad del texto extraído del PDF.
- Si el PDF contiene imágenes o tablas, puede perderse información relevante.
- Un embedding mal configurado puede afectar la recuperación de información..
- Necesita una buena estructura de carpetas para mantener organizados los documentos.
- Los modelos de embeddings ligeros pueden perder matices importantes.



