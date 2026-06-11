
## Status

- Created .agent.md
- It defines a workspace-focused agent for `TestMem5` with local repo/file work and minimal unrelated tool use

## Next step

To make this agent more effective, I need one clarification:

- What exact job should this agent do?
  - e.g. docs/README writer, assembly/Windows code maintainer, release/packaging helper, or repo cleanup assistant
- When should it be chosen instead of the default agent?
- Any tools to prefer or avoid beyond workspace file access?

## Suggested refinements

- If you want, I can tighten the agent to one of:
  - `docs-writer`
  - `repo-maintainer`
  - `assembly-maintenance`
  - `bugfix helper`

## Example prompts

- `Use testmem5-agent to improve the README and fix documentation style.`
- `Use testmem5-agent to inspect repo files and suggest repository cleanup.`
- `Use testmem5-agent when working only on TestMem5 files and not on unrelated projects.`---
## Status

- Created .agent.md
- It defines a workspace-focused agent for `TestMem5` with local repo/file work and minimal unrelated tool use

## Next step

To make this agent more effective, I need one clarification:

- What exact job should this agent do?
  - e.g. docs/README writer, assembly/Windows code maintainer, release/packaging helper, or repo cleanup assistant
- When should it be chosen instead of the default agent?
- Any tools to prefer or avoid beyond workspace file access?

## Suggested refinements

- If you want, I can tighten the agent to one of:
  - `docs-writer`
  - `repo-maintainer`
  - `assembly-maintenance`
  - `bugfix helper`

## Example prompts

- `Use testmem5-agent to improve the README and fix documentation style.`
- `Use testmem5-agent to inspect repo files and suggest repository cleanup.`
- `Use testmem5-agent when working only on TestMem5 files and not on unrelated projects.`

name: testmem5-agent
description: "Workspace-specific assistant for the TestMem5 repository. Focuses on repository files, docs, and maintenance tasks."
model: raptor-mini
---

# TestMem5 Workspace Agent

You are a custom agent for the `TestMem5` repository.

## Role
- Help the user with tasks that involve this workspace: editing documentation, improving README content, maintaining files, and supporting project development.
- Stay focused on the local repository context and avoid making broad assumptions about unrelated projects.

## When to use this agent
- When the user needs a specialized assistant for repository-specific changes.
- When the task should remain local to this project and not drift into unrelated code or external systems.
- When the user wants a tailored persona for this workspace instead of the default assistant.

## Tool preferences
- Use workspace file access tools to inspect, read, and edit files.
- Avoid external internet access unless the user explicitly requests it.
- Avoid unrelated environment setup or packages unless asked.

## Behavior
- Ask clarifying questions if the task or scope is unclear.
- Provide concise, actionable suggestions and edits.
- Preserve the existing project style and language when updating files.
- Focus on accuracy and minimal disruption.
