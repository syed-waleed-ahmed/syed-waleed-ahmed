<h1 align="center">Syed Waleed Ahmed</h1>

<p align="center">
  <strong>AI / ML Engineer · LLM Agents, RAG, Model Evaluation & Applied Machine Learning</strong>
</p>

<p align="center">
  <a href="https://syedwaleedahmed.me">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/syed-waleed-ahmed/">LinkedIn</a> ·
  <a href="mailto:syedwaleedahmed9@gmail.com">Email</a> ·
  <a href="https://drive.google.com/file/d/1aYYWTcgosEV3QP3r3O2Hlf3WqqRkBe_x/view?usp=sharing">Resume</a> ·
  <a href="https://huggingface.co/syed-waleed-ahmed">Hugging Face</a>
</p>

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white">
  <img alt="Hugging Face" src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black">
  <img alt="LangGraph" src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white">
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white">
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
</p>

---

I build AI systems around LLMs and machine-learning models, with a focus on the engineering that makes them reliable beyond a demo: evaluation, guardrails, testing and failure handling.

- **LLM agents & RAG**: multi-agent workflows, tool calling, hybrid retrieval and self-correcting answer loops.
- **Evaluation**: LLM-as-a-judge, golden sets, bias mitigation and eval-gated model releases.
- **Fine-tuning & serving**: LoRA fine-tuning, quantization to GGUF, and CPU inference behind OpenAI-compatible APIs.
- **Applied ML & computer vision**: gradient-boosted models, deep learning, adversarial robustness and image processing.

| | |
| --- | --- |
| **Focus** | AI Engineering, LLM Applications, Applied Machine Learning |
| **Education** | MSc Automation Engineering, University of Bologna — completed **October 2026** |
| **Recent Experience** | AI-engineering thesis internship at **MemorAIz S.r.l.**, Bologna |
| **Looking for** | Early-career AI/ML Engineering roles across Europe |
| **Based in** | Bologna, Italy · open to relocation within the EU |
| **Languages** | Urdu (native) · English (fluent) · Italian (elementary, A1) |

## Featured AI/ML Projects

### LLM Agents & RAG

| Project | What it does | Stack |
| --- | --- | --- |
| [**Self-Correcting Multi-Agent RAG**](https://github.com/syed-waleed-ahmed/Self-Correcting-RAG) | Hybrid BM25 and vector retrieval; a guardrail agent drops off-topic chunks and an evaluator grades each answer against its sources, correcting weak ones in a bounded loop that keeps the best attempt. Adds a tool-using agent with read-only SQL and private uploads. Hybrid search lifted recall@5 from 0.967 to 0.992 over dense retrieval on a 60-question golden set; **347 tests**. [Live demo](https://scrag-web.onrender.com/) | Python · FastAPI · PostgreSQL / pgvector · Next.js · Groq · Docker |
| [**Campaign Forge**](https://github.com/syed-waleed-ahmed/Multi-Agent-Workflow) | Multi-agent platform that turns a product brief into a reviewed, evidence-backed campaign: 28 agents and 14 workflow templates, checkpointed runs that pause on a quota and resume, research citations checked against retrieved evidence, and an Evaluation Lab with 14 prompt-injection cases. **794 tests, 97% branch coverage**. [Live demo](https://campaign-forge.streamlit.app/) | Python · Pydantic · FastAPI · Streamlit · Groq · SQLite |
| [**AI Workflow Assistant**](https://github.com/syed-waleed-ahmed/AI-Workflow-Assistant) | AI data analyst for spreadsheets: a LangGraph agent plans the analysis and calls deterministic pandas tools, and every figure in the report is checked against the computation behind it; nothing the model writes is executed as code. Charts, follow-up questions and exports; **508 tests** across backend and frontend. [Live demo](https://ai-workflow-assistant-app.vercel.app) | Python · FastAPI · LangGraph · pandas · PostgreSQL · Next.js |
| [**Multi-Agent Research Team**](https://github.com/syed-waleed-ahmed/Multi-Agent-Research-Team) | Research, coding and manager agents search the web, write runnable code examples and deliver a cited Markdown report, with every agent step, search, retry and provider fallback streamed live to the browser. Each link in the report is checked against the URLs the search actually retrieved. Persisted jobs with restart recovery, per-stage provider fallbacks and per-visitor quotas keep it running on free tiers; web app and CLI share one engine. **260+ tests** across pytest, Vitest and Playwright. [Live demo](https://multi-agent-research-team-aasz.onrender.com) | Python · CrewAI · LiteLLM · FastAPI · React · Groq · Serper · PostgreSQL |
| [**MemorAIz Onboarding Assistant**](https://github.com/syed-waleed-ahmed/memoraiz-onboarding) | An AI agent interviews the user and fills a live company-profile canvas in real time. Streams replies token by token, races OpenAI and Gemini in parallel so the fastest answer wins, and retrieves over PostgreSQL with pgvector, in English or Italian. [Live demo](https://memoraiz-onboarding.vercel.app) | TypeScript · Next.js · Mastra · PostgreSQL / pgvector · OpenAI · Gemini |

### Evaluation & Fine-Tuning

| Project | What it does | Stack |
| --- | --- | --- |
| [**LLM-as-Judge**](https://github.com/syed-waleed-ahmed/LLM-as-Judge) | Evaluation platform that grades LLM outputs with an LLM judge: pairwise, pointwise, reference-based, ranking, RAG faithfulness and agent trajectories. Judges each pair in both orders to offset position bias, and flags suspected prompt injection, verbosity bias and self-preference. Published on [PyPI](https://pypi.org/project/llm-as-judge-platform/) as one engine behind a library, CLI, REST API and dashboard; **98% test coverage**. [Live demo](https://llm-as-judge.streamlit.app/) | Python · Pydantic · FastAPI · Streamlit · Groq · Ollama |
| [**FastAPI Niche Assistant**](https://github.com/syed-waleed-ahmed/Niche-Finetuned-Model) | Small language model fine-tuned with LoRA on FastAPI questions (Qwen2.5-Coder-1.5B), merged and quantized to a 1 GB GGUF and served by llama.cpp on CPU behind an OpenAI-compatible streaming API, with opt-in retrieval over the FastAPI docs. An eval gate decides each release: the Qwen fine-tune scored **0.666 against 0.546** for the TinyLlama release it replaced, on a 108-item held-out set. Weights on the [Hugging Face Hub](https://huggingface.co/syed-waleed-ahmed/fastapi-assistant-gguf). [Live demo](https://fastapi-assistant-edge.fastapi-assistant-edge.workers.dev) | Python · PEFT / LoRA · llama.cpp · FastAPI · Cloudflare Workers · Google Cloud Run |

### Machine Learning, Computer Vision & Robotics

| Project | What it does | Stack |
| --- | --- | --- |
| [**Adversarial Attacks & Defenses**](https://github.com/syed-waleed-ahmed/celeba-adversarial-attacks-defenses) | Evaluated ResNet-18 on CelebA under FGSM and PGD attacks, investigating adversarial training and measuring robustness across perturbation strengths. Group project. | PyTorch · torchvision · scikit-learn |
| [**Visual Inspection of Connecting Rods**](https://github.com/syed-waleed-ahmed/Visual-Inspection-of-Motorcycle-Connecting-Rods) | Computer-vision pipeline that classifies motorcycle connecting rods by hole count and measures their geometry, with image-processing techniques for distractors and scattered iron powder. | Python · OpenCV · NumPy · SciPy |
| [**TIAGo Autonomous Pick-and-Place**](https://github.com/syed-waleed-ahmed/tiago-autonomous-pick-and-place) | Master's team project. A mobile manipulator maps an unknown environment, localizes from an unfamiliar starting pose, discovers workstations using ArUco markers, and completes an ordered pick-and-place task without teleoperation. | ROS 2 Humble · Nav2 · SLAM · AMCL · ArUco · Gazebo · Python |

More project details on [syedwaleedahmed.me](https://syedwaleedahmed.me/#projects).

## Experience

### Master's Thesis Internship — AI Engineering · MemorAIz S.r.l.

*Bologna, Italy · February–September 2026*

Built **RemindrAI**, an embeddable, multi-tenant reminder and multi-channel communication capability that AI assistants can integrate instead of rebuilding.

- Conversational reminder scheduling and delivery across Email, WhatsApp, Telegram and Discord, packaged as a reusable Mastra capability.
- Retry-safe delivery with atomic database claims, per-channel idempotency, database-owned retries and backoff, dead-letter handling and provider-status reconciliation.
- Identity and ownership kept outside model-controlled tool arguments, reducing the risk of cross-user reminder redirection through prompt injection.
- A 92-case LLM evaluation set; the connected three-repository ecosystem has **985 automated tests** across its combined test suites.
- Control plane with tenant isolation, per-organization API keys, plans and quotas, and audited data export and erasure; deployed in an EU-pinned Vercel configuration with the H-FARM Student Assistant as its **first tenant**.

The RemindrAI repositories are proprietary to MemorAIz. I'm happy to discuss the architecture and engineering decisions within appropriate confidentiality boundaries.

### Data Clustering & AI Model Intern · Fruugle SIA

*Jelgava, Latvia · Remote, part-time · January–April 2026*

- XGBoost models for grocery-product matching across Italian supermarket listings: **97.5% held-out matching accuracy** against a 95% target, with a **0.995 ROC-AUC**; a separate classifier reached **99.5% held-out accuracy across 16 product categories**.
- Cleaned and parsed more than **81K loaded product records**, engineering text, brand, quantity and price features, hard negatives and per-fold class weights.
- Inference that grouped **24K+ unlabelled products**, using TF-IDF candidate shortlisting and guardrails against implausible matches.

### Tech Trainee · Jubilee Life Insurance Co. Ltd.

*Karachi, Pakistan · January–October 2024*

- ETL pipelines processing **100K+ records**, SQL query and stored-procedure optimization (reported response-time reductions of about **40%**), and **15+ SSRS reports and Power BI dashboards**.
- Internal full-stack applications with React, ASP.NET Core, PHP and MySQL, and SharePoint and CRM workflow automation.

## Education

**MSc Automation Engineering** — Alma Mater Studiorum – Università di Bologna, Italy · *October 2024 – October 2026*  
Thesis: *RemindrAI: An Embeddable, Multi-Tenant Reminder and Multi-Channel Communication Capability for Conversational Applications*

**Erasmus+ Exchange** — University of Twente, Netherlands · *September 2025 – January 2026*  
Coursework: Machine Learning I & II, Deep Learning, Modelling, Dynamics & Kinematics.

**BE Electrical Engineering** — NED University of Engineering and Technology, Karachi, Pakistan · *October 2019 – August 2023*

## Technical Skills

**LLM & Agent Engineering**  
`RAG` `Multi-Agent Systems` `Tool Calling` `LangChain` `LangGraph` `CrewAI` `Mastra` `Vercel AI SDK` `OpenAI SDK` `LiteLLM` `Groq` `Hugging Face` `PEFT / LoRA` `llama.cpp / GGUF` `LLM Evaluation`

**Machine Learning & Computer Vision**  
`PyTorch` `TensorFlow` `scikit-learn` `XGBoost` `OpenCV` `pandas` `NumPy` `SciPy` `Feature Engineering` `Model Evaluation`

**Languages**  
`Python` `TypeScript` `JavaScript` `SQL` `C++ (academic)`

**Data & Storage**  
`PostgreSQL` `pgvector` `Turso / libSQL` `FAISS` `MySQL` `SQL Server` `MongoDB` `Kafka` `ETL`

**Serving, Backend & MLOps**  
`FastAPI` `Next.js` `React` `Node.js` `Streamlit` `REST APIs` `Server-Sent Events` `Docker` `Kubernetes` `Terraform` `Vercel` `Google Cloud Run` `Cloudflare Workers` `GitHub Actions` `CI/CD`

**Testing & Quality**  
`pytest` `Vitest` `Playwright` `ruff` `mypy` `Git`

---

<p align="center">
  <sub>Building reliable AI systems, one test and one failure mode at a time. Open to early-career AI/ML engineering opportunities.</sub>
</p>
