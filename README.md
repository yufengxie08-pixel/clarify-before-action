# Clarify Before Action

一个面向 Codex 的通用需求澄清 Skill：明确的任务直接执行；只有存在会实质影响结果的歧义时，才先向用户提问，澄清后复述理解并等待确认。

## 工作方式

- 需求明确：立即执行，不机械复述，也不要求形式化确认。
- 存在关键歧义：先提出简洁、必要的问题，不提前开始任务。
- 歧义解决：复述已确认的目标、范围和关键约束，等待用户明确确认。
- 确认时附带明确且不冲突的新要求：直接纳入执行，不重复触发确认流程。
- 执行阶段：Codex 自主选择方案、工具和实现细节，不限制模型发挥。

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
