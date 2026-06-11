# Intégration Claude Code

The Agency a été conçu pour Claude Code. Aucune conversion nécessaire — les agents fonctionnent
nativement avec le format `.md` + frontmatter YAML existant.

## Installation

```bash
# Copy all agents to your Claude Code agents directory
./scripts/install.sh --tool claude-code

# Or manually copy a category
cp engineering/*.md ~/.claude/agents/
```

## Activer un agent

Dans n'importe quelle session Claude Code, référencez un agent par son nom :

```
Activate Frontend Developer and help me build a React component.
```

```
Use the Reality Checker agent to verify this feature is production-ready.
```

## Répertoire des agents

Les agents sont organisés en divisions. Voir le [README principal](../../README.md) pour
le roster complet de The Agency.
