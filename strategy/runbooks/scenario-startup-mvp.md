# 🚀 Runbook : Build d'un MVP de startup

> **Mode** : NEXUS-Sprint | **Durée** : 4-6 semaines | **Agents** : 18-22

---

## Scénario

Vous construisez un MVP de startup — un nouveau produit qui doit valider rapidement son product-market fit. La vitesse compte, mais la qualité aussi. Vous devez passer de l'idée au produit en ligne avec de vrais utilisateurs en 4-6 semaines.

## Effectif d'agents

### Équipe centrale (toujours active)
| Agent | Rôle |
|-------|------|
| Agents Orchestrator | Contrôleur de pipeline |
| Senior Project Manager | Conversion spec-vers-tâches |
| Sprint Prioritizer | Gestion du backlog |
| UX Architect | Fondation technique |
| Frontend Developer | Implémentation de l'UI |
| Backend Architect | API et base de données |
| DevOps Automator | CI/CD et déploiement |
| Evidence Collector | QA pour chaque tâche |
| Reality Checker | Porte qualité finale |

### Équipe Growth (activée à partir de la semaine 3)
| Agent | Rôle |
|-------|------|
| Growth Hacker | Stratégie d'acquisition |
| Content Creator | Contenu de lancement |
| Social Media Strategist | Campagne sociale |

### Équipe de support (selon les besoins)
| Agent | Rôle |
|-------|------|
| Brand Guardian | Identité de marque |
| Analytics Reporter | Métriques et tableaux de bord |
| Rapid Prototyper | Expériences de validation rapides |
| AI Engineer | Si le produit inclut des fonctionnalités IA |
| Performance Benchmarker | Test de charge avant le lancement |
| Infrastructure Maintainer | Mise en place de la production |

## Exécution semaine par semaine

### Semaine 1 : Discovery + Architecture (phase 0 + phase 1 compressées)

```
Day 1-2: Compressed Discovery
├── Trend Researcher → Quick competitive scan (1 day, not full report)
├── UX Architect → Wireframe key user flows
└── Senior Project Manager → Convert spec to task list

Day 3-4: Architecture
├── UX Architect → CSS design system + component architecture
├── Backend Architect → System architecture + database schema
├── Brand Guardian → Quick brand foundation (colors, typography, voice)
└── Sprint Prioritizer → RICE-scored backlog + sprint plan

Day 5: Foundation Setup
├── DevOps Automator → CI/CD pipeline + environments
├── Frontend Developer → Project scaffolding
├── Backend Architect → Database + API scaffold
└── Quality Gate: Architecture Package approved
```

### Semaines 2-3 : Build du cœur (phase 2 + phase 3)

```
Sprint 1 (Week 2):
├── Agents Orchestrator manages Dev↔QA loop
├── Frontend Developer → Core UI (auth, main views, navigation)
├── Backend Architect → Core API (auth, CRUD, business logic)
├── Evidence Collector → QA every completed task
├── AI Engineer → ML features if applicable
└── Sprint Review at end of week

Sprint 2 (Week 3):
├── Continue Dev↔QA loop for remaining features
├── Growth Hacker → Design viral mechanics + referral system
├── Content Creator → Begin launch content creation
├── Analytics Reporter → Set up tracking and dashboards
└── Sprint Review at end of week
```

### Semaine 4 : Finitions + Durcissement (phase 4)

```
Day 1-2: Quality Sprint
├── Evidence Collector → Full screenshot suite
├── Performance Benchmarker → Load testing
├── Frontend Developer → Fix QA issues
├── Backend Architect → Fix API issues
└── Brand Guardian → Brand consistency audit

Day 3-4: Reality Check
├── Reality Checker → Final integration testing
├── Infrastructure Maintainer → Production readiness
└── DevOps Automator → Production deployment prep

Day 5: Gate Decision
├── Reality Checker verdict
├── IF NEEDS WORK: Quick fix cycle (2-3 days)
├── IF READY: Proceed to launch
└── Executive Summary Generator → Stakeholder briefing
```

### Semaines 5-6 : Lancement + Croissance (phase 5)

```
Week 5: Launch
├── DevOps Automator → Production deployment
├── Growth Hacker → Activate acquisition channels
├── Content Creator → Publish launch content
├── Social Media Strategist → Cross-platform campaign
├── Analytics Reporter → Real-time monitoring
└── Support Responder → User support active

Week 6: Optimize
├── Growth Hacker → Analyze and optimize channels
├── Feedback Synthesizer → Collect early user feedback
├── Experiment Tracker → Launch A/B tests
├── Analytics Reporter → Week 1 analysis
└── Sprint Prioritizer → Plan iteration sprint
```

## Décisions clés

| Point de décision | Quand | Qui décide |
|---------------|------|-------------|
| Go/No-Go sur le concept | Fin du jour 2 | Studio Producer |
| Approbation de l'architecture | Fin du jour 4 | Senior Project Manager |
| Périmètre des fonctionnalités du MVP | Planification de sprint | Sprint Prioritizer |
| Aptitude à la production | Semaine 4, jour 5 | Reality Checker |
| Timing du lancement | Après le verdict READY du Reality Checker | Studio Producer |

## Critères de réussite

| Métrique | Cible |
|--------|--------|
| Délai jusqu'au produit en ligne | ≤ 6 semaines |
| Fonctionnalités centrales complètes | 100 % du périmètre du MVP |
| Premiers utilisateurs onboardés | Dans les 48 heures suivant le lancement |
| Uptime du système | > 99 % la première semaine |
| Feedback utilisateur collecté | ≥ 50 réponses dans les 2 premières semaines |

## Pièges fréquents & parades

| Piège | Parade |
|---------|-----------|
| Dérive du périmètre pendant le build | Le Sprint Prioritizer fait respecter le MoSCoW — « Won't » signifie qu'on ne le fait pas |
| Sur-ingénierie pour la montée en charge | État d'esprit Rapid Prototyper — valider d'abord, passer à l'échelle ensuite |
| Sauter la QA pour gagner du temps | L'Evidence Collector intervient sur CHAQUE tâche — sans exception |
| Lancer sans monitoring | L'Infrastructure Maintainer met en place le monitoring dès la semaine 1 |
| Aucun mécanisme de feedback | Analytics + collecte de feedback intégrés dès le sprint 1 |
