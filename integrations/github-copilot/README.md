# Intégration GitHub Copilot

The Agency fonctionne avec GitHub Copilot d'emblée. Aucune conversion nécessaire —
les agents utilisent le format `.md` + frontmatter YAML existant.

## Installation

```bash
# Copy all agents to your GitHub Copilot agents directories
./scripts/install.sh --tool copilot

# Or manually copy a category
cp engineering/*.md ~/.github/agents/
cp engineering/*.md ~/.copilot/agents/
```

## Activer un agent

Dans n'importe quelle session GitHub Copilot, référencez un agent par son nom :

```
Activate Frontend Developer and help me build a React component.
```

```
Use the Reality Checker agent to verify this feature is production-ready.
```

## Répertoire des agents

Les agents sont organisés en divisions. Voir le [README principal](../../README.md) pour
le roster actuel complet.
