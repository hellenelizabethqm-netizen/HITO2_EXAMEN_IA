# Supervisión Inteligente de EPP

Proyecto académico de **IA Generativa para la Gestión Industrial**, orientado a apoyar la supervisión de Elementos de Protección Personal (EPP) mediante inteligencia artificial y automatización.

## ¿Qué desarrollamos?

Un sistema que integra distintas herramientas:

- **YOLOv8n:** detección de personas y EPP mediante imágenes.
- **Series temporales:** pronóstico de revisiones mediante LSTM y Holt-Winters.
- **Transformer:** clasificación automática de reportes de seguridad.
- **RAG:** recuperación de procedimientos para contextualizar recomendaciones.
- **Gemini y n8n:** generación de informes, automatización y notificaciones.
- **Streamlit:** visualización de resultados.

## Principales resultados

- **YOLOv8n:** 70,4 % de precisión y 55,4 % de mAP50.
- **Transformer:** 98,6 % de accuracy y F1-macro de 0,905.
- **RAG con MiniLM:** 100 % de recuperación correcta en Top-3 sobre 8 consultas de prueba.

## Uso de inteligencia artificial

Se utilizaron **ChatGPT y Claude** como herramientas de apoyo para programación, depuración, análisis de resultados y redacción de documentación, incluyendo este README.

**Gemini** forma parte del sistema desarrollado, generando diagnósticos y recomendaciones a partir de los resultados procesados.

El equipo revisó y evaluó los resultados obtenidos.

## Limitaciones

El proyecto es un prototipo académico. Algunos módulos utilizan datos y procedimientos simulados. Por restricciones de memoria, el RAG desplegado utiliza TF-IDF en lugar de MiniLM.

El sistema busca **apoyar, no reemplazar, la supervisión humana**. Su aplicación real requiere validación adicional.

---

*Proyecto desarrollado con fines académicos — 2026.*
