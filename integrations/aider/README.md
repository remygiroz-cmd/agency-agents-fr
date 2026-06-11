# Intégration Aider

L'ensemble du roster de The Agency est regroupé dans un seul fichier `CONVENTIONS.md`.
Aider lit ce fichier automatiquement lorsqu'il est présent à la racine de votre projet.

## Installation

```bash
# Run from your project root
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

## Activer un agent

Dans votre session Aider, référencez l'agent par son nom :

```
Use the Frontend Developer agent to refactor this component.
```

```
Apply the Reality Checker agent to verify this is production-ready.
```

## Utilisation manuelle

Vous pouvez aussi passer le fichier de conventions directement :

```bash
aider --read CONVENTIONS.md
```

## Régénérer

```bash
./scripts/convert.sh --tool aider
```
