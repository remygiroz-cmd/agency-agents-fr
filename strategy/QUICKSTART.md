# ⚡ Guide de démarrage rapide NEXUS

> **Passez de zéro à un pipeline multi-agents orchestré en 5 minutes.**

---

## Qu'est-ce que NEXUS ?

**NEXUS** (Network of EXperts, Unified in Strategy) transforme les spécialistes IA de The Agency en un pipeline coordonné. Au lieu d'activer les agents un par un en espérant qu'ils travaillent ensemble, NEXUS définit exactement qui fait quoi, quand, et comment la qualité est vérifiée à chaque étape.

## Choisissez votre mode

| Je veux... | Utiliser | Agents | Durée |
|-------------|-----|--------|------|
| Construire un produit complet à partir de zéro | **NEXUS-Full** | Tous | 12-24 semaines |
| Construire une fonctionnalité ou un MVP | **NEXUS-Sprint** | 15-25 | 2-6 semaines |
| Réaliser une tâche précise (correction de bug, campagne, audit) | **NEXUS-Micro** | 5-10 | 1-5 jours |

---

## 🚀 NEXUS-Full : démarrer un projet complet

**Copiez ce prompt pour activer le pipeline complet :**

```
Activate Agents Orchestrator in NEXUS-Full mode.

Project: [YOUR PROJECT NAME]
Specification: [DESCRIBE YOUR PROJECT OR LINK TO SPEC]

Execute the complete NEXUS pipeline:
- Phase 0: Discovery (Trend Researcher, Feedback Synthesizer, UX Researcher, Analytics Reporter, Legal Compliance Checker, Tool Evaluator)
- Phase 1: Strategy (Studio Producer, Senior Project Manager, Sprint Prioritizer, UX Architect, Brand Guardian, Backend Architect, Finance Tracker)
- Phase 2: Foundation (DevOps Automator, Frontend Developer, Backend Architect, UX Architect, Infrastructure Maintainer)
- Phase 3: Build (Dev↔QA loops — all engineering + Evidence Collector)
- Phase 4: Harden (Reality Checker, Performance Benchmarker, API Tester, Legal Compliance Checker)
- Phase 5: Launch (Growth Hacker, Content Creator, all marketing agents, DevOps Automator)
- Phase 6: Operate (Analytics Reporter, Infrastructure Maintainer, Support Responder, ongoing)

Quality gates between every phase. Evidence required for all assessments.
Maximum 3 retries per task before escalation.
```

---

## 🏃 NEXUS-Sprint : construire une fonctionnalité ou un MVP

**Copiez ce prompt :**

```
Activate Agents Orchestrator in NEXUS-Sprint mode.

Feature/MVP: [DESCRIBE WHAT YOU'RE BUILDING]
Timeline: [TARGET WEEKS]
Skip Phase 0 (market already validated).

Sprint team:
- PM: Senior Project Manager, Sprint Prioritizer
- Design: UX Architect, Brand Guardian
- Engineering: Frontend Developer, Backend Architect, DevOps Automator
- QA: Evidence Collector, Reality Checker, API Tester
- Support: Analytics Reporter

Begin at Phase 1 with architecture and sprint planning.
Run Dev↔QA loops for all implementation tasks.
Reality Checker approval required before launch.
```

---

## 🎯 NEXUS-Micro : réaliser une tâche précise

**Choisissez votre scénario et copiez le prompt :**

### Corriger un bug
```
Activate Backend Architect to investigate and fix [BUG DESCRIPTION].
After fix, activate API Tester to verify the fix.
Then activate Evidence Collector to confirm no visual regressions.
```

### Lancer une campagne marketing
```
Activate Social Media Strategist as campaign lead for [CAMPAIGN DESCRIPTION].
Team: Content Creator, Twitter Engager, Instagram Curator, Reddit Community Builder.
Brand Guardian reviews all content before publishing.
Analytics Reporter tracks performance daily.
Growth Hacker optimizes channels weekly.
```

### Réaliser un audit de conformité
```
Activate Legal Compliance Checker for comprehensive compliance audit.
Scope: [GDPR / CCPA / HIPAA / ALL]
After audit, activate Executive Summary Generator to create stakeholder report.
```

### Investiguer des problèmes de performance
```
Activate Performance Benchmarker to diagnose performance issues.
Scope: [API response times / Page load / Database queries / All]
After diagnosis, activate Infrastructure Maintainer for optimization.
DevOps Automator deploys any infrastructure changes.
```

### Recherche de marché
```
Activate Trend Researcher for market intelligence on [DOMAIN].
Deliverables: Competitive landscape, market sizing, trend forecast.
After research, activate Executive Summary Generator for executive brief.
```

### Amélioration de l'UX
```
Activate UX Researcher to identify usability issues in [FEATURE/PRODUCT].
After research, activate UX Architect to design improvements.
Frontend Developer implements changes.
Evidence Collector verifies improvements.
```

---

## 📁 Documents de stratégie

| Document | Objet | Emplacement |
|----------|---------|----------|
| **Stratégie maîtresse** | Doctrine NEXUS complète | `strategy/nexus-strategy.md` |
| **Playbook phase 0** | Discovery et intelligence | `strategy/playbooks/phase-0-discovery.md` |
| **Playbook phase 1** | Stratégie et architecture | `strategy/playbooks/phase-1-strategy.md` |
| **Playbook phase 2** | Fondations et scaffolding | `strategy/playbooks/phase-2-foundation.md` |
| **Playbook phase 3** | Build et itération | `strategy/playbooks/phase-3-build.md` |
| **Playbook phase 4** | Qualité et durcissement | `strategy/playbooks/phase-4-hardening.md` |
| **Playbook phase 5** | Lancement et croissance | `strategy/playbooks/phase-5-launch.md` |
| **Playbook phase 6** | Exploitation et évolution | `strategy/playbooks/phase-6-operate.md` |
| **Prompts d'activation** | Prompts d'agents prêts à l'emploi | `strategy/coordination/agent-activation-prompts.md` |
| **Modèles de passation** | Formats de passation standardisés | `strategy/coordination/handoff-templates.md` |
| **Runbook MVP de startup** | Build de MVP en 4-6 semaines | `strategy/runbooks/scenario-startup-mvp.md` |
| **Runbook fonctionnalité entreprise** | Développement de fonctionnalité entreprise | `strategy/runbooks/scenario-enterprise-feature.md` |
| **Runbook campagne marketing** | Campagne multicanal | `strategy/runbooks/scenario-marketing-campaign.md` |
| **Runbook réponse aux incidents** | Gestion d'incident en production | `strategy/runbooks/scenario-incident-response.md` |

---

## 🔑 Concepts clés en 30 secondes

1. **Portes qualité (Quality Gates)** — Aucune phase n'avance sans une approbation fondée sur les preuves
2. **Boucle Dev↔QA** — Chaque tâche est construite puis testée ; PASS pour avancer, FAIL pour réessayer (max 3)
3. **Passations (Handoffs)** — Transfert de contexte structuré entre agents (ne jamais démarrer à froid)
4. **Reality Checker** — Autorité qualité finale ; par défaut « NEEDS WORK »
5. **Agents Orchestrator** — Contrôleur de pipeline gérant l'ensemble du flux
6. **La preuve plutôt que les affirmations** — Captures d'écran, résultats de tests et données — pas des assertions

---

## 🎭 Les agents en un coup d'œil

```
ENGINEERING         │ DESIGN              │ MARKETING
Frontend Developer  │ UI Designer         │ Growth Hacker
Backend Architect   │ UX Researcher       │ Content Creator
Mobile App Builder  │ UX Architect        │ Twitter Engager
AI Engineer         │ Brand Guardian      │ TikTok Strategist
DevOps Automator    │ Visual Storyteller  │ Instagram Curator
Rapid Prototyper    │ Whimsy Injector     │ Reddit Community Builder
Senior Developer    │ Image Prompt Eng.   │ App Store Optimizer
                    │                     │ Social Media Strategist
────────────────────┼─────────────────────┼──────────────────────
PRODUCT             │ PROJECT MGMT        │ TESTING
Sprint Prioritizer  │ Studio Producer     │ Evidence Collector
Trend Researcher    │ Project Shepherd    │ Reality Checker
Feedback Synthesizer│ Studio Operations   │ Test Results Analyzer
                    │ Experiment Tracker  │ Performance Benchmarker
                    │ Senior Project Mgr  │ API Tester
                    │                     │ Tool Evaluator
                    │                     │ Workflow Optimizer
────────────────────┼─────────────────────┼──────────────────────
SUPPORT             │ SPATIAL             │ SPECIALIZED
Support Responder   │ XR Interface Arch.  │ Agents Orchestrator
Analytics Reporter  │ macOS Spatial/Metal │ Analytics Reporter
Finance Tracker     │ XR Immersive Dev    │ LSP/Index Engineer
Infra Maintainer    │ XR Cockpit Spec.    │ Sales Data Extraction
Legal Compliance    │ visionOS Spatial    │ Data Consolidation
Exec Summary Gen.   │ Terminal Integration│ Report Distribution
```

---

<div align="center">

**Commencez par un mode. Suivez le playbook. Faites confiance au pipeline.**

`strategy/nexus-strategy.md` — La doctrine complète

</div>
