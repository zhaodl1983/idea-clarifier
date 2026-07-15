# Gate Rubric

Use this rubric to make gate judgments. Do not average away fatal gaps.

## PM Gate Rubric

Score each dimension 0-2:

- Target user: 0 vague group, 1 segment named, 2 concrete persona with frequency and context
- Problem: 0 abstract pain, 1 plausible pain, 2 recurring urgent pain with current workaround
- Value: 0 feature-led, 1 benefit stated, 2 single measurable value anchor
- Core flow: 0 no flow, 1 partial flow, 2 complete input-to-output loop
- MVP scope: 0 broad platform, 1 reduced but bloated, 2 smallest validation loop
- Success metric: 0 none, 1 vanity metric, 2 behavior or business metric tied to value

Judgment:

- `不通过`: any dimension is 0, or total score < 8
- `有条件通过`: total score 8-10 with explicit assumptions
- `通过`: total score >= 11 and no dimension below 1

## Investment Gate Rubric

Score each dimension 0-2:

- Market: 0 hand-wavy, 1 plausible segment, 2 clear segment with growth or budget signal
- Payer: 0 unknown, 1 user and payer guessed, 2 payer named with buying trigger
- Pricing and ROI: 0 absent, 1 rough price, 2 value-to-price logic with payback view
- Acquisition: 0 "do marketing", 1 channel guessed, 2 first-channel path with CAC assumption
- Competition: 0 ignored, 1 named competitors, 2 substitutes plus structural advantage
- Risk test: 0 no test, 1 weak test, 2 cheap falsifiable test with kill criteria

Judgment:

- `不投`: any dimension is 0, or total score < 8
- `观察`: total score 8-10 with clear validation plan
- `可小额试投`: total score >= 11 and validation cost is limited

## Harshness Rules

- Call a vague user group "无法立项的人群定义".
- Call a feature list without pain "自嗨功能堆叠".
- Call market claims without payer or channel "投资叙事，不是商业假设".
- Call a PRD request before gates pass "过早文档化，会掩盖核心不确定性".
