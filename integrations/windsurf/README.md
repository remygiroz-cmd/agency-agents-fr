# Intégration Windsurf

L'ensemble du roster de The Agency est regroupé dans un seul fichier `.windsurfrules`.
Les règles sont **à portée projet** — installez-les depuis la racine de votre projet.

## Installation

```bash
# Run from your project root
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

## Activer un agent

Dans Windsurf, référencez un agent par son nom dans votre prompt :

```
Use the Frontend Developer agent to build this component.
```

## Régénérer

```bash
./scripts/convert.sh --tool windsurf
```
