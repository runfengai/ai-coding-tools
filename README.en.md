# AI Coding Tools

A curated collection of AI programming tools to boost development efficiency.

[中文](README.md)

## Tool Directory

### AI Frameworks

Frameworks and systems for optimizing and enhancing AI agents.

| Tool                                                                  | Description                                                                                                                                                                                              | Stars |
| --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| [everything-claude-code](tools/ai-frameworks/everything-claude-code/) | Performance optimization system for AI agent harnesses (Claude Code, Codex, Cursor, etc.), covering skills, memory, security scanning, and MCP configuration. Anthropic Hackathon award-winning project. | 50K+  |
| [superpowers](tools/ai-frameworks/superpowers/)                       | AI agent execution engine supporting multi-stage task management (brainstorm → plan → execute), compatible with Spec Kit and Everything-claude-code.                                                     | 40K+  |

### Spec-Driven Development

Define specifications before implementation to reduce rework and improve AI coding quality.

| Tool                                    | Description                                                                                                                                                  | Stars |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----- |
| [spec-kit](tools/spec-driven/spec-kit/) | GitHub's spec-driven development toolkit, converting specs into executable workflows via Specify CLI. Supports major AI agents like Copilot and Claude Code. | 83K+  |

### Code Completion

AI-driven code completion tools.

| Tool                                      | Description                                                                                                          |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| [tabnine](tools/code-completion/tabnine/) | AI-powered multi-language code completion tool, supporting various editor plugins, enhancing developer productivity. |

# Superpowers and Spec Kit Workflow Analysis

## Conclusion

* Some overlap, but not conflicting
* Can be used together with clear primary/secondary roles
* Combining them maximizes efficiency

## Core Differences

### Superpowers

* Execution workflow engine
* Stages: brainstorm → plan → execute
* Emphasizes task progression
* Analogy: project manager + executor
* Serves as main workflow management tool, integrates with Spec Kit and Everything-claude-code

### Spec Kit

* Spec-driven development approach
* Define specs (requirements/interfaces/constraints) before implementation
* Emphasizes clarity before action
* Analogy: architect / documentation system
* Serves as a pre-definition layer to reduce rework

## Overlap

| Stage          | Superpowers | Spec Kit          |
| -------------- | ----------- | ----------------- |
| Requirements   | brainstorm  | clarify / analyze |
| Design         | plan        | spec / design     |
| Implementation | execute     | implement         |

## Key Distinction

* Superpowers = controls "how to do it"
* Spec Kit = defines "what to do"

## Correct Combination

### Step 1: Define clearly with Spec Kit

* speckit.analyze
* speckit.clarify
* speckit.design

Output: requirement boundaries, data structures, APIs, constraints

### Step 2: Execute with Superpowers

* /brainstorm (optional supplement)
* /plan (task breakdown)
* /execute (implementation)

### Step 3: Support with Everything-claude-code

* Prompts, debugging, review capabilities
* Performance scanning and MCP configuration

## Analogy

* Spec Kit = 📐 blueprint
* Superpowers = 👷 construction team
* Everything-claude-code = 🛠️ advanced toolkit

## Common Mistakes

1. Treating both as main workflow → context confusion
2. Implementing before completing Spec Kit → lots of rework
3. Importing Everything-claude-code fully → rule conflicts and AI context pollution

## Best Practices

* Spec Kit (strict constraints)

  * Define interfaces / data / boundaries
* Superpowers (execution)

  * Break down tasks and drive implementation
* Everything-claude-code (support)

  * Provide prompt/debug/review capabilities
  * Select modules as needed to avoid full load

## Advanced Suggestions

Combine the three into a complete command habit:

```text
/feature start
→ Auto workflow:
  speckit.analyze
  speckit.clarify
  speckit.design
  superpowers.plan
  superpowers.execute
  everything-claude-code.debug
```

* Forms a complete workflow
* Improves mobile development efficiency
* Supports modular selection, balancing flexibility and stability

## Contribution

PRs welcome to add more useful AI programming tools or optimize workflow configur
