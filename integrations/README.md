# 🔌 Intégrations

Ce répertoire contient les intégrations de The Agency et les formats convertis pour
les outils de codage agentiques pris en charge.

## Outils pris en charge

- **[Claude Code](#claude-code)** — agents `.md`, utiliser le dépôt directement
- **[GitHub Copilot](#github-copilot)** — agents `.md`, utiliser le dépôt directement
- **[Antigravity](#antigravity)** — un `SKILL.md` par agent dans `antigravity/`
- **[Gemini CLI](#gemini-cli)** — fichiers d'agent `.md` dans `gemini-cli/agents/`
- **[OpenCode](#opencode)** — fichiers d'agent `.md` dans `opencode/`
- **[OpenClaw](#openclaw)** — espaces de travail `SOUL.md` + `AGENTS.md` + `IDENTITY.md`
- **[Cursor](#cursor)** — fichiers de règles `.mdc` dans `cursor/`
- **[Aider](#aider)** — `CONVENTIONS.md` dans `aider/`
- **[Windsurf](#windsurf)** — `.windsurfrules` dans `windsurf/`
- **[Kimi Code](#kimi-code)** — spécifications d'agent YAML dans `kimi/`
- **[Qwen Code](#qwen-code)** — SubAgents `.md` à portée projet dans `.qwen/agents/`
- **[Codex](#codex)** — agents personnalisés `.toml` dans `codex/`

## Installation rapide

```bash
# Install for all detected tools automatically
./scripts/install.sh

# Install a specific home-scoped tool
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool claude-code
./scripts/install.sh --tool codex

# Gemini CLI needs generated integration files on a fresh clone
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli

# Qwen Code also needs generated SubAgent files on a fresh clone
./scripts/convert.sh --tool qwen
./scripts/install.sh --tool qwen
```

Si vous installez OpenClaw et que la passerelle (gateway) tourne déjà, redémarrez-la après l'installation :

```bash
openclaw gateway restart
```

Pour les outils à portée projet tels qu'OpenCode, Cursor, Aider, Windsurf et Qwen
Code, lancez
l'installateur depuis la racine de votre projet cible comme indiqué dans les sections
propres à chaque outil ci-dessous.

## Régénérer les fichiers d'intégration

Si vous ajoutez ou modifiez des agents, régénérez tous les fichiers d'intégration :

```bash
./scripts/convert.sh
```

---

## Claude Code

The Agency a été conçu à l'origine pour Claude Code. Les agents fonctionnent nativement
sans conversion.

```bash
cp -r <category>/*.md ~/.claude/agents/
# or install everything at once:
./scripts/install.sh --tool claude-code
```

Voir [claude-code/README.md](claude-code/README.md) pour plus de détails.

---

## GitHub Copilot

The Agency fonctionne aussi nativement avec GitHub Copilot. Les agents peuvent être copiés
directement dans `~/.github/agents/` et `~/.copilot/agents/` sans conversion.

```bash
./scripts/install.sh --tool copilot
```

Voir [github-copilot/README.md](github-copilot/README.md) pour plus de détails.

---

## Antigravity

Les skills sont installés dans `~/.gemini/antigravity/skills/`. Chaque agent devient
un skill distinct préfixé par `agency-` pour éviter les conflits de noms.

```bash
./scripts/install.sh --tool antigravity
```

Voir [antigravity/README.md](antigravity/README.md) pour plus de détails.

---

## Gemini CLI

Les agents sont packagés sous forme de subagents Gemini CLI.
Les subagents sont installés dans `~/.gemini/agents/`.
Comme les fichiers d'agent sont des artefacts générés, lancez
`./scripts/convert.sh --tool gemini-cli` avant l'installation depuis un clone neuf.

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

Voir [gemini-cli/README.md](gemini-cli/README.md) pour plus de détails.

---

## OpenCode

Chaque agent devient un fichier `.md` à portée projet dans `.opencode/agents/`.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool opencode
```

Voir [opencode/README.md](opencode/README.md) pour plus de détails.

---

## OpenClaw

Chaque agent devient un espace de travail OpenClaw contenant `SOUL.md`, `AGENTS.md`
et `IDENTITY.md`.

Avant l'installation, générez les espaces de travail OpenClaw :

```bash
./scripts/convert.sh --tool openclaw
```

Puis installez-les :

```bash
./scripts/install.sh --tool openclaw
```

Voir [openclaw/README.md](openclaw/README.md) pour plus de détails.

---

## Cursor

Chaque agent devient un fichier de règle `.mdc`. Les règles sont à portée projet — lancez
l'installateur depuis la racine de votre projet.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool cursor
```

Voir [cursor/README.md](cursor/README.md) pour plus de détails.

---

## Aider

Tous les agents sont regroupés dans un seul fichier `CONVENTIONS.md` qu'Aider
lit automatiquement lorsqu'il est présent à la racine de votre projet.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool aider
```

Voir [aider/README.md](aider/README.md) pour plus de détails.

---

## Windsurf

Tous les agents sont regroupés dans un seul fichier `.windsurfrules` pour la
racine de votre projet.

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool windsurf
```

Voir [windsurf/README.md](windsurf/README.md) pour plus de détails.

---

## Kimi Code

Chaque agent est converti en une spécification d'agent Kimi Code CLI (format YAML avec
des fichiers de system prompt séparés). Les agents sont installés dans `~/.config/kimi/agents/`.

Comme les fichiers d'agent Kimi sont générés à partir du Markdown source, lancez
`./scripts/convert.sh --tool kimi` avant l'installation depuis un clone neuf.

```bash
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

### Utilisation

Après installation, utilisez un agent avec l'option `--agent-file` :

```bash
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml
```

Ou dans un projet spécifique :

```bash
cd /your/project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project
```

Voir [kimi/README.md](kimi/README.md) pour plus de détails.

---

## Qwen Code

Chaque agent devient un fichier SubAgent `.md` à portée projet dans `.qwen/agents/`.

Depuis un clone neuf, générez d'abord les fichiers Qwen :

```bash
./scripts/convert.sh --tool qwen
```

Puis installez-les depuis la racine de votre projet :

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool qwen
```

Voir [qwen/README.md](qwen/README.md) pour plus de détails.

---

## Codex

Chaque agent est converti en un fichier TOML d'agent personnalisé Codex autonome et
installé dans `~/.codex/agents/`.

Comme Codex utilise des fichiers TOML générés plutôt que le Markdown source
directement, lancez le convertisseur avant l'installation depuis un clone neuf :

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

Voir [codex/README.md](codex/README.md) pour plus de détails.
