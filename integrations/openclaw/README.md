# Intégration OpenClaw

Les agents OpenClaw sont installés sous forme d'espaces de travail contenant les fichiers `SOUL.md`, `AGENTS.md`
et `IDENTITY.md`. L'installateur copie chaque espace de travail dans
`~/.openclaw/agency-agents/` et l'enregistre lorsque la CLI `openclaw` est
disponible.

Avant l'installation, générez les espaces de travail OpenClaw :

```bash
./scripts/convert.sh --tool openclaw
```

## Installation

```bash
./scripts/install.sh --tool openclaw
```

## Activer un agent

Après installation, les agents sont disponibles via leur `agentId` dans les sessions OpenClaw.

Si la passerelle (gateway) OpenClaw tourne déjà, redémarrez-la après l'installation :

```bash
openclaw gateway restart
```

## Régénérer

```bash
./scripts/convert.sh --tool openclaw
```
