# 🏀 SBL AI Scout – Project Plan

## 📌 Vision

Bygga ett AI-drivet scouting-system för SBL som kombinerar:

- 📊 Matchdata  
- 🧠 Feature engineering  
- 🤖 LLM-genererad scouting report  
- 🌐 FastAPI backend  

Systemet ska kunna:

> “Scout Borås Basket inför nästa match”

Och generera en strukturerad scouting-rapport.

---

# 🧱 PHASE 1 – Foundation (Data Layer)

## 🎯 Mål
Bygga pipeline för att hämta, lagra och strukturera matchdata.

## 1️⃣ Data Ingestion

### Du ska:
- Hämta matchdata (scraping/API)
- Spara raw-data
- Strukturera till clean dataset

### Struktur:

```
data/
  raw/
  processed/
```

### 📚 Lär dig om (sök på):

- python web scraping tutorial
- requests vs beautifulsoup
- pandas data cleaning
- handling missing values pandas
- sports data scraping python
- sqlite with python tutorial

---

## 2️⃣ Databas (valfritt men starkt)

Börja med:
- CSV (enkelt)

Utveckla senare:
- SQLite eller Postgres

### 📚 Sök på:

- sqlite python example
- sql joins explained
- designing relational schema
- star schema data warehouse

---

# 🧠 PHASE 2 – Analytics Engine

## 🎯 Mål
Bygga ett system som räknar fram scouting-metrics.

## 1️⃣ Feature Engineering

Exempelmetrics:

- Offensive rating  
- Defensive rating  
- Pace  
- 3P rate  
- Rebound margin  
- Turnover rate  
- Last 5 games form  

### 📚 Sök på:

- basketball advanced stats explained
- offensive rating formula
- feature engineering sports analytics
- rolling average pandas
- groupby pandas tutorial

---

## 2️⃣ Scouting Logic Layer

Skapa regler:

```python
if three_point_rate > league_avg:
    tag = "High 3PT Volume Team"
```

Detta är “intelligence layer”.

### 📚 Sök på:

- rule based system python
- designing analytics engine
- software architecture layered design

---

# 🤖 PHASE 3 – AI Report Generation (LLM Layer)

## 🎯 Mål
Generera scouting-rapporter med LLM.

## 1️⃣ Structured Prompting

LLM får:
- Statistik
- Tags
- Eventuellt artiklar

Den ska generera:

- Strengths
- Weaknesses
- Tactical tendencies
- Summary

### 📚 Sök på:

- prompt engineering best practices
- structured prompting llm
- few shot prompting
- reducing hallucinations llm

---

## 2️⃣ Retrieval (senare expansion)

Om du vill bygga RAG:

- Scrape artiklar
- Chunk text
- Skapa embeddings
- Vector search

### 📚 Sök på:

- rag architecture explained
- faiss tutorial
- vector database basics
- text chunking strategies

---

# 🧮 PHASE 4 – Optional: Prediction Model

## 🎯 Mål
Predicera matchvinnare.

## 1️⃣ Enkel ML-modell

Features:
- Offensive rating
- Rebound margin
- Home/away
- Form

Model:
- Logistic regression
- Random Forest

### 📚 Sök på:

- logistic regression sklearn
- train test split explained
- model evaluation metrics classification
- feature importance sklearn

---

# 🌐 PHASE 5 – API Layer

## 🎯 Mål
Exponera systemet via FastAPI.

Endpoint:

```
GET /scout/{team}
```

Return:
- JSON scouting report

### 📚 Sök på:

- fastapi tutorial
- pydantic models
- rest api design best practices
- async python basics

---

# 📦 PHASE 6 – MLOps Polish

## 1️⃣ Struktur

- Modular code
- requirements.txt
- Dockerfile
- README

## 2️⃣ Reproducibility

- Separera ingestion / feature engineering
- Spara processed data
- Versionshantera dataset

### 📚 Sök på:

- ml project structure best practices
- cookiecutter data science
- dockerizing fastapi app
- model versioning basics

---

# 🚀 Definition of Done (MVP)

✔ Matchdata hämtas  
✔ Metrics räknas korrekt  
✔ Structured scouting report genereras  
✔ API endpoint fungerar  
✔ README förklarar arkitektur  

---

# 📈 Expansion Roadmap (Senare)

- Player scouting  
- Comparison mode  
- Web dashboard  
- Authentication  
- Cloud deployment  
- CI/CD  
