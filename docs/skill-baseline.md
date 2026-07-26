# Skill Baseline

Scoring scale:
- 0: cannot explain yet
- 1: can define basic concepts
- 2: can implement and debug with documentation
- 3: can design, compare alternatives, and operate in production

| Skill area | Score | Evidence |
|---|---:|---|
| Product requirements vs SLOs | 1 | Can define the difference after P1-00 discussion; needs practice writing measurable requirements. |
| Git branches and PR workflow | 1 | Understands commits and PRs at a basic level; needs disciplined branch and review practice. |
| Python packaging and `uv` | 0 | Not yet implemented a `uv` workspace for this project. |
| FastAPI backend APIs | 1 | Understands FastAPI as the API layer; needs implementation and testing practice. |
| RAG fundamentals | 1 | Can name retrieval-augmented generation; needs hands-on baseline, chunking, embeddings, citations, and evaluation. |
| Vector databases and pgvector | 0 | No implementation evidence yet. |
| OpenSearch hybrid retrieval | 0 | No implementation evidence yet. |
| AWS service selection | 1 | Understands that access patterns influence Aurora, DynamoDB, OpenSearch, and S3 choices; needs deeper design practice. |
| IAM and cloud security | 0 | No project evidence yet. |
| CI/CD and GitHub Actions | 0 | No project pipeline evidence yet. |
| Testing strategy | 1 | Understands tests are required; needs unit, contract, integration, evaluation, and security test practice. |
| GenAI evaluation | 0 | No evaluation suite built yet. |
| Prompt injection and safety | 0 | No threat model or tests yet. |
| Observability | 0 | No traces, metrics, logs, or dashboards yet. |
| System design trade-offs | 1 | Can discuss basic database choice trade-offs; needs capacity, failure-mode, cost, and rollback practice. |

## Current Learning Gaps

- Writing measurable acceptance criteria and SLOs
- Designing from access patterns before choosing services
- Building a reproducible Python monorepo
- Implementing RAG from a simple baseline
- Separating retrieval metrics from generation metrics
- Writing ADRs with rejected alternatives
- Using AWS safely with least privilege and budgets
- Creating test evidence strong enough for a portfolio review