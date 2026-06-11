# Intégration Gemini CLI

Packagent tous les agents de The Agency sous forme de subagents Gemini CLI. Ces agents
s'installent dans `~/.gemini/agents/`.

## Installation

```bash
# Generate the Gemini CLI agent files first
./scripts/convert.sh --tool gemini-cli

# Then install them to ~/.gemini/agents/
./scripts/install.sh --tool gemini-cli
```

## Utiliser un agent

Dans Gemini CLI, référencez un agent par son nom dans votre prompt :

```
Use the frontend-developer agent to help me build this UI.
```

Ou invoquez l'agent directement si votre version de Gemini CLI le prend en charge :

```bash
gemini --agent frontend-developer "How should I structure this React component?"
```

## Structure

```
~/.gemini/agents/
  frontend-developer.md
  backend-architect.md
  reality-checker.md
  ...
```

## Régénérer

```bash
./scripts/convert.sh --tool gemini-cli
```
