# Nexus Spatial : exercice de découverte par l'agence au complet

> **Type d'exercice :** Découverte produit multi-agents
> **Date :** 5 mars 2026
> **Agents déployés :** 8 (en parallèle)
> **Durée :** ~10 minutes en temps réel
> **Objectif :** Démontrer l'orchestration de l'agence entière, de l'identification d'une opportunité jusqu'à une planification complète

---

## Table des matières

1. [L'opportunité](#1-the-opportunity)
2. [Validation de marché](#2-market-validation)
3. [Architecture technique](#3-technical-architecture)
4. [Stratégie de marque](#4-brand-strategy)
5. [Go-to-Market et croissance](#5-go-to-market--growth)
6. [Blueprint du support client](#6-customer-support-blueprint)
7. [Recherche UX et direction de design](#7-ux-research--design-direction)
8. [Plan d'exécution du projet](#8-project-execution-plan)
9. [Architecture de l'interface spatiale](#9-spatial-interface-architecture)
10. [Synthèse inter-agents](#10-cross-agent-synthesis)

---

## 1. L'opportunité

### Comment elle a été trouvée

Une recherche web sur plusieurs sources a identifié trois tendances convergentes :

- **L'infrastructure/orchestration d'IA** est la catégorie logicielle à la croissance la plus rapide (marché de l'orchestration d'IA évalué à ~13,5 Md$ en 2026, TCAC de plus de 22 %)
- **Le spatial computing** (Vision Pro, WebXR) gagne en maturité mais manque d'applications killer pour l'entreprise
- Tous les outils de workflow IA existants (LangSmith, n8n, Flowise, CrewAI) sont des **tableaux de bord 2D plats**

### Le concept : Nexus Spatial

Un centre de commandement d'agents IA en spatial computing — une application VisionOS + WebXR qui fournit un centre de commandement 3D immersif pour orchestrer, surveiller et interagir avec des agents IA. Les utilisateurs visualisent les pipelines d'agents sous forme de graphes de nœuds 3D, surveillent les sorties en temps réel dans des panneaux spatiaux, construisent des workflows par glisser-déposer dans l'espace 3D et collaborent dans des environnements spatiaux partagés.

### Pourquoi cette agence est idéalement positionnée

L'agence dispose d'une expertise approfondie en spatial computing (développeurs XR, ingénieurs VisionOS, spécialistes Metal, architectes d'interface) aux côtés d'une stack complète d'engineering, de design, de marketing et d'opérations — une combinaison rare pour un produit qui exige à la fois une maîtrise du spatial computing et la rigueur du logiciel d'entreprise.

### Sources

- [Profitable SaaS Ideas 2026 (273K+ Reviews)](https://bigideasdb.com/profitable-saas-micro-saas-ideas-2026)
- [2026 SaaS and AI Revolution: 20 Top Trends](https://fungies.io/the-2026-saas-and-ai-revolution-20-top-trends/)
- [Top 21 Underserved Markets 2026](https://mktclarity.com/blogs/news/list-underserved-niches)
- [Fastest Growing Products 2026 - G2](https://www.g2.com/best-software-companies/fastest-growing)
- [PwC 2026 AI Business Predictions](https://www.pwc.com/us/en/tech-effect/ai-analytics/ai-predictions.html)

---

## 2. Validation de marché

**Agent :** Product Trend Researcher

### Verdict : GO CONDITIONNEL — la 2D d'abord, le spatial ensuite

### Taille du marché

| Segment | Valeur 2026 | Croissance |
|---------|-----------|--------|
| Outils d'orchestration d'IA | 13,5 Md$ | TCAC de 22,3 % |
| Agents IA autonomes | 8,5 Md$ | TCAC de 45,8 % jusqu'à 50,3 Md$ d'ici 2030 |
| Réalité étendue (XR) | 10,64 Md$ | TCAC de 40,95 % |
| Spatial computing (au sens large) | 170-220 Md$ | Variable selon la définition |

### Paysage concurrentiel

**Orchestration d'agents IA (tous en 2D) :**

| Outil | Force | Lacune UX |
|------|----------|--------|
| LangChain/LangSmith | Orchestration par graphes, 39 $/utilisateur/mois | Tableau de bord plat ; graphes complexes illisibles à grande échelle |
| CrewAI | Plus de 100 000 développeurs, exécution rapide | CLI d'abord, outillage visuel minimal |
| Microsoft Agent Framework | Intégration entreprise | Embarqué dans le portail Azure, pas d'UI autonome |
| n8n | Constructeur de workflow visuel, 20-50 $/mois | Le canvas 2D peine avec les relations entre agents |
| Flowise | Flux IA en glisser-déposer | Limité aux flux linéaires, pas de monitoring multi-agents |

**Produits « Mission Control » (émergents, tous en 2D) :**
- cmd-deck : tableau Kanban pour agents de codage IA
- Supervity Agent Command Center : observabilité d'entreprise
- OpenClaw Command Center : gestion de flottes d'agents
- Mission Control AI : gestion de travailleurs synthétiques
- Mission Control HQ : coordination par escouades

**La lacune :** les produits sont soit spatiaux-mais-pas-axés-IA, soit axés-IA-mais-2D-plats. Aucun produit ne se situe à l'intersection.

### Mise au point sur la réalité du Vision Pro

- Base installée : ~1 M d'unités dans le monde (ventes en baisse de 95 % depuis le lancement)
- Apple a réorienté sa stratégie vers des lunettes AR légères
- Seulement ~3 000 applications spécifiques à VisionOS existent
- **Implication :** NE PAS mener avec VisionOS. Mener avec le web, ajouter WebXR, le natif VisionOS en dernier.

### WebXR comme déblocage de la distribution

- Safari a adopté la WebXR Device API fin 2025
- Augmentation de 40 % de l'adoption de WebXR en 2026
- WebGPU offre un rendu quasi natif dans les navigateurs
- Android XR prend en charge les standards WebXR et OpenXR

### Personas cibles et pricing

| Niveau | Prix | Cible |
|------|-------|--------|
| Explorer | Gratuit | Développeurs, créateurs solo (3 agents, visionneuse WebXR) |
| Pro | 99 $/utilisateur/mois | Petites équipes (25 agents, collaboration) |
| Team | 249 $/utilisateur/mois | Équipes IA du mid-market (agents illimités, analytics) |
| Enterprise | Sur mesure (2-10 K$/mois) | Grandes entreprises (SSO, RBAC, on-prem, SLA) |

### Stratégie progressive recommandée

1. **Mois 1-6 :** Construire un tableau de bord web 2D premium avec des capacités 2,5D Three.js. Objectif : 50 équipes payantes, 60 K$ de MRR.
2. **Mois 6-12 :** Ajouter un mode spatial WebXR optionnel (dans le navigateur). Objectif : 200 équipes, 300 K$ de MRR.
3. **Mois 12-18 :** Application VisionOS native uniquement si la demande spatiale est validée. Objectif : 500 équipes, plus de 1 M$ de MRR.

### Risques clés

| Risque | Gravité |
|------|----------|
| La base installée du Vision Pro est dramatiquement faible | ÉLEVÉE |
| « Une solution spatiale en quête d'un problème » — la 3D est-elle vraiment 10x meilleure que la 2D ? | ÉLEVÉE |
| Positionnement « mission control » encombré (déjà plus de 5 produits) | MODÉRÉE |
| Adoption du spatial computing en entreprise encore précoce | MODÉRÉE |
| Complexité d'intégration entre les frameworks d'IA | MODÉRÉE |

### Sources

- [MarketsandMarkets - AI Orchestration Market](https://www.marketsandmarkets.com/Market-Reports/ai-orchestration-market-148121911.html)
- [Deloitte - AI Agent Orchestration Predictions 2026](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/ai-agent-orchestration.html)
- [Mordor Intelligence - Extended Reality Market](https://www.mordorintelligence.com/industry-reports/extended-reality-xr-market)
- [Fintool - Vision Pro Production Halted](https://fintool.com/news/apple-vision-pro-production-halt)
- [MadXR - WebXR Browser-Based Experiences 2026](https://www.madxr.io/webxr-browser-immersive-experiences-2026.html)

---

## 3. Architecture technique

**Agent :** Backend Architect

### Vue d'ensemble du système

Une architecture à 8 services avec des frontières de responsabilité claires, conçue pour la mise à l'échelle horizontale et une intégration IA agnostique du fournisseur.

```
+------------------------------------------------------------------+
|                     CLIENT TIER                                   |
|  VisionOS Native (Swift/RealityKit)  |  WebXR (React Three Fiber) |
+------------------------------------------------------------------+
                              |
+-----------------------------v------------------------------------+
|                      API GATEWAY (Kong / AWS API GW)              |
|  Rate limiting | JWT validation | WebSocket upgrade | TLS        |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                      SERVICE TIER                                 |
|  Auth | Workspace | Workflow | Orchestration (Rust) |             |
|  Collaboration (Yjs CRDT) | Streaming (WS) | Plugin | Billing    |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                      DATA TIER                                    |
|  PostgreSQL 16 | Redis 7 Cluster | S3 | ClickHouse | NATS        |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                    AI PROVIDER TIER                                |
|  OpenAI | Anthropic | Google | Local Models | Custom Plugins      |
+------------------------------------------------------------------+
```

### Stack technique

| Composant | Technologie | Justification |
|-----------|------------|-----------|
| Moteur d'orchestration | **Rust** | Ordonnancement sous la milliseconde, zéro pause GC, sûreté mémoire pour le sandboxing des agents |
| Services API | TypeScript / NestJS | Vélocité de développement pour les services à forte composante CRUD |
| Client VisionOS | Swift 6, SwiftUI, RealityKit | Spatial computing de premier ordre avec Liquid Glass |
| Client WebXR | TypeScript, React Three Fiber | WebXR de qualité production avec le modèle de composants React |
| Broker de messages | NATS JetStream | Léger, livraison exactly-once, plus simple que Kafka |
| Collaboration | Yjs (CRDT) + WebRTC | Édition concurrente de graphes 3D sans conflit |
| Base de données principale | PostgreSQL 16 | JSONB pour les configs flexibles, Row-Level Security pour l'isolation des locataires |

### Modèle de données central

14 tables couvrant :
- **Identité et accès :** users, workspaces, team_memberships, api_keys
- **Workflows :** workflows, workflow_versions, nodes, edges
- **Exécutions :** executions, execution_steps, step_output_chunks
- **Collaboration :** collaboration_sessions, session_participants
- **Identifiants :** provider_credentials (chiffrés en AES-256-GCM)
- **Facturation :** subscriptions, usage_records
- **Audit :** audit_log (append-only)

### Registre des types de nœuds

```
Built-in Node Types:
  ai_agent          -- Calls an AI provider with a prompt
  prompt_template   -- Renders a template with variables
  conditional       -- Routes based on expression
  transform         -- Sandboxed code snippet (JS/Python)
  input / output    -- Workflow entry/exit points
  human_review      -- Pauses for human approval
  loop              -- Repeats subgraph
  parallel_split    -- Fans out to branches
  parallel_join     -- Waits for branches
  webhook_trigger   -- External HTTP trigger
  delay             -- Timed pause
```

### Canaux WebSocket

Streaming en temps réel via WSS avec :
- Numéros de séquence par canal pour l'ordonnancement
- Détection de trous avec demandes de rejeu
- Récupération par snapshot quand le retard dépasse 1000 événements
- Throttling côté client pour les appareils moins puissants

### Architecture de sécurité

| Couche | Mécanisme |
|-------|-----------|
| Auth utilisateur | OAuth 2.0 (GitHub, Google, Apple) + e-mail/mot de passe + MFA TOTP optionnel |
| Clés API | Hachées en SHA-256, à portée définie, expiration optionnelle |
| Service à service | mTLS via service mesh |
| Auth WebSocket | Tickets à usage unique avec expiration de 30 secondes |
| Stockage des identifiants | Chiffrement par enveloppe (AES-256-GCM + AWS KMS) |
| Sandboxing du code | microVMs gVisor/Firecracker (pas de réseau, 256 Mo de RAM, 30 s de CPU) |
| Isolation des locataires | Row-Level Security PostgreSQL + politiques IAM S3 + scoping des sujets NATS |

### Objectifs de mise à l'échelle

| Métrique | Année 1 | Année 2 |
|--------|--------|--------|
| Exécutions d'agents simultanées | 5 000 | 50 000 |
| Connexions WebSocket | 10 000 | 100 000 |
| Latence API P95 | < 150 ms | < 100 ms |
| Latence d'événement WS P95 | < 80 ms | < 50 ms |

### Phases du MVP

1. **Semaines 1-6 :** Éditeur web 2D, exécution séquentielle, adaptateurs OpenAI + Anthropic
2. **Semaines 7-12 :** Mode 3D WebXR, exécution parallèle, suivi des mains, RBAC
3. **Semaines 13-20 :** Collaboration multi-utilisateurs, VisionOS natif, facturation
4. **Semaines 21-30 :** SSO entreprise, SDK de plugins, SOC 2, durcissement pour la mise à l'échelle

---

## 4. Stratégie de marque

**Agent :** Brand Guardian

### Positionnement

**Création de catégorie plutôt que concurrence dans une catégorie.** Nexus Spatial définit une nouvelle catégorie — **Spatial AI Operations (SpatialAIOps)** — plutôt que de se battre pour une position dans l'espace encombré des tableaux de bord d'observabilité IA.

**Énoncé de positionnement :** Pour les équipes techniques qui gèrent des workflows d'agents IA complexes, Nexus Spatial est le centre de commandement 3D immersif qui offre une conscience spatiale de l'orchestration d'agents, contrairement aux tableaux de bord 2D plats, parce que le spatial computing transforme la surveillance : on passe de la lecture de tableaux de bord à l'habitation de son infrastructure.

### Validation du nom

« Nexus Spatial » est **validé comme fort :**
- « Nexus » se rattache au framework d'orchestration NEXUS (Network of EXperts, Unified in Strategy)
- « Nexus » signifie indépendamment « point de connexion central » — parfait pour un centre de commandement
- « Spatial » est le descripteur standard du secteur qu'Apple et l'industrie ont normalisé
- Phonétiquement équilibré : trois syllabes, puis deux
- **Action nécessaire :** Vérification de marque dans les classes de Nice 9, 42 et 38

### Personnalité de marque : Le Commandant

| Trait | Expression | Évite |
|-------|------------|--------|
| **Autoritaire** | Clair, direct, techniquement précis | Hype, superlatifs, futurisme vague |
| **Posé** | Design épuré, rythme mesuré, espace blanc | L'urgence pour l'urgence, le chaos |
| **Pionnier** | Fierté discrète, références retenues au nouveau paradigme | « Révolutionnaire », « qui change la donne » |
| **Précis** | Specs exactes, métriques réelles, exigences honnêtes | Affirmations vagues, mots à la mode marketing |
| **Accessible** | Langage d'interaction naturel, métaphores spatiales | Condescendance, élitisme |

### Slogans (classés)

1. **« Mission Control for the Agent Era »** — RECOMMANDÉ COMME PRINCIPAL
2. « See Your Agents in Space »
3. « Orchestrate in Three Dimensions »
4. « Where AI Operations Become Spatial »
5. « Command Center. Reimagined in Space. »
6. « The Dimension Your Dashboards Are Missing »
7. « AI Agents Deserve More Than Flat Screens »

### Système de couleurs

| Couleur | Hex | Usage |
|-------|-----|-------|
| Deep Space Indigo | `#1B1F3B` | Canvas sombre fondamental, arrière-plans |
| Nexus Blue | `#4A7BF7` | Couleur signature de la marque, actions principales |
| Signal Cyan | `#00D4FF` | Accents spatiaux, connexions de données |
| Command Green | `#00E676` | Systèmes en bonne santé, succès |
| Alert Amber | `#FFB300` | Avertissements, attention requise |
| Critical Red | `#FF3D71` | Erreurs, défaillances |

Ratio d'usage : Deep Space Indigo 60 %, Nexus Blue 25 %, Signal Cyan 10 %, sémantique 5 %.

### Typographie

- **Principale :** Inter (UI, corps, libellés)
- **Monospace :** JetBrains Mono (code, logs, sortie des agents)
- **Display :** Space Grotesk (titres marketing uniquement)

### Concepts de logo

Trois directions à explorer :

1. **The Spatial Nexus Mark** — Lignes convergentes se rejoignant en un nœud central lumineux, avec une subtile profondeur de perspective
2. **The Dimensional Window** — Fenêtre stylisée avec des lignes de perspective créant l'effet de regarder dans un espace 3D
3. **The Orbital Array** — Anneaux orbitaux autour d'un point central suggérant des agents coordonnés en mouvement

### Valeurs de marque

- **Spatial Truthfulness** — Représentation honnête de l'état du système, sans lissage cosmétique
- **Operational Gravity** — Conçu pour la production, pas pour les démos
- **Dimensional Generosity** — WebXR garantit que la valeur spatiale est accessible à tous
- **Composure Under Complexity** — Plus le système est complexe, plus l'interface est calme

### Design tokens

```css
:root {
  --nxs-deep-space:       #1B1F3B;
  --nxs-blue:             #4A7BF7;
  --nxs-cyan:             #00D4FF;
  --nxs-green:            #00E676;
  --nxs-amber:            #FFB300;
  --nxs-red:              #FF3D71;
  --nxs-void:             #0A0E1A;
  --nxs-slate-900:        #141829;
  --nxs-slate-700:        #2A2F45;
  --nxs-slate-500:        #4A5068;
  --nxs-slate-300:        #8B92A8;
  --nxs-slate-100:        #C8CCE0;
  --nxs-cloud:            #E8EBF5;
  --nxs-white:            #F8F9FC;
  --nxs-font-primary:     'Inter', sans-serif;
  --nxs-font-mono:        'JetBrains Mono', monospace;
  --nxs-font-display:     'Space Grotesk', sans-serif;
}
```

---

## 5. Go-to-Market et croissance

**Agent :** Growth Hacker

### North Star Metric

**Weekly Active Pipelines (WAP)** — pipelines d'agents uniques ayant eu au moins une interaction spatiale au cours des 7 derniers jours. Capture à la fois la création et l'engagement, corrèle avec la valeur et n'est pas manipulable.

### Pricing

| Niveau | Annuel | Mensuel | Cible |
|------|--------|---------|--------|
| Explorer | Gratuit | Gratuit | 3 pipelines, aperçu WebXR, communauté |
| Pro | 29 $/utilisateur/mois | 39 $/utilisateur/mois | Pipelines illimités, VisionOS, historique de 30 jours |
| Team | 59 $/utilisateur/mois | 79 $/utilisateur/mois | Collaboration, RBAC, SSO, historique de 90 jours |
| Enterprise | Sur mesure (~150+ $) | Sur mesure | Infra dédiée, SLA, option on-prem |

Stratégie : essai inversé de 14 jours (fonctionnalités Pro, puis rétrogradation vers Free). Objectif de conversion gratuit-vers-payant de 5 à 8 %.

### GTM en 3 phases

**Phase 1 : Vente menée par les fondateurs (mois 1-3)**
- Cible : Ingénieurs IA individuels dans des startups qui utilisent LangChain/CrewAI et possèdent un Vision Pro
- Tactiques : DM à 200 ingénieurs IA de premier plan, posts hebdomadaires de build-in-public, clips de démo de 30 secondes
- Canaux : X/Twitter, LinkedIn, serveurs Discord axés IA, Reddit

**Phase 2 : Communauté de développeurs (mois 4-6)**
- Lancement Product Hunt (calé pour cette phase, pas la Phase 1)
- Show HN sur Hacker News, articles Dev.to, conférences
- Annonces d'intégration avec des frameworks d'IA populaires

**Phase 3 : Entreprise (mois 7-12)**
- Pipeline de recommandation entreprise Apple, campagnes ABM LinkedIn
- Études de cas entreprise, briefings d'analystes (Gartner, Forrester)
- Premier recrutement d'AE entreprise, conformité SOC 2

### Boucles de croissance

1. **Boucle de démo « facteur wow »** — Les démos spatiales sont intrinsèquement partageables. Un « Share Spatial Preview » en un clic génère un lien WebXR ou une vidéo. Objectif K = 0,3-0,5.
2. **Marketplace de templates** — Les utilisateurs avancés publient des templates de pipelines, repérables par la recherche, générant de nouvelles inscriptions.
3. **Expansion par sièges de collaboration** — Un ingénieur adopte, partage avec ses coéquipiers, l'équipe passe à un plan payant (playbook Slack/Figma).
4. **Découverte tirée par les intégrations** — Référencements dans les annuaires partenaires LangChain, n8n, OpenAI/Anthropic.

### Stratégie open-source

**Open-source (Apache 2.0) :**
- `nexus-spatial-sdk` — SDK TypeScript/Python pour connecter les frameworks d'agents
- `nexus-webxr-components` — Bibliothèque de composants React Three Fiber pour les pipelines 3D
- `nexus-agent-schemas` — Schémas standardisés pour représenter les pipelines d'agents en 3D

**À garder propriétaire :** application VisionOS native, moteur de collaboration, fonctionnalités entreprise, infrastructure hébergée.

### Objectifs de revenus

| Métrique | Mois 6 | Mois 12 |
|--------|---------|----------|
| MRR | 8-15 K$ | 50-80 K$ |
| Comptes gratuits | 5 000 | 15 000 |
| Sièges payants | 300 | 1 200 |
| Membres Discord | 2 000 | 5 000 |
| Stars GitHub (SDK) | 500 | 2 000 |

### Premier budget de 50 K$

| Catégorie | Montant | % |
|----------|--------|---|
| Production de contenu | 12 000 $ | 24 % |
| Relations développeurs | 10 000 $ | 20 % |
| Tests d'acquisition payante | 8 000 $ | 16 % |
| Communauté et outils | 5 000 $ | 10 % |
| Product Hunt et lancement | 3 000 $ | 6 % |
| Maintenance open-source | 3 000 $ | 6 % |
| RP et prospection | 4 000 $ | 8 % |
| Partenariats | 2 000 $ | 4 % |
| Réserve | 3 000 $ | 6 % |

### Partenariats clés

- **Niveau 1 (Critique) :** Anthropic, OpenAI — intégrations API de premier ordre, référencements dans les programmes partenaires
- **Niveau 2 (Adoption) :** LangChain, CrewAI, n8n — intégrations de frameworks, pollinisation croisée des communautés
- **Niveau 3 (Plateforme) :** Apple — kit développeur Vision Pro, mise en avant App Store, WWDC
- **Niveau 4 (Écosystème) :** GitHub, Hugging Face, Docker — intégrations de plateformes développeurs

### Sources

- [AI Orchestration Market Size - MarketsandMarkets](https://www.marketsandmarkets.com/Market-Reports/ai-orchestration-market-148121911.html)
- [Spatial Computing Market - Precedence Research](https://www.precedenceresearch.com/spatial-computing-market)
- [How to Price AI Products - Aakash Gupta](https://www.news.aakashg.com/p/how-to-price-ai-products)
- [Product Hunt Launch Guide 2026](https://calmops.com/indie-hackers/product-hunt-launch-guide/)

---

## 6. Blueprint du support client

**Agent :** Support Responder

### Structure des niveaux de support

| Attribut | Explorer (Gratuit) | Builder (Pro) | Command (Enterprise) |
|-----------|-----------------|---------------|---------------------|
| SLA de première réponse | Au mieux (48 h) | 4 heures (heures ouvrées) | 30 min (P1), 2 h (P2) |
| SLA de résolution | 5 jours ouvrés | 24 h (P1/P2), 72 h (P3) | 4 h (P1), 12 h (P2) |
| Canaux | Communauté, KB, assistant IA | + Chat en direct, e-mail, vidéo (2/mois) | + Slack dédié, CSE nommé, 24/7 |
| Périmètre | Questions générales, docs | Dépannage technique, intégrations | Intégration complète, conception sur mesure, conformité |

### Définitions des priorités

- **P1 Critique :** Orchestration en panne, risque de perte de données, faille de sécurité
- **P2 Élevée :** Fonctionnalité majeure dégradée, contournement existant
- **P3 Moyenne :** Problèmes non bloquants, anomalies mineures
- **P4 Faible :** Demandes de fonctionnalités, problèmes cosmétiques

### Le Nexus Guide : support intégré au produit, propulsé par l'IA

La décision de conception phare : l'agent de support vit comme un nœud visible **à l'intérieur de l'espace de travail spatial de l'utilisateur**. Il a le contexte complet de la disposition de l'utilisateur, des agents actifs et des erreurs récentes.

**Capacités :**
- Questions-réponses en langage naturel sur les fonctionnalités
- Diagnostic d'agents en temps réel (« Pourquoi l'Agent X est-il lent ? »)
- Suggestions de configuration (« Votre topologie serait plus performante en maillage »)
- Parcours guidés de dépannage spatial
- Création de tickets avec rattachement automatique du contexte

**Auto-réparation :**

| Scénario | Détection | Auto-résolution |
|----------|-----------|-----------------|
| Boucle infinie d'agent | Pic de CPU/tokens | Arrêt et redémarrage avec la dernière config valide |
| Chute d'images de rendu | FPS sous le seuil | Réduction de la fidélité visuelle, suggestion de fermer des panneaux |
| Expiration d'identifiants | Réponses API 401 | Invite à se réauthentifier, mise en pause propre des agents |
| Timeout de communication | Pic de latence | Réacheminement des messages par un chemin alternatif |

### Parcours d'onboarding

Onboarding adaptatif basé sur le profilage de l'utilisateur :

| Expérience IA | Expérience spatiale | Parcours |
|---------------|-------------------|------|
| Faible | Faible | Visite guidée complète (20 min) |
| Élevée | Faible | Axé spatial (12 min) |
| Faible | Élevée | Axé agents (12 min) |
| Élevée | Élevée | Configuration express (5 min) |

Première étape critique : calibrage spatial de 60 secondes (suivi des mains, regard, vérification du confort) avant toute interaction avec le produit.

**Jalon d'activation** (l'utilisateur est « onboardé » lorsqu'il a) :
- Créé au moins un agent personnalisé
- Connecté deux agents ou plus dans une topologie
- Ancré au moins un tableau de bord de monitoring
- Réutilisé le produit pour une troisième session

### Constitution de l'équipe

| Phase | Effectif | Rôles |
|-------|-----------|-------|
| Mois 0-6 | 4 | Head of CX, 2 Support Engineers, Technical Writer |
| Mois 6-12 | 8 | + 2 Support Engineers, CSE, Community Manager, Ops Analyst |
| Mois 12-24 | 16 | + 4 Engineers (24/7), Spatial Specialist, Integration Specialist, KB Manager, Engineering Manager |

### Communauté : Discord d'abord

```
NEXUS SPATIAL DISCORD
  INFORMATION: #announcements, #changelog, #status
  SUPPORT: #help-getting-started, #help-agents, #help-spatial
  DISCUSSION: #general, #show-your-workspace, #feature-requests
  PLATFORMS: #visionos, #webxr, #api-and-sdk
  EVENTS: office-hours (weekly voice), community-demos (monthly)
  PRO MEMBERS: #pro-lounge, #beta-testing
  ENTERPRISE: per-customer private channels
```

**Programme de champions (« Nexus Navigators ») :** 5 à 10 utilisateurs avancés initiaux avec badge Navigator, Slack direct avec l'équipe produit, niveau Pro gratuit, accès anticipé aux fonctionnalités et sommet annuel.

---

## 7. Recherche UX et direction de design

**Agent :** UX Researcher

### Personas utilisateurs

**Maya Chen — AI Platform Engineer (32 ans, San Francisco)**
- Gère 15 à 30 workflows d'agents actifs, utilise n8n + LangSmith
- Passe 40 % de son temps à déboguer des échecs d'agents en inspectant les logs
- Sceptique vis-à-vis du spatial computing : « Est-ce vraiment plus rapide, ou juste plus cool ? »
- Besoin principal : Réduire le délai moyen de diagnostic de 45 min à moins de 10

**David Okoro — Technical Product Manager (38 ans, Londres)**
- Examine et valide les conceptions de workflows d'agents, présente au comité de direction
- Ne peut pas contribuer utilement aux revues de workflow car les outils exigent une compréhension au niveau du code
- Besoin principal : Comprendre et communiquer les architectures d'agents sans lire de code

**Dr. Amara Osei — Research Scientist (45 ans, Zurich)**
- Conçoit des workflows de recherche multi-agents avec comparaisons A/B
- A 12 variations du même pipeline sans bon moyen de les comparer
- Besoin principal : Comparaison côte à côte de pipelines variants dans l'espace 3D

**Jordan Rivera — Creative Technologist (27 ans, Austin)**
- Utilisateur quotidien du Vision Pro, construit des installations artistiques propulsées par l'IA
- Veut des outils qui ressemblent à des instruments, pas à des tableaux de bord
- Besoin principal : Construire rapidement des workflows d'agents avec un retour spatial immédiat

### Constat clé : le débogage est le cas d'usage killer

La superposition spatiale des traces d'exécution sur la structure du workflow résout un point de douleur réel et quantifié qu'aucun outil 2D ne gère bien. Ce workflow devrait recevoir le plus gros investissement en design et en engineering.

### Insight de design critique

Le spatial apporte de la valeur pour les tâches **structurelles** (placer, connecter, réarranger des nœuds) mais crée de la friction pour les tâches de **paramétrage** (saisie de texte, configuration). L'interface doit fondre de façon transparente les modes spatial et 2D — des panneaux 2D ancrés à des positions spatiales.

### 7 principes de design

1. **Le spatial mérite sa place** — Si la 2D est plus claire, utiliser la 2D. Chaque revue devrait demander : « Serait-ce mieux en plat ? »
2. **Lisible d'un coup d'œil avant d'être inspectable** — Information critique perceptible en moins de 2 secondes via couleur, taille, mouvement, position
3. **Le mains-libres est la base** — Regard + voix couvrent toutes les opérations de lecture/navigation ; les mains ajoutent de la précision mais ne sont pas requises
4. **Respecter la gravité cognitive** — Étendre les modèles mentaux 2D (flux de gauche à droite), ne pas les remplacer ; l'axe z ajoute des couches
5. **Complexité spatiale progressive** — Les nouveaux utilisateurs démarrent en quasi-2D ; les capacités spatiales se révèlent à mesure que la confiance grandit
6. **Métaphores physiques, capacités numériques** — Les nœuds se « prennent en main » (physique) mais se dupliquent et se versionnent aussi (numérique)
7. **Le silence est une fonctionnalité** — Les systèmes en bonne santé semblent calmes ; couleur et mouvement signalent l'écart par rapport à la normale

### Paradigme de navigation : zoom sémantique à 4 niveaux

| Niveau | Ce que vous voyez |
|-------|-------------|
| Vue Flotte | Tous les workflows en formes abstraites, codés par couleur selon le statut |
| Vue Workflow | Graphe de nœuds avec libellés et connexions |
| Vue Nœud | Configuration développée, E/S récentes, métriques de statut |
| Vue Trace | Trace d'exécution complète avec inspection des données |

### Synthèse UX concurrentielle

| Capacité | n8n | Flowise | LangSmith | Langflow | Objectif Nexus Spatial |
|-----------|-----|---------|-----------|----------|---------------------|
| Construction visuelle de workflow | A | B+ | N/A | A | A+ (spatial) |
| Débogage/tracing | C+ | C | A | B | A+ (superposition spatiale) |
| Monitoring | B | C | A | B | A (flotte spatiale) |
| Collaboration | D | D | C | D | A (co-présence spatiale) |
| Scalabilité des gros workflows | C | C | B | C | A (espace 3D) |

### Exigences d'accessibilité

- Chaque interaction réalisable via au moins deux modalités
- Aucune information transmise par la couleur seule
- Mode haut contraste, mode mouvement réduit, mode aplatissement de la profondeur
- Compatibilité lecteur d'écran avec descriptions des éléments spatiaux
- Avertissements de durée de session toutes les 20-30 minutes
- Toutes les tâches centrales réalisables assis, à une main, dans un cône de mouvement de 30 degrés

### Plan de recherche (16 semaines)

| Phase | Semaines | Études |
|-------|-------|---------|
| Fondamentale | 1-4 | Entretiens sur les modèles mentaux (15-20 participants), analyse comparative des tâches |
| Validation du concept | 5-8 | Tests de prototype spatial en Magicien d'Oz, tri de cartes 3D pour l'architecture de l'information |
| Tests d'utilisabilité | 9-14 | Expérience de première utilisation (20 utilisateurs), étude de journal longitudinale de 4 semaines, tests de collaboration en binôme |
| Audit d'accessibilité | 12-16 | Évaluation heuristique experte, tests avec des utilisateurs en situation de handicap |

---

## 8. Plan d'exécution du projet

**Agent :** Project Shepherd

### Calendrier : 35 semaines (9 mars — 6 novembre 2026)

| Phase | Semaines | Durée | Objectif |
|-------|-------|----------|------|
| Découverte et recherche | S1-3 | 3 semaines | Valider la faisabilité, définir le périmètre |
| Fondation | S4-9 | 6 semaines | Infrastructure centrale, coques des deux plateformes, design system |
| Construction du MVP | S10-19 | 10 semaines | Centre de commandement d'agents mono-utilisateur avec orchestration |
| Bêta | S20-27 | 8 semaines | Collaboration, peaufinage, durcissement, 50-100 utilisateurs bêta |
| Lancement | S28-31 | 4 semaines | Lancement App Store + web, poussée marketing |
| Mise à l'échelle | S32-35+ | En continu | Marketplace de plugins, fonctionnalités avancées, croissance |

### Jalon critique : semaine 12 (29 mai)

**Première exécution de workflow de bout en bout.** Un utilisateur crée et exécute un workflow d'agents à 3 nœuds en 3D. C'est le moment où le produit prouve sa proposition de valeur centrale. Si ce jalon glisse, tout l'aval se décale.

### Les 6 premiers sprints (65 tickets)

**Sprint 1 (9-20 mars) :** Audit du SDK VisionOS, matrice de compatibilité WebXR, faisabilité du moteur d'orchestration, entretiens avec les parties prenantes, prototypes jetables pour les deux plateformes.

**Sprint 2 (23 mars - 3 avr.) :** Architecture decision records, verrouillage du périmètre MVP avec MoSCoW, PRD v1.0, recherche sur les patterns d'UI spatiale, définition du modèle d'interaction, lancement du design system.

**Sprint 3 (6-17 avr.) :** Mise en place du monorepo, service d'auth (OAuth2), schéma de base de données, API gateway, init du projet Xcode VisionOS, init du projet WebXR, pipelines CI/CD.

**Sprint 4 (20 avr. - 1er mai) :** Serveur WebSocket + SDK clients, gestion des fenêtres spatiales, bibliothèque de composants 3D, couche d'entrée pour le suivi des mains, CRUD des équipes, tests d'intégration.

**Sprint 5 (4-15 mai) :** Cœur du moteur d'orchestration (Rust), machine à états des agents, moteurs de rendu de graphe de nœuds (les deux plateformes), interface de plugin v0, plugin du fournisseur OpenAI.

**Sprint 6 (18-29 mai) :** Persistance + versionnement des workflows, exécution de DAG, visualisation d'exécution en temps réel, plugin du fournisseur Anthropic, intégration du suivi oculaire, audio spatial.

### Allocation de l'équipe

5 escouades opérant à travers les phases :

| Escouade | Membres clés | Phases actives |
|-------|-------------|---------------|
| Architecture centrale | Backend Architect, XR Interface Architect, Senior Dev, VisionOS Engineer | De la Découverte au MVP |
| Expérience spatiale | XR Immersive Dev, XR Cockpit Specialist, Metal Engineer, UX Architect, UI Designer | De la Fondation à la Bêta |
| Orchestration | AI Engineer, Backend Architect, Senior Dev, API Tester | Du MVP à la Bêta |
| Livraison plateforme | Frontend Dev, Mobile App Builder, VisionOS Engineer, DevOps | Du MVP au Lancement |
| Lancement | Growth Hacker, Content Creator, App Store Optimizer, Visual Storyteller, Brand Guardian | De la Bêta à la Mise à l'échelle |

### Top 5 des risques

| Risque | Probabilité | Impact | Atténuation |
|------|------------|--------|------------|
| Apple rejette l'app VisionOS | Moyenne | Critique | Engager Apple Developer Relations en semaine 4, pré-revue d'ici la semaine 20 |
| Fragmentation des navigateurs WebXR | Élevée | Élevé | Matrice de support navigateur en semaine 1, tests cross-navigateurs automatisés |
| Conflits de synchronisation multi-utilisateurs | Moyenne | Élevé | Synchronisation basée sur CRDT (Yjs) dès le départ, prototype en Fondation |
| L'orchestration ne passe pas à l'échelle | Moyenne | Critique | Mise à l'échelle horizontale dès le premier jour, test de charge à 10x d'ici la semaine 22 |
| Performance RealityKit pour plus de 100 nœuds | Moyenne | Élevé | Profiler tôt, implémenter le culling LOD, le rendu instancié |

### Budget : 121 500 $ — 155 500 $ (hors personnel)

| Catégorie | Coût estimé |
|----------|---------------|
| Infrastructure cloud (35 semaines) | 35 000 $ - 45 000 $ |
| Matériel (3 Vision Pro, 2 Quest 3, Mac Studio) | 17 500 $ |
| Licences et services | 15 000 $ - 20 000 $ |
| Services externes (juridique, sécurité, RP) | 30 000 $ - 45 000 $ |
| Coûts d'API IA (dev/test) | 8 000 $ |
| Contingence (15 %) | 16 000 $ - 20 000 $ |

---

## 9. Architecture de l'interface spatiale

**Agent :** XR Interface Architect

### Le Command Theater

L'espace de travail est organisé comme un théâtre incurvé autour de l'utilisateur :

```
                        OVERVIEW CANOPY
                     (pipeline topology)
                    ~~~~~~~~~~~~~~~~~~~~~~~~
                   /                        \
                  /     FOCUS ARC (120 deg)   \
                 /    primary node graph work   \
                /________________________________\
               |                                  |
    LEFT       |        USER POSITION             |       RIGHT
    UTILITY    |        (origin 0,0,0)            |       UTILITY
    RAIL       |                                  |       RAIL
               |__________________________________|
                \                                /
                 \      SHELF (below sightline) /
                  \   agent status, quick tools/
                   \_________________________ /
```

- **Focus Arc** (120 degrés, 1,2-2,0 m) : Espace de travail principal du graphe de nœuds
- **Overview Canopy** (au-dessus, 2,5-4,0 m) : Topologie miniature du pipeline + heatmap de santé
- **Utility Rails** (flancs gauche/droit) : Bibliothèque d'agents, monitoring, logs
- **Shelf** (sous la ligne de mire, 0,8-1,0 m) : Run/stop, undo/redo, outils rapides

### Système de profondeur à trois couches

| Couche | Profondeur | Contenu | Opacité |
|-------|-------|---------|---------|
| Premier plan | 0,8 - 1,2 m | Panneaux actifs, inspecteurs, modales | 100 % |
| Plan intermédiaire | 1,2 - 2,5 m | Graphe de nœuds, connexions, espace de travail | 100 % |
| Arrière-plan | 2,5 - 5,0 m | Carte d'ensemble, statut d'ambiance | 40-70 % |

### Graphe de nœuds en 3D

**Les données s'écoulent vers l'utilisateur.** Les nœuds s'organisent le long de l'axe z par ordre d'exécution :

```
USER (here)
  z=0.0m   [Output Nodes]     -- Results
  z=0.3m   [Transform Nodes]  -- Processors
  z=0.6m   [Agent Nodes]      -- LLM calls
  z=0.9m   [Retrieval Nodes]  -- RAG, APIs
  z=1.2m   [Input Nodes]      -- Triggers
```

Les branches parallèles s'étendent horizontalement (axe x). Les branches conditionnelles s'étendent verticalement (axe y).

**Représentation des nœuds (3 LODs) :**
- **LOD-0** (au repos, >1,5 m) : Rectangle en verre dépoli de 12x8 cm avec icône de type, nom, halo de statut
- **LOD-1** (survol, regard de 400 ms) : S'agrandit à 14x10 cm, révèle les ports, infos de la dernière exécution
- **LOD-2** (sélectionné) : Glisse au premier plan, s'agrandit en un panneau de détail de 30x40 cm avec édition de config en direct

**Connexions sous forme de tubes lumineux :**
- 4 mm de diamètre au repos, 8 mm quand elles transportent des données
- Codées par couleur selon le type de données (blanc=texte, cyan=structuré, magenta=images, ambre=audio, vert=appels d'outils)
- Des particules animées montrent le sens et la vitesse du flux
- Auto-regroupement quand plus de 3 s'exécutent en parallèle entre les mêmes couches

### 7 états d'agent

| État | Halo de bordure | Intérieur | Son | Particules |
|-------|-----------|----------|-------|-----------|
| Idle | Vert stable, faible | Verre dépoli statique | Aucun | Aucune |
| Queued | Ambre pulsé, 1 Hz | Rotation légère | Aucun | Dérive lente à l'entrée |
| Running | Bleu stable, moyen | Miroitement animé | Bourdonnement spatial doux | Flux rapide sur les connexions |
| Streaming | Bleu + flux de sortie | Miroitement + fragments de texte | Bourdonnement | Fragments de texte s'écoulant vers l'avant |
| Completed | Flash blanc, puis vert | Statique | Carillon de fin | Aucune |
| Error | Rouge pulsé, 2 Hz | Teinte rouge | Tonalité d'alerte (une fois) | Aucune |
| Paused | Ambre stable | Image figée + icône pause | Aucun | Figées en place |

### Modèle d'interaction

| Action | VisionOS | Manettes WebXR | Voix |
|--------|----------|-------------------|-------|
| Sélectionner un nœud | Regard + pincement | Rayon de pointage + gâchette | « Select [name] » |
| Déplacer un nœud | Pincement + glissement | Grip + déplacement | -- |
| Connecter des ports | Pincement du port + glissement | Gâchette sur le port + glissement | « Connect [A] to [B] » |
| Déplacer l'espace de travail | Glissement à deux mains | Stick analogique | « Pan left/right » |
| Zoom | Écartement/pincement à deux mains | Poussée/tirage du stick | « Zoom in/out » |
| Inspecter un nœud | Pincement + tirage vers soi | Double gâchette | « Inspect [name] » |
| Lancer le pipeline | Appui sur le bouton de la Shelf | Bouton gâchette | « Run pipeline » |
| Annuler | Double tap à deux doigts | Bouton B | « Undo » |

### Présence en collaboration

Chaque collaborateur est représenté par :
- **Proxy de tête :** Sphère translucide avec image de profil, pivotant avec l'orientation de la tête
- **Proxies de mains :** Modèles de mains fantômes montrant les états de pincement/saisie
- **Cône de regard :** Cône subtil de 10 degrés montrant où il regarde
- **Étiquette de nom :** Rendue en billboard, affiche l'action en cours (« editing Node X »)

**Résolution de conflits :** Le premier éditeur obtient le verrou d'écriture ; le second voit « locked by [name] » avec l'option de demander l'accès ou de dupliquer le nœud.

### Disposition adaptative

| Environnement | Échelle des nœuds | Max nœuds LOD-2 | Étalement Z du graphe |
|-------------|-----------|-----------------|----------------|
| Fenêtre VisionOS | 4x3 cm | 5 | 0,05 m/couche |
| VisionOS immersif | 12x8 cm | 15 | 0,3 m/couche |
| WebXR Desktop | 120x80 px | 8 (superpositions) | Projection en perspective |
| WebXR immersif | 12x8 cm | 12 | 0,3 m/couche |

### Chorégraphie des transitions

Toutes les transitions servent l'orientation. Maximum 600 ms pour les transitions majeures, 200 ms pour les mineures, 0 ms pour la sélection.

| Transition | Durée | Mouvement clé |
|-----------|----------|------------|
| Vue d'ensemble vers Focus | 600 ms | La caméra dérive vers la cible, les autres régions s'estompent à 30 % |
| Focus vers Détail | 500 ms | Le nœud glisse vers l'avant, s'agrandit, les connexions se mettent en surbrillance |
| Détail vers Vue d'ensemble | 600 ms | Le panneau se replie, le nœud recule, la topologie complète est visible |
| Changement de zone | 500 ms | La zone actuelle sort latéralement, la nouvelle entre |
| Fenêtre vers Immersif | 1000 ms | Les bordures se dissolvent, les nœuds s'étendent à leurs positions spatiales complètes |

### Mesures de confort

- Aucun mouvement initié par la caméra sans action de l'utilisateur
- Horizon stable (le plan horizontal ne s'incline jamais)
- Interaction principale entre 0,8 et 2,5 m, à +/-15 degrés de la ligne de regard
- Invite au repos après 45 minutes (changement d'éclairage d'ambiance, non modal)
- Vignette périphérique pendant les mouvements rapides
- Toutes les commandes fréquemment utilisées accessibles bras le long du corps (poignet/doigts uniquement)

---

## 10. Synthèse inter-agents

### Points d'accord entre les 8 agents

1. **La 2D d'abord, le spatial ensuite.** Chaque agent est arrivé indépendamment à cette conclusion. Construire d'abord un excellent tableau de bord web, puis ajouter progressivement des capacités spatiales.

2. **Le débogage est le cas d'usage killer.** Le Product Researcher, l'UX Researcher et le XR Interface Architect ont tous convergé là-dessus : la superposition spatiale des traces d'exécution sur la structure du workflow est là où la 3D bat véritablement la 2D.

3. **WebXR plutôt que VisionOS pour la portée initiale.** La base installée d'environ 1 M du Vision Pro ne peut pas soutenir une activité. WebXR dans le navigateur est le déblocage de la distribution.

4. **Le scénario de collaboration « war room ».** Plusieurs agents ont mis en avant la réponse collaborative aux incidents comme la proposition de valeur spatiale la plus forte — des équipes entrant dans un espace 3D partagé pour déboguer ensemble un pipeline défaillant.

5. **La divulgation progressive est essentielle.** La Recherche UX, l'UI spatiale et le Support ont tous souligné que la complexité spatiale doit être révélée graduellement, jamais imposée d'un coup à un nouvel utilisateur.

6. **La voix comme accélérateur pour utilisateurs avancés.** L'UX Researcher comme le XR Interface Architect ont identifié les commandes vocales comme la « ligne de commande du spatial computing » — essentielle pour l'accessibilité et l'efficacité des experts.

### Tensions clés à résoudre

| Tension | Position A | Position B | Résolution nécessaire |
|---------|-----------|-----------|-------------------|
| **Pricing** | Growth Hacker : 29-59 $/utilisateur/mois | Trend Researcher : 99-249 $/utilisateur/mois | Test A/B en bêta |
| **Priorité VisionOS** | Architecture : Phase 3 (semaine 13+) | UI spatiale : Spec complète prête | Construire WebXR d'abord, VisionOS une fois validé |
| **Langage d'orchestration** | Architecture : Rust | Plan de projet : Non précisé | Rust est le bon choix pour l'exécution de DAG critique en performance |
| **Périmètre du MVP** | Architecture : 2D uniquement en Phase 1 | Marque : Mener avec le spatial | La 2D d'abord, mais s'assurer que le spatial est dans chaque démo |
| **Plateforme communautaire** | Support : Discord d'abord | Marketing : Discord + open-source | Les deux — Discord pour la communauté, GitHub pour l'engagement des développeurs |

### Ce que cet exercice démontre

Ce document de découverte a été produit par 8 agents spécialisés tournant en parallèle, chacun apportant une expertise approfondie de son domaine à un objectif commun. Les agents sont arrivés indépendamment à des conclusions cohérentes tout en faisant émerger des insights propres à leur domaine, qu'il serait difficile pour un seul généraliste de produire :

- Le **Product Trend Researcher** a trouvé les données dégrisantes de ventes du Vision Pro qui ont recadré toute la stratégie
- Le **Backend Architect** a conçu un moteur d'orchestration en Rust qu'aucune équipe axée marketing n'aurait envisagé
- Le **Brand Guardian** a créé une catégorie (« SpatialAIOps ») plutôt que de concourir dans une catégorie existante
- L'**UX Researcher** a identifié que le spatial computing crée de la friction pour les tâches de paramétrage — un constat contre-intuitif
- Le **XR Interface Architect** a conçu la topologie « les données s'écoulent vers vous » qui correspond à la cognition spatiale naturelle
- Le **Project Shepherd** a identifié les trois rôles goulots d'étranglement critiques qui pourraient faire dérailler tout le calendrier
- Le **Growth Hacker** a conçu des boucles virales propres au caractère intrinsèquement partageable du spatial computing
- Le **Support Responder** a transformé les propres capacités d'IA du produit en un différenciateur de support

Le résultat est un plan produit complet et transverse qui pourrait servir de base à un développement réel — produit en une seule session par une agence d'agents IA travaillant de concert.
