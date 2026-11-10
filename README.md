# Portafolio de Ingeniería
> Selección de trabajos en ingeniería de software: Abstracciones arquitectónicas, soluciones Cloud-Native y demostraciones técnicas de proyectos.

## 🚀 Proyectos Destacados

### 1. Arpada Trading System: Del Monolito a la IA Serverless
**Rol:** Ingeniero de Datos Principal & Arquitecto Cloud
**Stack:** Python, Django, DigitalOcean Functions (Serverless), Redis, PostgreSQL (pgvector), GenAI Platform.

Una evolución arquitectónica completa de un sistema de ingesta de datos financieros. Este proyecto documenta el ciclo de vida de una plataforma de alta concurrencia, pasando de un MVP síncrono a una arquitectura distribuida orientada a eventos que utiliza IA para el análisis cualitativo.

* **Arquitectura Evolutiva:** Estudio de caso detallado sobre la migración desde un Droplet monolítico hacia una infraestructura PaaS/Serverless totalmente gestionada.
* **Diseño Orientado a Eventos:** Implementación de **Redis** como orquestador de estados de alta velocidad para cientos de funciones de *scraping* concurrentes.
* **Integración GenAI:** Uso de **RAG (Generación Aumentada por Recuperación)** con Búsqueda Vectorial para transformar datos financieros crudos en narrativas estratégicas automatizadas.

[**📄 Leer el Estudio de Arquitectura completo →**](./arpada-trading-system)

---

### 2. D2M: Plataforma de Inteligencia Editorial y Datos
**Rol:** Director técnico y de producto (arquitectura, dirección del desarrollo con asistentes de IA y operación en producción)
**Stack:** Python, Django, PostgreSQL, Docker, DigitalOcean, modelos de lenguaje.

Sistema que automatiza la cobertura diaria de una comunidad de videojuegos de habla hispana: un pipeline editorial con IA que propone y una persona que aprueba, un extractor que convierte cada nueva versión de los datos en información versionada y auditable, y un portal web multilingüe que se reconstruye sobre esa base.

* **Editorial con supervisión humana:** en producción a diario desde abril de 2026, con módulos especializados por canal y un registro de cobertura que evita repetir contenido.
* **Datos reproducibles:** el conjunto completo se regenera con 0 diferencias en 4.281 ficheros y 13 idiomas, y cada versión produce su changelog automático. En la primera actualización real detectó cambios que las notas oficiales no mencionaban.
* **Migración con los datos como fuente de verdad:** el contraste con la web anterior sacó a la luz 331 errores heredados que no se migran.

[**📄 Leer el Estudio de Arquitectura completo →**](./d2mantix-architecture)

---

### 3. AI Content Engine: ETL de Alta Eficiencia e Inferencia
**Rol:** Ingeniero Backend
**Stack:** Python, Inferencia Serverless (Llama 3 / Mistral), Pinecone, Docker.

Un pipeline automatizado diseñado para normalizar estructuras de datos complejas (JSON) y generar contenido semántico a escala.

* **Inferencia Serverless:** Transición desde modelos locales con recursos restringidos (límites de 1GB RAM) hacia APIs de Inferencia en la Nube escalables, permitiendo el uso de LLMs potentes sin sobrecarga de hardware.
* **ETL Cognitivo:** Limpieza y vectorización automatizada de fuentes de datos no estructuradas para aplicaciones RAG posteriores.

## 🛠 Habilidades Técnicas

| Dominio | Tecnologías |
| :--- | :--- |
| **Cloud & DevOps** | DigitalOcean (Functions, App Platform), AWS (S3, CloudFront), Docker, CI/CD |
| **Backend & Data** | Python, Django, Redis, PostgreSQL, Bases de Datos Vectoriales (pgvector, Pinecone) |
| **IA & ML** | Arquitecturas RAG, Integración de LLMs (Llama 3, Mistral), Embeddings, Prompt Engineering |

---
*© 2025 - Portafolio de Ingeniería. Todas las arquitecturas aquí documentadas están basadas en despliegues reales en producción.*
