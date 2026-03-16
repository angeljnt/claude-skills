# claude-skills

Custom Claude Code skills by [@angeljnt](https://github.com/angeljnt).

## Available Skills

| Skill | Description |
|-------|-------------|
| [sota-research](sota-research/SKILL.md) | State of the Art research — synthesizes 5 pillars (scientific papers, standards, industry reports, best practices, expert opinions) with built-in file-based planning |

---

## Install

```bash
SKILL=sota-research
mkdir -p ~/.claude/skills/$SKILL
curl -L https://raw.githubusercontent.com/angeljnt/claude-skills/main/$SKILL/SKILL.md \
  > ~/.claude/skills/$SKILL/SKILL.md
```

Open any Claude Code session and run `/sota-research [topic]` to verify.

---

# `sota-research` — State of the Art Research

Use this skill before building anything non-trivial. It prevents reinventing the wheel by establishing what already exists, what's proven, and what's standard in any technical or theoretical area.

## What it does

Researches a topic across **5 pillars** and produces a structured report:

| Pillar | What it finds |
|--------|--------------|
| Scientific papers | Empirically validated approaches (arXiv, IEEE, ACM) |
| International standards | Normalized specs (ISO, RFC, NIST, W3C, OMG) |
| Industry reports | Real adoption data (Gartner, State of X, ThoughtWorks Radar) |
| Best practices | What works in production (engineering blogs, ADRs, patterns) |
| Expert opinions | Field consensus and active debates (HN, InfoQ, QCon) |

It also applies **planning-with-files** automatically — all findings are written to disk as you go, so nothing is lost in long research sessions.

## Output

After running, you'll have in your working directory:
- `sota_task_plan.md` — research phases and decisions
- `sota_findings.md` — organized findings per pillar
- `sota_progress.md` — session log
- `sota_report_[topic].md` — final 11-section synthesis report

---

## Usage examples

### Architecture decisions

```
/sota-research multi-tenant database isolation strategies
```
> Use before deciding between row-level security, schema-per-tenant, or database-per-tenant.

```
/sota-research event sourcing vs traditional CRUD for audit-heavy systems
```
> Use when designing a system that requires a full audit trail.

```
/sota-research API versioning strategies REST
```
> Use before designing your first versioned API endpoint.

---

### Modeling and data design

```
/sota-research state machine modeling for multi-step business workflows
```
> Use when designing approval flows, onboarding funnels, or legal procedures with multiple stages.

```
/sota-research legal document data models ontologies
```
> Use before designing schemas for legal acts, judgments, or regulatory documents.

```
/sota-research knowledge graph vs relational database for legal entities
```
> Use when choosing between graph and relational storage for interconnected legal data.

---

### AI and search

```
/sota-research semantic search in legal documents
```
> Use before building a vector search system on legal corpora.

```
/sota-research RAG hallucination mitigation techniques 2024
```
> Use before tuning a Retrieval-Augmented Generation pipeline.

```
/sota-research LLM agent orchestration patterns
```
> Use before designing a multi-agent system architecture.

---

### Infrastructure and SaaS patterns

```
/sota-research background job queue architectures NestJS
```
> Use when choosing between Bull, BullMQ, or other queue systems.

```
/sota-research SaaS subscription billing architecture patterns
```
> Use before integrating a payment provider into a multi-plan product.

```
/sota-research full-text search engines comparison Elasticsearch MeiliSearch Typesense
```
> Use when choosing a search backend for a document-heavy application.

---

### Process and methodology

```
/sota-research legal case management systems UX patterns
```
> Use before designing a case manager feature for lawyers or legal teams.

```
/sota-research BPMN vs custom state machines for legal procedure modeling
```
> Use when deciding how to represent administrative procedures in code.

```
/sota-research user onboarding activation patterns SaaS 2024
```
> Use before designing an onboarding flow for a new product.

---

## Tips

- **Be specific**: `/sota-research semantic search legal documents Spanish` beats `/sota-research search`.
- **Include your constraint**: `/sota-research background jobs NestJS small team` gives more transferable results than a generic search.
- **Use it before, not after**: The point is to inform a decision, not to validate one you already made.
- **The report is reusable**: `sota_report_[topic].md` can be attached to an ADR, shared with the team, or used as input to a `/planning-with-files` session.
