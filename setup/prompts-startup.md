Below is a production-grade master project prompt you can use with Copilot, agents, or builders to generate the full system.


---

📦 PROJECT PROMPT — Collaborative Data Analytics & Modeling OS

🧠 Project Name

Analytics OS (Data → Model → Insight Platform)


---

🎯 Objective

Build a full-stack web application that ingests raw data, cleans it, analyzes it, and allows users to create models and custom statistics through equations and AI-assisted workflows.

The system must support:

individuals (solo analysts)

teams (collaborative projects)

embeddable dashboards + API access



---

🏗️ Core System Vision

This platform is a: Data Pipeline + Analysis Lab + Model Engine + Dashboard Builder + Collaboration Workspace

All in one system.


---

⚙️ Core Workflow (Must Be Enforced)
```
1. Data Ingestion
2. Data Cleanin
3. Analysis / Feature Engineering
4. Modeling / Equation Creation
5. Dashboard + API Output
6. Collaboration + Iteration

```


---

🧩 Core Modules (Required)

1. Data Lab

upload CSV / connect API

schema detection

column mapping

data cleaning pipeline

validation rules

preview before commit



---

2. Analysis Lab

SQL editor + no-code query builder

pivot tables

aggregations + filters

time splits (7d, 30d, YTD)

saved queries

chart generation



---

3. Model Lab (CRITICAL FEATURE)

equation builder (visual + code)

variable selector

weight sliders

real-time output preview

leaderboard generation

model versioning (v1, v2, v3)

backtesting engine



---

4. Notebook Workspace

Python + SQL execution

markdown + code cells

saved notebooks

execution history



---

5. Dashboard Builder

drag-and-drop widgets

charts, tables, KPI cards

advanced filtering system

saved views

public/private dashboards

embeddable widgets (iframe/script)



---

6. API + Embed System

REST API (FastAPI)

API key management

query endpoints

model output endpoints

embed generator (3rd party sites)



---

7. AI Assistant Layer

natural language → SQL

natural language → Python

natural language → formulas

data cleaning suggestions

model optimization suggestions



---

8. Collaboration System

Project-Based Workspaces

datasets

models

dashboards

notebooks

tasks

discussions


Roles

Owner

Admin

Editor

Viewer


Features

comments on datasets/models/charts

activity feed

real-time collaboration (optional v2)

shared query/model library



---

9. Chatboard

project-based channels

threaded discussions

attach datasets/models

AI summaries



---

10. Project Manager (Repo Style)

roadmap view

task board (kanban)

milestones

changelog

documentation hub



---

🧱 Tech Stack Requirements

Frontend

React + Vite + TypeScript

Tailwind CSS

TanStack Table (advanced filtering)

TanStack Query

Charting: Apache ECharts or Recharts


Backend

FastAPI (Python)

PostgreSQL

Redis (cache)

Celery or Prefect (jobs)


Data / Modeling

Pandas

NumPy

scikit-learn

SymPy (formula parsing)


AI Layer

OpenAI API

LangChain (optional orchestration)



---

🗄️ Database Design (High-Level)

Schemas

auth

users

roles

permissions

API keys


projects

projects

members

tasks

milestones


data_core

raw_tables

cleaned_tables

ingestion_logs


analytics

features

metrics

aggregates

time_splits


models

model_registry

model_versions

model_weights

model_outputs


notebooks

notebook_files

executions


discussion

threads

comments


embeds

tokens

configs



---

🎨 UI Layout

Global Layout

Top Bar → project selector, search, AI input

Left Sidebar → modules navigation

Main Canvas → workspace

Right Panel → comments, activity, collaborators



---

Core Pages

Project Dashboard (overview + activity)

Data Lab

Analysis Lab

Model Lab

Notebooks

Dashboard Builder

API / Embeds

Chatboard

Task Manager



---

🔁 Key System Principles

everything is versioned

everything is linkable

everything is queryable

everything is shareable

AI assists but does not auto-execute without confirmation



---

🚀 Build Order

1. Auth + Project system


2. Database schemas


3. FastAPI backend


4. React app shell + navigation


5. Data ingestion + cleaning module


6. Analysis (query + table system)


7. Model Lab (equation engine)


8. Dashboard builder


9. API + embed system


10. AI assistant layer


11. Collaboration + chatboard


12. Task/roadmap system




---

🧠 Stretch Features (Post-MVP)

backtesting engine

model performance scoring

anomaly detection

auto feature discovery

scenario simulation

marketplace (share models/datasets)



---

📌 Final Instruction

Build this system as a modular analytics operating system where:

users can go from raw data → insight → model → dashboard → API

teams can collaborate on projects seamlessly

models become reusable, versioned assets

dashboards can be embedded anywhere

AI accelerates every step of the workflow



---

If you want next step:

I can convert this into a GitHub repo scaffold + folder structure

or generate a Copilot agent instruction file (.github/copilot-instructions.md)

or build UI component specs for React (ready to code)
