# ⚙️ Playbook phase 2 — Fondations & Scaffolding

> **Durée** : 3-5 jours | **Agents** : 6 | **Gardiens de porte** : DevOps Automator + Evidence Collector

---

## Objectif

Construire les fondations techniques et opérationnelles dont dépend tout le travail ultérieur. Faire tenir le squelette debout avant d'ajouter le muscle. À l'issue de cette phase, chaque développeur dispose d'un environnement fonctionnel, d'un pipeline déployable et d'un design system pour construire.

## Pré-conditions

- [ ] Porte qualité de la phase 1 franchie (package d'architecture approuvé)
- [ ] Package de passation de la phase 1 reçu
- [ ] Tous les documents d'architecture finalisés

## Séquence d'activation des agents

### Flux de travail A : Infrastructure (jour 1-3, en parallèle)

#### 🚀 DevOps Automator — Pipeline CI/CD + Infrastructure
```
Activate DevOps Automator for infrastructure setup on [PROJECT].

Input: Backend Architect system architecture + deployment requirements
Deliverables required:
1. CI/CD Pipeline (GitHub Actions / GitLab CI)
   - Security scanning stage
   - Automated testing stage
   - Build and containerization stage
   - Deployment stage (blue-green or canary)
   - Automated rollback capability
2. Infrastructure as Code
   - Environment provisioning (dev, staging, production)
   - Container orchestration setup
   - Network and security configuration
3. Environment Configuration
   - Secrets management
   - Environment variable management
   - Multi-environment parity

Files to create:
- .github/workflows/ci-cd.yml (or equivalent)
- infrastructure/ (Terraform/CDK templates)
- docker-compose.yml
- Dockerfile(s)

Format: Working CI/CD pipeline with IaC templates
Timeline: 3 days
```

#### 🏗️ Infrastructure Maintainer — Infrastructure cloud + Monitoring
```
Activate Infrastructure Maintainer for monitoring setup on [PROJECT].

Input: DevOps Automator infrastructure + Backend Architect architecture
Deliverables required:
1. Cloud Resource Provisioning
   - Compute, storage, networking resources
   - Auto-scaling configuration
   - Load balancer setup
2. Monitoring Stack
   - Application metrics (Prometheus/DataDog)
   - Infrastructure metrics
   - Custom dashboards (Grafana)
3. Logging and Alerting
   - Centralized log aggregation
   - Alert rules for critical thresholds
   - On-call notification setup
4. Security Hardening
   - Firewall rules
   - SSL/TLS configuration
   - Access control policies

Format: Infrastructure Readiness Report with dashboard access
Timeline: 3 days
```

#### ⚙️ Studio Operations — Mise en place des processus
```
Activate Studio Operations for process setup on [PROJECT].

Input: Sprint Prioritizer plan + Project Shepherd coordination needs
Deliverables required:
1. Git Workflow
   - Branch strategy (GitFlow / trunk-based)
   - PR review process
   - Merge policies
2. Communication Channels
   - Team channels setup
   - Notification routing
   - Status update cadence
3. Documentation Templates
   - PR template
   - Issue template
   - Decision log template
4. Collaboration Tools
   - Project board setup
   - Sprint tracking configuration

Format: Operations Playbook
Timeline: 2 days
```

### Flux de travail B : Fondation applicative (jour 1-4, en parallèle)

#### 🎨 Frontend Developer — Scaffolding du projet + Bibliothèque de composants
```
Activate Frontend Developer for project scaffolding on [PROJECT].

Input: UX Architect CSS Design System + Brand Guardian identity
Deliverables required:
1. Project Scaffolding
   - Framework setup (React/Vue/Angular per architecture)
   - TypeScript configuration
   - Build tooling (Vite/Webpack/Next.js)
   - Testing framework (Jest/Vitest + Testing Library)
2. Design System Implementation
   - CSS design tokens from UX Architect
   - Base component library (Button, Input, Card, Layout)
   - Theme system (light/dark/system toggle)
   - Responsive utilities
3. Application Shell
   - Routing setup
   - Layout components (Header, Footer, Sidebar)
   - Error boundary implementation
   - Loading states

Files to create:
- src/ (application source)
- src/components/ (component library)
- src/styles/ (design tokens)
- src/layouts/ (layout components)

Format: Working application skeleton with component library
Timeline: 3 days
```

#### 🏗️ Backend Architect — Base de données + Fondation API
```
Activate Backend Architect for API foundation on [PROJECT].

Input: System Architecture Specification + Database Schema Design
Deliverables required:
1. Database Setup
   - Schema deployment (migrations)
   - Index creation
   - Seed data for development
   - Connection pooling configuration
2. API Scaffold
   - Framework setup (Express/FastAPI/etc.)
   - Route structure matching architecture
   - Middleware stack (auth, validation, error handling, CORS)
   - Health check endpoints
3. Authentication System
   - Auth provider integration
   - JWT/session management
   - Role-based access control scaffold
4. Service Communication
   - API versioning setup
   - Request/response serialization
   - Error response standardization

Files to create:
- api/ or server/ (backend source)
- migrations/ (database migrations)
- docs/api-spec.yaml (OpenAPI specification)

Format: Working API scaffold with database and auth
Timeline: 4 days
```

#### 🏛️ UX Architect — Implémentation du système CSS
```
Activate UX Architect for CSS system implementation on [PROJECT].

Input: Brand Guardian identity + own Phase 1 CSS Design System spec
Deliverables required:
1. Design Tokens Implementation
   - CSS custom properties (colors, typography, spacing)
   - Brand color palette with semantic naming
   - Typography scale with responsive adjustments
2. Layout System
   - Container system (responsive breakpoints)
   - Grid patterns (2-col, 3-col, sidebar)
   - Flexbox utilities
3. Theme System
   - Light theme variables
   - Dark theme variables
   - System preference detection
   - Theme toggle component
   - Smooth transition between themes

Files to create/update:
- css/design-system.css (or equivalent in framework)
- css/layout.css
- css/components.css
- js/theme-manager.js

Format: Implemented CSS design system with theme toggle
Timeline: 2 days
```

## Point de vérification (jour 4-5)

### Vérification par l'Evidence Collector
```
Activate Evidence Collector for Phase 2 foundation verification.

Verify the following with screenshot evidence:
1. CI/CD pipeline executes successfully (show pipeline logs)
2. Application skeleton loads in browser (desktop screenshot)
3. Application skeleton loads on mobile (mobile screenshot)
4. Theme toggle works (light + dark screenshots)
5. API health check responds (curl output)
6. Database is accessible (migration status)
7. Monitoring dashboards are active (dashboard screenshot)
8. Component library renders (component demo page)

Format: Evidence Package with screenshots
Verdict: PASS / FAIL with specific issues
```

## Check-list de la porte qualité

| # | Critère | Source de preuve | Statut |
|---|-----------|----------------|--------|
| 1 | Le pipeline CI/CD build, teste et déploie | Logs d'exécution du pipeline | ☐ |
| 2 | Schéma de base de données déployé avec toutes les tables/index | Sortie de succès des migrations | ☐ |
| 3 | Scaffold d'API répondant au health check | Preuve de réponse curl | ☐ |
| 4 | Le squelette frontend s'affiche dans le navigateur | Captures d'écran de l'Evidence Collector | ☐ |
| 5 | Tableaux de bord de monitoring affichant des métriques | Captures d'écran des tableaux de bord | ☐ |
| 6 | Tokens du design system implémentés | Démo de la bibliothèque de composants | ☐ |
| 7 | Bascule de thème fonctionnelle (light/dark/system) | Captures d'écran avant/après | ☐ |
| 8 | Workflow Git et processus documentés | Playbook de Studio Operations | ☐ |

## Décision de porte

**Double validation requise** : DevOps Automator (infrastructure) + Evidence Collector (visuel)

- **PASS** : squelette fonctionnel avec pipeline DevOps complet → activation de la phase 3
- **FAIL** : problèmes spécifiques d'infrastructure ou d'application → corriger et revérifier

## Passation vers la phase 3

```markdown
## Phase 2 → Phase 3 Handoff Package

### For all Developer Agents:
- Working CI/CD pipeline (auto-deploys on merge)
- Design system tokens and component library
- API scaffold with auth and health checks
- Database with schema and seed data
- Git workflow and PR process

### For Evidence Collector (ongoing QA):
- Application URLs (dev, staging)
- Screenshot capture methodology
- Component library reference
- Brand guidelines for visual verification

### For Agents Orchestrator (Dev↔QA loop management):
- Sprint Prioritizer backlog (from Phase 1)
- Task list with acceptance criteria (from Phase 1)
- Agent assignment matrix (from NEXUS strategy)
- Quality thresholds for each task type

### Environment Access:
- Dev environment: [URL]
- Staging environment: [URL]
- Monitoring dashboard: [URL]
- CI/CD pipeline: [URL]
- API documentation: [URL]
```

---

*La phase 2 est terminée lorsque l'application squelette tourne, que le pipeline CI/CD est opérationnel et que l'Evidence Collector a vérifié tous les éléments de fondation par captures d'écran.*
