# Clarify Before Action

一个面向 Codex 的通用需求澄清 Skill：在执行任何任务前先消除关键歧义、复述完整理解，并等待用户明确确认。

## 工作方式

- 存在关键歧义：先提出简洁、必要的问题，不提前开始任务。
- 需求已经明确：不提出多余问题，但仍会复述目标、范围和关键约束。
- 所有任务：在复述理解后等待用户明确确认，再开始执行。
- 执行阶段：Codex 自主选择方案、工具和实现细节，不限制模型发挥。
- 范围发生变化或出现新的关键歧义：暂停执行，重新澄清、复述并等待确认。

## 安装

将仓库克隆到 Codex 的 Skills 目录：

```bash
git clone https://github.com/yufengxie08-pixel/clarify-before-action.git ~/.codex/skills/clarify-before-action
```

重新打开 Codex 任务，使 Skill 列表刷新。

## 使用

Skill 已启用隐式调用，会自动参与所有任务的执行前判断。也可以显式调用：

```text
Use $clarify-before-action to handle this request.
```

## 文件结构

```text
clarify-before-action/
├── README.md
├── SKILL.md
└── agents/
    └── openai.yaml
```

核心行为规则位于 `SKILL.md`；`agents/openai.yaml` 提供 Codex 界面信息并启用隐式调用。
