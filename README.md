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

```
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
```

ORCA separates cognitive processing into distinct stages so that perception, context assembly, evidence integration, reasoning, and response synthesis remain separate responsibilities.

The runtime maintains persistent state across interactions so that reasoning can incorporate relevant context rather than relying only on the current prompt.

A diagram that includes the persistence layer is in [docs/architecture.md](docs/architecture.md).

---

## Core Capabilities

### Persistent Context

ORCA maintains structured context across interactions, allowing relevant user information, situations, goals, decisions, and conversation history to contribute to subsequent reasoning.

### Multi-Turn Reasoning

Conversation state is preserved across turns so that follow-up interactions can build on previous context rather than restarting from an isolated prompt.

### External Evidence

ORCA can incorporate information from external sources and represent observations together with source trust and agreement or conflict between evidence.

### Decision Support

The system organizes context, evidence, and reasoning into decision-oriented responses intended to improve clarity and judgment.

### Response Synthesis

The final response is generated from the assembled context, relevant evidence, persistent state, and reasoning process.

---

## Request Lifecycle

1. **Receive** — accept the user's request and conversation state.
2. **Perceive** — identify the user's situation and the relevant information.
3. **Assemble context** — retrieve relevant persistent state and conversation context.
4. **Gather evidence** — retrieve and incorporate relevant external information when required.
5. **Reason** — evaluate context and evidence through the reasoning layer.
6. **Synthesize** — produce a response grounded in the assembled state.
7. **Persist** — retain relevant state for subsequent interactions.

---

## Engineering Decisions

### Persistent state instead of prompt-only memory

Important context is persisted so that multi-turn reasoning does not depend entirely on the current conversation window.

### Separation of cognitive stages

Perception, context assembly, reasoning, evidence integration, and response synthesis are treated as distinct responsibilities to reduce coupling and make the runtime easier to evolve.

### External evidence as structured input

External information is represented as evidence rather than being treated as unquestioned truth. Source trust and agreement/conflict can therefore participate in reasoning.

### Private implementation, public architecture

The implementation remains private. This repository exposes the architecture and engineering reasoning needed to understand the system without publishing proprietary implementation details.

---

## Documentation

- [Architecture](docs/architecture.md) — stages, design principles, and diagram
- [Roadmap](ROADMAP.md)
- [Changelog](CHANGELOG.md)

---

## Project Vision

The objective of ORCA is to reduce cognitive fragmentation by helping users reason across information, context, and decisions rather than treating every interaction as an isolated prompt.

---

© ORCA
