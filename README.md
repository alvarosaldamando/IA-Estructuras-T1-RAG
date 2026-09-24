# IA-Estructuras-T1-RAG

## Trabajo Final Escalonado - T1

**Sistema RAG para consulta y comparación normativa en el diseño de elementos de concreto armado**

**Curso:** Aplicaciones de IA en Estructuras  
**Universidad:** Universidad Peruana de Ciencias Aplicadas (UPC)  
**Alumno:** Saldamando Montero, Alvaro Ted  
**Profesor:** Ing. Kurt Soncco  
**Fecha:** 23/09/2026

---

## 1. Objetivo general

Desarrollar y evaluar un prototipo de sistema RAG que permita recuperar información relevante y generar respuestas sustentadas en documentos normativos aplicables al diseño estructural de elementos de concreto armado.

## 2. Problema de ingeniería estructural

En el diseño y revisión de estructuras, la consulta de normas técnicas requiere localizar artículos, capítulos y requisitos específicos dentro de documentos extensos. Esta búsqueda manual puede demandar tiempo y dificultar la trazabilidad de la fuente utilizada.

El proyecto propone desarrollar un sistema basado en Inteligencia Artificial que permita consultar requisitos normativos de diseño estructural y responder las preguntas utilizando como fuente el corpus documental proporcionado.

## 3. Propuesta de solución mediante RAG

Se propone implementar un sistema de **Generación Aumentada por Recuperación (RAG)**.

El sistema procesará documentos normativos, los dividirá en fragmentos y generará una representación que permita recuperar los contenidos más relevantes ante una consulta. Posteriormente, un modelo de lenguaje utilizará dichos fragmentos para formular una respuesta, procurando conservar la referencia al documento y al contenido recuperado.

El alcance inicial se centrará en consultas relacionadas con el diseño de elementos de concreto armado.

El sistema no pretende sustituir el criterio del ingeniero ni emitir una aprobación de diseño; su función será facilitar la consulta y trazabilidad de información normativa.

## 4. Datos / corpus documental

El corpus documental inicial está constituido por **tres documentos normativos** aplicables al diseño estructural de elementos de concreto armado:

1. **ACI 318-25.** *Building Code Requirements for Structural Concrete.*
2. **NTE E.060.** *Concreto Armado*, del Reglamento Nacional de Edificaciones del Perú.
3. **AASHTO LRFD Bridge Design Specifications, 10th Edition (2024).**

### Características del corpus

- Número de documentos: **3**.
- Tipo de datos: **textual técnico-normativo**.
- Unidad de procesamiento: **fragmento de texto recuperado**.
- Trazabilidad: se conservará la **identificación y ubicación dentro de la norma**.
- La selección y utilización de los documentos deberá respetar las condiciones de disponibilidad y uso de cada fuente.

## 5. Marco VDS

El proyecto considera los principios de **predictibilidad, computabilidad y estabilidad**:

### Predictibilidad
Se espera que preguntas técnicas formuladas dentro del alcance del corpus permitan recuperar fragmentos relacionados con el tema consultado. Esta propiedad se verificará mediante un conjunto de preguntas de prueba con respuestas conocidas a partir de los documentos.

### Computabilidad
El procesamiento de documentos, generación de representaciones, recuperación y generación de respuestas deberá poder ejecutarse con los recursos computacionales disponibles para el curso.

### Estabilidad
Se analizará la consistencia del sistema frente a variaciones en la redacción de las preguntas, cambios en los fragmentos recuperados y modificaciones controladas del corpus. La evaluación permitirá identificar cuándo el sistema produce respuestas diferentes o carece de evidencia suficiente.

## 6. Repositorio y productos del T1

El proyecto se organiza en un repositorio de GitHub con el código Python, documentación, estructura de datos y registro de avances.

### Estructura del repositorio

```text
IA-Estructuras-T1-RAG/
├── informe/
├── datos/
├── codigo/
├── referencias/
├── .gitignore
└── README.md
```

### Alcance de T1

En T1 se desarrolla:

- Planteamiento del problema.
- Definición del corpus documental.
- Metodología inicial.
- Análisis de predictibilidad, computabilidad y estabilidad bajo el marco VDS.
- Estructura del repositorio.

Las siguientes entregas comprenderán el análisis exploratorio, implementación, evaluación y presentación final.

## 7. Bitácora de uso de Inteligencia Artificial

Durante la elaboración del Trabajo Final Escalonado - T1 se utilizó **ChatGPT** como apoyo para la estructuración de ideas, revisión de redacción, organización del documento y configuración inicial del entorno de trabajo.

El contenido técnico y las fuentes normativas son de revisión propia.

### 7.1. Definición inicial del proyecto

**Prompt:** definir un problema de ingeniería estructural que pudiera resolverse mediante IA y que fuera compatible con los lineamientos del curso.

**Iteraciones:** 2.

**Resultado:** se evaluaron alternativas y se seleccionó un sistema RAG orientado a la consulta de normativa estructural.

### 7.2. Definición de la solución RAG

**Prompt:** desarrollar la propuesta de un sistema RAG para consulta de requisitos normativos en diseño estructural.

**Iteraciones:** 2.

**Resultado:** se precisó que el sistema recuperará fragmentos relevantes de documentos normativos y generará respuestas sustentadas en dichos fragmentos, manteniendo la trazabilidad de la fuente.

### 7.3. Marco VDS

**Prompt:** desarrollar de forma breve los conceptos de predictibilidad, computabilidad y estabilidad aplicados al sistema RAG.

**Iteraciones:** 2.

**Resultado:** se incorporaron criterios de evaluación mediante preguntas de prueba, recursos computacionales disponibles y análisis de consistencia frente a variaciones controladas.

### 7.4. Configuración del entorno y repositorio

**Prompt:** orientar paso a paso la configuración de Python, Git, GitHub y la estructura de carpetas del proyecto.

**Iteraciones:** 2.

**Resultado:** se configuró el entorno de trabajo, se creó el repositorio de GitHub y se organizaron las carpetas para informe, datos, código y referencias.

## 8. Referencias bibliográficas

- Lewis, P., Perez, E., Piktus, A., Petroni, F., Karpukhin, V., Goyal, N., Küttler, H., Lewis, M., Yih, W.-t., Rocktäschel, T., Riedel, S., & Kiela, D. (2020). *Retrieval-augmented generation for knowledge-intensive NLP tasks*. Advances in Neural Information Processing Systems, 33, 9459–9474.
- Yu, B., & Barter, R. L. (2024). *Veridical data science: The practice of responsible data analysis and decision making*. The MIT Press.
- Zhao, S., Yang, Y., Wang, Z., He, Z., Qiu, L. K., & Qiu, L. (2024). *Retrieval augmented generation (RAG) and beyond: A comprehensive survey on how to make your LLMs use external data more wisely*. Microsoft Research.
