# Workflow multi-agents : MVP de startup avec mémoire persistante

> Le même workflow de MVP de startup que [workflow-startup-mvp.md](workflow-startup-mvp.md), mais avec un serveur de mémoire MCP qui gère l'état entre les agents. Fini les transmissions par copier-coller.

## Le problème des transmissions manuelles

Dans le workflow standard, chaque transition d'un agent à l'autre ressemble à ceci :

```
Activate Backend Architect.

Here's our sprint plan: [paste Sprint Prioritizer output]
Here's our research brief: [paste UX Researcher output]

Design the API and database schema for RetroBoard.
...
```

C'est vous le ciment. Vous copiez-collez les sorties entre les agents, vous suivez ce qui a été fait et vous espérez ne pas perdre le contexte en chemin. Ça marche pour les petits projets, mais ça s'effondre quand :

- Les sessions expirent et vous perdez la sortie
- Plusieurs agents ont besoin du même contexte
- La QA échoue et vous devez revenir à un état précédent
- Le projet s'étale sur des jours ou des semaines à travers de nombreuses sessions

## La solution

Avec un serveur de mémoire MCP installé, les agents stockent leurs livrables en mémoire et récupèrent automatiquement ce dont ils ont besoin. Les transmissions deviennent :

```
Activate Backend Architect.

Project: RetroBoard. Recall previous context for this project
and design the API and database schema.
```

L'agent cherche en mémoire le contexte de RetroBoard, trouve le plan de sprint et le brief de recherche stockés par les agents précédents, et reprend à partir de là.

## Mise en place

Installez n'importe quel serveur de mémoire compatible MCP qui prend en charge les opérations `remember`, `recall` et `rollback`. Voir [integrations/mcp-memory/README.md](../integrations/mcp-memory/README.md) pour la mise en place.

## Le scénario

Identique au workflow standard : un outil SaaS de rétrospective d'équipe (RetroBoard), 4 semaines jusqu'au MVP, développeur solo.

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

Chaque agent dispose d'une section Memory Integration dans son prompt (voir [integrations/mcp-memory/README.md](../integrations/mcp-memory/README.md) pour savoir comment l'ajouter).

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
Remember your sprint plan tagged for this project when done.
```

Le Sprint Prioritizer produit le plan de sprint et le stocke en mémoire avec les tags `sprint-prioritizer`, `retroboard` et `sprint-plan`.

**Étape 2 — Activer UX Researcher (en parallèle)**

```
Activate UX Researcher.

I'm building a team retrospective tool for remote teams (5-20 people).
Competitors: EasyRetro, Retrium, Parabol.

Run a quick competitive analysis and identify:
1. What features are table stakes
2. Where competitors fall short
3. One differentiator we could own

Output a 1-page research brief. Remember it tagged for this project when done.
```

L'UX Researcher stocke le brief de recherche avec les tags `ux-researcher`, `retroboard` et `research-brief`.

**Étape 3 — Transmettre au Backend Architect**

```
Activate Backend Architect.

Project: RetroBoard. Recall the sprint plan and research brief from previous agents.
Stack: Node.js, Express, PostgreSQL, Socket.io for real-time.

Design:
1. Database schema (SQL)
2. REST API endpoints list
3. WebSocket events for real-time board updates
4. Auth strategy recommendation

Remember each deliverable tagged for this project and for the frontend-developer.
```

Le Backend Architect récupère automatiquement le plan de sprint et le brief de recherche depuis la mémoire. Pas de copier-coller. Il stocke son schéma et sa spec d'API avec les tags `backend-architect`, `retroboard`, `api-spec` et `frontend-developer`.

### Semaine 2 : construction des fonctionnalités centrales

**Étape 4 — Activer Frontend Developer + Rapid Prototyper**

```
Activate Frontend Developer.

Project: RetroBoard. Recall the API spec and schema from the Backend Architect.

Build the RetroBoard React app:
- Stack: React, TypeScript, Tailwind, Socket.io-client
- Pages: Login, Dashboard, Board view
- Components: RetroCard, VoteButton, ActionItem, BoardColumn

Start with the Board view — it's the core experience.
Focus on real-time: when one user adds a card, everyone sees it.
Remember your progress tagged for this project.
```

Le Frontend Developer récupère la spec d'API depuis la mémoire et construit à partir d'elle.

**Étape 5 — Point de contrôle à mi-parcours**

```
Activate Reality Checker.

Project: RetroBoard. We're at week 2 of a 4-week MVP build.

Recall all deliverables from previous agents for this project.

Evaluate:
1. Can we realistically ship in 2 more weeks?
2. What should we cut to make the deadline?
3. Any technical debt that will bite us at launch?

Remember your verdict tagged for this project.
```

Le Reality Checker a une visibilité complète sur tout ce qui a été produit jusqu'ici — le plan de sprint, le brief de recherche, le schéma, la spec d'API et l'avancement du frontend — sans que vous ayez à tout rassembler et coller.

### Semaine 3 : peaufinage + landing page

**Étape 6 — Le Frontend Developer continue, le Growth Hacker démarre**

```
Activate Growth Hacker.

Product: RetroBoard — team retrospective tool, launching in 1 week.
Target: Engineering managers and scrum masters at remote-first companies.
Budget: $0 (organic launch only).

Recall the project context and Reality Checker's verdict.

Create a launch plan:
1. Landing page copy (hero, features, CTA)
2. Launch channels (Product Hunt, Reddit, Hacker News, Twitter)
3. Day-by-day launch sequence
4. Metrics to track in week 1

Remember the launch plan tagged for this project.
```

### Semaine 4 : lancement

**Étape 7 — Point de contrôle final**

```
Activate Reality Checker.

Project: RetroBoard, ready to launch.

Recall all project context, previous verdicts, and the launch plan.

Evaluate production readiness:
- Live URL: [url]
- Test accounts created: yes
- Error monitoring: Sentry configured
- Database backups: daily automated

Run through the launch checklist and give a GO / NO-GO decision.
Require evidence for each criterion.
```

### Quand la QA échoue : rollback

Dans le workflow standard, lorsque le Reality Checker rejette un livrable, vous retournez vers l'agent responsable et tentez d'expliquer ce qui n'a pas marché. Avec la mémoire, la boucle de récupération est plus resserrée :

```
Activate Backend Architect.

Project: RetroBoard. The Reality Checker flagged issues with the API design.
Recall the Reality Checker's feedback and your previous API spec.
Roll back to your last known-good schema and address the specific issues raised.
Remember the updated deliverables when done.
```

Le Backend Architect peut voir exactement ce que le Reality Checker a signalé, récupérer son propre travail précédent, revenir à un point de contrôle et produire un correctif — le tout sans que vous suiviez manuellement les versions.

## Avant et après

| Aspect | Workflow standard | Avec mémoire |
|--------|------------------|-------------|
| **Transmissions** | Copier-coller la sortie complète entre les agents | Les agents récupèrent automatiquement ce dont ils ont besoin |
| **Perte de contexte** | Les expirations de session font tout perdre | Les mémoires persistent à travers les sessions |
| **Contexte multi-agents** | Compiler manuellement le contexte de N agents | L'agent cherche en mémoire le tag du projet |
| **Récupération après échec de QA** | Décrire manuellement ce qui n'a pas marché | L'agent récupère le feedback + revient en arrière |
| **Projets sur plusieurs jours** | Réétablir le contexte à chaque session | L'agent reprend là où il s'était arrêté |
| **Mise en place requise** | Aucune | Installer un serveur de mémoire MCP |

## Patterns clés

1. **Taguez tout avec le nom du projet** : c'est ce qui fait fonctionner la récupération. Chaque mémoire reçoit le tag `retroboard` (ou le nom de votre projet).
2. **Taguez les livrables pour l'agent destinataire** : quand le Backend Architect termine une spec d'API, il tague la mémoire avec `frontend-developer` pour que le Frontend Developer la trouve à la récupération.
3. **Le Reality Checker obtient une visibilité complète** : comme tous les agents stockent leur travail en mémoire, le Reality Checker peut tout récupérer pour le projet sans que vous le compiliez.
4. **Le rollback remplace l'annulation manuelle** : quand quelque chose échoue, revenez au dernier point de contrôle au lieu d'essayer de comprendre ce qui a changé.

## Astuces

- Vous n'avez pas besoin de modifier chaque agent d'un coup. Commencez par ajouter Memory Integration aux agents que vous utilisez le plus, puis étendez à partir de là.
- Les instructions de mémoire sont des prompts, pas du code. Le LLM les interprète et appelle les outils MCP au besoin. Vous pouvez ajuster la formulation à votre style.
- N'importe quel serveur de mémoire compatible MCP qui prend en charge les outils `remember`, `recall`, `rollback` et `search` fonctionnera avec ce workflow.
