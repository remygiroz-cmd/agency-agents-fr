# Intégration Qwen Code

Qwen Code utilise des fichiers SubAgent `.md` à portée projet dans `.qwen/agents/`.

Les fichiers générés proviennent de `scripts/convert.sh --tool qwen`, qui écrit un
fichier Markdown SubAgent par agent de l'agency dans `integrations/qwen/agents/`.

## Générer

Depuis la racine du dépôt :

```bash
./scripts/convert.sh --tool qwen
```

## Installation

Lancez l'installateur depuis la racine de votre projet cible :

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool qwen
```

Cela copie les fichiers SubAgent générés dans :

```text
.qwen/agents/
```

## Rafraîchir dans Qwen Code

Après installation :

- lancez `/agents manage` dans Qwen Code pour rafraîchir la liste des agents, ou
- redémarrez la session Qwen Code en cours

## Notes

- Qwen Code est à portée projet, pas à portée utilisateur (home)
- Les fichiers Qwen générés utilisent un frontmatter minimal : `name`, `description` et
  `tools` optionnel
- Si vous mettez à jour des agents dans ce dépôt, régénérez la sortie Qwen avant
  de réinstaller
