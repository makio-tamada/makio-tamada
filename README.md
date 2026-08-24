<div align="right">

[![English](https://img.shields.io/badge/lang-English-0A66C2?style=flat)](./README.md)
[![日本語](https://img.shields.io/badge/lang-日本語-lightgrey?style=flat)](./README.ja.md)

</div>

# Tama

**Building end-to-end systems — from statistical modeling to shipped apps.**

Data/ML engineer at a Japanese e-commerce company. I work across the whole line: designing the statistical method, building the pipeline, wrapping it in an API, and shipping the app that sits on top of it.

- 📊 **Survival analysis & causal inference** — propensity score matching, Kaplan–Meier, Cox proportional hazards
- 🤖 **LLM applications** — RAG systems, agent pipelines, vector search
- 🛠️ **Automation** — turning manual, repetitive work into pipelines that run themselves
- ✍️ I write about what I build at [subbrain-works.net](https://subbrain-works.net/)

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

**Data & ML**

![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![statsmodels](https://img.shields.io/badge/statsmodels-3F4F75?style=flat)
![lifelines](https://img.shields.io/badge/lifelines-8B5CF6?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

**LLM & Retrieval**

![OpenAI API](https://img.shields.io/badge/OpenAI%20API-412991?style=flat)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Firestore Vector Store](https://img.shields.io/badge/Firestore%20Vector%20Store-FFCA28?style=flat&logo=firebase&logoColor=black)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat&logo=qdrant&logoColor=white)

**Cloud & Infra**

![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Cloud Run](https://img.shields.io/badge/Cloud%20Run-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

**Tooling**

![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat&logo=uv&logoColor=white)
![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat&logo=ruff&logoColor=black)
![mypy](https://img.shields.io/badge/mypy-2A6DB2?style=flat)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)

---

## Selected Work

> Most of these live in private repositories — clinical data and unreleased products.
> Happy to walk through the design and code in a conversation.

### 🏥 Survival Analysis Pipeline &nbsp;<sub>`private`</sub>

A reproducible pipeline for time-to-event analysis on clinical data, built for a research
collaboration in the healthcare domain.

- Confounder adjustment via **propensity score matching**, with balance diagnostics
- **Kaplan–Meier** survival curves and **Cox proportional hazards** modeling
- Packaged as a reusable `src/` library (preprocessing / matching / survival / evaluation / visualization) so that every result is reproducible from raw data

`Python` `lifelines` `scikit-survival` `statsmodels` `pandas`

### 🔍 Stera — Structured-text Extraction & Retrieval Assistant &nbsp;<sub>`private`</sub>

A multi-tenant SaaS that turns any WordPress site into a RAG-backed chat experience. Site owners
pick pages from the WP admin screen; an async pipeline crawls, embeds, and indexes them, and a
shortcode drops the chat widget onto the live site.

- **Firestore Vector Store** for retrieval — near-zero fixed cost, real-time updates, native GCP integration
- **FastAPI on Cloud Run** backend with per-tenant API key auth
- **React + TypeScript + Vite + Tailwind** console for RAG parameter tuning, knowledge management, and answer previews
- Fully reproducible locally via the Firestore Emulator, with CI on GitHub Actions

`FastAPI` `GCP` `Firestore` `React` `TypeScript` `PHP`

### 🎧 TM Beat Studio &nbsp;<sub>`private`</sub>

An end-to-end pipeline that generates long-form Lo-Fi music videos and publishes them to YouTube
without human intervention — a production system, not a demo.

- Audio generation with **diffusion models**, stitched into hour-long tracks
- Video composition and rendering via **MoviePy** / FFmpeg
- Automated upload, metadata, and scheduling through the **YouTube Data API**

`Python` `diffusers` `MoviePy` `YouTube Data API`

### 📱 iOS Apps & Engineering Templates &nbsp;<sub>`private`</sub>

- **Life is Quest** — a gamified task manager that reframes goals as RPG quests, with a retro-game UI (`Swift` / `SwiftUI`)
- **AWS CLF Exam App** — a certification study app with LLM-generated practice questions, a Firestore-backed Python service, and progress analytics (`Swift` / `Python` / `Firestore` / `OpenAI API`)
- **Python Analysis Template** — an opinionated starting point for analysis projects: `uv` + src layout + `Ruff` + `mypy` + `pytest`, so a new project is reproducible from day one

---

## Activity

<sub>Language and commit stats include private repositories — repository names and commit contents stay hidden.</sub>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github_dark/1-repos-per-language.svg">
  <img src="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github/1-repos-per-language.svg" width="49%" alt="Repos per language">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github_dark/2-most-commit-language.svg">
  <img src="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github/2-most-commit-language.svg" width="49%" alt="Most commit language">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github_dark/3-stats.svg">
  <img src="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github/3-stats.svg" width="49%" alt="Stats">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github_dark/4-productive-time.svg">
  <img src="https://raw.githubusercontent.com/makio-tamada/makio-tamada/main/profile-summary-card-output/github/4-productive-time.svg" width="49%" alt="Productive time">
</picture>

---

## Writing

I publish notes on data analysis, LLM applications, and automation at
**[subbrain-works.net](https://subbrain-works.net/)** — mostly write-ups of the problems I hit
while building the projects above.

---

## Contact

[![Blog](https://img.shields.io/badge/Blog-subbrain--works.net-0A66C2?style=flat&logo=googlechrome&logoColor=white)](https://subbrain-works.net/)
[![X](https://img.shields.io/badge/X-@tama__program-000000?style=flat&logo=x&logoColor=white)](https://x.com/tama_program)
