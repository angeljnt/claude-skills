# claude-skills

Custom Claude Code skills by [@angeljnt](https://github.com/angeljnt).

## Available Skills

| Skill | Description |
|-------|-------------|
| [sota-research](sota-research/SKILL.md) | State of the Art research — synthesizes 5 pillars (scientific papers, standards, industry reports, best practices, expert opinions) with built-in file-based planning |

---

## How to Install

### Install a single skill

```bash
SKILL=sota-research
mkdir -p ~/.claude/skills/$SKILL
curl -L https://raw.githubusercontent.com/angeljnt/claude-skills/main/$SKILL/SKILL.md \
  > ~/.claude/skills/$SKILL/SKILL.md
```

### Update an existing skill

Same command — it overwrites with the latest version.

### Verify installation

Open any Claude Code session and run `/sota-research [topic]`.

---

## How to Use `sota-research`

```
/sota-research Legal Case Management Systems
/sota-research State machines for multi-step workflows
/sota-research Multi-tenant SaaS architecture patterns
/sota-research Semantic search in legal documents
```

The skill will automatically:
1. Create `sota_task_plan.md`, `sota_findings.md`, `sota_progress.md` in your working directory
2. Research across 5 pillars: scientific papers, standards, industry reports, best practices, expert opinions
3. Apply the 2-Action Rule — write findings to disk after every 2 searches
4. Produce a final `sota_report_[topic].md` with 11 sections including "Don't reinvent the wheel" resources
