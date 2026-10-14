<h1 align="center">Syed Waleed Ahmed</h1>

<p align="center">
  <strong>AI Engineer | Agentic Systems, LLM Applications & Applied Machine Learning</strong>
</p>

<p align="center">
  <a href="https://syedwaleedahmed.me">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/syed-waleed-ahmed/">LinkedIn</a> ·
  <a href="mailto:syedwaleedahmed9@gmail.com">Email</a> ·
  <a href="https://drive.google.com/file/d/1aYYWTcgosEV3QP3r3O2Hlf3WqqRkBe_x/view?usp=sharing">Resume</a>
</p>

---

I build AI applications and software systems around LLMs and machine learning models, with a focus on the engineering that makes them reliable beyond a demo.

My work spans agentic workflows, retrieval-augmented generation (RAG), model evaluation, backend APIs, data pipelines, and applied machine learning. I care about the less visible parts of engineering too: testing, observability, typed interfaces, failure handling, retries, and reproducible evaluation.

| | |
| --- | --- |
| **Focus** | AI Engineering, LLM Applications, Applied ML, Backend & Full-Stack Software |
| **Education** | MSc Automation Engineering, University of Bologna — completed **October 2026** |
| **Recent Experience** | AI-engineering thesis internship at **MemorAIz S.r.l.**, Bologna |
| **Looking for** | Early-career AI/ML and Software Engineering roles across Europe |
| **Based in** | Bologna, Italy · open to relocation within the EU |
| **Languages** | Urdu (native) · English (fluent) · Italian (elementary, A1) |

## Experience

### Master's Thesis Internship — AI Engineering · MemorAIz S.r.l.

*Bologna, Italy · February–June 2026*  
*Thesis collaboration continued through September 2026.*

Built **RemindrAI**, an embeddable, multi-tenant reminder and multi-channel communication capability that AI assistants can integrate instead of rebuilding.

- Built conversational reminder scheduling and delivery across Email, WhatsApp, Telegram, and Discord, packaged as a reusable Mastra capability.
- Engineered retry-safe delivery using atomic database claims, per-channel idempotency, database-owned retries and backoff, dead-letter handling, and provider-status reconciliation.
- Kept identity and ownership outside model-controlled tool arguments, reducing the risk of cross-user reminder redirection through prompt injection.
- Built the control plane and operator console with tenant isolation, per-organization API keys, plans and quotas, a content-blind audit trail, and audited data export and erasure operations.
- Added a 92-case LLM evaluation set. The connected three-repository ecosystem has **985 automated tests** across its combined test suites.
- Deployed in an EU-pinned Vercel configuration, with the H-FARM Student Assistant as the capability's **first tenant**.

The RemindrAI repositories are proprietary to MemorAIz. I'm happy to discuss the architecture and engineering decisions within appropriate confidentiality boundaries.

### Data Clustering & AI Model Intern · Fruugle SIA

*Jelgava, Latvia · Remote, part-time · January–April 2026*

- Built XGBoost models for grocery-product matching across Italian supermarket listings, achieving **97.5% held-out matching accuracy** against a 95% target, with a **0.995 ROC-AUC**; a separate classifier reached **99.5% held-out accuracy across 16 product categories**.
- Cleaned and parsed more than **81K loaded product records**, engineering text, brand, quantity, and price features, hard negatives, and per-fold class weights. Model training used the labelled subset rather than the entire loaded dataset.
- Built inference that grouped **24K+ unlabelled products**, using TF-IDF candidate shortlisting and guardrails against implausible matches.

### Tech Trainee · Jubilee Life Insurance Co. Ltd.

*Karachi, Pakistan · January–October 2024*

- Built internal full-stack applications using React, ASP.NET Core, PHP, and MySQL, and developed ETL pipelines processing **100K+ records**.
- Optimized SQL queries and stored procedures, with reported database response-time reductions of approximately **40%**.
- Automated SharePoint and CRM workflows, with reported manual-effort reductions of approximately **60%**, and delivered **15+ SSRS reports and Power BI dashboards**.
- Rotated across software development, databases, networking, and security operations, including IBM QRadar monitoring.

## Selected Projects

### LLM & Agent Systems

| Project | What it does | Stack |
| --- | --- | --- |
| [**Self-Correcting RAG**](https://github.com/syed-waleed-ahmed/Self-Correcting-RAG) | Filters irrelevant retrieved chunks and evaluates answer grounding against sources. Uses a bounded self-correction loop that retains the best-scoring attempt. Includes a REST API, CLI, and 31 offline tests. | Python · FastAPI · Groq · sentence-transformers · FAISS · Docker |
| [**LLM-as-Judge**](https://github.com/syed-waleed-ahmed/LLM-as-Judge) | Evaluates and compares model outputs against configurable criteria. Uses A/B order swapping to mitigate position bias and supports concurrent batch grading over CSV/JSONL. | Python · Groq · Pydantic · Streamlit |
| [**Campaign Forge**](https://github.com/syed-waleed-ahmed/Multi-Agent-Workflow) | Four-agent workflow that transforms a short product brief into a structured campaign. Includes validated outputs, retries with backoff, self-repairing JSON, and an adversarial evaluation corpus. Verified coverage: **96.4% statement coverage and 84.7% branch coverage**. | Python · OpenAI-compatible APIs · Groq · Pydantic · pytest · mypy |
| [**Multi-Agent Research Team**](https://github.com/syed-waleed-ahmed/Multi-Agent-Research-Team) | CrewAI-based research, coding, and manager agents produce structured Markdown reports through a sequential workflow with typed exceptions and retry handling. | Python · CrewAI · Groq · Serper |
| [**Niche Fine-Tuned Model**](https://github.com/syed-waleed-ahmed/Niche-Finetuned-Model) | Fine-tuned TinyLlama with LoRA for domain-specific Q&A and served it as a FastAPI microservice, including adapter loading, health probes, and structured logs. | PyTorch · Transformers · PEFT / LoRA · FastAPI · Docker |
| [**AI Workflow Assistant**](https://github.com/syed-waleed-ahmed/AI-Workflow-Assistant) | ReAct-style agent plans and invokes data tools, observes results, and iterates to generate structured analytical reports from raw CSV data. | Python · LangGraph · LangChain · Groq · pandas |

### Machine Learning, Computer Vision & Robotics

| Project | What it does | Stack |
| --- | --- | --- |
| [**TIAGo Autonomous Pick-and-Place**](https://github.com/syed-waleed-ahmed/tiago-autonomous-pick-and-place) | Master's team project. A mobile manipulator maps an unknown environment, localizes from an unfamiliar starting pose, discovers workstations using ArUco markers, and completes an ordered pick-and-place task without teleoperation. | ROS 2 Humble · Nav2 · SLAM · AMCL · ArUco · Gazebo · Python |
| [**Adversarial Attacks & Defenses**](https://github.com/syed-waleed-ahmed/celeba-adversarial-attacks-defenses) | Evaluated ResNet-18 on CelebA under FGSM and PGD attacks, investigating adversarial training and measuring robustness across perturbation strengths. Group project. | PyTorch · torchvision · scikit-learn |
| [**Visual Inspection of Connecting Rods**](https://github.com/syed-waleed-ahmed/Visual-Inspection-of-Motorcycle-Connecting-Rods) | Computer-vision pipeline that classifies motorcycle connecting rods by hole count and measures their geometry, with image-processing techniques for distractors and scattered iron powder. | Python · OpenCV · NumPy · SciPy |

### Portfolio

[**Portfolio Repository**](https://github.com/syed-waleed-ahmed/Portfolio) — Personal website built with React 19, Vite, and Express, with an emphasis on performance, accessibility, and security. Includes a hash-pinned Content Security Policy and CI checks for linting, tests, dependency auditing, and secret scanning.

Explore more project details on [syedwaleedahmed.me](https://syedwaleedahmed.me/#projects).

## Education

**MSc Automation Engineering** — Alma Mater Studiorum – Università di Bologna, Italy  
*October 2024 – October 2026*

Thesis: *RemindrAI: An Embeddable, Multi-Tenant Reminder and Multi-Channel Communication Capability for Conversational Applications*

**Erasmus+ Exchange** — University of Twente, Netherlands  
*September 2025 – January 2026*

Relevant coursework: Machine Learning I & II, Deep Learning, Modelling, Dynamics & Kinematics.

**BE Electrical Engineering** — NED University of Engineering and Technology, Karachi, Pakistan  
*October 2019 – August 2023*

## Technical Skills

**Languages**  
`Python` `TypeScript` `JavaScript` `SQL` `C++ (academic)`

**LLM & Agent Engineering**  
`RAG` `Multi-Agent Systems` `Tool Calling` `LangChain` `LangGraph` `CrewAI` `Mastra` `Vercel AI SDK` `OpenAI SDK` `Groq` `Hugging Face` `PEFT / LoRA`

**Machine Learning & Computer Vision**  
`PyTorch` `scikit-learn` `XGBoost` `OpenCV` `pandas` `NumPy` `SciPy` `Feature Engineering` `Model Evaluation`

**Backend & Web**  
`FastAPI` `Next.js` `React` `Node.js` `Express` `REST APIs` `Webhooks` `Multi-Tenancy`

**Data & Storage**  
`PostgreSQL` `pgvector` `Turso / libSQL` `FAISS` `MySQL` `SQL Server` `ETL`

**Testing & Tooling**  
`Docker` `Vercel` `Git` `GitHub Actions` `pytest` `Vitest` `ruff` `mypy` `CI/CD`

---

<p align="center">
  <sub>Building reliable AI systems, one test and one failure mode at a time. Open to early-career AI/ML and software engineering opportunities.</sub>
</p>
