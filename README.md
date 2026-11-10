# Engineering Portfolio

🇪🇸 [Versión en español](README.es.md)

> Systems I have designed and led from architecture to production. I don't write the code myself: I define, decide and validate, and the implementation is carried out by AI coding agents working from my specifications, with every delivery reviewed.

## 🔭 Currently

### D2M: Editorial Intelligence and Data Platform
**Role:** Technical and product lead (architecture, leading development with AI assistants, production operations)
**Stack:** Python, Django, PostgreSQL, Docker, DigitalOcean, language models.

A system that automates daily coverage for a Spanish-speaking gaming community: an AI editorial pipeline that proposes and a human who approves, an extractor that turns every new version of the data into versioned, auditable information, and a multilingual web portal being rebuilt on top of that foundation.

* **Human-supervised editorial pipeline:** running daily in production since April 2026, with modules specialised by channel and a coverage log that prevents repeating content.
* **Reproducible data:** the full dataset regenerates with 0 differences across 4,281 files and 13 languages, and every version produces its own automatic changelog. On its first real update it caught changes the official release notes did not mention.
* **Migration with data as the source of truth:** comparing against the previous site surfaced 331 inherited errors that are not being carried over.

[**📄 Read the full architecture study →**](./d2mantix-architecture)

---

## 🚀 Featured Projects

### 1. Arpada Trading: Market Intelligence SaaS Platform
**Role:** Technical and product lead (architecture, leading development with AI agents, production operations)
**Stack:** Python, Django, Celery, Redis/Valkey, PostgreSQL, DigitalOcean App Platform, object storage, Stripe.

A subscription web platform that gathers scattered information about listed companies every day and presents it descriptively in a single dashboard. In production, in closed beta.

* **Asynchronous data pipeline:** more than 3,700 companies updated every trading day through 9 scheduled processes, always storing the original data before processing it.
* **Recovery of an inherited system:** from zero to around 350 automated tests, dead code removed, a binding decision log, and in-house observability with alerts for stalled processes.
* **Complete product, contained costs:** subscriptions with idempotent payments, five languages and GDPR compliance, all in production for about $15 a month.
* **Central source for other products:** a versioned read-only API with per-application keys, scopes, auditing, rate limiting, and a database user that cannot write.

[**📄 Read the full architecture study →**](./arpada-trading-system)

---

### 2. Automated Order Execution Engine
**Role:** End-to-end project lead (architecture, leading development with AI assistants, production operations)
**Stack:** Python, FastAPI, Django, PostgreSQL, Redis, Docker Compose, Caddy, Cloudflare, DigitalOcean.

A platform that turns external trading signals into broker orders, with no manual intervention and around the clock, full traceability and a control dashboard. In production in paper-trading mode since October 2026.

* **Safety first:** a per-bot lock and a position state machine; when in doubt, the system pauses instead of retrying, so an order is never duplicated. Validated with concurrency tests.
* **Automatic recovery:** outages caused by broker disconnections dropped from up to 16 hours to the broker's own daily maintenance window.
* **Verified accuracy:** the first complete cycle matches the broker's result to the cent.

[**📄 Read the full architecture study →**](./automated-execution-engine)

---

### 3. Normalised Financial Data Hub
**Role:** End-to-end development lead (architecture, data quality, leading development with AI assistants)
**Stack:** Python, Django, PostgreSQL, Docker, HTMX, DigitalOcean.

A platform that collects public financial information about listed companies, standardises it and computes comparable indicators, with every figure linked to its source document. It serves an editorial website and other applications through an API. In advanced development.

* **Immutable raw data:** everything else is recomputed from it, offline, and any figure can be audited. A gap is better than an invented number.
* **Measurable quality:** separating structural gaps from real errors cut alerts from 127 to 3 across 25 companies. Over 87% coverage of the main indicators across about 1,000 companies, with 382 tests.
* **Performance and cost:** from 976 to 29 queries and from 608 to 137 ms per company after the audit, on infrastructure budgeted at about $17 a month.

[**📄 Read the full architecture study →**](./financial-data-hub)

---

## 🗂 Other Projects

* **[Automated editorial engine](./editorial-automation-engine):** a daily pipeline that turns structured financial data into publish-ready content, with deterministic rules that select, AI that only writes, and an editor who approves. Node.js, ephemeral jobs on a PaaS and corporate SSO. In production since August 2026.
* **[Statistical data aggregation platform](./statistical-data-platform):** staged ingestion from several public agencies behind a single, stable API, with ingestion and serving decoupled and backups with tested restores. FastAPI and PostgreSQL. Working prototype.

---

## 🌐 Static Websites and CDN Delivery

Sites with no server and no database, built for people who don't edit code: near-free hosting, minimal attack surface, fast loading and publishing straight from the repository.

* **[Bilingual corporate website for an architecture studio](./architecture-studio-website):** natively bilingual, a minimal factual content model, motion with progressive enhancement, and a discovery layer generated on every build (structured data, sitemap and an LLM-readable file) to rank in both traditional and generative search engines.
* **[Corporate website for a law firm](./law-firm-website):** moving off a closed website builder, migrating domain and email (SPF, DKIM and DMARC) to accounts owned by the firm, a strict content security policy and conversion tracking. About €9 a year in infrastructure: the domain alone.
* **[Editorial portal for an esports community](./esports-community-portal):** migrated from a server-based application to a static site on a CDN with automatic deployment, removing the fixed server cost, with a content model designed so the home page is never empty.

**Shared stack:** Hugo, Markdown with front matter, HTML/CSS/JS without frameworks, GitHub, static hosting with CDN, managed DNS and certificates.

---

## 🛠 Technical Skills

| Domain | Technologies and practices |
| :--- | :--- |
| **Technical leadership** | Phased architecture with exit criteria, decision logs with trade-offs, testing strategy, observability, GDPR, leading development with AI agents |
| **Backend and data** | Python, Django, FastAPI, Celery, Node.js/Express, PostgreSQL, Redis/Valkey, S3-compatible object storage |
| **Cloud and operations** | DigitalOcean (App Platform, virtual servers, managed databases), Docker and Docker Compose, Caddy, Cloudflare, systemd, continuous deployment from GitHub |
| **AI** | Language models in human-supervised pipelines, AI as a writer and never as a source of figures, vector search (prototype) |
| **Web** | Hugo, HTML/CSS/JS without frameworks, HTMX, PWA, in-house design systems, technical SEO and generative search optimisation, Stripe payments |

---
*© 2026 · Engineering Portfolio. All projects are real systems; the status of each one (production, beta, development or prototype) is stated in its write-up. Brand names, data sources and business details are deliberately omitted.*
