# Workflow multi-agents : sprint de landing page

> Mettez en ligne une landing page optimisée pour la conversion en une journée, avec 4 agents.

## Le scénario

Vous avez besoin d'une landing page pour le lancement d'un nouveau produit. Elle doit être superbe, convertir les visiteurs et être en ligne avant la fin de la journée.

## L'équipe d'agents

| Agent | Rôle dans ce workflow |
|-------|---------------------|
| Content Creator | Rédiger le contenu |
| UI Designer | Concevoir la mise en page et les specs des composants |
| Frontend Developer | Le construire |
| Growth Hacker | Optimiser pour la conversion |

## Le workflow

### Matin : contenu + design (en parallèle)

**Étape 1a — Activer Content Creator**

```
Activate Content Creator.

Write landing page copy for "FlowSync" — an API integration platform
that connects any two SaaS tools in under 5 minutes.

Target audience: developers and technical PMs at mid-size companies.
Tone: confident, concise, slightly playful.

Sections needed:
1. Hero (headline + subheadline + CTA)
2. Problem statement (3 pain points)
3. How it works (3 steps)
4. Social proof (placeholder testimonial format)
5. Pricing (3 tiers: Free, Pro, Enterprise)
6. Final CTA

Keep it scannable. No fluff.
```

**Étape 1b — Activer UI Designer (en parallèle)**

```
Activate UI Designer.

Design specs for a SaaS landing page. Product: FlowSync (API integration platform).
Style: clean, modern, dark mode option. Think Linear or Vercel aesthetic.

Deliver:
1. Layout wireframe (section order + spacing)
2. Color palette (primary, secondary, accent, background)
3. Typography (font pairing, heading sizes, body size)
4. Component specs: hero section, feature cards, pricing table, CTA buttons
5. Responsive breakpoints (mobile, tablet, desktop)
```

### Milieu de journée : construction

**Étape 2 — Activer Frontend Developer**

```
Activate Frontend Developer.

Build a landing page from these specs:

Copy: [paste Content Creator output]
Design: [paste UI Designer output]

Stack: HTML, Tailwind CSS, minimal vanilla JS (no framework needed).
Requirements:
- Responsive (mobile-first)
- Fast (no heavy assets, system fonts OK)
- Accessible (proper headings, alt text, focus states)
- Include a working email signup form (action URL: /api/subscribe)

Deliver a single index.html file ready to deploy.
```

### Après-midi : optimisation

**Étape 3 — Activer Growth Hacker**

```
Activate Growth Hacker.

Review this landing page for conversion optimization:

[paste the HTML or describe the current page]

Evaluate:
1. Is the CTA above the fold?
2. Is the value proposition clear in under 5 seconds?
3. Any friction in the signup flow?
4. What A/B tests would you run first?
5. SEO basics: meta tags, OG tags, structured data

Give me specific changes, not general advice.
```

## Calendrier

| Heure | Activité | Agent |
|------|----------|-------|
| 9h00 | Lancement contenu + design (en parallèle) | Content Creator + UI Designer |
| 11h00 | Démarrage de la construction | Frontend Developer |
| 14h00 | Première version prête | — |
| 14h30 | Revue de conversion | Growth Hacker |
| 15h30 | Application des retours | Frontend Developer |
| 16h30 | Mise en ligne | Déploiement sur Vercel/Netlify |

## Patterns clés

1. **Lancement en parallèle** : le contenu et le design se font en même temps puisqu'ils sont indépendants
2. **Point de convergence** : le Frontend Developer a besoin des deux sorties avant de commencer
3. **Boucle de feedback** : le Growth Hacker passe en revue, puis le Frontend Developer applique les changements
4. **Cadré dans le temps** : chaque étape a un créneau clair pour éviter la dérive du périmètre
