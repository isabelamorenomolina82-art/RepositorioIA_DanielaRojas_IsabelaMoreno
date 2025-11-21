# Informe – Kaggle: Datasets, Experimentos y Colaboración  

## 1. Descripción Técnica

Kaggle es una de las plataformas más completas y utilizadas en ciencia de datos. Además de ofrecer miles de datasets públicos, también permite crear y ejecutar notebooks colaborativos directamente en la nube, sin necesidad de instalar nada de forma local.

Durante este laboratorio utilicé Kaggle como entorno para:

- buscar y seleccionar un dataset relevante,
- realizar un análisis exploratorio de datos (EDA),
- generar visualizaciones,
- publicar un notebook de manera colaborativa,
- y analizar las implicaciones de los datos dentro de un contexto educativo.

Su facilidad para cargar datos, graficar, ejecutar código y compartir resultados la convierte en una herramienta ideal tanto para investigación como para docencia.

---

## 2. Desarrollo del Trabajo

### **2.1 Selección del dataset**

Para este trabajo seleccioné un dataset relacionado con el rendimiento académico de estudiantes, ya que se ajusta directamente al enfoque educativo del laboratorio y permite analizar:

- factores que influyen en el rendimiento,
- patrones de comportamiento,
- posibles predictores de riesgo académico,
- y relaciones entre variables socioacadémicas.

El dataset elegido incluye información sobre horas de estudio, asistencia, participación, resultados académicos y otros atributos relevantes.

---

### **2.2 Realización del EDA**

Una vez cargado el dataset en un notebook de Kaggle, realicé un EDA completo. Estos fueron los pasos principales:

#### **Limpieza de datos**
- Eliminé valores nulos y registros duplicados.
- Verifiqué el tipo de datos de cada columna para asegurar su correcta interpretación.
- Normalicé algunos campos para facilitar el análisis.

#### **Análisis descriptivo**
Generé tablas estadísticas usando `df.describe()` para revisar:

- medias,
- medianas,
- desviación estándar,
- valores máximos y mínimos,
- y distribución general de las variables.

Esto me permitió tener una primera idea del comportamiento general de los datos.

#### **Visualizaciones**

Luego generé una serie de gráficos para identificar mejor las relaciones entre variables:

- histogramas para ver distribuciones,
- gráficos de dispersión para analizar relaciones como *horas de estudio vs nota final*,
- boxplots para detectar outliers,
- y un heatmap de correlación que ayudó a identificar asociaciones relevantes.

Los hallazgos más importantes del análisis fueron:

- Existe una correlación positiva entre **horas de estudio** y **rendimiento académico**.
- La asistencia también muestra una relación significativa con la nota final.
- Algunos factores socioemocionales tienen menor impacto sobre el rendimiento.
- Se evidencian patrones que permiten identificar estudiantes en riesgo.

---

### **2.3 Publicación del notebook colaborativo**

Después de finalizar el EDA, publiqué el notebook como recurso público en Kaggle. Esto es fundamental para garantizar:

- transparencia,
- reproducibilidad,
- trazabilidad,
- y colaboración con otros usuarios.

El link al notebook público (que incluyo como evidencia) permite que cualquier persona pueda ejecutar el código, visualizar los gráficos y revisar todos los análisis realizados.

---

### **2.4 Implicaciones del dataset en un caso educativo**

Con base en los resultados obtenidos, pude concluir que este tipo de dataset tiene un valor muy alto para instituciones educativas, ya que permite:

1. **Identificar estudiantes en riesgo**  
   A través de variables como asistencia y horas de estudio, se pueden establecer alertas tempranas.

2. **Diseñar estrategias de intervención**  
   El análisis facilita la toma de decisiones para apoyar a estudiantes con bajo rendimiento.

3. **Mejorar procesos pedagógicos**  
   Los docentes pueden ajustar metodologías y recursos a partir de patrones identificados.

4. **Respaldar decisiones con datos reales**  
   El uso de analítica educativa fortalece la gestión académica basada en evidencia.

---

## 3. Evidencias

Las evidencias generadas para esta actividad son:
<img width="1355" height="593" alt="image" src="https://github.com/user-attachments/assets/e80bb14e-5189-46b7-9fc1-166a2f155832" />
<img width="1366" height="559" alt="image" src="https://github.com/user-attachments/assets/4d3c14f8-d9cb-4e6b-8909-71baab150769" />
<img width="1356" height="556" alt="image" src="https://github.com/user-attachments/assets/d39bb0eb-e5bc-4030-aaab-571442f44152" />
<img width="873" height="309" alt="image" src="https://github.com/user-attachments/assets/3f8fc8bd-c119-4a6c-8a95-f64f3f486056" />
<img width="662" height="427" alt="image" src="https://github.com/user-attachments/assets/d550f552-f6a7-4d5e-908f-4f6f9e59371c" />


- **Notebook público en Kaggle:**  
https://www.kaggle.com/code/danielarojast/eda-student-performance-daniela-r-isabela-m


### Conclusiones del EDA
- La nota final (G3) muestra una distribución concentrada entre 8 y 14.
- Horas de estudio (`studytime`) tiene una correlación positiva con G3.
- Las notas previas G1 y G2 predicen fuertemente el resultado final G3.
- Se pueden diseñar alertas tempranas basadas en asistencia, estudio y notas parciales.

## 4. Conclusión

Kaggle fue una herramienta fundamental para este laboratorio, ya que me permitió trabajar con datos reales en un entorno profesional, generar visualizaciones de manera sencilla y compartir mis resultados públicamente.

Además de realizar un EDA completo, pude conectar los hallazgos con aplicaciones reales en el campo educativo, lo cual fortalece el enfoque práctico del laboratorio y demuestra cómo la analítica de datos puede apoyar procesos de enseñanza y aprendizaje.

---

**Fin del informe.**


**Fin del informe.**
