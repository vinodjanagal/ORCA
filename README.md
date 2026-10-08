<p align="center">
  <img src="assets/orcalogo.png" width="180" alt="ORCA Logo">
</p>

<h1 align="center">ORCA</h1>

<p align="center">
A cognitive runtime for structured reasoning, contextual intelligence, and decision support.
</p>

<p align="center">
<b>Personal Cognitive Operating System</b> · Beta — 2026
</p>

---

## Overview

ORCA is a Personal Cognitive Operating System designed to help users reason across context, information, and decisions rather than treating every interaction as an isolated prompt.

It combines persistent context, multi-turn conversation state, external evidence, structured reasoning, decision support, and response synthesis into a single backend-oriented cognitive runtime.

The system is designed around a pipeline of:

**Perception → Context Assembly → External Evidence → Reasoning → Synthesis**

The goal is not to replace human judgment, but to provide structured context and reasoning support for complex decisions.

---

## Status

**Beta — 2026**

ORCA is currently in beta. This public repository documents the architecture, system design, engineering decisions, and product concepts behind the system. The implementation repository remains private.

---

## Tech Stack

- **Backend:** Python, FastAPI
- **Database:** PostgreSQL
- **ORM & Migrations:** SQLAlchemy, Alembic
- **State & Caching:** Redis
- **Infrastructure:** Docker
- **Testing:** pytest
- **AI/LLM:** LLM APIs, multi-turn context management

---

## Architecture

```text
User Interaction
       │
       ▼
Perception
       │
       ▼
Context Assembly
       │
       ▼
External Evidence
       │
       ▼
Reasoning & Decision Support
       │
       ▼
Response Synthesis
       │
       ▼
Response
