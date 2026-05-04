# 👤 Gerald January

**Senior Data & AI Infrastructure Engineer · Health IT Specialist**

17+ years engineering data systems for critical health networks — enterprise data warehouses, clinical EHR pipelines, population health research datasets, and independently built AI infrastructure and healthcare analytics platforms.  
I build systems that work in the real world, under real constraints, for real people.

---

### 🔧 What I Work With

**Healthcare Data & EHR**  
SAS 9.4 · SAS Visual Analytics · SAS DI Studio · Cerner Millennium · CCL · HL7 · X12 EDI · eCQM/CMS reporting · HIPAA

**Databases & Data Engineering**  
SQL Server · Oracle · MySQL · PostgreSQL · ETL/ELT pipelines · Enterprise Data Warehouse architecture · dimensional modeling

**AI & ML Infrastructure**  
Ollama (LLM serving) · LangGraph agent orchestration · ComfyUI · Open WebUI · NVIDIA CUDA · Tesla T4 GPU cluster · Langfuse · LiteLLM proxy

**Infrastructure & DevOps**  
Docker · Kubernetes (k3s) · Proxmox VE · Linux (Debian) · Python · Bash · PowerShell · REST APIs · Git · Tailscale

---

### 🏥 Featured: Hospital Price Transparency Intelligence Platform

**🌐 Live API:** [hospital-rates-api.businessclub2050.workers.dev](https://hospital-rates-api.businessclub2050.workers.dev) · **📊 Try:** [`/v1/hospitals/adventist-tillamook/payer-intel`](https://hospital-rates-api.businessclub2050.workers.dev/v1/hospitals/adventist-tillamook/payer-intel) · **📖 Repo:** [`hospital-rates-platform`](https://github.com/businessclub2050/hospital-rates-platform)

Healthcare organizations have been required since 2021 (45 CFR §180.50) to publish machine-readable files (MRFs) listing their negotiated rates with every insurer. Almost no one has analyzed this data at scale — these files are multi-GB streaming JSON, structurally inconsistent across systems, and some hospital networks deliberately obscure per-payer data by filing a single blended rollup likely in violation of the regulation.

I built the full stack to ingest, normalize, and surface this data for executive competitive intelligence:

**Pipeline & Ingestion**
- Streaming MRF parser (DuckDB + Python) capable of processing 400–670 MB gzip/zip JSON files without loading into memory; handles non-standard ZIP compression variants (Deflate64)
- Ingest queue via Cloudflare Workers + R2 object storage; per-hospital run tracking in D1 with retry/resume on partial failures
- HCRIS FY2023 cost report integration for 711 hospitals: computes cost-charge ratios, markup multiples, charity care as % of total costs

**Rate Analysis**
- Rate index methodology uses `negotiated_avg ÷ gross_charge` (discount rate ratio) rather than raw rate averages — eliminates code-mix bias when comparing hospitals with different service mixes
- Peer comparison across same-state hospitals: "+18% vs peers" means this insurer pays 18% more per service at this hospital than at comparable facilities after controlling for service mix
- Automatic compliance detection: flags hospitals publishing single-payer rollups as likely non-compliant with the per-payer disclosure requirement — a meaningful signal for contract negotiators and regulators

**Scale (current)**
- 2.3M+ negotiated rate rows across 22 hospitals in Oregon, Kansas, and Missouri
- 21-hospital peer cohort for Oregon market rate comparisons
- HCRIS cost data loaded for 711 of 723 target KS/MO hospitals (FY2023)

**API & Frontend**
- Edge REST API: Cloudflare Workers + D1 (serverless SQLite), `/v1/hospitals/:id/payer-intel` with peer benchmarking baked in
- CEO executive dashboard in SvelteKit: markup multiple vs cost (visual bar), payer rate index vs state peers (color-coded ±%), quality star ratings, compliance status — no CPT jargon, just actionable intelligence

**Stack**: Python · DuckDB · Cloudflare Workers · D1 · TypeScript · SvelteKit · Tailwind CSS · HCRIS · CMS MRF schema

> This is the same dataset that healthcare analytics companies like Turquoise Health, Clarify Health, and Dais are building commercial products around. I designed and built the full stack independently — from raw MRF download to deployed API to executive-facing UI — combining 17 years of domain knowledge in hospital revenue cycle with modern data engineering.

---

### 📁 Projects

| Repository | Description |
|------------|-------------|
| [`hospital-rates-platform`](https://github.com/businessclub2050/hospital-rates-platform) | CMS MRF ingestion pipeline + payer intelligence engine — [live API](https://hospital-rates-api.businessclub2050.workers.dev) |
| [`janus-ai-node`](https://github.com/businessclub2050/janus-ai-node) | Self-hosted LLM inference cluster: dual T4 GPUs, Ollama, LangGraph, ComfyUI on Proxmox + k3s |
| [`flash-deploy-kit`](https://github.com/businessclub2050/flash-deploy-kit) | Modular provisioning scripts for repeatable AI/OS deployments on bare metal and VMs |

---

### 📜 Recognition & Publications

- **Nominated for the CDC Charles C. Shepard Award (2021)** — Awarded for outstanding scientific contribution to public health research
- Co-author: *[Community water service and incidence of infections in rural Alaska, 2013–2015](https://www.sciencedirect.com/science/article/pii/S1438463919310181)* — Int. J. Hygiene and Environmental Health, 2020
- Co-author: *[Health-related economic benefits of universal access to piped water in Arctic communities](https://www.sciencedirect.com/science/article/abs/pii/S1438463921002303)* — Int. J. Hygiene and Environmental Health
- Data contributor: *[Effectiveness of COVID-19 vaccines in Southwestern Alaska, Jan–Dec 2021](https://www.sciencedirect.com/science/article/pii/S0264410X23004966)* — Vaccine, 2023

---

### 📬 Connect

- LinkedIn: [linkedin.com/in/gerald-january](https://linkedin.com/in/gerald-january)
- Email: businessclub2050@gmail.com

---

*"Engineer clarity. Deploy with purpose. Optimize the system."*
