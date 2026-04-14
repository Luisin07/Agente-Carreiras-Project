# 🧠 Adaptive Career Agent (ACA)

An AI-powered career strategy assistant that analyzes automation risk, generates personalized upskilling and reskilling plans, and simulates technical interviews using LLMs.

## 🔗 Run on Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ua69ENIZElQ7JBIOpYJfo1zyefqExJJQ?usp=sharing)

> You'll need an OpenAI API key to run the notebook.

---

## Overview

The ACA processes a professional profile through 4 sequential stages, each powered by a specialized LLM agent with structured JSON output:

**F1 — Automation Risk Analysis**
Evaluates the automation probability of a given profession and identifies critical hard and soft skills.

**F2 — Upskilling Plan**
Generates a personalized skill enhancement plan with 5 learning resources based on the F1 output.

**F3 — Reskilling Roadmap**
Maps transferable skills and identifies the 5 new skills required for a career transition.

**F4 — Interview Simulation**
Simulates a technical interview with 3 questions, evaluates each response on clarity, relevance and depth, and generates a final feedback report.

---

## Architecture

Each stage is an independent agent with its own system prompt, enforcing structured JSON output. Stages are chained — F2 receives F1's output, F4 uses F3's target area.
F1 (Risk Analysis)
↓
F2 (Upskilling Plan) ← uses F1 skills
F3 (Reskilling Roadmap)
↓
F4 (Interview Simulation) ← uses F3 target area

**Key implementation decisions:**
- Zero-shot and few-shot prompt engineering for consistent JSON output
- Retry logic with exponential backoff for rate limit handling (429)
- JSON extraction utility that handles malformed LLM responses
- System role definition for each agent's behavior scope

---

## Tech Stack

- Python 3.x
- OpenAI API (GPT-4o-mini)
- Prompt Engineering (Zero-shot / Few-shot)
- Google Colab / Jupyter Notebook

---

## How to Run

1. Open the notebook via the Colab button above
2. Run the first cell and paste your OpenAI API key when prompted
3. Run all cells — the full F1→F4 pipeline executes automatically
4. The final report prints structured JSON output for each stage plus a markdown feedback summary

---

## Sample Input

```python
PROF_F1 = "Analista de Marketing Digital"
TAREFAS_F1 = "Gestão de campanhas pagas, criação de relatórios de performance, organização de dados de CRM."
AREA_INTERESSE_F3 = "Analista de Dados (foco em Business Intelligence)"
```

---

## Authors

- Luis Otavio Santini Feitosa — [GitHub](https://github.com/Luisin07)
- Lucas Andrade Souza

*Academic project — Computer Science @ FIAP | Prompt and Artificial Intelligence*
