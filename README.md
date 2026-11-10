# Portafolio de Ingeniería
> Selección de trabajos en ingeniería de software: Abstracciones arquitectónicas, soluciones Cloud-Native y demostraciones técnicas de proyectos.

## 🚀 Proyectos Destacados

### 1. Arpada Trading: Plataforma SaaS de Inteligencia de Mercados
**Rol:** Director técnico y de producto (arquitectura, dirección del desarrollo con agentes de IA y operación en producción)
**Stack:** Python, Django, Celery, Redis/Valkey, PostgreSQL, DigitalOcean App Platform, almacenamiento de objetos, Stripe.

Plataforma web por suscripción que reúne cada día información dispersa sobre empresas cotizadas y la presenta de forma descriptiva en un único panel. Está en producción y en beta cerrada.

* **Pipeline de datos asíncrono:** más de 3.700 empresas actualizadas cada día de mercado mediante 9 procesos programados, con el dato original guardado siempre antes de procesarlo.
* **Recuperación de un sistema heredado:** de cero a unas 350 pruebas automatizadas, eliminación de código muerto, registro de decisiones vinculante y observabilidad propia con alertas de procesos caídos.
* **Producto completo con costes contenidos:** suscripciones con pagos idempotentes, cinco idiomas, API con acceso de solo lectura y RGPD, todo en producción por unos 15 $ al mes.

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

### 3. Motor de Ejecución Automatizada de Órdenes
**Rol:** Director del proyecto de punta a punta (arquitectura, dirección del desarrollo con asistentes de IA y operación en producción)
**Stack:** Python, FastAPI, Django, PostgreSQL, Redis, Docker Compose, Caddy, Cloudflare, DigitalOcean.

Plataforma que convierte señales de trading externas en órdenes en un broker, sin intervención manual y las 24 horas, con trazabilidad completa y un panel de control. En producción en modo simulado desde octubre de 2026.

* **Seguridad ante todo:** candado por bot y máquina de estados de la posición; ante la duda, el sistema pausa en vez de reintentar, de modo que una orden nunca se duplica. Validado con pruebas de concurrencia.
* **Recuperación automática:** los cortes por desconexión del broker bajaron de hasta 16 horas a la ventana diaria de mantenimiento del propio broker.
* **Exactitud verificada:** el primer ciclo completo cuadra al céntimo con el resultado del broker.

[**📄 Leer el Estudio de Arquitectura completo →**](./automated-execution-engine)

---

### 4. AI Content Engine: ETL de Alta Eficiencia e Inferencia
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
