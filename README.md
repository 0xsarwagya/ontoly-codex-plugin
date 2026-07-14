# Ontoly Codex Plugin

Ontoly is a TypeScript-native software intelligence engine that builds a deterministic Software Graph.

This Codex plugin teaches agents to use Ontoly graph evidence, CLI reports, MCP, and the official Ontoly Agent Skills before falling back to broad repository search.

## What Is Included

- `.codex-plugin/plugin.json` declares the Codex plugin metadata.
- `skills/ontoly-software-graph/` teaches the graph-first workflow for architecture review, dependency analysis, impact analysis, request tracing, configuration analysis, security review, and codebase onboarding.
- The full Ontoly source and official task-specific skills live in [`0xsarwagya/ontoly`](https://github.com/0xsarwagya/ontoly).

## Install Official Ontoly Skills

```bash
npx skills add 0xsarwagya/ontoly --list
npx skills add 0xsarwagya/ontoly --skill architecture-review
npx skills add 0xsarwagya/ontoly --skill impact-analysis
npx skills add 0xsarwagya/ontoly --skill request-tracing
```

## Use Ontoly In A Repository

```bash
pnpm add -D @0xsarwagya/ontoly-cli
pnpm ontoly build .
pnpm ontoly stats .
pnpm ontoly mcp
```

## Validation

```bash
python3 /Users/shrey/.codex/skills/.system/plugin-creator/scripts/validate_plugin.py .
python3 /Users/shrey/.codex/skills/.system/skill-creator/scripts/quick_validate.py skills/ontoly-software-graph
plugin-scanner scan . --format text
```
