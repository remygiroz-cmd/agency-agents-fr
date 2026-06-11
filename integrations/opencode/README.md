# Intégration OpenCode

Les agents OpenCode sont des fichiers `.md` avec frontmatter YAML stockés dans
`.opencode/agents/`. Le convertisseur fait correspondre les couleurs nommées à des codes hexadécimaux et ajoute
`mode: subagent` afin que les agents soient invoqués à la demande via `@agent-name` plutôt
que d'encombrer le sélecteur d'agent principal.

## Installation

```bash
# Run from your project root
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

Cela crée des fichiers `.opencode/agents/<slug>.md` dans le répertoire de votre projet.

## Activer un agent

Dans OpenCode, invoquez un subagent avec le préfixe `@` :

```
@frontend-developer help build this component.
```

```
@reality-checker review this PR.
```

Vous pouvez aussi sélectionner des agents depuis le sélecteur d'agent de l'interface OpenCode.

## Format d'un agent

Chaque fichier d'agent généré contient :

```yaml
---
name: Frontend Developer
description: Expert frontend developer specializing in modern web technologies...
mode: subagent
color: "#00FFFF"
---
```

- **mode: subagent** — l'agent est disponible à la demande, non affiché dans la liste principale parcourue avec Tab
- **color** — code hexadécimal (les couleurs nommées des fichiers source sont converties automatiquement)

## Projet vs global

Les agents dans `.opencode/agents/` sont **à portée projet**. Pour les rendre disponibles
globalement dans tous les projets, générez d'abord les fichiers d'agent, puis installez
avec `--path` :

```bash
./scripts/convert.sh --tool opencode
./scripts/install.sh --tool opencode --path ~/.config/opencode/agents
```

## Régénérer

```bash
./scripts/convert.sh --tool opencode
```
