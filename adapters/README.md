# Adapters

Skills in [`skills/`](../skills/) are the **canonical** agent instructions for Plim Design. Adapters explain how to install or reference them in different agent environments without forking philosophy into tool-specific specs.

## Layout

| Path | Purpose |
| --- | --- |
| [generic/](generic/) | Environment-neutral usage (copy path, submodule, package) |
| [agents.md](agents.md) | Notes per agent product (add when verified) |

> TODO: Document verified adapter steps as tooling is tested.

## Rule

Adapters may **point to** repository content; they must not redefine design principles.
