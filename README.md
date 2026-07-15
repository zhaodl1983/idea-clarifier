# Idea Clarifier

`idea-clarifier` is an Agent Skill for ruthless pre-launch product clarification.

Use it when a user has a vague product idea, feature concept, startup direction, or premature PRD request. The skill forces the idea through two gates before documentation:

1. Senior product manager scrutiny: user, problem, value, MVP, core flow, success metric.
2. Skeptical investor scrutiny: market, monetization, growth, competition, ROI, kill criteria.

It produces gate judgments, a PRD, and low-fidelity ASCII logic wireframes. It does not produce high-fidelity UI, brand design, component libraries, or production code.

## Install

Copy this repository into any Agent Skills-compatible skills directory:

```bash
git clone https://github.com/zhaodl1983/idea-clarifier.git idea-clarifier
```

For Codex-style local usage:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/zhaodl1983/idea-clarifier.git ~/.codex/skills/idea-clarifier
```

## Usage

Invoke the skill explicitly:

```text
Use $idea-clarifier to challenge my product idea before writing a PRD.
```

Example prompt:

```text
我想做一个 AI 工具，帮职场人提升效率。请先拷问我的想法，不要直接写 PRD。
```

## Workflow

```text
Phase 0: Idea Intake
Phase 1: PM Interrogation
Phase 2: PM Gate
Phase 3: Investor Interrogation
Phase 4: Investment Gate
Phase 5: PRD Delivery
Phase 6: Logic Wireframe
```

Gate rules:

- PM Gate must be `有条件通过` or `通过` before investor scrutiny.
- Investment Gate must be `观察` or `可小额试投` before PRD delivery.
- Phase 3 must always appear before Phase 4, even when business context is already sufficient.

## Structure

```text
idea-clarifier/
├── SKILL.md
├── assets/
│   ├── gate-templates.md
│   ├── prd-template.md
│   └── wireframe-template.md
├── evals/
│   ├── evals.json
│   └── trigger-queries.json
└── references/
    ├── amazon_working_backwards.md
    ├── rubric.md
    ├── workflow.md
    └── writing-standards.md
```

## Validation

The skill follows the Agent Skills standard:

- `SKILL.md` contains required YAML frontmatter.
- `name` equals the directory/repository name: `idea-clarifier`.
- The description is concise and trigger-focused.
- Detailed workflow, rubrics, and templates are loaded progressively from `references/` and `assets/`.
- Eval cases are stored in `evals/`.

## Versioning

Current version: `v0.1`.

Future iterations increase by `0.1`: `v0.2`, `v0.3`, and so on.
