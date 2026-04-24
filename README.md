# ADR Skill

Architecture Decision Record management skill for AI coding agents. Compatible with Claude Code, Cursor, GitHub Copilot, and any agent supporting the [Agent Skills](https://agentskills.io) spec.

## What it does

Teaches AI agents to systematically create, maintain, and enforce Architecture Decision Records. Every significant architectural choice gets documented with context, alternatives considered, and consequences.

## What makes this different

Built on the ADR tradition but adds two patterns from modern agent skill design:

- **Anti-rationalization guards** -- a table of excuses AI agents use to skip documentation, with counterarguments. Prevents drift toward "I'll document it later" behavior.
- **Verification gates** -- four mandatory gates (Completeness, Evidence, Clarity, Consistency) that must pass before an ADR can be accepted. No vague claims, no missing alternatives, no hidden trade-offs.

## Install

### Claude Code (via skills CLI)

```bash
npx skills add Jvdbreemen/adr-skill
```

### Manual

Copy `SKILL.md` to your project's `.claude/skills/adr/SKILL.md` (Claude Code) or `.github/copilot-instructions.md` (Copilot).

## Usage

The skill activates automatically when:
- Making architectural changes
- Reviewing PRs for architectural compliance
- Choosing between technologies
- Refactoring that changes patterns

Or explicitly: "Create an ADR for choosing SQLite over PostgreSQL"

## ADR file structure

```
docs/adr/
  README.md                          # Index and navigation
  ADR-001-local-first-sqlite.md
  ADR-002-mcp-first-architecture.md
  ADR-003-tauri-desktop-shell.md
  ...
```

## Credits

Based on [Michael Nygard's ADR format](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions). Anti-rationalization pattern inspired by [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills). Verification gates inspired by [trailofbits/skills](https://github.com/trailofbits/skills).

## License

MIT
