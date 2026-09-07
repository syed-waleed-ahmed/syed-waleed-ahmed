<h1 align="center">Syed Waleed Ahmed</h1>
<p align="center">AI Engineer — multi-agent systems, RAG pipelines, and LLM services built to survive production.</p>

<p align="center">
  <a href="https://syedwaleedahmed.me">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/syed-waleed-ahmed/">LinkedIn</a> ·
  <a href="mailto:syedwaleedahmed9@gmail.com">Email</a> ·
  <a href="https://drive.google.com/file/d/1gPdW6Rf8X2NBD8h9NTKfysr-8Wx_3NoK/view?usp=sharing">Résumé</a>
</p>

---

I care about the parts most AI demos skip: evaluation, observability, and the engineering it takes to get from a working prototype to something a real team can rely on. Most of what I build ships with a test suite, typed configuration, and a CI pipeline, because that is the difference between a notebook and a service.

|  |  |
| --- | --- |
| **Now** | AI Engineer (Master's thesis) at **MemorAIz S.r.l.**, Bologna |
| **Education** | MSc Automation Engineering, University of Bologna — graduating **October 2026** |
| **Looking for** | AI / ML Engineer roles in Europe, available from **October 2026** |
| **Based in** | Bologna, Italy · open to relocation within the EU |

## Experience

**AI Engineer · Master's Thesis** — MemorAIz S.r.l., Bologna · *Feb 2026 – Present*

- Building **RemindrAI**, an embeddable multi-tenant reminder and communication capability that assistants adopt instead of rebuilding — one conversational agent scheduling over Email, WhatsApp, Telegram, and Discord.
- Made delivery correct under failure without a queue runtime: atomic database claim, per-channel idempotency, database-owned retries, dead-lettering, and reconciliation of provider status callbacks after a send.
- Built the control plane and operator console — plans, licences and quotas as data, tenancy enforced at four independent depths, a content-blind audit trail, and GDPR export and erasure — under **952 tests** across three repositories.
- Deployed EU-pinned on Vercel and published as a one-line Mastra capability, with H-FARM's Student Assistant as the first production tenant.

*The RemindrAI repositories are proprietary to MemorAIz and stay private. Happy to walk through the architecture.*

**Data Clustering & AI Model Intern** — Fruugle SIA, Latvia (remote) · *Jan 2026 – Apr 2026*

- Trained an **XGBoost** matcher that identifies the same grocery item across 6 Italian supermarket chains at **97.5% accuracy** against a 95% target, plus a category classifier reaching **99.5%** over 16 classes with class weighting so rare categories were not ignored.
- Engineered the pipeline over **80K+ scraped products** — Italian-text cleaning, a quantity parser, hard-negative sampling for ambiguous pairs — and shipped inference that grouped **24K+** unsorted products with guardrails against implausible matches.

**Tech Trainee** — Jubilee Life Insurance, Karachi · *Jan 2024 – Oct 2024*

- Built ETL pipelines over **100K+ records** and tuned queries and stored procedures, cutting database response times by **~40%**.
- Automated SharePoint and CRM workflows (**~60%** less manual effort) and delivered 15+ SSRS reports and Power BI dashboards.

## Selected projects

### LLM & agent systems

| Project | What it does | Stack |
| --- | --- | --- |
| **[Self-Correcting RAG](https://github.com/syed-waleed-ahmed/Self-Correcting-RAG)** | A guardrail agent scores and drops off-topic chunks before they pollute generation; an evaluator then scores the answer's grounding and triggers a bounded self-correction loop, always keeping the best attempt. Ships as both REST API and CLI. | Python · FastAPI · Groq · sentence-transformers · Docker |
| **[LLM-as-Judge](https://github.com/syed-waleed-ahmed/LLM-as-Judge)** | Scores and compares model outputs on custom criteria, with position-bias mitigation via A/B order swapping and concurrent batch grading over CSV/JSONL. Library, CLI, and Streamlit app on one core. | Python · Groq · Pydantic · Streamlit |
| **[Campaign Forge](https://github.com/syed-waleed-ahmed/Multi-Agent-Workflow)** | Research, copywriter, art-director, and manager agents turn a one-line product brief into a full campaign brief. Batch mode fans briefs across a thread pool with per-item error isolation. | Python · OpenAI-compatible APIs · Pydantic · mypy strict |
| **[Multi-Agent Research Team](https://github.com/syed-waleed-ahmed/Multi-Agent-Research-Team)** | A CrewAI CLI where research, coding, and manager agents turn any topic into a structured Markdown report — deterministic sequential pipeline, typed exceptions, backoff retries. | Python · CrewAI · Groq · Serper |
| **[Niche Fine-Tuned Model](https://github.com/syed-waleed-ahmed/Niche-Finetuned-Model)** | TinyLlama LoRA-fine-tuned for FastAPI Q&A and served as a real microservice: adapter loading through PEFT, completion-only loss, the tokenizer's native chat template, health probes and structured logs. | PyTorch · PEFT / LoRA · FastAPI · Docker |
| **[AI Workflow Assistant](https://github.com/syed-waleed-ahmed/AI-Workflow-Assistant)** | A ReAct agent that plans, calls data tools, observes, and iterates until it can write a structured analytical report over a raw CSV. | Python · LangGraph · LangChain · Groq · pandas |

### ML, computer vision & robotics

| Project | What it does | Stack |
| --- | --- | --- |
| **[TIAGo Pick-and-Place](https://github.com/syed-waleed-ahmed/tiago-autonomous-pick-and-place)** | A mobile manipulator that maps an unknown space, recovers its pose from a random start, finds two stations by their ArUco markers, and picks and places two cubes end to end — no teleoperation, and no map coordinates in the source. | ROS 2 Humble · Nav2 / SLAM · MoveIt 2 · ArUco · Gazebo |
| **[Adversarial Attacks & Defenses](https://github.com/syed-waleed-ahmed/celeba-adversarial-attacks-defenses)** | ResNet-18 on CelebA under FGSM and PGD, with adversarial training as a defense and robustness measured across increasing perturbation strength. | PyTorch · torchvision · scikit-learn |
| **[Visual Inspection of Connecting Rods](https://github.com/syed-waleed-ahmed/Visual-Inspection-of-Motorcycle-Connecting-Rods)** | Detects each motorcycle connecting rod in a grayscale image, classifies it by hole count, and measures position, orientation, length, width, and hole diameters. | Python · OpenCV · NumPy |

Also: **[Portfolio](https://github.com/syed-waleed-ahmed/Portfolio)** — my site, built for performance, accessibility and security (React 19 + Vite, Express API, hash-pinned CSP, CI with lint, tests, audit and secret scanning). More context on every project at [syedwaleedahmed.me](https://syedwaleedahmed.me/#projects).

## Tech I reach for

**Languages** `Python` `TypeScript` `SQL` `C++`

**LLM & agents** `LangChain` `LangGraph` `CrewAI` `Mastra` `Vercel AI SDK` `OpenAI` `Groq` `PEFT / LoRA`

**ML & CV** `PyTorch` `scikit-learn` `XGBoost` `OpenCV` `pandas` `NumPy`

**Backend & web** `FastAPI` `Next.js` `React` `Node.js` `REST` `Server Components`

**Data** `PostgreSQL` `pgvector` `Turso / libSQL` `MySQL`

**Tooling** `Docker` `Vercel` `GitHub Actions` `pytest` `Vitest` `ruff` `mypy`

---

<p align="center"><sub>Let's talk if you're hiring for AI/ML roles, or just want to compare notes on agentic systems.</sub></p>
