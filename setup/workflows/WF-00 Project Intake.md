---

Step 1 — Requirements Elicitation

Overview

You are building an Analytics Workstation Platform: A collaborative web app that transforms raw data → analysis → models → dashboards → API outputs.


---

Goals

Build a full data-to-model pipeline system

Enable individual + team collaboration

Allow creation of custom statistics/models (STORM-style)

Provide advanced dashboards with embeds + API access

Integrate AI to accelerate workflows



---

Scope

In Scope

Data ingestion + cleaning system

Analysis tools (queries, notebooks, features)

Model builder (formulas, weights, rankings)

Dashboard builder + visualization

API + embed system

Collaboration tools (comments, chatboard, shared assets)

AI assistant (NL → SQL/Python/formulas)

Project/workspace management


Out of Scope (for MVP)

Full real-time collaboration (Google Docs level)

Marketplace for models/datasets

Advanced ML training pipelines (keep simple first)

Enterprise billing system



---

Personas

1. Solo Analyst

builds models

explores data

creates dashboards


2. Data Scientist / Model Builder

creates formulas

tests models

runs backtesting


3. Team / Organization

collaborates on datasets and models

shares dashboards

tracks progress


4. Developer / Integrator

uses API

embeds dashboards

integrates external systems



---

Constraints

Modular monolith architecture (initially)

FastAPI + React stack

PostgreSQL primary DB

Must support future microservices split

Must be API-first

Must support large datasets (performance matters)



---

Assumptions

Users will work in project-based environments

Data sources will vary widely (CSV + APIs)

Models are primarily formula-based scoring systems

AI is assistive, not autonomous



---

Success Metrics

User can go from raw data → dashboard in one workflow

Models can be created and reused

Dashboards can be embedded externally

Queries + models are saved and versioned

Teams can collaborate inside projects



---

Step 2 — Project Brief

project_brief.md

# Project Brief — Analytics Workstation Platform

## Overview
A full-stack analytics platform that transforms raw data into models, statistics, dashboards, and APIs within a collaborative workspace.

## Objectives
- Build end-to-end data pipeline
- Enable model creation via formulas
- Support team collaboration
- Provide embeddable dashboards and APIs
- Integrate AI-assisted workflows

## Scope
Includes data ingestion, cleaning, analysis, modeling, visualization, API exposure, and collaboration tools.

## Out of Scope
- Advanced ML pipelines (initially)
- Marketplace systems
- Enterprise billing

## Stakeholders
- Founder / Product Owner
- Developers
- Analysts / Model Builders
- End Users

## Personas
- Solo Analyst
- Data Scientist
- Team/Org User
- API Developer

## Core Features
- Data Lab (ingestion + cleaning)
- Analysis Lab (queries + features)
- Model Lab (formula builder)
- Dashboard Studio (visuals)
- API + Embeds
- AI Assistant
- Collaboration System

## Constraints
- FastAPI backend
- React frontend
- PostgreSQL database
- Modular monolith architecture

## Success Metrics
- End-to-end workflow completed in-app
- Models reusable and versioned
- Dashboards embeddable
- Teams collaborate effectively


---

Step 3 — Roadmap

roadmap.md

# Roadmap

## Prototype Phase
- Core docs
- Basic UI shell
- Data ingestion (CSV)
- Basic query system
- Simple dashboard

## MVP Phase
- Full Data Lab (cleaning + validation)
- Analysis Lab (queries + features)
- Model Lab (formula builder)
- Dashboard builder
- API endpoints
- Basic collaboration

## Production Phase
- AI assistant
- advanced collaboration
- embed system
- worker pipelines
- performance optimization
- monitoring + security


---

milestones.md

# Milestones

| Milestone | Phase | Description |
|----------|------|------------|
| M1 | Prototype | Basic app shell + data ingestion |
| M2 | Prototype | Query system + simple dashboard |
| M3 | MVP | Data cleaning + validation |
| M4 | MVP | Model Lab (formula engine) |
| M5 | MVP | Dashboard builder |
| M6 | MVP | API endpoints |
| M7 | Production | AI assistant integration |
| M8 | Production | Collaboration system |
| M9 | Production | Worker pipelines + scaling |


---

Step 4 — Risk Register

risk_register.md

# Risk Register

| Risk | Category | Likelihood | Impact | Mitigation |
|------|----------|-----------|--------|------------|
| Poor data quality | Data | High | High | Strong validation + cleaning pipeline |
| Over-engineering AI early | Technical | Medium | High | Scope AI to assistive features only |
| Performance issues with large datasets | Technical | Medium | High | Use caching, pagination, optimized queries |
| Complex UI overwhelm | Product | Medium | Medium | Strong design system + phased UI rollout |
| Scope creep | Timeline | High | High | Strict phase-based roadmap |


---

Step 5 — Orchestrator Sign-off

Status

APPROVED


---

Final Output Summary

Generated:

✅ project_brief.md

✅ roadmap.md

✅ milestones.md

✅ risk_register.md



---

Next Workflow

Proceed to:

WF-01 → Architecture Setup


---

If you want next:

I can auto-run WF-01 and generate full backend + frontend architecture

or convert this into your task system / GitHub Issues instantly

or inject this directly into your .ai workflow registry
