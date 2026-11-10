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

### 4. Hub de Datos Financieros Normalizados
**Rol:** Director del desarrollo de principio a fin (arquitectura, calidad de datos y dirección con asistentes de IA)
**Stack:** Python, Django, PostgreSQL, Docker, HTMX, DigitalOcean.

Plataforma que recoge información financiera pública de empresas cotizadas, la homogeneiza y calcula indicadores comparables, con cada cifra enlazada a su documento de origen. La sirve a una web editorial y a otras aplicaciones a través de una API. En desarrollo avanzado.

* **Datos en bruto inmutables:** todo lo demás se recalcula desde ellos, sin red, y cualquier cifra es auditable. Un hueco antes que un número inventado.
* **Calidad medible:** al separar los huecos estructurales de los errores reales, las alertas bajaron de 127 a 3 en 25 empresas. Más del 87 % de cobertura en los indicadores principales sobre unas 1.000 empresas, con 382 tests.
* **Rendimiento y coste:** de 976 a 29 consultas y de 608 a 137 ms por empresa tras la auditoría, con una infraestructura prevista de unos 17 $ al mes.

[**📄 Leer el Estudio de Arquitectura completo →**](./financial-data-hub)

---

### 5. Plataforma de Agregación de Datos Estadísticos
**Rol:** Dirección técnica y de producto (arquitectura, especificaciones y dirección con asistentes de IA)
**Stack:** Python, FastAPI, PostgreSQL, Docker Compose, almacenamiento de objetos.

Plataforma que recoge datos estadísticos públicos de varios organismos, cada uno con sus propios formatos, códigos y calendarios, y los sirve mediante una API única y estable. Prototipo operativo en entorno local.

* **Ingesta y servicio desacoplados:** la API solo consulta la base propia, así que una fuente caída o cambiada nunca rompe el servicio.
* **Reprocesable y trazable:** copia original inmutable, etapas que guardan su resultado y detección de cambios en cada nueva publicación de la fuente.
* **Respaldo probado de verdad:** restauración completa verificada sobre unos 9 millones de observaciones.

[**📄 Leer el Estudio de Arquitectura completo →**](./statistical-data-platform)

---

### 6. Motor Editorial Automatizado
**Rol:** Dirección de producto y técnica de punta a punta (arquitectura, costes, dirección con agentes de IA y operación)
**Stack:** Node.js, Express, PostgreSQL, DigitalOcean (PaaS con jobs programados), SSO corporativo, modelos de lenguaje.

Pipeline que convierte cada día datos financieros estructurados en contenido listo para publicar (posts, piezas visuales, avisos y newsletter semanal), con un editor humano que decide qué sale. En producción y en uso diario desde agosto de 2026.

* **La IA solo redacta:** una capa de reglas deterministas, configurable desde el panel, decide qué merece contenido. Coste acotado, resultados auditables y menos alucinaciones.
* **Infraestructura ligera:** jobs efímeros que solo cuestan mientras se ejecutan, y piezas visuales generadas en el navegador del editor en lugar de en el servidor.
* **Evolución pragmática:** de un prompt usado a mano en un chat a un panel instalable con SSO, con más de 150 ejecuciones del job diario en producción.

[**📄 Leer el Estudio de Arquitectura completo →**](./editorial-automation-engine)

---

### 7. Web Corporativa Bilingüe para un Estudio de Arquitectura
**Rol:** Dirección técnica y de producto de principio a fin (colaboración con un estudio)
**Stack:** Hugo, HTML/CSS/JS sin frameworks, Markdown, GitHub, hosting estático.

Sitio estático y bilingüe para un estudio de arquitectura y reformas: una marca premium que debía encontrarse en búsquedas locales y en asistentes de IA, con coste y mantenimiento mínimos para un equipo que no edita código. En producción.

* **Sin servidor ni base de datos:** alojamiento casi gratuito, superficie de ataque mínima y carga rápida.
* **Diseñada para ser citada:** cada build genera datos estructurados, sitemap, un archivo legible por modelos de lenguaje e imagen social por proyecto.
* **Contenido verificable:** modelo de datos mínimo y factual, taxonomía cerrada y normas editoriales que prohíben inventar datos o simular obra con imágenes generadas.

[**📄 Leer el Estudio de Arquitectura completo →**](./architecture-studio-website)

---

### 8. AI Content Engine: ETL de Alta Eficiencia e Inferencia
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
