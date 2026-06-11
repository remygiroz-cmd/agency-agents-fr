# Intégration Codex

Convertit tous les agents de The Agency en fichiers TOML d'agent personnalisé Codex. Chaque agent
source devient un fichier `.toml` autonome contenant les champs minimaux requis par Codex :
`name`, `description` et `developer_instructions`.

## Installation

### Prérequis

- [Codex](https://developers.openai.com/codex/overview) installé

### Convertir et installer

```bash
# Generate integration files (required on fresh clone)
./scripts/convert.sh --tool codex

# Install agents
./scripts/install.sh --tool codex
```

Cela copie les fichiers d'agent générés vers `~/.codex/agents/`.

## Format généré

Chaque fichier généré se trouve dans :

```text
integrations/codex/agents/<slug>.toml
```

Le mapping est volontairement minimal :

- `name` est copié depuis le frontmatter source sans modification
- `description` est copié depuis le frontmatter source sans modification
- `developer_instructions` contient l'intégralité du corps Markdown sans modification

Les métadonnées propres à la source telles que `color`, `emoji`, `vibe` et d'autres champs de
frontmatter non pris en charge sont omises.

## Utilisation

Après installation, référencez l'agent personnalisé par son nom dans Codex :

```text
Use the Frontend Developer agent to review this component.
```

Codex utilise le champ `name` à l'intérieur du fichier TOML comme source de vérité, de sorte que le
slug du nom de fichier généré ne sert qu'à la sécurité du système de fichiers.

## Régénérer

Après avoir modifié des agents source :

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

## Dépannage

### Intégration Codex introuvable

Générez les artefacts Codex avant l'installation :

```bash
./scripts/convert.sh --tool codex
```

### Codex non détecté

Assurez-vous que `codex` est dans votre PATH, ou que `~/.codex/` existe déjà :

```bash
which codex
codex --help
```
