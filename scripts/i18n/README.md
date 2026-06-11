# 🇨🇳 Localisation en chinois (zh-CN)

Localise les champs `name` et `description` des agents (dans le frontmatter YAML) en chinois simplifié. Cela rend les noms d'agents lisibles dans le sélecteur d'agent de Copilot Chat pour les utilisateurs sinophones.

## Fichiers

| Fichier | Description |
|------|-------------|
| `agent-names-zh.json` | Correspondance entre noms d'agents anglais → traductions chinoises (130+ entrées) |
| `localize-agents-zh.ps1` | Script PowerShell qui lit le JSON et met à jour les fichiers d'agent installés |

## Utilisation

Après avoir installé les agents avec `install.sh --tool copilot` :

```powershell
# Localize agent names to Chinese
powershell -ExecutionPolicy Bypass -File scripts/i18n/localize-agents-zh.ps1
```

Par défaut, le script traite :
- `%USERPROFILE%\.github\agents\`
- `%USERPROFILE%\.copilot\agents\`

Passez des chemins personnalisés si nécessaire :

```powershell
powershell -File scripts/i18n/localize-agents-zh.ps1 -TargetDirs @("C:\custom\path\agents")
```

## Fonctionnement

1. Lit `agent-names-zh.json` (encodé en UTF-8) pour obtenir la table de traduction
2. Pour chaque fichier `.md` des répertoires cibles :
   - Extrait le champ `name:` du frontmatter YAML
   - Recherche la traduction chinoise
   - Remplace les champs `name:` et `description:`
   - Réécrit le fichier en UTF-8

## Résultat

Avant :
```yaml
---
name: Security Engineer
description: Threat modeling, secure code review, security architecture
---
```

Après :
```yaml
---
name: 安全工程师
description: 威胁建模、安全代码审查与应用安全架构专家
---
```

## Notes

- Ne modifie que les **copies installées** (dans `~/.github/agents/`), pas les fichiers source
- À relancer après chaque mise à jour `install.sh` (qui écrase avec les originaux en anglais)
- Le fichier JSON est la source de vérité unique pour les traductions — ajoutez-y les nouveaux agents
- Le script est en pur ASCII (pour éviter les problèmes d'encodage PowerShell) ; tout le texte chinois réside dans le JSON
