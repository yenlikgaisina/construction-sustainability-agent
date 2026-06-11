# Construction Sustainability Research Agent

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)](https://python.org)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)]()
[![Framework](https://img.shields.io/badge/Framework-CrewAI-orange)]()
[![LLM](https://img.shields.io/badge/LLM-Gemini%202.0%20Flash-purple)]()
[![License](https://img.shields.io/badge/License-MIT-2D6A4F)]()

> Automating UK construction sustainability research using a three-agent CrewAI pipeline, from raw query to structured briefing in under 10 minutes.

---

## Business Question

> "Can a multi-agent AI system autonomously research, analyse, and synthesise Scope 3 and embodied carbon intelligence for UK construction projects, reducing research time from days to minutes?"

UK construction sustainability managers spend 2-3 days per month manually researching Scope 3 emissions data, embodied carbon benchmarks, and regulatory requirements from fragmented sources (UKGBC, RICS, HM Treasury, GHG Protocol). This project automates that research pipeline using a three-agent CrewAI system that searches live regulatory sources, validates findings, and produces a professional briefing.

---

## Agent Architecture

```
INPUT: Research topic (e.g. "Scope 3 Category 1 for UK construction subcontractors 2024")
         |
         v
+-------------------+  Tools: SerperDev search, web scraper
| RESEARCHER AGENT  |  Finds primary sources: UKGBC, RICS,
|  Senior           |  GHG Protocol, BREEAM, gov.uk
|  Sustainability   |
|  Researcher       |
+-------------------+
         |
         | raw findings (URLs, excerpts, data)
         v
+-------------------+  No external tools
|  ANALYST AGENT    |  Cross-checks figures, identifies
|  Carbon Data      |  benchmarks, flags inconsistencies
|  Analyst          |
+-------------------+
         |
         | validated analysis (metrics, gaps)
         v
+-------------------+  No external tools
|  WRITER AGENT     |  Synthesises: Executive Summary,
|  Technical Report |  Regulatory Context, Key Findings,
|  Writer           |  Recommended Actions
+-------------------+
         |
         v
OUTPUT: Professional Markdown briefing (800-1200 words)
```

---

## Agents

| Agent | Role | Goal |
|-------|------|------|
| Researcher | Senior Sustainability Researcher | Surface current Scope 3, embodied carbon, and regulatory guidance from live UK sources |
| Analyst | Carbon Data Analyst | Cross-reference and validate findings; extract key metrics and identify data gaps |
| Writer | Technical Report Writer | Synthesise findings into a professional, action-oriented sustainability briefing |

---

## Tasks

| Task | Agent | Output |
|------|-------|--------|
| Search for recent regulatory guidance and industry data on the given topic | Researcher | Structured findings package with source URLs, excerpts, and confidence ratings |
| Analyse extracted data: validate figures, build metrics table, flag gaps | Analyst | Validated metrics table with compliance deadlines and data quality notes |
| Write professional briefing: Executive Summary, Regulatory Context, Key Findings, Recommended Actions | Writer | Final Markdown briefing (800-1200 words) |

---

## Sample Research Topics

The system has been tested on the following UK construction sustainability topics:

1. Scope 3 Category 1: Purchased Goods & Services for UK general contractors (2024 reporting cycle)
2. Embodied carbon benchmarks for concrete-frame commercial buildings (RICS/LETI targets)
3. Whole-life carbon assessment requirements under UK Net Zero Carbon Buildings Standard
4. BREEAM UK New Construction 2018: Materials and Waste credits pathway
5. Circular economy procurement strategies for demolition and fit-out waste

---

## Technical Stack

| Component | Technology |
|-----------|------------|
| Agent Framework | CrewAI |
| LLM | Gemini 2.0 Flash (Google AI API) |
| Web Search | SerperDev API |
| Orchestration | LangChain |
| Notebook | Google Colab |
| Output Format | Markdown |

---

## Running the Notebook

1. Open the notebook in [Google Colab](https://colab.research.google.com/github/yenlikgaisina/construction-sustainability-agent/blob/main/notebook/construction_sustainability_agent.ipynb)
2. Add your API keys in Colab Secrets (key icon in sidebar):
   - `GOOGLE_API_KEY` -- from [Google AI Studio](https://aistudio.google.com/)
   - `SERPER_API_KEY` -- from [serper.dev](https://serper.dev/) (free tier available)
3. Run all cells. The crew executes sequentially and produces a briefing in the final cell.
4. To change the research topic, edit the `RESEARCH_TOPIC` variable in Section 6.

---

## Repository Structure

```
construction-sustainability-agent/
|-- notebook/
|   +-- construction_sustainability_agent.ipynb
+-- README.md
```

---

## Skills Demonstrated

`Python` `CrewAI` `LangChain` `Google Gemini API` `Agentic AI` `Multi-Agent Systems` `Prompt Engineering` `Scope 3 Emissions` `Embodied Carbon` `Construction Sustainability`

---

## Author

**Yenlik Gaisina** | Data & Analytics Consultant | Cambridge Data Science with ML & AI Programme

[LinkedIn](https://www.linkedin.com/in/yenlik-gaisina/) | [Portfolio](https://gaisina.co.uk/portfolio.html)
