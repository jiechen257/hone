# Hone

Hone is a Codex Desktop-first skill for maintaining a local agent harness. It helps discover frontier AI coding practices, turn them into reusable local agent assets, apply changes behind an explicit write boundary, and audit Codex / Claude skill, rule, hook, and MCP drift.

## What It Does

Hone routes a single conversational entrypoint through four internal stages:

```text
discover -> shape -> apply -> check
```

- `discover`: scan recent public signals and shortlist useful ideas.
- `shape`: turn a selected signal into a practical local agent practice brief.
- `apply`: draft skills, rules, hooks, or MCP config changes before any real write.
- `check`: inspect high-value local harness entrypoints for drift, duplication, or stale behavior.

## Install

Clone the repository, then link it into your Codex skills directory:

```bash
git clone https://github.com/jiechen257/hone.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/hone" ~/.codex/skills/hone
```

For Claude Code, link the same checkout into `~/.claude/skills/hone` if desired.

## Files

```text
hone/
├── SKILL.md
├── references/
│   ├── apply.md
│   ├── check.md
│   ├── discover.md
│   ├── output-formats.md
│   ├── safety-boundaries.md
│   └── shape.md
└── templates/
    ├── check-report.md
    ├── hook-draft.md
    ├── mcp-config-draft.md
    ├── practice-brief.md
    ├── rule-draft.md
    └── skill-draft.md
```

## Safety Model

Hone defaults to read-only inspection and draft-first writes:

```text
Draft -> Stage -> Apply
```

Real writes require explicit confirmation. Draft artifacts are written under `~/work-pro/agent-space/hone/asset-drafts/` by default.

## License

MIT
