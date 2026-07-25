# Agent Tool Orchestration Skill

A reusable skill for designing reliable, context-efficient agent workflows across memory, files, code execution, web research, external connectors, structured input, and interactive outputs.

## What it provides

- An `inspect → plan → execute → verify → present` operating loop
- Layered working, conversation, and persistent memory
- Progressive loading of skills, schemas, and references
- Dynamic connector discovery
- Read-modify-verify patterns for stateful resources
- Confirmation gates for consequential actions
- Context-budget and failure-recovery guidance
- Prompt-injection boundaries for external content
- Tool and output selection matrices
- Seven end-to-end workflow examples

## Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── architecture-patterns.md
│   └── tool-selection-matrix.md
└── examples/
    └── workflows.md
```

## Usage

Install or load the skill in a compatible agent environment, then invoke it for tasks that require several tools, durable state, external actions, or careful verification.

Example:

```text
Use $agent-tool-orchestration to design a workflow that reads support tickets,
updates a project tracker, drafts customer replies, and verifies every write.
```

## License

MIT
