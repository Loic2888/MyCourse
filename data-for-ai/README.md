# Data for AI

A 25-course curriculum on preparing data for AI systems — from foundational data skills to production-grade data tooling. Built with the same custom Claude Code `create-course` skill used across this repository, and designed to run entirely in the browser.

> **Note:** All course content is written in **French**. This README is in English.

---

## How it works

Each course is a **single standalone HTML file** — no server, no dependencies, no setup.

To open a course:
1. Navigate into the relevant block folder below
2. Open the course's `.html` file directly in **Chrome** or Firefox
3. That's it — everything runs in your browser

Every course includes:
- Sidebar navigation across modules and lessons
- Progress tracking saved in your browser (`localStorage`)
- Syntax-highlighted code examples
- Pitfall callouts and hands-on exercises in every lesson
- Mobile-friendly layout

Files are named `{number}_{slug}.html` and live directly inside their block folder (no per-course subfolder).

---

## Course Blocks

The series progresses from general-purpose data skills toward increasingly specialized, production-oriented data preparation for AI — each block builds on the ones before it.

### Block 1 — Data Foundations (prerequisites)

Prerequisite data skills the rest of the series assumes: SQL, Python/pandas, statistics, and file formats.

| # | Course |
|---|--------|
| 1 | [Advanced SQL for Data — Joins, Window Functions, CTEs, and Aggregations](./1.fondations-data/1_sql-avance.html) |
| 2 | [Python for Data — Pandas, NumPy, and Dataset Profiling](./1.fondations-data/2_python-data-pandas-numpy.html) |
| 3 | [Applied Descriptive Statistics — Distribution, Outliers, and Correlation for Data Analysts](./1.fondations-data/3_statistiques-descriptives.html) |
| 4 | [Data Formats — CSV, JSON, Parquet, XML: Structure, Usage, and Technical Choices](./1.fondations-data/4_formats-de-donnees.html) |

### Block 2 — Classic Data Cleaning

Domain-agnostic data cleaning techniques that apply regardless of what you build downstream.

| # | Course |
|---|--------|
| 5 | [Data Cleaning — Deduplication, Normalization, and Encoding Management](./2.data-cleaning-classique/5_nettoyage-donnees.html) |
| 6 | [Handling Missing Values — Deletion, Imputation, and Business Decisions](./2.data-cleaning-classique/6_valeurs-manquantes.html) |
| 7 | [Anomaly and Outlier Detection — Statistical Methods and Business Rules](./2.data-cleaning-classique/7_detection-anomalies-outliers.html) |
| 8 | [Data Schema Validation — Types, Constraints, and Consistency](./2.data-cleaning-classique/8_validation-schema-donnees.html) |

### Block 3 — Data Preparation for RAG

Preparing text specifically for Retrieval-Augmented Generation: chunking, embeddings, metadata, and vector stores.

| # | Course |
|---|--------|
| 9 | [Chunking Documents for RAG — Strategies by Size, Semantics, and Structure](./3.prepa-data-pour-RAG/9_chunking-documents-rag.html) |
| 10 | [Embeddings and Vector Search — Understanding the Text-to-Vector Transformation](./3.prepa-data-pour-RAG/10_embeddings-recherche-vectorielle.html) |
| 11 | [Cleaning Unstructured Text — PDF, Word, HTML Extraction and Noise Removal](./3.prepa-data-pour-RAG/11_nettoyage-texte-non-structure.html) |
| 12 | [Metadata Enrichment for RAG — Structuring Context to Improve Retrieval](./3.prepa-data-pour-RAG/12_enrichissement-metadonnees-rag.html) |
| 13 | [Vector Databases — Chroma, Pinecone, Weaviate Concepts for Data Preparation](./3.prepa-data-pour-RAG/13_bases-donnees-vectorielles.html) |

### Block 4 — Unstructured Data

Extracting usable structure from messier sources: scanned documents, complex layouts, and basic NLP.

| # | Course |
|---|--------|
| 14 | [OCR and Scanned Document Extraction — Tesseract and API Solutions](./4.data-non-structur%C3%A9es/14_ocr-extraction-documents-scannes.html) |
| 15 | [Parsing Complex Documents — PDF Tables and Multi-Column Layouts](./4.data-non-structur%C3%A9es/15_parsing-documents-complexes.html) |
| 16 | [Basic NLP for Structuring — Tokenization and Named Entity Recognition](./4.data-non-structur%C3%A9es/16_nlp-tokenization-ner.html) |

### Block 5 — Data Preparation for AI Agents

Structuring, freshness, and observability concerns specific to agents that call tools and act in the world.

| # | Course |
|---|--------|
| 17 | [Structuring Data for Function Calling — JSON Schemas and Strict Validation](./5.prepa-data-for-agent-IA/17_function-calling-schemas-json.html) |
| 18 | [Real-Time vs Static Data — Managing Data in an Agentic Context](./5.prepa-data-for-agent-IA/18_donnees-temps-reel-vs-statiques.html) |
| 19 | [Logs and Traces of AI Agents — Cleaning and Structuring for Debugging and Improvement](./5.prepa-data-for-agent-IA/19_logs-traces-agents-ia.html) |

### Block 6 — Data Preparation for Fine-Tuning

Building datasets an LLM can actually be trained on: correct format, low bias/duplication, and high per-example quality.

| # | Course |
|---|--------|
| 20 | [Formatting Training Datasets — Instruction/Response Format and JSONL](./6.prepa-data-for-fine-tuning/20_formatage-datasets-instruction-jsonl.html) |
| 21 | [Bias and Duplication Detection in Fine-Tuning Datasets](./6.prepa-data-for-fine-tuning/21_detection-biais-duplication-datasets.html) |
| 22 | [Quality Filtering of Datasets — Heuristics and LLM-as-Judge](./6.prepa-data-for-fine-tuning/22_filtrage-qualite-datasets-llm-judge.html) |

### Block 7 — Tooling and Industrialization

Turning a working pipeline into a production-grade one: automated validation, reproducibility, and continuous quality monitoring.

| # | Course |
|---|--------|
| 23 | [Automated Data Validation — Great Expectations and Pandera in Python](./7.outillage-industrialisation/23_validation-donnees-great-expectations-pandera.html) |
| 24 | [Reproducible Data Transformation Pipelines — Versioning and Tests](./7.outillage-industrialisation/24_pipelines-reproductibles-versionnage-tests.html) |
| 25 | [Data Quality Monitoring — Detecting Source Degradation Over Time](./7.outillage-industrialisation/25_monitoring-qualite-donnees-degradation.html) |

---

## How courses are generated

Each course is produced by the same `create-course` skill used throughout this repository:
1. Maps the subject into modules and lessons (fundamentals → advanced)
2. Chooses a visual identity, reused consistently across the whole series for a shared identity
3. Writes each lesson in depth — concept, concrete example, common pitfall, exercise — with explicit cross-references to earlier courses in the series
4. Assembles everything into a single self-contained HTML file, written module by module

The full course roadmap (all 7 blocks, all 25 titles) is tracked in [`cours-a-faire-data.md`](./cours-a-faire-data.md).

---

## Repository structure

```
data-for-ai/
├── README.md
├── cours-a-faire-data.md              ← Course roadmap (all 7 blocks)
├── 1.fondations-data/                  ← Block 1: prerequisites
├── 2.data-cleaning-classique/          ← Block 2: classic data cleaning
├── 3.prepa-data-pour-RAG/              ← Block 3: data prep for RAG
├── 4.data-non-structurées/             ← Block 4: unstructured data
├── 5.prepa-data-for-agent-IA/          ← Block 5: data prep for AI agents
├── 6.prepa-data-for-fine-tuning/       ← Block 6: data prep for fine-tuning
└── 7.outillage-industrialisation/      ← Block 7: tooling & industrialization
```

Each block folder contains its courses directly as `.html` files — no further nesting.

Last updated: **July 2026**
