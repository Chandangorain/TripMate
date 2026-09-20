# TripMate
# TripMate

![GitHub stars](https://img.shields.io/github/stars/Chandangorain/TripMate?style=for-the-badge&logo=github) ![GitHub forks](https://img.shields.io/github/forks/Chandangorain/TripMate?style=for-the-badge&logo=github) ![GitHub issues](https://img.shields.io/github/issues/Chandangorain/TripMate?style=for-the-badge&logo=github) ![Last commit](https://img.shields.io/github/last-commit/Chandangorain/TripMate?style=for-the-badge&logo=github) ![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

## 📝 Description

TripMate is an AI-powered travel planning application built with FastAPI, LangGraph, OpenAI, PostgreSQL, and JavaScript. It helps users plan trips by combining flight search, hotel discovery, AI-generated itineraries, budget-aware recommendations, and conversational travel assistance in a single platform.

## 🛠️ Tech Stack

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

**Notable libraries:** LangChain, Uvicorn

## 🏗️ Architecture

A high-level view of how the main pieces fit together:


                         TRIPMATE
                            │
              ┌─────────────┴─────────────┐
              │                           │
          FRONTEND                     BACKEND
              │                           │
       index.html + JS                  app.py
              │                           │
              └────────── HTTP ──────────┘
                                          │
                                      backend.py
                                          │
                                      LangGraph
                                          │
                 ┌────────────────────────┼──────────────────────┐
                 │                        │                      │
           ✈️ Flight Agent          🏨 Hotel Agent        🗓️ Itinerary Agent
                 │                        │                      │
          Flight API                  Tavily                  OpenAI
                 │                        │                      │
                 └────────────────────────┼──────────────────────┘
                                          │
                                   Final Response
                                          │
                                      PostgreSQL
                                   (Thread Memory)
```

## ⚡ Quick Start

```bash

# 1. Clone the repository
git clone https://github.com/Chandangorain/TripMate.git

# 2. Create & activate a virtualenv
python -m venv venv && source venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt

# Run the API
uvicorn main:app --reload
```

## 📦 Key Dependencies

```
langgraph: 1.2.2
langchain: 1.3.2
langchain-groq: 1.1.3
langchain-community: 0.4.2
langchain-tavily: 0.2.18
psycopg: [binary]==3.3.4
psycopg_pool: 3.3.1
python-dotenv: 1.2.2
tavily-python: 0.7.24
requests: 2.34.2
langgraph-checkpoint-postgres: 3.1.0
airportsdata: 20260315
pycountry: 26.2.16
fastapi: 0.136.3
uvicorn: 0.48.0
```

## 📁 Project Structure

```
.
├── LICENSE
├── app.py
├── backend.py
├── demo.excalidraw
├── requirements.txt
├── static
│   ├── script.js
│   └── style.css
├── templates
│   └── index.html
├── test.py
└── tools
    ├── flight_tool.py
    └── tavily_tool.py
```

## 🛠️ Development Setup

### Python
1. Install Python (v3.10+ recommended)
2. `python -m venv venv && source venv/bin/activate`  (Windows: `venv\Scripts\activate`)
3. `pip install -r requirements.txt`

## 📜 License

This project is licensed under the **MIT** License.

---

<div align="center">

[![Made with ReadmeBuddy](https://img.shields.io/badge/Made%20with-ReadmeBuddy-8B5CFF?style=for-the-badge&logo=markdown&logoColor=white)](https://readmebuddy.com)

<sub>Generate beautiful READMEs in seconds → <a href="https://readmebuddy.com">readmebuddy.com</a></sub>

</div>
