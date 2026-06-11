# 🛡️ Playbook phase 4 — Qualité & Durcissement

> **Durée** : 3-7 jours | **Agents** : 8 | **Gardien de porte** : Reality Checker (autorité unique)

---

## Objectif

L'épreuve qualité finale. Le Reality Checker se positionne par défaut sur « NEEDS WORK » — vous devez prouver l'aptitude à la production avec des preuves écrasantes. Cette phase existe parce que les premières implémentations nécessitent généralement 2 à 3 cycles de révision, et c'est sain.

## Pré-conditions

- [ ] Porte qualité de la phase 3 franchie (toutes les tâches passées en QA)
- [ ] Package de passation de la phase 3 reçu
- [ ] Toutes les fonctionnalités implémentées et vérifiées individuellement

## État d'esprit critique

> **Le verdict par défaut du Reality Checker est NEEDS WORK.**
> 
> Ce n'est pas du pessimisme — c'est du réalisme. L'aptitude à la production exige :
> - Des parcours utilisateurs complets fonctionnant de bout en bout
> - Une cohérence cross-device (desktop, tablette, mobile)
> - De la performance sous charge (pas seulement le happy path)
> - Une validation de sécurité (pas juste « on a ajouté l'auth »)
> - Une conformité à la spécification (chaque exigence, pas la plupart)
>
> Une note B/B+ au premier passage est normale et attendue.

## Séquence d'activation des agents

### Étape 1 : Collecte des preuves (jour 1-2, tout en parallèle)

#### 📸 Evidence Collector — Preuves visuelles exhaustives
```
Activate Evidence Collector for comprehensive system evidence on [PROJECT].

Deliverables required:
1. Full screenshot suite:
   - Desktop (1920x1080) — every page/view
   - Tablet (768x1024) — every page/view
   - Mobile (375x667) — every page/view
2. Interaction evidence:
   - Navigation flows (before/after clicks)
   - Form interactions (empty, filled, submitted, error states)
   - Modal/dialog interactions
   - Accordion/expandable content
3. Theme evidence:
   - Light mode — all pages
   - Dark mode — all pages
   - System preference detection
4. Error state evidence:
   - 404 pages
   - Form validation errors
   - Network error handling
   - Empty states

Format: Screenshot Evidence Package with test-results.json
Timeline: 2 days
```

#### 🔌 API Tester — Régression API complète
```
Activate API Tester for complete API regression on [PROJECT].

Deliverables required:
1. Endpoint regression suite:
   - All endpoints tested (GET, POST, PUT, DELETE)
   - Authentication/authorization verification
   - Input validation testing
   - Error response verification
2. Integration testing:
   - Cross-service communication
   - Database operation verification
   - External API integration
3. Edge case testing:
   - Rate limiting behavior
   - Large payload handling
   - Concurrent request handling
   - Malformed input handling

Format: API Test Report with pass/fail per endpoint
Timeline: 2 days
```

#### ⚡ Performance Benchmarker — Test de charge
```
Activate Performance Benchmarker for load testing on [PROJECT].

Deliverables required:
1. Load test at 10x expected traffic:
   - Response time distribution (P50, P95, P99)
   - Throughput under load
   - Error rate under load
   - Resource utilization (CPU, memory, network)
2. Core Web Vitals measurement:
   - LCP (Largest Contentful Paint) < 2.5s
   - FID (First Input Delay) < 100ms
   - CLS (Cumulative Layout Shift) < 0.1
3. Database performance:
   - Query execution times
   - Connection pool utilization
   - Index effectiveness
4. Stress test results:
   - Breaking point identification
   - Graceful degradation behavior
   - Recovery time after overload

Format: Performance Certification Report
Timeline: 2 days
```

#### ⚖️ Legal Compliance Checker — Audit de conformité final
```
Activate Legal Compliance Checker for final compliance audit on [PROJECT].

Deliverables required:
1. Privacy compliance verification:
   - Privacy policy accuracy
   - Consent management functionality
   - Data subject rights implementation
   - Cookie consent implementation
2. Security compliance:
   - Data encryption (at rest and in transit)
   - Authentication security
   - Input sanitization
   - OWASP Top 10 check
3. Regulatory compliance:
   - GDPR requirements (if applicable)
   - CCPA requirements (if applicable)
   - Industry-specific requirements
4. Accessibility compliance:
   - WCAG 2.1 AA verification
   - Screen reader compatibility
   - Keyboard navigation

Format: Compliance Certification Report
Timeline: 2 days
```

### Étape 2 : Analyse (jour 3-4, en parallèle, après l'étape 1)

#### 📊 Test Results Analyzer — Agrégation des métriques qualité
```
Activate Test Results Analyzer for quality metrics aggregation on [PROJECT].

Input: ALL Step 1 reports
Deliverables required:
1. Aggregate quality dashboard:
   - Overall quality score
   - Category breakdown (visual, functional, performance, security, compliance)
   - Issue severity distribution
   - Trend analysis (if multiple test cycles)
2. Issue prioritization:
   - Critical issues (must fix before production)
   - High issues (should fix before production)
   - Medium issues (fix in next sprint)
   - Low issues (backlog)
3. Risk assessment:
   - Production readiness probability
   - Remaining risk areas
   - Recommended mitigations

Format: Quality Metrics Dashboard
Timeline: 1 day
```

#### 🔄 Workflow Optimizer — Revue de l'efficacité des processus
```
Activate Workflow Optimizer for process efficiency review on [PROJECT].

Input: Phase 3 execution data + Step 1 findings
Deliverables required:
1. Process efficiency analysis:
   - Dev↔QA loop efficiency (first-pass rate, average retries)
   - Bottleneck identification
   - Time-to-resolution for different issue types
2. Improvement recommendations:
   - Process changes for Phase 6 operations
   - Automation opportunities
   - Quality improvement suggestions

Format: Optimization Recommendations Report
Timeline: 1 day
```

#### 🏗️ Infrastructure Maintainer — Contrôle d'aptitude à la production
```
Activate Infrastructure Maintainer for production readiness on [PROJECT].

Deliverables required:
1. Production environment validation:
   - All services healthy and responding
   - Auto-scaling configured and tested
   - Load balancer configuration verified
   - SSL/TLS certificates valid
2. Monitoring validation:
   - All critical metrics being collected
   - Alert rules configured and tested
   - Dashboard access verified
   - Log aggregation working
3. Disaster recovery validation:
   - Backup systems operational
   - Recovery procedures documented and tested
   - Failover mechanisms verified
4. Security validation:
   - Firewall rules reviewed
   - Access controls verified
   - Secrets management confirmed
   - Vulnerability scan clean

Format: Infrastructure Readiness Report
Timeline: 1 day
```

### Étape 3 : Jugement final (jour 5-7, en séquentiel)

#### 🔍 Reality Checker — LE VERDICT FINAL
```
Activate Reality Checker for final integration testing on [PROJECT].

MANDATORY PROCESS — DO NOT SKIP:

Step 1: Reality Check Commands
- Verify what was actually built (ls, grep for claimed features)
- Cross-check claimed features against specification
- Run comprehensive screenshot capture
- Review all evidence from Step 1 and Step 2

Step 2: QA Cross-Validation
- Review Evidence Collector findings
- Cross-reference with API Tester results
- Verify Performance Benchmarker data
- Confirm Legal Compliance Checker findings

Step 3: End-to-End System Validation
- Test COMPLETE user journeys (not individual features)
- Verify responsive behavior across ALL devices
- Check interaction flows end-to-end
- Review actual performance data

Step 4: Specification Reality Check
- Quote EXACT text from original specification
- Compare with ACTUAL implementation evidence
- Document EVERY gap between spec and reality
- No assumptions — evidence only

VERDICT OPTIONS:
- READY: Overwhelming evidence of production readiness (rare first pass)
- NEEDS WORK: Specific issues identified with fix list (expected)
- NOT READY: Major architectural issues requiring Phase 1/2 revisit

Format: Reality-Based Integration Report
Default: NEEDS WORK unless proven otherwise
```

## Porte qualité — LA PORTE FINALE

| # | Critère | Seuil | Preuve requise |
|---|-----------|-----------|-------------------|
| 1 | Parcours utilisateurs complets | Tous les chemins critiques fonctionnent de bout en bout | Captures d'écran du Reality Checker |
| 2 | Cohérence cross-device | Desktop + tablette + mobile fonctionnent tous | Captures d'écran responsive |
| 3 | Performance certifiée | P95 < 200ms, LCP < 2.5s, uptime > 99,9 % | Rapport du Performance Benchmarker |
| 4 | Sécurité validée | Zéro vulnérabilité critique | Scan de sécurité + rapport de conformité |
| 5 | Conformité certifiée | Toutes les exigences réglementaires remplies | Rapport du Legal Compliance Checker |
| 6 | Conformité à la spécification | 100 % des exigences de la spec implémentées | Vérification point par point |
| 7 | Infrastructure prête | Environnement de production validé | Rapport de l'Infrastructure Maintainer |

## Décision de porte

**Autorité unique** : Reality Checker

### Si READY (passer à la phase 5) :
```markdown
## Phase 4 → Phase 5 Handoff Package

### For Launch Team:
- Reality Checker certification report
- Performance certification
- Compliance certification
- Infrastructure readiness report
- Known limitations (if any)

### For Growth Hacker:
- Product ready for users
- Feature list for marketing messaging
- Performance data for credibility

### For DevOps Automator:
- Production deployment approved
- Blue-green deployment plan
- Rollback procedures confirmed
```

### Si NEEDS WORK (retour à la phase 3) :
```markdown
## Phase 4 → Phase 3 Return Package

### Fix List (from Reality Checker):
1. [Critical Issue 1]: [Description + evidence + fix instruction]
2. [Critical Issue 2]: [Description + evidence + fix instruction]
3. [High Issue 1]: [Description + evidence + fix instruction]
...

### Process:
- Issues enter Dev↔QA loop (Phase 3 mechanics)
- Each fix must pass Evidence Collector QA
- When all fixes complete → Return to Phase 4 Step 3
- Reality Checker re-evaluates with updated evidence

### Expected: 2-3 revision cycles is normal
```

### Si NOT READY (retour à la phase 1/2) :
```markdown
## Phase 4 → Phase 1/2 Return Package

### Architectural Issues Identified:
1. [Fundamental Issue]: [Why it can't be fixed in Phase 3]
2. [Structural Problem]: [What needs to change at architecture level]

### Recommended Action:
- [ ] Revise system architecture (Phase 1)
- [ ] Rebuild foundation (Phase 2)
- [ ] Descope and redefine (Phase 1)

### Studio Producer Decision Required
```

---

*La phase 4 est terminée lorsque le Reality Checker émet un verdict READY avec des preuves écrasantes. NEEDS WORK est le résultat attendu au premier passage — cela signifie que le système fonctionne mais nécessite des finitions.*
