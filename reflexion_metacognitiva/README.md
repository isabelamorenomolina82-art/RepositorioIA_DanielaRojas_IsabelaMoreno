# Reflexión Metacognitiva

## 1. Reflexión sobre el razonamiento analítico y técnico

**Qué tareas, consultas o decisiones dentro del laboratorio exigieron el uso más intenso de razonamiento analítico, verificación técnica o pensamiento lógico**

- La configuración de los pipelines de RAG con LLaMaIndex (ingestión, indexación y consultas) exigió revisar rutas, tipos de modelos y compatibilidad de versiones.
- El uso de Hugging Face para cargar distintos modelos (NLP, visión y audio) y entender sus limitaciones de entrada/salida.
- La comparación entre código manual y código generado por copilotos (Copilot, Codeium), verificando que los resultados fueran equivalentes y no solo “bonitos”.

**En qué momento tuviste que ir más allá de seguir instrucciones y empezar a diseñar, deducir, comparar o validar por tu cuent?**

Cuando aparecían errores en Colab (versiones de `transformers`, rutas de PDFs, llaves de API) tuve que: Leer el traceback, deducir qué paquete fallaba, buscar alternativas (cambiar modelo, quitar dependencias, adaptar el código).
Para organizar el repositorio en GitHub, no bastaba seguir el enunciado: tuve que diseñar una estructura coherente de carpetas y READMEs para que todo tuviera sentido técnico y narrativo.

## 2. Reflexión sobre corrección de supuestos y evolución conceptual

**¿Qué ideas iniciales tuviste sobre las plataformas o modelos que luego resultaron incompletas o erróneas?**

Al inicio pensaba que los copilotos “siempre” generaban código correcto sin necesidad de revisión. En la práctica vi que: A veces proponen soluciones que no se ajustan a la versión de las librerías o generan código demasiado genérico, sin considerar el contexto educativo del caso. También asumía que un pipeline RAG era “simplemente” preguntar a los documentos, pero descubrí que: La calidad depende mucho del embedding, del preprocesamiento de los textos, y  de cómo se formula la consulta.

**¿Cómo cambió tu comprensión de los modelos, pipelines o herramientas después de enfrentarte a la práctica real?**

Pasé de ver las herramientas como “cajas mágicas” a entenderlas como componentes de una arquitectura: LLM + embeddings + índice + orquestación.
Entendí que cada plataforma (Hugging Face, LLaMaIndex, copilotos, Google AI Studio, etc.) resuelve solo una parte del problema y que el diseño global sigue siendo responsabilidad del ingeniero.

## 3. Reflexión sobre estrategias de resolución de problemas

**¿Qué estrategias cognitivas utilizaste para resolver problemas o interpretar resultados (por ejemplo, descomposición, contrastación de fuentes, experimentación iterativa, comparación de outputs, lectura de documentación, análisis de errores, etc.)?**

- **Descomposición:** dividir el problema en pasos pequeños (instalar librerías, probar un modelo simple, luego integrarlo).
- **Experimentación iterativa:** cambiar parámetros (modelo, temperatura, prompts) 
- **Lectura de errores:** usar el traceback como guía para ubicar el origen del problema en lugar de solo volver a ejecutar.
- **Comparación de outputs:** ver respuestas de Copilot, Codeium y Perplexity para validar consistencia.
- **Lectura de documentación:** revisar README de modelos y documentación oficial cuando las sugerencias automáticas no eran suficientes.

**¿Qué estrategia fue la más útil y por que?**
La descomposición + lectura de errores fue la más útil, porque: Permitió avanzar aunque algo fallara, evitó que me bloqueara frente a un error grande y me obligó a entender qué hacía cada bloque de código.


## 4. Reflexión sobre integración de plataformas y transferencia de conocimiento

**¿Qué aprendiste sobre cómo se integran entre sí las plataformas, modelos, APIs, copilotos o frameworks utilizados?**

- Que los modelos por sí solos no bastan: hay que integrarlos con frameworks (LLaMaIndex, LangChain), plataformas (Hugging Face, Google AI Studio) y copilotos.
- Que la **API** suele ser el punto común para conectar servicios distintos (por ejemplo, modelos alojados en la nube con código en Colab o VS Code).

**¿Qué decisiones debiste tomar para que el caso integrador funcionara técnicamente?**

- Elegir modelos que no dependieran de llaves privadas o recursos de pago.
- Organizar los documentos en una carpeta clara (`documentos/`) para que el pipeline RAG pudiera leerlos sin problemas de ruta.
- Simplificar algunas configuraciones (por ejemplo, usar embeddings disponibles localmente o por defecto) para garantizar reproducibilidad.

**¿Qué conocimientos transferiste de una herramienta a otra?**

- El concepto de prompting lo apliqué tanto en copilotos de código como en Google AI Studio y Perplexity.
- La lógica de evaluar respuestas (coherencia, grounding, precisión) la usé tanto para modelos de texto como para asistentes de búsqueda y RAG.
- Patrones de organización de repositorios y README aprendidos en Hugging Face los apliqué en GitHub para documentar el laboratorio.

## 5. Reflexión sobre mi crecimiento profesional y rol como ingeniero

**¿Cómo fortaleció este laboratorio tu identidad como ingeniero o profesional en I?**

Me hizo sentir menos como “usuario de herramientas” y más como diseñador de solucione el cual es el que decide: qué modelo escoger cómo integrarlo y cómo documentar el proceso.

**¿Qué descubriste sobre tu capacidad para aprender herramientas nuevas, integrar sistemas, evaluar tecnologías y documentar proceso?**

- Que soy capaz de aprender herramientas nuevas relativamente rapido, tener un contro de experimento, leer y hacer documentación,
- Que puedo evaluar tecnologías comparando outputs, facilidad de uso y requisitos técnicos.

**¿En qué áreas te sientes más fuerte ahora y qué deberías seguir reforzand?**

**- Más fuerte:**
  - Integración básica de modelos y plataformas
  - Uso de copilotos para acelerar tareas repetitivas
  - Documentación técnica en Markdown.
**- A reforzar:**
  - Profundizar en arquitecturas de RAG y agentes autónomos
  - Buenas prácticas de pruebas automatizadas
  - Aspectos éticos y de seguridad en sistemas basados en IA.

## 6. Reflexión sobre el cambio de paradigma y la profesión en la era de la IA

**¿Qué cambios percibes en el rol tradicional del desarrollador de software a partir del uso de modelos generativos, copilotos de código y herramientas de automatización vistas en este laboratorio?**

- El desarrollador deja de ser solo “escritor de código” y pasa a ser:
  **orquestador de herramientas de IA,** diseñador de prompts, responsable de validar y corregir lo que produce la máquina.
  - Muchas tareas mecánicas (boilerplate, funciones estándar, documentación básica) empiezan a automatizarse.

**¿Qué tareas crees que tenderán a automatizarse y qué nuevas responsabilidades (técnicas, éticas, de supervisión, de diseño de sistemas) aparecen para los ingenieros de software e ingenieros de IA?**
 **- Tareas que tenderán a automatizarse:**
  - generación de código repetitivo,
  - refactorización simple,
  - creación de tests básicos,
  - documentación inicial.
**- Nuevas responsabilidades:**
  - supervisión y validación del código generado por IA,
  - diseño de arquitecturas que integren múltiples modelos,
  - definición de criterios de calidad y ética en el uso de datos,
  - explicación de limitaciones y riesgos a usuarios no técnicos.

**¿¿Cómo te ves a ti mismo dentro de este nuevo contexto? ¿Qué deberías aprender, fortalecer o cambiar en tu forma de trabajar para seguir siendo relevante y aportar valor en la era de la IA??**

- Me veo como un profesional capaz de:
  - combinar conocimiento técnico con herramientas de IA
  - construir soluciones más rápido sin perder el criterio crítico.
- Debo seguir aprendiendo:
  - fundamentos de modelos generativos
  - patrones de diseño para sistemas con IA,
  - y habilidades de comunicación para explicar decisiones técnicas.
- Para seguir siendo relevante y aportar valor:
  - no basta con saber “usar” la IA,
  - tengo que entender cómo diseñar sistemas completos
  - Asumir un rol activo en la evaluación ética y la calidad del software.


