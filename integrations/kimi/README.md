# Intégration Kimi Code CLI

Convertit tous les agents de The Agency en spécifications d'agent Kimi Code CLI. Chaque agent
devient un répertoire contenant `agent.yaml` (spécification de l'agent) et `system.md` (system
prompt).

## Installation

### Prérequis

- [Kimi Code CLI](https://github.com/MoonshotAI/kimi-cli) installé

### Installer

```bash
# Generate integration files (required on fresh clone)
./scripts/convert.sh --tool kimi

# Install agents
./scripts/install.sh --tool kimi
```

Cela copie les agents vers `~/.config/kimi/agents/`.

## Utilisation

### Activer un agent

Utilisez l'option `--agent-file` pour charger un agent spécifique :

```bash
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml
```

### Dans un projet

```bash
cd /your/project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project \
     "Review this React component for performance issues"
```

### Lister les agents installés

```bash
ls ~/.config/kimi/agents/
```

## Structure d'un agent

Chaque répertoire d'agent contient :

```
~/.config/kimi/agents/frontend-developer/
├── agent.yaml    # Agent specification (tools, subagents)
└── system.md     # System prompt with personality and instructions
```

### Format de agent.yaml

```yaml
version: 1
agent:
  name: frontend-developer
  extend: default  # Inherits from Kimi's built-in default agent
  system_prompt_path: ./system.md
  tools:
    - "kimi_cli.tools.shell:Shell"
    - "kimi_cli.tools.file:ReadFile"
    # ... all default tools
```

## Régénérer

Après avoir modifié des agents source :

```bash
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

## Dépannage

### Fichier d'agent introuvable

Assurez-vous d'avoir lancé `convert.sh` avant `install.sh` :

```bash
./scripts/convert.sh --tool kimi
```

### Kimi CLI non détecté

Assurez-vous que `kimi` est dans votre PATH :

```bash
which kimi
kimi --version
```

### YAML invalide

Validez les fichiers générés :

```bash
python3 -c "import yaml; yaml.safe_load(open('integrations/kimi/frontend-developer/agent.yaml'))"
```
