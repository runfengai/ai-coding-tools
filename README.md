# AI Coding Tools

精选 AI 编程工具集合，提升开发效率。

[English](README.en.md)

## 工具目录

### AI 框架（AI Frameworks）

用于 AI agent 优化与增强的框架和系统。

| 工具                                                                    | 描述                                                                                                            | Stars |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| [everything-claude-code](tools/ai-frameworks/everything-claude-code/) | 面向 AI agent harness（Claude Code、Codex、Cursor 等）的性能优化系统，涵盖 skills、memory、安全扫描、MCP 配置。Anthropic Hackathon 获奖项目。 | 50K+  |
| [superpowers](tools/ai-frameworks/superpowers/)                       | AI agent 执行流程引擎，支持多阶段任务管理（brainstorm → plan → execute），可与 Spec Kit、Everything-claude-code 配合使用。               | 40K+  |

### 规范驱动开发（Spec-Driven Development）

先定义规范再实现，减少返工，提升 AI 编码质量。

| 工具                                      | 描述                                                                                     | Stars |
| --------------------------------------- | -------------------------------------------------------------------------------------- | ----- |
| [spec-kit](tools/spec-driven/spec-kit/) | GitHub 出品的规范驱动开发工具集，通过 Specify CLI 将 spec 变为可执行驱动，支持 Copilot、Claude Code 等主流 AI agent。 | 83K+  |

### 代码补全（Code Completion）

AI 驱动的代码补全工具。

| 工具                                        | 描述                                    |
| ----------------------------------------- | ------------------------------------- |
| [tabnine](tools/code-completion/tabnine/) | AI 驱动的跨语言代码补全工具，支持多编辑器插件，帮助开发者提高编写效率。 |

# Superpowers 与 Spec Kit 工作流分析

## 结论

* 有重叠，但不冲突
* 可以一起使用，但需要分清主次
* 组合使用能最大化效率

## 工具本质区别

### Superpowers

* 偏“执行流程引擎”
* 阶段：brainstorm → plan → execute
* 强调推进任务
* 类比：项目经理 + 执行官
* 可作为主工作流管理工具，与 Spec Kit、Everything-claude-code 配合使用

### Spec Kit

* 偏“规范驱动开发”
* 先写 spec（需求/接口/约束）再实现
* 强调定义清楚再行动
* 类比：架构师 / 设计文档体系
* 可作为前置规范定义，减少返工

## 重叠点

| 阶段 | Superpowers | Spec Kit          |
| -- | ----------- | ----------------- |
| 需求 | brainstorm  | clarify / analyze |
| 设计 | plan        | spec / design     |
| 实现 | execute     | implement         |

## 核心区别

* Superpowers = 控制“怎么做”
* Spec Kit = 定义“做什么”

## 正确组合方式

### Step 1：用 Spec Kit 定义清楚

* speckit.analyze
* speckit.clarify
* speckit.design

输出：需求边界、数据结构、API、约束

### Step 2：交给 Superpowers 执行

* /brainstorm（可选补充）
* /plan（拆任务）
* /execute（实现）

### Step 3：辅助 Everything-claude-code

* prompt / debug / review 能力
* 性能扫描和 MCP 配置

## 类比

* Spec Kit = 📐 施工图纸
* Superpowers = 👷 施工队
* Everything-claude-code = 🛠️ 高级工具箱

## 错误用法

1. 两个都当主流程 → 上下文混乱
2. Spec Kit 写一半就开干 → 返工多
3. 全量导入 Everything-claude-code → 规则冲突，AI 上下文污染

## 最优实践

* Spec Kit（强约束）

  * 定义接口 / 数据 / 边界
* Superpowers（执行）

  * 拆任务 + 推进实现
* Everything-claude-code（辅助）

  * 提供 prompt / debug / review 能力
  * 按需挑选功能模块，避免全量加载

## 进阶建议

可以将三者融合成一个完整命令习惯：

```text
/feature start
→ 自动走：
  speckit.analyze
  speckit.clarify
  speckit.design
  superpowers.plan
  superpowers.execute
  everything-claude-code.debug
```

* 形成完整 workflow
* 提升移动端开发效率
* 支持模块化选择，兼顾灵活性与稳定性

## 贡献

欢迎提交 PR 添加更多有用的 AI 编程工具或优化工作流配置！
