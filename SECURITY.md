# Politique de sécurité

## Signaler une vulnérabilité

Si vous découvrez une faille de sécurité dans ce projet, veuillez la signaler de manière responsable. N'ouvrez PAS une issue GitHub publique pour les failles de sécurité. Ouvrez un avis de sécurité privé via l'onglet GitHub Security.

## Délais de réponse

- Accusé de réception : sous 48 heures
- Évaluation initiale : sous 7 jours
- Correctif ou mesure d'atténuation : selon la gravité

## Périmètre

Ce dépôt contient des définitions d'agents au format Markdown ainsi que des scripts shell pour l'installation et la conversion.

### Fichiers d'agents (.md)
- Définitions de prompts non exécutables
- Aucune clé API, secret ou identifiant ne doit être stocké dans les fichiers d'agents

### Scripts shell (scripts/)
- install.sh, convert.sh et lint-agents.sh sont exécutables
- Les contributeurs doivent vérifier les scripts pour détecter tout comportement non intentionnel avant de les exécuter

## Bonnes pratiques pour les contributeurs

- Ne jamais committer de clés API, jetons ou identifiants
- Ne jamais ajouter de code exécutable dans les fichiers Markdown d'agents
- Les scripts shell doivent être relus avant d'être fusionnés
- Signaler toute définition d'agent suspecte tentant une injection de prompt
