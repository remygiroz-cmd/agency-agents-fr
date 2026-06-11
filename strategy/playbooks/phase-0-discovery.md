# 🔍 Playbook phase 0 — Intelligence & Discovery

> **Durée** : 3-7 jours | **Agents** : 6 | **Gardien de porte** : Executive Summary Generator

---

## Objectif

Valider l'opportunité avant d'engager des ressources. Aucune construction tant que le problème, le marché et le paysage réglementaire ne sont pas compris.

## Pré-conditions

- [ ] Un brief de projet ou un concept initial existe
- [ ] Un sponsor parmi les parties prenantes est identifié
- [ ] Le budget de la phase de discovery est approuvé

## Séquence d'activation des agents

### Vague 1 : lancement parallèle (jour 1)

#### 🔍 Trend Researcher — Responsable de l'intelligence de marché
```
Activate Trend Researcher for market intelligence on [PROJECT DOMAIN].

Deliverables required:
1. Competitive landscape analysis (direct + indirect competitors)
2. Market sizing: TAM, SAM, SOM with methodology
3. Trend lifecycle mapping: where is this market in the adoption curve?
4. 3-6 month trend forecast with confidence intervals
5. Investment and funding trends in the space

Sources: Minimum 15 unique, verified sources
Format: Strategic Report with executive summary
Timeline: 3 days
```

#### 💬 Feedback Synthesizer — Analyse des besoins utilisateurs
```
Activate Feedback Synthesizer for user needs analysis on [PROJECT DOMAIN].

Deliverables required:
1. Multi-channel feedback collection plan (surveys, interviews, reviews, social)
2. Sentiment analysis across existing user touchpoints
3. Pain point identification and prioritization (RICE scored)
4. Feature request analysis with business value estimation
5. Churn risk indicators from feedback patterns

Format: Synthesized Feedback Report with priority matrix
Timeline: 3 days
```

#### 🔍 UX Researcher — Analyse du comportement utilisateur
```
Activate UX Researcher for user behavior analysis on [PROJECT DOMAIN].

Deliverables required:
1. User interview plan (5-10 target users)
2. Persona development (3-5 primary personas)
3. Journey mapping for primary user flows
4. Usability heuristic evaluation of competitor products
5. Behavioral insights with statistical validation

Format: Research Findings Report with personas and journey maps
Timeline: 5 days
```

### Vague 2 : lancement parallèle (jour 1, indépendant de la vague 1)

#### 📊 Analytics Reporter — Évaluation du paysage de données
```
Activate Analytics Reporter for data landscape assessment on [PROJECT DOMAIN].

Deliverables required:
1. Existing data source audit (what data is available?)
2. Signal identification (what can we measure?)
3. Baseline metrics establishment
4. Data quality assessment with completeness scoring
5. Analytics infrastructure recommendations

Format: Data Audit Report with signal map
Timeline: 2 days
```

#### ⚖️ Legal Compliance Checker — Scan réglementaire
```
Activate Legal Compliance Checker for regulatory scan on [PROJECT DOMAIN].

Deliverables required:
1. Applicable regulatory frameworks (GDPR, CCPA, HIPAA, etc.)
2. Data handling requirements and constraints
3. Jurisdiction mapping for target markets
4. Compliance risk assessment with severity ratings
5. Blocking vs. manageable compliance issues

Format: Compliance Requirements Matrix
Timeline: 3 days
```

#### 🛠️ Tool Evaluator — Paysage technologique
```
Activate Tool Evaluator for technology landscape assessment on [PROJECT DOMAIN].

Deliverables required:
1. Technology stack assessment for the problem domain
2. Build vs. buy analysis for key components
3. Integration feasibility with existing systems
4. Open source vs. commercial evaluation
5. Technology risk assessment

Format: Tech Stack Assessment with recommendation matrix
Timeline: 2 days
```

## Point de convergence (jour 5-7)

Les six agents livrent leurs rapports. L'Executive Summary Generator les synthétise :

```
Activate Executive Summary Generator to synthesize Phase 0 findings.

Input documents:
1. Trend Researcher → Market Analysis Report
2. Feedback Synthesizer → Synthesized Feedback Report
3. UX Researcher → Research Findings Report
4. Analytics Reporter → Data Audit Report
5. Legal Compliance Checker → Compliance Requirements Matrix
6. Tool Evaluator → Tech Stack Assessment

Output: Executive Summary (≤500 words, SCQA format)
Decision required: GO / NO-GO / PIVOT
Include: Quantified market opportunity, validated user needs, regulatory path, technology feasibility
```

## Check-list de la porte qualité

| # | Critère | Source de preuve | Statut |
|---|-----------|----------------|--------|
| 1 | Opportunité de marché validée avec un TAM > seuil minimal viable | Rapport du Trend Researcher | ☐ |
| 2 | ≥3 pain points utilisateurs validés, étayés par des données | Feedback Synthesizer + UX Researcher | ☐ |
| 3 | Aucun problème de conformité bloquant identifié | Matrice du Legal Compliance Checker | ☐ |
| 4 | Indicateurs clés et sources de données identifiés | Audit de l'Analytics Reporter | ☐ |
| 5 | Stack technologique faisable et évaluée | Évaluation du Tool Evaluator | ☐ |
| 6 | Synthèse exécutive livrée avec recommandation GO/NO-GO | Executive Summary Generator | ☐ |

## Décision de porte

- **GO** : passer à la phase 1 — Stratégie & Architecture
- **NO-GO** : archiver les conclusions, documenter les enseignements, réorienter les ressources
- **PIVOT** : modifier le périmètre/la direction d'après les conclusions, relancer une discovery ciblée

## Passation vers la phase 1

```markdown
## Phase 0 → Phase 1 Handoff Package

### Documents to carry forward:
1. Market Analysis Report (Trend Researcher)
2. Synthesized Feedback Report (Feedback Synthesizer)
3. User Personas and Journey Maps (UX Researcher)
4. Data Audit Report (Analytics Reporter)
5. Compliance Requirements Matrix (Legal Compliance Checker)
6. Tech Stack Assessment (Tool Evaluator)
7. Executive Summary with GO decision (Executive Summary Generator)

### Key constraints identified:
- [Regulatory constraints from Legal Compliance Checker]
- [Technical constraints from Tool Evaluator]
- [Market timing constraints from Trend Researcher]

### Priority user needs (for Sprint Prioritizer):
1. [Pain point 1 — from Feedback Synthesizer]
2. [Pain point 2 — from UX Researcher]
3. [Pain point 3 — from Feedback Synthesizer]
```

---

*La phase 0 est terminée lorsque l'Executive Summary Generator livre une décision GO étayée par les preuves des six agents de discovery.*
