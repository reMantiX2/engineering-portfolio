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

[**📄 Leer el Estudio de Arquitectura completo →**](./projects/arpada-trading-system.md)

---

### 2. D2MantiX: Arquitectura Web Segura Cloud-Native
**Rol:** Arquitecto de Soluciones
**Stack:** AWS S3, CloudFront (CDN), Static Site Generation (SSG), Pipeline Local-to-Cloud.

Una infraestructura web diseñada con enfoque "Security-First" (Seguridad ante todo), eliminando vulnerabilidades del lado del servidor al desacoplar la generación del contenido de su entrega.

* **Infraestructura Inmutable:** Despliegue de una arquitectura estática de alto rendimiento distribuida globalmente vía CDN.
* **Seguridad Local-to-Cloud:** Pipeline personalizado "Air-Gapped" donde el contenido se genera en un entorno local aislado y se empuja de forma segura al *edge*, eliminando la exposición de la base de datos a la internet pública.

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
