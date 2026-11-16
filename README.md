# Supervisión Inteligente de EPP

**Proyecto académico | IA Generativa para la Gestión Industrial | 2026**

Este proyecto busca apoyar la supervisión de Elementos de Protección Personal (EPP) en entornos industriales mediante inteligencia artificial, visión computacional y automatización de procesos.

La solución permite analizar fotografías de trabajadores, identificar elementos de protección, generar recomendaciones preventivas y registrar los resultados para facilitar el seguimiento por parte de los responsables de seguridad.

El objetivo es **agilizar la supervisión y apoyar la toma de decisiones**, sin reemplazar la evaluación humana.

## Tecnologías utilizadas

| Tecnología | Aplicación |
|---|---|
| **YOLOv8n** | Detección de personas y EPP en fotografías. |
| **ONNX y FastAPI** | Ejecución y publicación del modelo de detección. |
| **LSTM y Holt-Winters** | Pronóstico de trabajadores con EPP no confirmado. |
| **Transformer + regresión logística** | Clasificación de reportes de seguridad. |
| **RAG (TF-IDF y MiniLM)** | Búsqueda de procedimientos de seguridad relevantes. |
| **Gemini** | Generación de diagnósticos y recomendaciones estructuradas. |
| **n8n** | Automatización de procesos, registros y notificaciones. |
| **Streamlit** | Visualización de indicadores y resultados. |

## Funcionamiento del sistema

El sistema se organiza en las siguientes etapas:

1. **Recepción de datos:** se ingresa una fotografía y la información correspondiente a la zona de trabajo.
2. **Detección de EPP:** YOLOv8n identifica personas y elementos de protección, considerando las reglas de cada zona.
3. **Análisis complementario:** los módulos de series temporales y clasificación de reportes aportan información para la supervisión.
4. **Generación de recomendaciones:** Gemini interpreta los resultados disponibles y genera un diagnóstico estructurado.
5. **Automatización:** n8n coordina el procesamiento, registro de resultados y envío de notificaciones.
6. **Visualización:** Streamlit permite consultar indicadores y resultados de supervisión.

Adicionalmente, se desarrolló un módulo RAG para recuperar procedimientos de seguridad que puedan utilizarse como contexto en las recomendaciones.

## Principales resultados

Durante el proyecto se entrenaron, evaluaron y compararon distintos métodos.

| Componente | Resultado destacado |
|---|---|
| **YOLOv8n** | 70,4 % de precisión y 55,4 % de mAP50. |
| **Comparación YOLO** | YOLOv8n superó al YOLOv8s externo en F1-score promedio: 0,6441 frente a 0,1388. |
| **Clasificación de reportes** | 98,6 % de accuracy y F1-macro de 0,905. |
| **RAG con MiniLM** | 100 % de recuperación correcta en Top-3 sobre 8 consultas de prueba. |
| **Series temporales** | Se evaluaron modelos ingenuos, Holt-Winters y LSTM, seleccionando según resultados de validación por zona. |

Los resultados permitieron identificar tanto las capacidades de los modelos como sus principales oportunidades de mejora.

## Datos utilizados

Se trabajó con dos tipos de información:

- **Datos de imágenes:** conjunto SH17, utilizado para entrenar y evaluar la detección de personas y EPP.
- **Datos simulados:** registros históricos, reportes de seguridad y siete procedimientos diseñados para evaluar los módulos del Hito 2.

Los datos simulados corresponden a escenarios académicos y no representan registros de una empresa real.

## Limitaciones y mejoras futuras

El proyecto constituye un prototipo académico y presenta algunas limitaciones:

- La detección de ciertos EPP, especialmente guantes y chalecos, requiere mejoras.
- MiniLM obtuvo mejores resultados de recuperación, pero el despliegue en Render utilizó TF-IDF por restricciones de memoria.
- Algunos módulos requieren completar o validar su integración con el flujo principal.
- Es necesario evaluar el sistema con información real y procedimientos validados por especialistas.

En futuras versiones se busca fortalecer la integración, mejorar los modelos y ampliar la validación en condiciones industriales reales.

## Uso de inteligencia artificial

Durante el desarrollo se utilizaron **ChatGPT y Claude como herramientas de apoyo** en tareas de programación, depuración, análisis de resultados y redacción de documentación, incluyendo la elaboración de este README.

Asimismo, **Gemini forma parte de la solución implementada**, permitiendo generar diagnósticos y recomendaciones a partir de resultados estructurados.

El equipo participó en el desarrollo, revisión, pruebas y evaluación del proyecto, considerando las limitaciones de las herramientas utilizadas.

## Equipo

- Catalina Cornejo
- Hellen Quiñones
- Gustavo Sánchez

---

*Proyecto desarrollado con fines académicos durante 2026. La herramienta está diseñada como apoyo a la supervisión de seguridad y no sustituye las inspecciones ni las decisiones de profesionales especializados.*
