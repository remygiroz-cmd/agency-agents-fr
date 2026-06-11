# 🚨 Runbook : Réponse aux incidents

> **Mode** : NEXUS-Micro | **Durée** : de quelques minutes à quelques heures | **Agents** : 3-8

---

## Scénario

Quelque chose est cassé en production. Des utilisateurs sont impactés. La rapidité de réponse compte, mais bien faire les choses aussi. Ce runbook couvre de la détection au post-mortem.

## Classification de la gravité

| Niveau | Définition | Exemples | Délai de réponse |
|-------|-----------|----------|--------------|
| **P0 — Critique** | Service totalement down, perte de données, faille de sécurité | Corruption de base de données, attaque DDoS, panne du système d'auth | Immédiat (toutes ressources) |
| **P1 — Élevé** | Fonctionnalité majeure cassée, dégradation significative des performances | Traitement des paiements down, taux d'erreur 50 %+, latence x10 | < 1 heure |
| **P2 — Moyen** | Fonctionnalité mineure cassée, contournement disponible | Recherche en panne, erreurs d'API non critiques | < 4 heures |
| **P3 — Faible** | Problème cosmétique, gêne mineure | Bug de style, faute de frappe, glitch d'UI mineur | Sprint suivant |

## Équipes de réponse par gravité

### P0 — Équipe de réponse aux incidents critiques
| Agent | Rôle | Action |
|-------|------|--------|
| **Infrastructure Maintainer** | Commandant de l'incident | Évaluer l'ampleur, coordonner la réponse |
| **DevOps Automator** | Déploiement/rollback | Exécuter le rollback si nécessaire |
| **Backend Architect** | Investigation de la cause racine | Diagnostiquer les problèmes système |
| **Frontend Developer** | Investigation côté UI | Diagnostiquer les problèmes côté client |
| **Support Responder** | Communication utilisateur | Mises à jour de la page de statut, notifications aux utilisateurs |
| **Executive Summary Generator** | Communication aux parties prenantes | Points exécutifs en temps réel |

### P1 — Équipe de réponse élevée
| Agent | Rôle |
|-------|------|
| **Infrastructure Maintainer** | Commandant de l'incident |
| **DevOps Automator** | Support au déploiement |
| **Agent développeur concerné** | Implémentation du correctif |
| **Support Responder** | Communication utilisateur |

### P2 — Réponse moyenne
| Agent | Rôle |
|-------|------|
| **Agent développeur concerné** | Implémentation du correctif |
| **Evidence Collector** | Vérifier le correctif |

### P3 — Réponse faible
| Agent | Rôle |
|-------|------|
| **Sprint Prioritizer** | Ajouter au backlog |

## Séquence de réponse aux incidents

### Étape 1 : Détection & Tri (0-5 minutes)

```
TRIGGER: Alert from monitoring / User report / Agent detection

Infrastructure Maintainer:
1. Acknowledge alert
2. Assess scope and impact
   - How many users affected?
   - Which services are impacted?
   - Is data at risk?
3. Classify severity (P0/P1/P2/P3)
4. Activate appropriate response team
5. Create incident channel/thread

Output: Incident classification + response team activated
```

### Étape 2 : Investigation (5-30 minutes)

```
PARALLEL INVESTIGATION:

Infrastructure Maintainer:
├── Check system metrics (CPU, memory, network, disk)
├── Review error logs
├── Check recent deployments
└── Verify external dependencies

Backend Architect (if P0/P1):
├── Check database health
├── Review API error rates
├── Check service communication
└── Identify failing component

DevOps Automator:
├── Review recent deployment history
├── Check CI/CD pipeline status
├── Prepare rollback if needed
└── Verify infrastructure state

Output: Root cause identified (or narrowed to component)
```

### Étape 3 : Mitigation (15-60 minutes)

```
DECISION TREE:

IF caused by recent deployment:
  → DevOps Automator: Execute rollback
  → Infrastructure Maintainer: Verify recovery
  → Evidence Collector: Confirm fix

IF caused by infrastructure issue:
  → Infrastructure Maintainer: Scale/restart/failover
  → DevOps Automator: Support infrastructure changes
  → Verify recovery

IF caused by code bug:
  → Relevant Developer Agent: Implement hotfix
  → Evidence Collector: Verify fix
  → DevOps Automator: Deploy hotfix
  → Infrastructure Maintainer: Monitor recovery

IF caused by external dependency:
  → Infrastructure Maintainer: Activate fallback/cache
  → Support Responder: Communicate to users
  → Monitor for external recovery

THROUGHOUT:
  → Support Responder: Update status page every 15 minutes
  → Executive Summary Generator: Brief stakeholders (P0 only)
```

### Étape 4 : Vérification de la résolution (après correctif)

```
Evidence Collector:
1. Verify the fix resolves the issue
2. Screenshot evidence of working state
3. Confirm no new issues introduced

Infrastructure Maintainer:
1. Verify all metrics returning to normal
2. Confirm no cascading failures
3. Monitor for 30 minutes post-fix

API Tester (if API-related):
1. Run regression on affected endpoints
2. Verify response times normalized
3. Confirm error rates at baseline

Output: Incident resolved confirmation
```

### Étape 5 : Post-mortem (sous 48 heures)

```
Workflow Optimizer leads post-mortem:

1. Timeline reconstruction
   - When was the issue introduced?
   - When was it detected?
   - When was it resolved?
   - Total user impact duration

2. Root cause analysis
   - What failed?
   - Why did it fail?
   - Why wasn't it caught earlier?
   - 5 Whys analysis

3. Impact assessment
   - Users affected
   - Revenue impact
   - Reputation impact
   - Data impact

4. Prevention measures
   - What monitoring would have caught this sooner?
   - What testing would have prevented this?
   - What process changes are needed?
   - What infrastructure changes are needed?

5. Action items
   - [Action] → [Owner] → [Deadline]
   - [Action] → [Owner] → [Deadline]
   - [Action] → [Owner] → [Deadline]

Output: Post-Mortem Report → Sprint Prioritizer adds prevention tasks to backlog
```

## Modèles de communication

### Mise à jour de la page de statut (Support Responder)
```
[TIMESTAMP] — [SERVICE NAME] Incident

Status: [Investigating / Identified / Monitoring / Resolved]
Impact: [Description of user impact]
Current action: [What we're doing about it]
Next update: [When to expect the next update]
```

### Point exécutif (Executive Summary Generator — P0 uniquement)
```
INCIDENT BRIEF — [TIMESTAMP]

SITUATION: [Service] is [down/degraded] affecting [N users/% of traffic]
CAUSE: [Known/Under investigation] — [Brief description if known]
ACTION: [What's being done] — ETA [time estimate]
IMPACT: [Business impact — revenue, users, reputation]
NEXT UPDATE: [Timestamp]
```

## Matrice d'escalade

| Condition | Escalader vers | Action |
|-----------|------------|--------|
| P0 non résolu en 30 min | Studio Producer | Ressources supplémentaires, escalade fournisseur |
| P1 non résolu en 2 heures | Project Shepherd | Réallocation des ressources |
| Faille de données suspectée | Legal Compliance Checker | Évaluation de la notification réglementaire |
| Données utilisateurs impactées | Legal Compliance Checker + Executive Summary Generator | Notification GDPR/CCPA |
| Impact sur le chiffre d'affaires > X $ | Finance Tracker + Studio Producer | Évaluation de l'impact métier |
