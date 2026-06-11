# 🔨 Playbook phase 3 — Build & Itération

> **Durée** : 2-12 semaines (selon le périmètre) | **Agents** : 15-30+ | **Gardien de porte** : Agents Orchestrator

---

## Objectif

Implémenter toutes les fonctionnalités via des boucles Dev↔QA continues. Chaque tâche est validée avant que la suivante ne commence. C'est ici que se concentre l'essentiel du travail — et là où l'orchestration de NEXUS apporte le plus de valeur.

## Pré-conditions

- [ ] Porte qualité de la phase 2 franchie (fondation vérifiée)
- [ ] Backlog du Sprint Prioritizer disponible avec scores RICE
- [ ] Pipeline CI/CD opérationnel
- [ ] Design system et bibliothèque de composants prêts
- [ ] Scaffold d'API avec système d'authentification prêt

## La boucle Dev↔QA — Mécanique centrale

L'Agents Orchestrator gère chaque tâche à travers ce cycle :

```
FOR EACH task IN sprint_backlog (ordered by RICE score):

  1. ASSIGN task to appropriate Developer Agent (see assignment matrix)
  2. Developer IMPLEMENTS task
  3. Evidence Collector TESTS task
     - Visual screenshots (desktop, tablet, mobile)
     - Functional verification against acceptance criteria
     - Brand consistency check
  4. IF verdict == PASS:
       Mark task complete
       Move to next task
     ELIF verdict == FAIL AND attempts < 3:
       Send QA feedback to Developer
       Developer FIXES specific issues
       Return to step 3
     ELIF attempts >= 3:
       ESCALATE to Agents Orchestrator
       Orchestrator decides: reassign, decompose, defer, or accept
  5. UPDATE pipeline status report
```

## Matrice d'attribution des agents

### Attribution du développeur principal

| Catégorie de tâche | Agent principal | Agent de secours | Agent QA |
|--------------|--------------|-------------|----------|
| **UI React/Vue/Angular** | Frontend Developer | Rapid Prototyper | Evidence Collector |
| **API REST/GraphQL** | Backend Architect | Senior Developer | API Tester |
| **Opérations base de données** | Backend Architect | — | API Tester |
| **Mobile (iOS/Android)** | Mobile App Builder | — | Evidence Collector |
| **Modèle/pipeline ML** | AI Engineer | — | Test Results Analyzer |
| **CI/CD/Infrastructure** | DevOps Automator | Infrastructure Maintainer | Performance Benchmarker |
| **Fonctionnalité premium/complexe** | Senior Developer | Backend Architect | Evidence Collector |
| **Prototype/POC rapide** | Rapid Prototyper | Frontend Developer | Evidence Collector |
| **WebXR/immersif** | XR Immersive Developer | — | Evidence Collector |
| **visionOS** | visionOS Spatial Engineer | macOS Spatial/Metal Engineer | Evidence Collector |
| **Contrôles cockpit** | XR Cockpit Interaction Specialist | XR Interface Architect | Evidence Collector |
| **Outils CLI/terminal** | Terminal Integration Specialist | — | API Tester |
| **Intelligence du code** | LSP/Index Engineer | — | Test Results Analyzer |
| **Optimisation des performances** | Performance Benchmarker | Infrastructure Maintainer | Performance Benchmarker |

### Support de spécialistes (activé selon les besoins)

| Spécialiste | Quand l'activer | Déclencheur |
|-----------|-----------------|---------|
| UI Designer | Un composant nécessite un raffinement visuel | Le développeur demande un avis design |
| Whimsy Injector | Une fonctionnalité a besoin d'enchantement/personnalité | Une revue UX identifie une opportunité |
| Visual Storyteller | Du contenu narratif visuel est nécessaire | Le contenu requiert des assets visuels |
| Brand Guardian | Préoccupation de cohérence de marque | La QA détecte une déviation de marque |
| XR Interface Architect | Conception d'interaction spatiale nécessaire | Une fonctionnalité XR requiert un avis UX |
| Analytics Reporter | Analyse de données approfondie nécessaire | Une fonctionnalité requiert une intégration analytics |

## Pistes de build parallèles

Pour les déploiements NEXUS-Full, quatre pistes tournent simultanément :

### Piste A : Développement du produit central
```
Managed by: Agents Orchestrator (Dev↔QA loop)
Agents: Frontend Developer, Backend Architect, AI Engineer,
        Mobile App Builder, Senior Developer
QA: Evidence Collector, API Tester, Test Results Analyzer

Sprint cadence: 2-week sprints
Daily: Task implementation + QA validation
End of sprint: Sprint review + retrospective
```

### Piste B : Préparation Growth & Marketing
```
Managed by: Project Shepherd
Agents: Growth Hacker, Content Creator, Social Media Strategist,
        App Store Optimizer

Sprint cadence: Aligned with Track A milestones
Activities:
- Growth Hacker → Design viral loops and referral mechanics
- Content Creator → Build launch content pipeline
- Social Media Strategist → Plan cross-platform campaign
- App Store Optimizer → Prepare store listing (if mobile)
```

### Piste C : Qualité & Opérations
```
Managed by: Agents Orchestrator
Agents: Evidence Collector, API Tester, Performance Benchmarker,
        Workflow Optimizer, Experiment Tracker

Continuous activities:
- Evidence Collector → Screenshot QA for every task
- API Tester → Endpoint validation for every API task
- Performance Benchmarker → Periodic load testing
- Workflow Optimizer → Process improvement identification
- Experiment Tracker → A/B test setup for validated features
```

### Piste D : Finitions Marque & Expérience
```
Managed by: Brand Guardian
Agents: UI Designer, Brand Guardian, Visual Storyteller,
        Whimsy Injector

Triggered activities:
- UI Designer → Component refinement when QA identifies visual issues
- Brand Guardian → Periodic brand consistency audit
- Visual Storyteller → Visual narrative assets as features complete
- Whimsy Injector → Micro-interactions and delight moments
```

## Modèle d'exécution de sprint

### Planification du sprint (jour 1)

```
Sprint Prioritizer activates:
1. Review backlog with updated RICE scores
2. Select tasks for sprint based on team velocity
3. Assign tasks to developer agents
4. Identify dependencies and ordering
5. Set sprint goal and success criteria

Output: Sprint Plan with task assignments
```

### Exécution quotidienne (jour 2 à jour N-1)

```
Agents Orchestrator manages:
1. Current task status check
2. Dev↔QA loop execution
3. Blocker identification and resolution
4. Progress tracking and reporting

Status report format:
- Tasks completed today: [list]
- Tasks in QA: [list]
- Tasks in development: [list]
- Blocked tasks: [list with reason]
- QA pass rate: [X/Y]
```

### Revue de sprint (jour N)

```
Project Shepherd facilitates:
1. Demo completed features
2. Review QA evidence for each task
3. Collect stakeholder feedback
4. Update backlog based on learnings

Participants: All active agents + stakeholders
Output: Sprint Review Summary
```

### Rétrospective de sprint

```
Workflow Optimizer facilitates:
1. What went well?
2. What could improve?
3. What will we change next sprint?
4. Process efficiency metrics

Output: Retrospective Action Items
```

## Logique de décision de l'orchestrateur

### Gestion d'échec de tâche

```
WHEN task fails QA:
  IF attempt == 1:
    → Send specific QA feedback to developer
    → Developer fixes ONLY the identified issues
    → Re-submit for QA
    
  IF attempt == 2:
    → Send accumulated QA feedback
    → Consider: Is the developer agent the right fit?
    → Developer fixes with additional context
    → Re-submit for QA
    
  IF attempt == 3:
    → ESCALATE
    → Options:
      a) Reassign to different developer agent
      b) Decompose task into smaller sub-tasks
      c) Revise approach/architecture
      d) Accept with known limitations (document)
      e) Defer to future sprint
    → Document decision and rationale
```

### Gestion des tâches parallèles

```
WHEN multiple tasks have no dependencies:
  → Assign to different developer agents simultaneously
  → Each runs independent Dev↔QA loop
  → Orchestrator tracks all loops concurrently
  → Merge completed tasks in dependency order

WHEN task has dependencies:
  → Wait for dependency to pass QA
  → Then assign dependent task
  → Include dependency context in handoff
```

## Check-list de la porte qualité

| # | Critère | Source de preuve | Statut |
|---|-----------|----------------|--------|
| 1 | Toutes les tâches du sprint passent la QA (100 % de complétion) | Captures d'écran de l'Evidence Collector par tâche | ☐ |
| 2 | Tous les endpoints d'API validés | Rapport de régression de l'API Tester | ☐ |
| 3 | Lignes de base de performance atteintes (P95 < 200ms) | Rapport du Performance Benchmarker | ☐ |
| 4 | Cohérence de marque vérifiée (95 %+ de conformité) | Audit du Brand Guardian | ☐ |
| 5 | Aucun bug critique (zéro P0/P1 ouvert) | Synthèse du Test Results Analyzer | ☐ |
| 6 | Tous les critères d'acceptation remplis | Vérification tâche par tâche | ☐ |
| 7 | Revue de code réalisée pour toutes les PR | Preuve dans l'historique Git | ☐ |

## Décision de porte

**Gardien de porte** : Agents Orchestrator

- **PASS** : application complète en fonctionnalités → activation de la phase 4
- **CONTINUE** : davantage de sprints nécessaires → poursuivre la phase 3
- **ESCALATE** : problèmes systémiques → intervention du Studio Producer

## Passation vers la phase 4

```markdown
## Phase 3 → Phase 4 Handoff Package

### For Reality Checker:
- Complete application (all features implemented)
- All QA evidence from Dev↔QA loops
- API Tester regression results
- Performance Benchmarker baseline data
- Brand Guardian consistency audit
- Known issues list (if any accepted limitations)

### For Legal Compliance Checker:
- Data handling implementation details
- Privacy policy implementation
- Consent management implementation
- Security measures implemented

### For Performance Benchmarker:
- Application URLs for load testing
- Expected traffic patterns
- Performance budgets from architecture

### For Infrastructure Maintainer:
- Production environment requirements
- Scaling configuration needs
- Monitoring alert thresholds
```

---

*La phase 3 est terminée lorsque toutes les tâches du sprint passent la QA, que tous les endpoints d'API sont validés, que les lignes de base de performance sont atteintes et qu'aucun bug critique ne reste ouvert.*
