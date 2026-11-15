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
| [**Self-Correcting Multi-Agent RAG**](https://github.com/syed-waleed-ahmed/Self-Correcting-RAG) | Hybrid BM25 and vector retrieval; a guardrail agent drops off-topic chunks and an evaluator grades each answer against its sources, correcting weak ones in a bounded loop that keeps the best attempt. Adds a tool-using agent with read-only SQL and private uploads. Hybrid search lifted recall@5 from 0.967 to 0.992 over dense retrieval on a 60-question golden set; **347 tests**. [Live demo](https://scrag-web.onrender.com/) | Python · FastAPI · PostgreSQL / pgvector · Next.js · Groq · Docker |
| [**LLM-as-Judge**](https://github.com/syed-waleed-ahmed/LLM-as-Judge) | Evaluation platform that grades LLM outputs with an LLM judge: pairwise, pointwise, reference-based, ranking, RAG faithfulness and agent trajectories. Judges each pair in both orders to offset position bias, and flags suspected prompt injection, verbosity bias and self-preference. Published on [PyPI](https://pypi.org/project/llm-as-judge-platform/) as one engine behind a library, CLI, REST API and dashboard; **98% test coverage**. [Live demo](https://llm-as-judge.streamlit.app/) | Python · Pydantic · FastAPI · Streamlit · Groq · Ollama |
| [**Campaign Forge**](https://github.com/syed-waleed-ahmed/Multi-Agent-Workflow) | Multi-agent marketing platform that turns a product brief into a reviewed, evidence-backed campaign: 28 agents and 14 workflow templates, checkpointed runs that pause on a quota and resume, research citations checked against retrieved evidence, and an Evaluation Lab with 14 prompt-injection cases. **97% branch coverage**. [Live demo](https://campaign-forge.streamlit.app/) | Python · Pydantic · FastAPI · Streamlit · Groq · SQLite |
| [**FastAPI Niche Assistant**](https://github.com/syed-waleed-ahmed/Niche-Finetuned-Model) | Small language model fine-tuned with LoRA on FastAPI questions (Qwen2.5-Coder-1.5B), merged and quantized to a 1 GB GGUF and served by llama.cpp on CPU behind an OpenAI-compatible streaming API, with opt-in retrieval over the FastAPI docs. A Cloudflare Worker handles keys and rate limits in front of Google Cloud Run, on free tiers. An eval gate decides each release: the Qwen fine-tune scored **0.666 against 0.546** for the TinyLlama release it replaced, on a 108-item held-out set. Weights on the [Hugging Face Hub](https://huggingface.co/syed-waleed-ahmed/fastapi-assistant-gguf). [Live demo](https://fastapi-assistant-edge.fastapi-assistant-edge.workers.dev) | Python · PEFT / LoRA · llama.cpp · FastAPI · Cloudflare Workers · Google Cloud Run |
| [**AI Workflow Assistant**](https://github.com/syed-waleed-ahmed/AI-Workflow-Assistant) | AI data analyst for spreadsheets: upload a CSV or Excel file, ask a question in plain language, and get a report with metrics, charts, findings and recommendations. A LangGraph agent plans the analysis and calls deterministic pandas tools; every figure in the report is checked against the computation behind it, and nothing the model writes is executed as code. Private accounts and datasets, follow-up questions, and exports to Markdown, PDF, Excel and CSV; **508 tests** across backend and frontend. [Live demo](https://ai-workflow-assistant-app.vercel.app) | Python · FastAPI · LangGraph · pandas · PostgreSQL · Next.js |
| [**MemorAIz Onboarding Assistant**](https://github.com/syed-waleed-ahmed/memoraiz-onboarding) | Conversational onboarding: an AI agent interviews the user and fills a live company-profile canvas in real time. Streams replies token by token, races OpenAI and Gemini in parallel so the fastest answer wins, and retrieves over PostgreSQL with pgvector, in English or Italian. [Live demo](https://memoraiz-onboarding.vercel.app) | TypeScript · Next.js · Mastra · PostgreSQL / pgvector · OpenAI · Gemini |
| [**Multi-Agent Research Team**](https://github.com/syed-waleed-ahmed/Multi-Agent-Research-Team) | CrewAI-based research, coding, and manager agents produce structured Markdown reports through a sequential workflow with typed exceptions and retry handling. | Python · CrewAI · Groq · Serper |

### Machine Learning, Computer Vision & Robotics

| Project | What it does | Stack |
| --- | --- | --- |
| [**TIAGo Autonomous Pick-and-Place**](https://github.com/syed-waleed-ahmed/tiago-autonomous-pick-and-place) | Master's team project. A mobile manipulator maps an unknown environment, localizes from an unfamiliar starting pose, discovers workstations using ArUco markers, and completes an ordered pick-and-place task without teleoperation. | ROS 2 Humble · Nav2 · SLAM · AMCL · ArUco · Gazebo · Python |
| [**Adversarial Attacks & Defenses**](https://github.com/syed-waleed-ahmed/celeba-adversarial-attacks-defenses) | Evaluated ResNet-18 on CelebA under FGSM and PGD attacks, investigating adversarial training and measuring robustness across perturbation strengths. Group project. | PyTorch · torchvision · scikit-learn |
| [**Adversarial RL on LunarLander**](https://github.com/syed-waleed-ahmed/LunarLander_AdversaryLearning) | PPO, recurrent PPO (LSTM) and SAC landers train in alternating rounds against an adversary that controls a budgeted wind force, with the wind visible or hidden, then face a fixed-wind robustness test. Group project. | Python · Stable-Baselines3 · Gymnasium |
| [**Visual Inspection of Connecting Rods**](https://github.com/syed-waleed-ahmed/Visual-Inspection-of-Motorcycle-Connecting-Rods) | Computer-vision pipeline that classifies motorcycle connecting rods by hole count and measures their geometry, with image-processing techniques for distractors and scattered iron powder. | Python · OpenCV · NumPy · SciPy |

### More Projects

- [**Mastra Course**](https://github.com/syed-waleed-ahmed/Mastra-Course): TypeScript agents with custom tools, multi-step workflows, evaluation scorers, libSQL-backed memory and MCP integration.
- [**Exam Sprint Planner**](https://github.com/syed-waleed-ahmed/exam-sprint-planner): local-first study planner that builds adaptive sprints from exam deadlines and topic confidence, with AI flashcards, quizzes and mind maps. React · Vite · Tailwind CSS. [Live](https://syed-waleed-ahmed.github.io/exam-sprint-planner/)
- [**EDU Capability Velocity Explorer**](https://github.com/syed-waleed-ahmed/edu-velocity): scores Skill and MCP capabilities, shortlists the top 10, runs hello-world tests with logged evidence and renders the results. TypeScript · React · Vitest. [Live](https://syed-waleed-ahmed.github.io/edu-velocity/)
- [**GTM Intelligence Platform**](https://github.com/syed-waleed-ahmed/GTM-Intelligence-Platform): collects news signals from Google News RSS, classifies them into go-to-market themes and writes a recommendation per theme, with a Slack digest. Python.
- [**LinkedIn Growth Report**](https://github.com/syed-waleed-ahmed/Linkedin-Report): scores a post's performance and its audience against an Ideal Customer Profile, with an HTML report and a Streamlit dashboard. Python.
- [**Netflix EDA**](https://github.com/syed-waleed-ahmed/Netflix-EDA): exploratory analysis of Netflix's 2021 catalog: cleaning, feature engineering, and trends by genre, rating and country. pandas · seaborn.

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
`RAG` `Multi-Agent Systems` `Tool Calling` `LangChain` `LangGraph` `CrewAI` `Mastra` `Vercel AI SDK` `OpenAI SDK` `Groq` `Hugging Face` `PEFT / LoRA` `llama.cpp / GGUF`

**Machine Learning & Computer Vision**  
`PyTorch` `TensorFlow` `scikit-learn` `XGBoost` `OpenCV` `pandas` `NumPy` `SciPy` `Feature Engineering` `Model Evaluation`

**Backend & Web**  
`FastAPI` `Next.js` `React` `Node.js` `Express` `REST APIs` `Webhooks` `Multi-Tenancy`

**Data & Storage**  
`PostgreSQL` `pgvector` `Turso / libSQL` `FAISS` `MySQL` `SQL Server` `MongoDB` `Kafka` `ETL`

**Testing & Tooling**  
`Docker` `Kubernetes` `Terraform` `Vercel` `Google Cloud Run` `Cloudflare Workers` `Git` `GitHub Actions` `pytest` `Vitest` `ruff` `mypy` `CI/CD`

---

<p align="center">
  <sub>Building reliable AI systems, one test and one failure mode at a time. Open to early-career AI/ML and software engineering opportunities.</sub>
</p>
