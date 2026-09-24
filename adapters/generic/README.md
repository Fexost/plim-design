# Generic adapter

Use Plim skills from this repository without rewriting them.

## Recommended approach

1. Clone or submodule `plim-design` into a stable path in your environment.
2. Point the agent at root [AGENTS.md](../../AGENTS.md) for orientation.
3. Enable individual skills from [`skills/`](../../skills/) as your agent supports (project skills directory, personal skills directory, or explicit `@` references).

## Canonical sources

| Need | Path |
| --- | --- |
| Philosophy | [`philosophy/philosophy.md`](../../philosophy/philosophy.md) |
| Core skill | [`skills/plim-design/SKILL.md`](../../skills/plim-design/SKILL.md) |
| Workflows | [`recipes/`](../../recipes/) |

> TODO: Add packaging or install script if the project later publishes a distributable skill bundle.

Do not duplicate skill bodies into adapter files—link to `skills/*/SKILL.md` instead.
