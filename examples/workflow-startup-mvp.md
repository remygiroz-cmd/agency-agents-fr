# Workflow multi-agents : MVP de startup

> Un exemple pas à pas de coordination de plusieurs agents pour passer de l'idée à un MVP mis en ligne.

## Le scénario

Vous construisez un MVP de SaaS — un outil de rétrospective d'équipe pour les équipes à distance. Vous avez 4 semaines pour livrer un produit fonctionnel avec inscriptions des utilisateurs, une fonctionnalité centrale et une landing page.

## L'équipe d'agents

| Agent | Rôle dans ce workflow |
|-------|---------------------|
| Sprint Prioritizer | Découper le projet en sprints hebdomadaires |
| UX Researcher | Valider l'idée par de rapides entretiens utilisateurs |
| Backend Architect | Concevoir l'API et le modèle de données |
| Frontend Developer | Construire l'app React |
| Rapid Prototyper | Faire tourner la première version rapidement |
| Growth Hacker | Planifier la stratégie de lancement pendant la construction |
| Reality Checker | Valider chaque jalon avant de poursuivre |

## Le workflow

### Semaine 1 : découverte + architecture

**Étape 1 — Activer Sprint Prioritizer**

```
Activate Sprint Prioritizer.

Project: RetroBoard — a real-time team retrospective tool for remote teams.
Timeline: 4 weeks to MVP launch.
Core features: user auth, create retro boards, add cards, vote, action items.
Constraints: solo developer, React + Node.js stack, deploy to Vercel + Railway.

Break this into 4 weekly sprints with clear deliverables and acceptance criteria.
```

**Étape 2 — Activer UX Researcher (en parallèle)**

```
Activate UX Researcher.

I'm building a team retrospective tool for remote teams (5-20 people).
Competitors: EasyRetro, Retrium, Parabol.

Run a quick competitive analysis and identify:
1. What features are table stakes
2. Where competitors fall short
3. One differentiator we could own

Output a 1-page research brief.
```

**Étape 3 — Transmettre au Backend Architect**

```
Activate Backend Architect.

Here's our sprint plan: [paste Sprint Prioritizer output]
Here's our research brief: [paste UX Researcher output]

Design the API and database schema for RetroBoard.
Stack: Node.js, Express, PostgreSQL, Socket.io for real-time.

Deliver:
1. Database schema (SQL)
2. REST API endpoints list
3. WebSocket events for real-time board updates
4. Auth strategy recommendation
```

### Semaine 2 : construction des fonctionnalités centrales

**Étape 4 — Activer Frontend Developer + Rapid Prototyper**

```
Activate Frontend Developer.

Here's the API spec: [paste Backend Architect output]

Build the RetroBoard React app:
- Stack: React, TypeScript, Tailwind, Socket.io-client
- Pages: Login, Dashboard, Board view
- Components: RetroCard, VoteButton, ActionItem, BoardColumn

Start with the Board view — it's the core experience.
Focus on real-time: when one user adds a card, everyone sees it.
```

**Étape 5 — Point de contrôle à mi-parcours**

```
Activate Reality Checker.

We're at week 2 of a 4-week MVP build for RetroBoard.

Here's what we have so far:
- Database schema: [paste]
- API endpoints: [paste]
- Frontend components: [paste]

Evaluate:
1. Can we realistically ship in 2 more weeks?
2. What should we cut to make the deadline?
3. Any technical debt that will bite us at launch?
```

### Semaine 3 : peaufinage + landing page

**Étape 6 — Le Frontend Developer continue, le Growth Hacker démarre**

```
Activate Growth Hacker.

Product: RetroBoard — team retrospective tool, launching in 1 week.
Target: Engineering managers and scrum masters at remote-first companies.
Budget: $0 (organic launch only).

Create a launch plan:
1. Landing page copy (hero, features, CTA)
2. Launch channels (Product Hunt, Reddit, Hacker News, Twitter)
3. Day-by-day launch sequence
4. Metrics to track in week 1
```

### Semaine 4 : lancement

**Étape 7 — Point de contrôle final**

```
Activate Reality Checker.

RetroBoard is ready to launch. Evaluate production readiness:

- Live URL: [url]
- Test accounts created: yes
- Error monitoring: Sentry configured
- Database backups: daily automated

Run through the launch checklist and give a GO / NO-GO decision.
Require evidence for each criterion.
```

## Patterns clés

1. **Transmissions séquentielles** : la sortie de chaque agent devient l'entrée de l'agent suivant
2. **Travail en parallèle** : l'UX Researcher et le Sprint Prioritizer peuvent tourner simultanément en semaine 1
3. **Points de contrôle qualité** : le Reality Checker à mi-parcours et avant le lancement évite de mettre en ligne du code cassé
4. **Transmission du contexte** : collez toujours les sorties des agents précédents dans le prompt suivant — les agents ne partagent pas de mémoire

## Astuces

- Copiez-collez les sorties des agents entre les étapes — ne résumez pas, utilisez la sortie complète
- Si un Reality Checker signale un problème, revenez vers le spécialiste concerné pour le corriger
- Gardez à l'esprit l'agent Orchestrator pour automatiser ce flux une fois à l'aise avec la version manuelle
