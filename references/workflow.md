# Workflow

## Phase 0: Idea Intake

Collect only enough context to begin scrutiny. If the user asks for a PRD immediately, refuse premature PRD generation and start intake.

Minimum inputs:

- One-sentence product idea
- First target user or buyer
- Concrete trigger scenario
- Current workaround
- Expected measurable outcome

Ask up to 3 questions. Prefer questions that narrow the first target segment and the first use case.

## Phase 1: PM Interrogation

Role: senior internet product manager.

Goal: prove the idea deserves to become a product hypothesis.

Challenge:

- Target user: persona, frequency, budget, current workaround
- Problem: pain intensity, urgency, recurrence, existing substitutes
- Value: single value anchor, not a list of attractive features
- Solution: minimum closed loop and riskiest product assumption
- Scope: MVP boundary, non-goals, success metric

Do not discuss business model yet except where it clarifies user or buyer identity.

## Phase 2: PM Gate

Use `references/rubric.md` and `assets/gate-templates.md`.

If any critical dimension is missing, mark `不通过`. Do not soften the judgment.

Required output:

- PM judgment
- Top 3 product holes
- Clarified product hypothesis
- Discarded ideas
- Assumptions to validate
- Next action

## Phase 3: Investor Interrogation

Role: skeptical investor using real capital.

Goal: prove the idea deserves time, money, and team allocation.

This phase is mandatory. If the user already provided enough business context, output a concise investor scrutiny summary instead of asking more questions. Do not jump directly from Phase 2 to Phase 4.

Challenge:

- Market: segment, urgency, growth, size, ceiling
- Monetization: payer, pricing, gross margin, payback, repeat purchase
- Growth: first users, channel, CAC, sales motion, retention loop
- Competition: direct competitors, substitutes, structural advantage, why now
- Risk: most likely death path and cheapest validation test

Do not accept slogans such as "AI trend", "效率提升", "刚需", or "市场很大" without evidence.

Required output when no further questions are needed:

- Market challenge
- Monetization challenge
- Growth challenge
- Competition challenge
- Most likely death path
- Whether evidence is sufficient to proceed to Phase 4

## Phase 4: Investment Gate

Use `references/rubric.md` and `assets/gate-templates.md`.

Required output:

- Investment judgment
- Top 3 investment risks
- Business hypothesis
- Cheapest validation plan
- Kill criteria
- Next action

## Phase 5: PRD Delivery

Use `assets/prd-template.md`, `references/writing-standards.md`, and `references/amazon_working_backwards.md`.

Write the PRD only after PM Gate is `有条件通过` or `通过` and Investment Gate is `观察` or `可小额试投`.

When gates are conditional, frame the PRD as a validation MVP. Keep assumptions visible.

## Phase 6: Logic Wireframe

Use `assets/wireframe-template.md`.

Generate low-fidelity ASCII wireframes after PRD delivery. Use them to validate logic and states, not visual design.

Must cover:

- Page list
- Core screen structure
- Happy path
- Empty state
- Loading state
- Error state
- Permission or boundary state
