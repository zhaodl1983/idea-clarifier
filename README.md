# Idea Clarifier

`idea-clarifier` 是一个用于产品立项前澄清的 Agent Skill。

当用户只有模糊的产品想法、功能概念、创业方向，或在需求尚未想清楚时就要求生成 PRD，可以使用这个 Skill。它会先后通过两个门禁审查想法：

1. 资深产品经理视角：审查用户、问题、价值、MVP、核心链路和成功指标。
2. 投资人视角：审查市场、商业模式、增长路径、竞争、投入产出比和终止条件。

它可以产出门禁判断、PRD 和低保真 ASCII 逻辑线框图。它不负责高保真 UI、品牌视觉、组件库或生产代码。

## 安装

把本仓库复制到任何兼容 Agent Skills 标准的 skills 目录：

```bash
git clone https://github.com/zhaodl1983/idea-clarifier.git idea-clarifier
```

Codex 本地使用示例：

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/zhaodl1983/idea-clarifier.git ~/.codex/skills/idea-clarifier
```

## 使用方法

显式调用：

```text
使用 $idea-clarifier，在写 PRD 前先拷问并澄清我的产品想法。
```

中文示例：

```text
我想做一个 AI 工具，帮职场人提升效率。请先拷问我的想法，不要直接写 PRD。
```

## 工作流

```text
阶段 0：想法输入
阶段 1：产品经理追问
阶段 2：产品门禁
阶段 3：投资人追问
阶段 4：投资门禁
阶段 5：PRD 交付
阶段 6：逻辑线框图
```

门禁规则：

- 产品门禁必须达到 `有条件通过` 或 `通过`，才能进入投资人审查。
- 投资门禁必须达到 `观察` 或 `可小额试投`，才能进入 PRD 交付。
- 即使商业背景已经充分，也必须先输出阶段 3，再进入阶段 4。

## 目录结构

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

## 标准兼容性

本 Skill 遵循 Agent Skills 标准：

- `SKILL.md` 包含必需的 YAML frontmatter。
- `name` 与目录名、仓库名一致：`idea-clarifier`。
- `description` 保持简洁，并聚焦触发场景。
- 详细流程、评分规则和模板通过 `references/` 与 `assets/` 渐进加载。
- 测试样例存放在 `evals/`。

## 版本规则

当前版本：`v0.1`。

后续每次迭代只增加 `0.1`：`v0.2`、`v0.3`，依此类推。
