# Intégration Cursor

Convertit l'ensemble du roster de The Agency en fichiers de règles `.mdc` Cursor. Les règles sont
**à portée projet** — installez-les depuis la racine de votre projet.

## Installation

```bash
# Run from your project root
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

Cela crée des fichiers `.cursor/rules/<agent-slug>.mdc` dans votre projet.

## Activer une règle

Dans Cursor, référencez un agent dans votre prompt :

```
@frontend-developer Review this React component for performance issues.
```

Ou activez une règle en mode toujours actif en modifiant son frontmatter :

```yaml
---
description: Expert frontend developer...
globs: "**/*.tsx,**/*.ts"
alwaysApply: true
---
```

## Régénérer

```bash
./scripts/convert.sh --tool cursor
```
