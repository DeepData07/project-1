# Project Charter: Adaptive Multimodal Learning Copilot

## Project Goal

Build a production-grade AI learning platform that helps students learn from course material through grounded explanations, progressive hints, personalized support, safe code debugging, video question answering, citations, evaluation, and AWS deployment.

The goal is not to build a generic chatbot. The goal is to learn and demonstrate production GenAI engineering through small reviewed tasks, tests, architecture decisions, and pull requests.

## Product Scope

In scope:
- Course-document question answering with citations
- Concept explanations adjusted to student level
- Progressive Socratic hints without direct answer leakage
- Personalized doubt resolution using a student profile
- Safe code-debugging workflow
- Video Q&A with timestamp citations
- Retrieval baselines before advanced RAG
- Evaluation for retrieval, generation, hints, safety, and agents
- FastAPI backend and Next.js frontend at planned checkpoints
- AWS-native deployment with CI/CD, observability, security, and rollback

## Scope Exclusions

Out of scope for the first release:
- Generic chat-with-PDF behavior without learning policy
- Autocomplete-style coding assistant
- Massive web-scale ingestion
- Production GraphRAG before benchmark evidence
- Running untrusted student code before sandbox security is accepted
- Direct browser access to AWS services
- Hard-coded model IDs or unverified cloud assumptions
- Training/fine-tuning before Project 2 and baseline evidence

## Delivery Rules

- Work one roadmap task at a time.
- Do not generate the full repository at once.
- Use short-lived branches and pull requests.
- Keep `main` releasable.
- Record major decisions in ADRs.
- Use tests and evidence for every implementation task.
- Keep notebooks exploratory only; production logic must move into importable Python modules.
- Never commit secrets, large datasets, model weights, generated indexes, or `.env` files.

## Budget and Environment Assumptions

Initial environment: local development.

AWS region: undecided.

Budget ceiling: no paid AWS resources until explicitly approved. Initial learning budget target is `0 USD/month` locally, then a maximum of `25 USD/month` for early AWS dev experiments unless revised in an ADR.

Local substitutes are required before cloud deployment where possible, especially for databases, queues, mocked model providers, and evaluation smoke tests.

## Freshness Rule

Before using any AWS service, model, SDK, managed capability, or dependency version, I will re-check official documentation, record the date checked, and capture the selected version or model/profile in an ADR or configuration file.

## Outcome-to-Phase Mapping

| Outcome | Future phase |
|---|---|
| Product requirements and acceptance scenarios | Phase 1 |
| Architecture and ADR backlog | Phase 1 |
| Reproducible repository and CI | Phase 2 |
| Pilot corpus and licensing | Phase 3 |
| PostgreSQL and pgvector baseline | Phase 4 |
| Ingestion, parsing, chunking, embeddings | Phase 5 |
| Naive RAG and evaluation baseline | Phase 6 |
| OpenSearch hybrid retrieval and reranking | Phase 7 |
| Learning policy, hints, personalization | Phase 8 |
| Code debugging and video Q&A | Phase 9 |
| LangGraph, tools, MCP, approvals | Phase 10 |
| FastAPI and UI integration | Phase 11 |
| Guardrails, observability, AWS deployment | Phase 12 |
| Staging, production, rollback, interview package | Phase 13 |