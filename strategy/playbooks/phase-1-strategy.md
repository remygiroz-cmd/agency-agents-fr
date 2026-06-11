# 🏗️ Playbook phase 1 — Stratégie & Architecture

> **Durée** : 5-10 jours | **Agents** : 8 | **Gardiens de porte** : Studio Producer + Reality Checker

---

## Objectif

Définir ce que l'on construit, comment c'est structuré et à quoi ressemble le succès — avant d'écrire la moindre ligne de code. Chaque décision d'architecture est documentée. Chaque fonctionnalité est priorisée. Chaque dollar est justifié.

## Pré-conditions

- [ ] Porte qualité de la phase 0 franchie (décision GO)
- [ ] Package de passation de la phase 0 reçu
- [ ] Alignement des parties prenantes sur le périmètre du projet

## Séquence d'activation des agents

### Étape 1 : Cadrage stratégique (jour 1-3, en parallèle)

#### 🎬 Studio Producer — Alignement du portefeuille stratégique
```
Activate Studio Producer for strategic portfolio alignment on [PROJECT].

Input: Phase 0 Executive Summary + Market Analysis Report
Deliverables required:
1. Strategic Portfolio Plan with project positioning
2. Vision, objectives, and ROI targets
3. Resource allocation strategy
4. Risk/reward assessment
5. Success criteria and milestone definitions

Align with: Organizational strategic objectives
Format: Strategic Portfolio Plan Template
Timeline: 3 days
```

#### 🎭 Brand Guardian — Système d'identité de marque
```
Activate Brand Guardian for brand identity development on [PROJECT].

Input: Phase 0 UX Research (personas, journey maps)
Deliverables required:
1. Brand Foundation (purpose, vision, mission, values, personality)
2. Visual Identity System (colors, typography, spacing as CSS variables)
3. Brand Voice and Messaging Architecture
4. Logo system specifications (if new brand)
5. Brand usage guidelines

Format: Brand Identity System Document
Timeline: 3 days
```

#### 💰 Finance Tracker — Planification du budget et des ressources
```
Activate Finance Tracker for financial planning on [PROJECT].

Input: Studio Producer strategic plan + Phase 0 Tech Stack Assessment
Deliverables required:
1. Comprehensive project budget with category breakdown
2. Resource cost projections (agents, infrastructure, tools)
3. ROI model with break-even analysis
4. Cash flow timeline
5. Financial risk assessment with contingency reserves

Format: Financial Plan with ROI Projections
Timeline: 2 days
```

### Étape 2 : Architecture technique (jour 3-7, en parallèle, une fois les sorties de l'étape 1 disponibles)

#### 🏛️ UX Architect — Architecture technique + Fondation UX
```
Activate UX Architect for technical architecture on [PROJECT].

Input: Brand Guardian visual identity + Phase 0 UX Research
Deliverables required:
1. CSS Design System (variables, tokens, scales)
2. Layout Framework (Grid/Flexbox patterns, responsive breakpoints)
3. Component Architecture (naming conventions, hierarchy)
4. Information Architecture (page flow, content hierarchy)
5. Theme System (light/dark/system toggle)
6. Accessibility Foundation (WCAG 2.1 AA baseline)

Files to create:
- css/design-system.css
- css/layout.css
- css/components.css
- docs/ux-architecture.md

Format: Developer-Ready Foundation Package
Timeline: 4 days
```

#### 🏗️ Backend Architect — Architecture système
```
Activate Backend Architect for system architecture on [PROJECT].

Input: Phase 0 Tech Stack Assessment + Compliance Requirements
Deliverables required:
1. System Architecture Specification
   - Architecture pattern (microservices/monolith/serverless/hybrid)
   - Communication pattern (REST/GraphQL/gRPC/event-driven)
   - Data pattern (CQRS/Event Sourcing/CRUD)
2. Database Schema Design with indexing strategy
3. API Design Specification with versioning
4. Authentication and Authorization Architecture
5. Security Architecture (defense in depth)
6. Scalability Plan (horizontal scaling strategy)

Format: System Architecture Specification
Timeline: 4 days
```

#### 🤖 AI Engineer — Architecture ML (le cas échéant)
```
Activate AI Engineer for ML system architecture on [PROJECT].

Input: Backend Architect system architecture + Phase 0 Data Audit
Deliverables required:
1. ML System Design
   - Model selection and training strategy
   - Data pipeline architecture
   - Inference strategy (real-time/batch/edge)
2. AI Ethics and Safety Framework
3. Model monitoring and retraining plan
4. Integration points with main application
5. Cost projections for ML infrastructure

Condition: Only activate if project includes AI/ML features
Format: ML System Design Document
Timeline: 3 days
```

#### 👔 Senior Project Manager — Conversion spec-vers-tâches
```
Activate Senior Project Manager for task list creation on [PROJECT].

Input: ALL Phase 0 documents + Architecture specs (as available)
Deliverables required:
1. Comprehensive Task List
   - Quote EXACT requirements from spec (no luxury features)
   - Each task has clear acceptance criteria
   - Dependencies mapped between tasks
   - Effort estimates (story points or hours)
2. Work Breakdown Structure
3. Critical path identification
4. Risk register for implementation

Rules:
- Do NOT add features not in the specification
- Quote exact text from requirements
- Be realistic about effort estimates

Format: Task List with acceptance criteria
Timeline: 3 days
```

### Étape 3 : Priorisation (jour 7-10, en séquentiel, après l'étape 2)

#### 🎯 Sprint Prioritizer — Priorisation des fonctionnalités
```
Activate Sprint Prioritizer for backlog prioritization on [PROJECT].

Input:
- Senior Project Manager → Task List
- Backend Architect → System Architecture
- UX Architect → UX Architecture
- Finance Tracker → Budget Framework
- Studio Producer → Strategic Plan

Deliverables required:
1. RICE-scored backlog (Reach, Impact, Confidence, Effort)
2. Sprint assignments with velocity-based estimation
3. Dependency map with critical path
4. MoSCoW classification (Must/Should/Could/Won't)
5. Release plan with milestone mapping

Validation: Studio Producer confirms strategic alignment
Format: Prioritized Sprint Plan
Timeline: 2 days
```

## Check-list de la porte qualité

| # | Critère | Source de preuve | Statut |
|---|-----------|----------------|--------|
| 1 | L'architecture couvre 100 % des exigences de la spec | Liste de tâches du Senior PM recoupée avec l'architecture | ☐ |
| 2 | Système de marque complet (logo, couleurs, typographie, voix) | Livrable du Brand Guardian | ☐ |
| 3 | Tous les composants techniques ont une voie d'implémentation | Specs Backend Architect + UX Architect | ☐ |
| 4 | Budget approuvé et dans les limites | Plan du Finance Tracker | ☐ |
| 5 | Le plan de sprint est fondé sur la vélocité et réaliste | Backlog du Sprint Prioritizer | ☐ |
| 6 | Architecture de sécurité définie | Spec de sécurité du Backend Architect | ☐ |
| 7 | Exigences de conformité intégrées à l'architecture | Exigences légales rattachées aux décisions techniques | ☐ |

## Décision de porte

**Double validation requise** : Studio Producer (stratégique) + Reality Checker (technique)

- **APPROVED** : passer à la phase 2 avec le package d'architecture complet
- **REVISE** : des éléments précis nécessitent une reprise (revenir à l'étape concernée)
- **RESTRUCTURE** : problèmes d'architecture fondamentaux (recommencer la phase 1)

## Passation vers la phase 2

```markdown
## Phase 1 → Phase 2 Handoff Package

### Architecture Package:
1. Strategic Portfolio Plan (Studio Producer)
2. Brand Identity System (Brand Guardian)
3. Financial Plan (Finance Tracker)
4. CSS Design System + UX Architecture (UX Architect)
5. System Architecture Specification (Backend Architect)
6. ML System Design (AI Engineer — if applicable)
7. Comprehensive Task List (Senior Project Manager)
8. Prioritized Sprint Plan (Sprint Prioritizer)

### For DevOps Automator:
- Deployment architecture from Backend Architect
- Environment requirements from System Architecture
- Monitoring requirements from Infrastructure needs

### For Frontend Developer:
- CSS Design System from UX Architect
- Brand Identity from Brand Guardian
- Component architecture from UX Architect
- API specification from Backend Architect

### For Backend Architect (continuing):
- Database schema ready for deployment
- API scaffold ready for implementation
- Auth system architecture defined
```

---

*La phase 1 est terminée lorsque le Studio Producer et le Reality Checker valident tous deux le package d'architecture.*
