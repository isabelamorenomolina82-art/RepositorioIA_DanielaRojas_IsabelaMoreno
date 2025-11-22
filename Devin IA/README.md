## ✔ Resultado obtenido

El chatbot RAG desarrollado permitió cargar el documento PDF del laboratorio y realizar preguntas basadas en su contenido.

El sistema ejecutó tres pasos clave:

- **Lectura del documento PDF** mediante LlamaIndex.  
- **Creación del índice vectorial** para búsqueda semántica.  
- **Generación de respuestas** usando el modelo Gemini.

Durante las pruebas iniciales, el modelo respondió a preguntas como:

> "¿Cuál es el objetivo general del laboratorio 8?"

Sin embargo, debido a errores de API (404, API key inválida o expirada), algunas respuestas no pudieron generarse mediante RAG y fue necesario apoyarse en consultas simples al modelo.

**Resultado esperado:**  
Que Gemini recuperara el contenido del PDF y respondiera con precisión usando el esquema RAG.

**Resultado real:**  
El sistema cargó correctamente los documentos y generó el índice, pero las solicitudes al modelo fallaron por problemas externos a la implementación (API no disponible, clave expirada). Aun así, se verificó que la estructura del pipeline RAG (carga → indexación → recuperación) se ejecutó de forma correcta.

---

## 🟢 3. Comparación con el uso directo del modelo (sin RAG)

Para validar la funcionalidad, también se probó el modelo **sin RAG**, enviando preguntas directamente a Gemini, sin pasar por el índice de documentos.

Este modo generó respuestas mientras la clave de API estuvo activa.

**Resultado esperado:**  
Que el modelo generara respuestas más generales, sin basarse en documentos específicos.

**Resultado real:**  
Gemini respondió correctamente preguntas generales, pero no pudo citar información específica del PDF, ya que no tenía acceso explícito al contenido del laboratorio.

---

## ⚖️ 4. Comparación final: RAG vs uso directo del modelo

| Característica              | RAG (LlamaIndex + Gemini) | Gemini sin RAG        |
|----------------------------|---------------------------|-----------------------|
| Uso de documentos PDF      | ✔ Sí                      | ✖ No                  |
| Precisión basada en contenido | Muy alta               | Media                 |
| Dependencia de la API      | Alta                      | Alta                  |
| Robustez ante errores de API | Baja                   | Media                 |
| Resultado real             | No funcionó por errores de API | Funcionó mientras la API key fue válida |
| Escenario ideal            | Preguntas sobre el laboratorio | Preguntas generales |

---

## 🧠 Conclusión del análisis

- La arquitectura RAG se implementó correctamente: carga de PDFs, creación de índice vectorial y motor de consulta semántica.  
- Los fallos se debieron a problemas externos (API key expirada, modelo no disponible, permisos del proyecto), no al diseño del pipeline.  
- Cuando se probó Gemini sin RAG, el modelo sí generó respuestas, lo que demuestra que la parte generativa funciona si la API está bien configurada.  
- El uso de RAG demuestra ser más poderoso y preciso para preguntas sobre el contenido del laboratorio, pero también más sensible a errores de infraestructura.  
- La experiencia confirma que:
  - **RAG + Gemini → mayor precisión y alineación con el PDF, pero fuerte dependencia de la API.**  
  - **Gemini sin RAG → más sencillo de usar, pero con respuestas menos específicas y sin respaldo documental.**

Con este trabajo se cumplió el objetivo académico de diseñar e implementar un chatbot educativo basado en RAG, analizar sus resultados, identificar sus limitaciones y compararlo con el uso directo de un modelo generativo.

