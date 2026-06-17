# Frontend UX Heuristics

A skill for designing, implementing, and reviewing frontend UI/UX against the 10 core usability heuristics. Compatible with any runtime that implements the [Agent Skills specification](https://agentskills.io/specification).

## What it does

Loads only the heuristic and context helpers relevant to the task and produces concrete, heuristic-tagged UI changes rather than vague principles. Covers forms, dashboards, search, interaction patterns, and complex applications.

## Install

The skill is a directory (`frontend-ux-heuristics/`) containing `SKILL.md` plus `references/`. The directory name must match the `name` field in `SKILL.md` (per the Agent Skills spec), so install by cloning, copying, or symlinking the directory under your agent's skills folder — keep the name as-is.

### Claude Code

Personal (available in every project):

```bash
git clone https://github.com/misiura-codes/frontend-ux-heuristics.git ~/.claude/skills/frontend-ux-heuristics
```

Per-project:

```bash
git clone https://github.com/misiura-codes/frontend-ux-heuristics.git <your-project>/.claude/skills/frontend-ux-heuristics
```

Restart the session. Claude Code auto-discovers the skill from `SKILL.md` frontmatter and invokes it via the `Skill` tool.

### Codex

```bash
git clone https://github.com/misiura-codes/frontend-ux-heuristics.git "${CODEX_HOME:-$HOME/.codex}/skills/frontend-ux-heuristics"
```

### Gemini CLI

Clone into your Gemini CLI skills path (check your version's docs for the exact location — typically under `~/.gemini/` or a project-local `.gemini/skills/`). Gemini activates skills via its `activate_skill` tool.

```bash
git clone https://github.com/misiura-codes/frontend-ux-heuristics.git ~/.gemini/skills/frontend-ux-heuristics
```

### Other runtimes

Any runtime implementing the [Agent Skills specification](https://agentskills.io/specification) reads the same `SKILL.md`. Clone the directory into that runtime's skills path.

### Updating

```bash
cd ~/.claude/skills/frontend-ux-heuristics  # or wherever you installed it
git pull
```

### Without git

If you'd rather not clone, download the directory as a zip and place it at the same path. The `cp -r frontend-ux-heuristics <skills-dir>/` form also works.

## Usage

The skill triggers naturally on frontend UI/UX work — design, review, forms, dashboards, error states, navigation. To invoke explicitly:

> "Use frontend-ux-heuristics to review this dashboard."

For implementation, the skill loads only the heuristic helpers relevant to the surface under review. For a full evaluation, ask for a "heuristic evaluation" and all H1–H10 helpers will be loaded.

## Layout

```
frontend-ux-heuristics/
├── agents/
│   └── openai.yaml
├── SKILL.md
├── README.md
└── references/
    ├── index.md
    ├── heuristics/      # H1–H10 helpers
    └── context/         # Forms, search, complex apps, interaction patterns
```

## Attribution

The 10 usability heuristic names and framework are credited to Jakob Nielsen:
[10 Usability Heuristics for User Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/).
This skill adds original agent-oriented review prompts and operational guidance; it is not affiliated with Nielsen Norman Group.
