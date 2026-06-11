# 🏢 Runbook : Développement d'une fonctionnalité entreprise

> **Mode** : NEXUS-Sprint | **Durée** : 6-12 semaines | **Agents** : 20-30

---

## Scénario

Vous ajoutez une fonctionnalité majeure à un produit entreprise existant. La conformité, la sécurité et les portes qualité sont non négociables. Plusieurs parties prenantes doivent être alignées. La fonctionnalité doit s'intégrer sans accroc aux systèmes existants.

## Effectif d'agents

### Équipe centrale
| Agent | Rôle |
|-------|------|
| Agents Orchestrator | Contrôleur de pipeline |
| Project Shepherd | Coordination transverse |
| Senior Project Manager | Conversion spec-vers-tâches |
| Sprint Prioritizer | Gestion du backlog |
| UX Architect | Fondation technique |
| UX Researcher | Validation utilisateur |
| UI Designer | Conception des composants |
| Frontend Developer | Implémentation de l'UI |
| Backend Architect | API et intégration système |
| Senior Developer | Implémentation complexe |
| DevOps Automator | CI/CD et déploiement |
| Evidence Collector | QA visuelle |
| API Tester | Validation des endpoints |
| Reality Checker | Porte qualité finale |
| Performance Benchmarker | Test de charge |

### Conformité & Gouvernance
| Agent | Rôle |
|-------|------|
| Legal Compliance Checker | Conformité réglementaire |
| Brand Guardian | Cohérence de marque |
| Finance Tracker | Suivi du budget |
| Executive Summary Generator | Reporting aux parties prenantes |

### Assurance qualité
| Agent | Rôle |
|-------|------|
| Test Results Analyzer | Métriques qualité |
| Workflow Optimizer | Amélioration des processus |
| Experiment Tracker | Tests A/B |

## Plan d'exécution

### Phase 1 : Exigences & Architecture (semaine 1-2)

```
Week 1: Stakeholder Alignment
├── Project Shepherd → Stakeholder analysis + communication plan
├── UX Researcher → User research on feature need
├── Legal Compliance Checker → Compliance requirements scan
├── Senior Project Manager → Spec-to-task conversion
└── Finance Tracker → Budget framework

Week 2: Technical Architecture
├── UX Architect → UX foundation + component architecture
├── Backend Architect → System architecture + integration plan
├── UI Designer → Component design + design system updates
├── Sprint Prioritizer → RICE-scored backlog
├── Brand Guardian → Brand impact assessment
└── Quality Gate: Architecture Review (Project Shepherd + Reality Checker)
```

### Phase 2 : Fondations (semaine 3)

```
├── DevOps Automator → Feature branch pipeline + feature flags
├── Frontend Developer → Component scaffolding
├── Backend Architect → API scaffold + database migrations
├── Infrastructure Maintainer → Staging environment setup
└── Quality Gate: Foundation verified (Evidence Collector)
```

### Phase 3 : Build (semaine 4-9)

```
Sprint 1-3 (Week 4-9):
├── Agents Orchestrator → Dev↔QA loop management
├── Frontend Developer → UI implementation (task by task)
├── Backend Architect → API implementation (task by task)
├── Senior Developer → Complex/premium features
├── Evidence Collector → QA every task (screenshots)
├── API Tester → Endpoint validation every API task
├── Experiment Tracker → A/B test setup for key features
│
├── Bi-weekly:
│   ├── Project Shepherd → Stakeholder status update
│   ├── Executive Summary Generator → Executive briefing
│   └── Finance Tracker → Budget tracking
│
└── Sprint Reviews with stakeholder demos
```

### Phase 4 : Durcissement (semaine 10-11)

```
Week 10: Evidence Collection
├── Evidence Collector → Full screenshot suite
├── API Tester → Complete regression suite
├── Performance Benchmarker → Load test at 10x traffic
├── Legal Compliance Checker → Final compliance audit
├── Test Results Analyzer → Quality metrics dashboard
└── Infrastructure Maintainer → Production readiness

Week 11: Final Judgment
├── Reality Checker → Integration testing (default: NEEDS WORK)
├── Fix cycle if needed (2-3 days)
├── Re-verification
└── Executive Summary Generator → Go/No-Go recommendation
```

### Phase 5 : Déploiement (semaine 12)

```
├── DevOps Automator → Canary deployment (5% → 25% → 100%)
├── Infrastructure Maintainer → Real-time monitoring
├── Analytics Reporter → Feature adoption tracking
├── Support Responder → User support for new feature
├── Feedback Synthesizer → Early feedback collection
└── Executive Summary Generator → Launch report
```

## Cadence de communication aux parties prenantes

| Auditoire | Fréquence | Agent | Format |
|----------|-----------|-------|--------|
| Sponsors exécutifs | Bimensuel | Executive Summary Generator | Synthèse SCQA (≤500 mots) |
| Équipe produit | Hebdomadaire | Project Shepherd | Rapport de statut |
| Équipe d'ingénierie | Quotidien | Agents Orchestrator | Statut du pipeline |
| Équipe conformité | Mensuel | Legal Compliance Checker | Statut de conformité |
| Finance | Mensuel | Finance Tracker | Rapport budgétaire |

## Exigences de qualité

| Exigence | Seuil | Vérification |
|-------------|-----------|-------------|
| Couverture de code | > 80 % | Test Results Analyzer |
| Temps de réponse de l'API | P95 < 200ms | Performance Benchmarker |
| Accessibilité | WCAG 2.1 AA | Evidence Collector |
| Sécurité | Zéro vulnérabilité critique | Legal Compliance Checker |
| Cohérence de marque | 95 %+ de conformité | Brand Guardian |
| Conformité à la spec | 100 % | Reality Checker |
| Gestion de la charge | 10x le trafic actuel | Performance Benchmarker |

## Gestion des risques

| Risque | Probabilité | Impact | Parade | Responsable |
|------|------------|--------|-----------|-------|
| Complexité d'intégration | Élevée | Élevé | Tests d'intégration précoces, API Tester à chaque sprint | Backend Architect |
| Dérive du périmètre | Moyenne | Élevé | Le Sprint Prioritizer fait respecter le MoSCoW, le Project Shepherd gère les changements | Sprint Prioritizer |
| Problèmes de conformité | Moyenne | Critique | Legal Compliance Checker impliqué dès le jour 1 | Legal Compliance Checker |
| Régression de performance | Moyenne | Élevé | Le Performance Benchmarker teste à chaque sprint | Performance Benchmarker |
| Désalignement des parties prenantes | Faible | Élevé | Briefings exécutifs bimensuels, coordination du Project Shepherd | Project Shepherd |
