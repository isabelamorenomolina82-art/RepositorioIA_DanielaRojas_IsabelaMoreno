# google_ai_studio
# 2.3 Ingeniería de Prompts y Prototipos — Google AI Studio

## Descripción Técnica
Google AI Studio es un entorno profesional para diseñar, probar y ajustar prompts dirigidos a modelos generativos como Gemini. Permite configurar temperatura, top-k, top-p y manejo avanzado del contexto, así como crear prototipos, agentes conversacionales y flujos de interacción. Su uso es ideal para procesos de ingeniería de prompts y experimentación controlada.

---

## Desarrollo

### 1. Creación de dos prompts profesionales

#### 📌 Prompt Técnico
**Objetivo:** Analizar un texto técnico e identificar brechas, mejoras y efectos.

**Prompt utilizado:**
> *"Eres un analista experto en sistemas distribuidos. A partir del siguiente texto, identifica las brechas tecnológicas, propone tres mejoras viables y explica sus implicaciones en rendimiento, seguridad y escalabilidad. Utiliza un lenguaje técnico y preciso. Si algo no está en el texto, no lo inventes."*

---

#### 📌 Prompt Creativo
**Objetivo:** Producir narrativa original con identidad cultural y tono evocador.

**Prompt utilizado:**
> *"Imagina que eres un narrador afrocolombiano del Pacífico. Crea un relato corto que conecte tradición oral, naturaleza y música de marimba. El tono debe ser poético, evocador y culturalmente respetuoso. Inspírate en ritmos, paisajes y personajes representativos de la región."*

---

### 2. Iteraciones Documentadas

#### 🧪 Iteraciones del Prompt Técnico

**Iteración 1**
- Temperatura: 0.2  
- Resultado: respuesta muy precisa, estilo rígido.  
- Observación: faltaban ejemplos.

**Iteración 2**
- Temperatura: 0.5  
- Ajuste: se añadió “incluye un ejemplo práctico por cada recomendación”.  
- Resultado: más claridad y aplicabilidad.

**Iteración 3**
- Temperatura: 0.5  
- Ajuste: se agregó más contexto del documento técnico.  
- Resultado: respuestas más alineadas al contenido fuente.

---

#### 🧪 Iteraciones del Prompt Creativo

**Iteración 1**
- Temperatura: 0.8  
- Resultado: mucha creatividad pero incoherencias en ritmo.

**Iteración 2**
- Temperatura: 0.6  
- Ajuste: se añadió “mantén coherencia temporal y espacial”.  
- Resultado: relato más estable.

**Iteración 3**
- Temperatura: 0.9  
- Ajuste: se indicó “usa metáforas relacionadas con el mar y el bosque”.  
- Resultado: texto más poético y profundo.

---

### 3. Evaluación del impacto de parámetros

| Parámetro | Efecto en Prompt Técnico | Efecto en Prompt Creativo |
|----------|---------------------------|----------------------------|
| **Temperatura baja (0.2–0.4)** | Respuestas precisas, poco creativas. | Reduce expresividad y metáforas. |
| **Temperatura media (0.5–0.7)** | Buen equilibrio entre claridad y detalle. | Creatividad controlada y estable. |
| **Temperatura alta (0.8–1.0)** | Riesgo de invenciones. | Mayor riqueza narrativa y variedad. |
| **Top-k bajo (20–40)** | Respuestas más repetitivas y controladas. | Limita la diversidad creativa. |
| **Top-k alto (50–80)** | Aumenta variabilidad; puede introducir ruido. | Más alternativas narrativas. |
| **Top-p bajo (0.2–0.5)** | Selección conservadora; alta precisión. | Menor expresividad. |
| **Top-p alto (0.7–0.9)** | Respuestas más flexibles y profundas. | Mayor riqueza cultural y poética. |
| **Contexto ampliado** | Mejora alineación con el texto técnico. | Aumenta coherencia cultural y temática. |

---

## Reflexión Técnica
El uso de Google AI Studio permitió evaluar cómo los parámetros modifican el comportamiento de los modelos generativos. En prompts técnicos, temperaturas y top-p bajos ayudaron a mantener precisión y evitar invenciones. En prompts creativos, valores más altos permitieron ampliar la expresividad y variedad narrativa. Las iteraciones demostraron que ajustar progresivamente el prompt mejora coherencia, profundidad y relevancia. El contexto adicional incrementó la fidelidad del análisis técnico y fortaleció el marco cultural en la narración creativa. La ingeniería de prompts se confirmó como un proceso iterativo donde cada parámetro influye significativamente en el tipo y calidad de la respuesta generada.

---

