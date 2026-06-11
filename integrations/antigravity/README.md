# Intégration Antigravity

Installe l'ensemble du roster de The Agency sous forme de skills Antigravity. Chaque agent est préfixé
par `agency-` pour éviter les conflits avec les skills existants.

## Installation

```bash
./scripts/install.sh --tool antigravity
```

Cela copie les fichiers depuis `integrations/antigravity/` vers
`~/.gemini/antigravity/skills/`.

## Activer un skill

Dans Antigravity, activez un agent par son slug :

```
Use the agency-frontend-developer skill to review this component.
```

Les slugs disponibles suivent le motif `agency-<agent-name>`, par exemple :
- `agency-frontend-developer`
- `agency-backend-architect`
- `agency-reality-checker`
- `agency-growth-hacker`

## Régénérer

Après avoir modifié des agents, régénérez les fichiers de skill :

```bash
./scripts/convert.sh --tool antigravity
```

## Format de fichier

Chaque skill est un fichier `SKILL.md` avec un frontmatter compatible Antigravity :

```yaml
---
name: agency-frontend-developer
description: Expert frontend developer specializing in...
risk: low
source: community
date_added: '2026-03-08'
---
```
