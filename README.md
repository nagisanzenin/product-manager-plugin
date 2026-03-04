# Product Manager Plugin for Claude Code

AI Product Manager that interviews stakeholders, writes BRDs/PRDs, and autonomously verifies engineering implementation against business requirements.

## What it does

- **Interviews you as CEO** — 3-5 focused questions to nail down requirements
- **Writes BRD/PRD docs** — Creates a `BRD/` folder in your project with structured requirement docs
- **Researches the domain** — Uses web search when the domain is unfamiliar
- **Verifies implementation** — Autonomously spawns agents to check code against acceptance criteria
- **Tracks multiple features** — Each feature gets its own doc, all tracked via `BRD/INDEX.md`

## Installation

### Option 1: Load directly (for testing)

```bash
claude --plugin-dir /path/to/product-manager-plugin
```

### Option 2: Install from marketplace

If published to a marketplace:

```bash
claude plugin install product-manager@your-marketplace
```

## Usage

The skill triggers automatically when you describe a new feature or business requirement:

```
> I want to add a payment system to my SaaS app
> We need user authentication with SSO
> New feature: export reports to PDF
```

Or invoke directly:

```
/product-manager:product-manager
```

## Workflow

1. **Interview** — Quick focused questions to understand the feature
2. **Research** — Online research if domain is unfamiliar
3. **Write BRD** — Structured doc with acceptance criteria and business rules
4. **Approve** — CEO reviews and approves the BRD
5. **Verify** — Autonomous agents check implementation against BRD

## Output

Creates in your project root:

```
BRD/
  INDEX.md                       # Living table of contents
  2026-03-04-feature-name.md     # One doc per feature
```

## License

MIT
