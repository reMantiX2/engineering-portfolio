# Portafolio de Ingeniería

🇬🇧 [English version](README.md)

> Sistemas que he diseñado y dirigido de la arquitectura a producción. No programo: defino, decido y valido, y la implementación la ejecutan agentes de IA a partir de mis especificaciones y con revisión de cada entrega.

## 🔭 Actualmente

### D2M: Plataforma de Inteligencia Editorial y Datos
**Rol:** Director técnico y de producto (arquitectura, dirección del desarrollo con asistentes de IA y operación en producción)
**Stack:** Python, Django, PostgreSQL, Docker, DigitalOcean, modelos de lenguaje.

Sistema que automatiza la cobertura diaria de una comunidad de videojuegos de habla hispana: un pipeline editorial con IA que propone y una persona que aprueba, un extractor que convierte cada nueva versión de los datos en información versionada y auditable, y un portal web multilingüe que se reconstruye sobre esa base.

* **Editorial con supervisión humana:** en producción a diario desde abril de 2026, con módulos especializados por canal y un registro de cobertura que evita repetir contenido.
* **Datos reproducibles:** el conjunto completo se regenera con 0 diferencias en 4.281 ficheros y 13 idiomas, y cada versión produce su changelog automático. En la primera actualización real detectó cambios que las notas oficiales no mencionaban.
* **Migración con los datos como fuente de verdad:** el contraste con la web anterior sacó a la luz 331 errores heredados que no se migran.

[**📄 Leer el Estudio de Arquitectura completo →**](./d2mantix-architecture/README.es.md)

---

## 🚀 Proyectos Destacados

### 1. Arpada Trading: Plataforma SaaS de Inteligencia de Mercados
**Rol:** Director técnico y de producto (arquitectura, dirección del desarrollo con agentes de IA y operación en producción)
**Stack:** Python, Django, Celery, Redis/Valkey, PostgreSQL, DigitalOcean App Platform, almacenamiento de objetos, Stripe.

Plataforma web por suscripción que reúne cada día información dispersa sobre empresas cotizadas y la presenta de forma descriptiva en un único panel. Está en producción y en beta cerrada.

* **Pipeline de datos asíncrono:** más de 3.700 empresas actualizadas cada día de mercado mediante 9 procesos programados, con el dato original guardado siempre antes de procesarlo.
* **Recuperación de un sistema heredado:** de cero a unas 350 pruebas automatizadas, eliminación de código muerto, registro de decisiones vinculante y observabilidad propia con alertas de procesos caídos.
* **Producto completo con costes contenidos:** suscripciones con pagos idempotentes, cinco idiomas y RGPD, todo en producción por unos 15 $ al mes.
* **Fuente central para otros productos:** API versionada de solo lectura, con claves por aplicación, alcances, auditoría, límite de peticiones y un usuario de base de datos que no puede escribir.

[**📄 Leer el Estudio de Arquitectura completo →**](./arpada-trading-system/README.es.md)

---

### 2. Motor de Ejecución Automatizada de Órdenes
**Rol:** Director del proyecto de punta a punta (arquitectura, dirección del desarrollo con asistentes de IA y operación en producción)
**Stack:** Python, FastAPI, Django, PostgreSQL, Redis, Docker Compose, Caddy, Cloudflare, DigitalOcean.

Plataforma que convierte señales de trading externas en órdenes en un broker, sin intervención manual y las 24 horas, con trazabilidad completa y un panel de control. En producción en modo simulado desde octubre de 2026.

* **Seguridad ante todo:** candado por bot y máquina de estados de la posición; ante la duda, el sistema pausa en vez de reintentar, de modo que una orden nunca se duplica. Validado con pruebas de concurrencia.
* **Recuperación automática:** los cortes por desconexión del broker bajaron de hasta 16 horas a la ventana diaria de mantenimiento del propio broker.
* **Exactitud verificada:** el primer ciclo completo cuadra al céntimo con el resultado del broker.

[**📄 Leer el Estudio de Arquitectura completo →**](./automated-execution-engine/README.es.md)

---

### 3. Hub de Datos Financieros Normalizados
**Rol:** Director del desarrollo de principio a fin (arquitectura, calidad de datos y dirección con asistentes de IA)
**Stack:** Python, Django, PostgreSQL, Docker, HTMX, DigitalOcean.

Plataforma que recoge información financiera pública de empresas cotizadas, la homogeneiza y calcula indicadores comparables, con cada cifra enlazada a su documento de origen. La sirve a una web editorial y a otras aplicaciones a través de una API. En desarrollo avanzado.

* **Datos en bruto inmutables:** todo lo demás se recalcula desde ellos, sin red, y cualquier cifra es auditable. Un hueco antes que un número inventado.
* **Calidad medible:** al separar los huecos estructurales de los errores reales, las alertas bajaron de 127 a 3 en 25 empresas. Más del 87 % de cobertura en los indicadores principales sobre unas 1.000 empresas, con 382 tests.
* **Rendimiento y coste:** de 976 a 29 consultas y de 608 a 137 ms por empresa tras la auditoría, con una infraestructura prevista de unos 17 $ al mes.

[**📄 Leer el Estudio de Arquitectura completo →**](./financial-data-hub/README.es.md)

---

## 🗂 Otros Proyectos

* **[Motor editorial automatizado](./editorial-automation-engine/README.es.md):** pipeline diario que convierte datos financieros estructurados en contenido listo para publicar, con reglas deterministas que eligen, IA que solo redacta y un editor que aprueba. Node.js, jobs efímeros en PaaS y SSO corporativo. En producción desde agosto de 2026.
* **[Plataforma de agregación de datos estadísticos](./statistical-data-platform/README.es.md):** ingesta por etapas desde varios organismos públicos y una API única y estable, con ingesta y servicio desacoplados y respaldo con restauración probada. FastAPI y PostgreSQL. Prototipo operativo.

---

## 🌐 Webs Estáticas y Distribución por CDN

Sitios sin servidor ni base de datos para personas que no editan código: alojamiento casi gratuito, superficie de ataque mínima, carga rápida y publicación desde el repositorio.

* **[Web corporativa bilingüe para un estudio de arquitectura](./architecture-studio-website/README.es.md):** bilingüe nativa, modelo de contenido mínimo y factual, movimiento con mejora progresiva y una capa de descubrimiento generada en cada build (datos estructurados, sitemap y archivo legible por modelos de lenguaje) para posicionar en buscadores tradicionales y generativos.
* **[Web corporativa para un despacho jurídico](./law-firm-website/README.es.md):** salida de un constructor web cerrado, con migración de dominio y correo (SPF, DKIM y DMARC) a cuentas propiedad del despacho, política de seguridad de contenido estricta y medición de conversiones. Unos 9 € al año de infraestructura, solo el dominio.
* **[Portal editorial para una comunidad de esports](./esports-community-portal/README.es.md):** migración de una aplicación con servidor a un sitio estático en CDN con despliegue automático, eliminando el coste fijo del servidor, y un modelo de contenido diseñado para que la portada nunca quede vacía.

**Stack común:** Hugo, Markdown con metadatos, HTML/CSS/JS sin frameworks, GitHub, hosting estático con CDN, DNS y certificados gestionados.

---

## 🛠 Habilidades Técnicas

| Dominio | Tecnologías y prácticas |
| :--- | :--- |
| **Dirección técnica** | Arquitectura por fases con criterios de cierre, registro de decisiones con contrapartidas, estrategia de pruebas, observabilidad, RGPD, dirección del desarrollo con agentes de IA |
| **Backend y datos** | Python, Django, FastAPI, Celery, Node.js/Express, PostgreSQL, Redis/Valkey, almacenamiento de objetos compatible con S3 |
| **Cloud y operación** | DigitalOcean (App Platform, servidores virtuales, bases de datos gestionadas), Docker y Docker Compose, Caddy, Cloudflare, systemd, despliegue continuo desde GitHub |
| **IA** | Modelos de lenguaje en pipelines con supervisión humana, IA como redactora y nunca como fuente de cifras, búsqueda vectorial (prototipo) |
| **Web** | Hugo, HTML/CSS/JS sin frameworks, HTMX, PWA, sistemas de diseño propios, SEO técnico y para buscadores generativos, pagos con Stripe |

---
*© 2026 · Portafolio de Ingeniería. Todos los proyectos son sistemas reales; el estado de cada uno (producción, beta, desarrollo o prototipo) se indica en su ficha. Nombres comerciales, fuentes de datos y detalles de negocio se omiten deliberadamente.*
