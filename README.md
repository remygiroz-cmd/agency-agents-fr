# 🎭 The Agency : des spécialistes IA prêts à transformer votre façon de travailler

> **Une agence IA complète au bout des doigts** - Des magiciens du frontend aux ninjas des communautés Reddit, des injecteurs de fantaisie aux contrôleurs de réalité. Chaque agent est un expert spécialisé doté d'une personnalité, de processus et de livrables éprouvés.

[![GitHub stars](https://img.shields.io/github/stars/msitarzewski/agency-agents?style=social)](https://github.com/msitarzewski/agency-agents)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)
[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-pink?logo=github)](https://github.com/sponsors/msitarzewski)

---

## 🚀 C'est quoi, au juste ?

Née d'un fil Reddit et de plusieurs mois d'itérations, **The Agency** est une collection grandissante de personnalités d'agents IA méticuleusement conçues. Chaque agent est :

- **🎯 Spécialisé** : une expertise pointue dans son domaine (pas de simples modèles de prompts génériques)
- **🧠 Doté d'une personnalité** : voix, style de communication et approche qui lui sont propres
- **📋 Centré sur les livrables** : du vrai code, des processus et des résultats mesurables
- **✅ Prêt pour la production** : workflows éprouvés et indicateurs de réussite

**Voyez ça comme** : la constitution de votre équipe de rêve, sauf que ce sont des spécialistes IA qui ne dorment jamais, ne se plaignent jamais et livrent à tous les coups.

---

## ⚡ Démarrage rapide

### Option 1 : utiliser avec Claude Code (recommandé)

```bash
# Install all agents to your Claude Code directory
./scripts/install.sh --tool claude-code

# Or manually copy a category if you only want one division
cp engineering/*.md ~/.claude/agents/

# Then activate any agent in your Claude Code sessions:
# "Hey Claude, activate Frontend Developer mode and help me build a React component"
```

### Option 2 : utiliser comme référence

Chaque fichier d'agent contient :
- Identité et traits de personnalité
- Mission principale et workflows
- Livrables techniques avec exemples de code
- Indicateurs de réussite et style de communication

Parcourez les agents ci-dessous et copiez/adaptez ceux dont vous avez besoin !

### Option 3 : utiliser avec d'autres outils (GitHub Copilot, Antigravity, Gemini CLI, OpenCode, OpenClaw, Cursor, Aider, Windsurf, Kimi Code, Codex)

```bash
# Step 1 -- generate integration files for all supported tools
./scripts/convert.sh

# Step 2 -- install interactively (auto-detects what you have installed)
./scripts/install.sh

# Or target a specific tool directly
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool gemini-cli
./scripts/install.sh --tool opencode
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool cursor
./scripts/install.sh --tool aider
./scripts/install.sh --tool windsurf
./scripts/install.sh --tool kimi
./scripts/install.sh --tool codex
```

**N'installez que les équipes dont vous avez besoin** (tout le monde ne veut pas les 16 divisions) :

```bash
./scripts/install.sh                                    # interactive wizard: pick tools + teams
./scripts/install.sh --tool claude-code --division engineering,security
./scripts/install.sh --tool cursor --agent frontend-developer,ui-designer
./scripts/install.sh --list teams                       # see every team + agent count
./scripts/install.sh --tool opencode --division engineering --dry-run
```

> **Note OpenCode :** le runtime d'OpenCode n'enregistre actuellement que ~119 agents et ignore silencieusement les autres ([bug en amont](https://github.com/anomalyco/opencode/issues/27988)). Installer un sous-ensemble avec `--division` vous maintient sous cette limite. L'installateur vous prévient lorsqu'une sélection la dépasserait.

Consultez la section [Intégrations multi-outils](#-multi-tool-integrations) ci-dessous pour tous les détails.

---

## 🎨 L'effectif de The Agency

### 💻 Division Engineering

Construire l'avenir, un commit à la fois.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🎨 [Frontend Developer](engineering/engineering-frontend-developer.md) | React/Vue/Angular, intégration d'UI, performance | Applications web modernes, UI au pixel près, optimisation des Core Web Vitals |
| 🏗️ [Backend Architect](engineering/engineering-backend-architect.md) | Conception d'API, architecture de bases de données, scalabilité | Systèmes côté serveur, microservices, infrastructure cloud |
| 📱 [Mobile App Builder](engineering/engineering-mobile-app-builder.md) | iOS/Android, React Native, Flutter | Applications mobiles natives et multiplateformes |
| 🤖 [AI Engineer](engineering/engineering-ai-engineer.md) | Modèles de ML, déploiement, intégration d'IA | Fonctionnalités de machine learning, pipelines de données, applications boostées à l'IA |
| 🚀 [DevOps Automator](engineering/engineering-devops-automator.md) | CI/CD, automatisation d'infrastructure, ops cloud | Développement de pipelines, automatisation du déploiement, supervision |
| ⚡ [Rapid Prototyper](engineering/engineering-rapid-prototyper.md) | Développement rapide de POC, MVP | Preuves de concept rapides, projets de hackathon, itération rapide |
| 💎 [Senior Developer](engineering/engineering-senior-developer.md) | Laravel/Livewire, patterns avancés | Implémentations complexes, décisions d'architecture |
| 🔧 [Filament Optimization Specialist](engineering/engineering-filament-optimization-specialist.md) | UX admin Filament PHP, refonte structurelle des formulaires, optimisation des ressources | Restructurer les ressources/formulaires/tables Filament pour des workflows admin plus rapides et plus clairs |
| ⚡ [Autonomous Optimization Architect](engineering/engineering-autonomous-optimization-architect.md) | Routage LLM, optimisation des coûts, shadow testing | Systèmes autonomes nécessitant une sélection d'API intelligente et des garde-fous de coûts |
| 🔩 [Embedded Firmware Engineer](engineering/engineering-embedded-firmware-engineer.md) | Bare-metal, RTOS, firmware ESP32/STM32/Nordic | Systèmes embarqués et objets connectés de qualité production |
| 🚨 [Incident Response Commander](engineering/engineering-incident-response-commander.md) | Gestion des incidents, post-mortems, astreinte | Piloter les incidents de production et bâtir la préparation aux incidents |
| ⛓️ [Solidity Smart Contract Engineer](engineering/engineering-solidity-smart-contract-engineer.md) | Contrats EVM, optimisation du gas, DeFi | Smart contracts sécurisés et optimisés en gas, protocoles DeFi |
| 🧭 [Codebase Onboarding Engineer](engineering/engineering-codebase-onboarding-engineer.md) | Onboarding rapide des développeurs, exploration de code en lecture seule, explication factuelle | Aider les nouveaux développeurs à comprendre vite des dépôts inconnus en lisant le code, en traçant les chemins d'exécution et en énonçant des faits sur la structure et le comportement |
| 📚 [Technical Writer](engineering/engineering-technical-writer.md) | Docs développeur, référence d'API, tutoriels | Documentation technique claire et précise |
| 💬 [WeChat Mini Program Developer](engineering/engineering-wechat-mini-program-developer.md) | Écosystème WeChat, Mini Programs, intégration de paiement | Construire des applications performantes pour l'écosystème WeChat |
| 👁️ [Code Reviewer](engineering/engineering-code-reviewer.md) | Revue de code constructive, sécurité, maintenabilité | Revues de PR, contrôles qualité du code, mentorat par la revue |
| 🗄️ [Database Optimizer](engineering/engineering-database-optimizer.md) | Conception de schémas, optimisation des requêtes, stratégies d'indexation | Tuning PostgreSQL/MySQL, débogage de requêtes lentes, planification de migrations |
| 🌿 [Git Workflow Master](engineering/engineering-git-workflow-master.md) | Stratégies de branches, commits conventionnels, Git avancé | Conception de workflow Git, nettoyage d'historique, gestion de branches adaptée à la CI |
| 🏛️ [Software Architect](engineering/engineering-software-architect.md) | Conception de systèmes, DDD, patterns d'architecture, analyse d'arbitrages | Décisions d'architecture, modélisation du domaine, stratégie d'évolution du système |
| 🛡️ [SRE](engineering/engineering-sre.md) | SLO, error budgets, observabilité, chaos engineering | Fiabilité en production, réduction du toil, planification de capacité |
| 🧬 [AI Data Remediation Engineer](engineering/engineering-ai-data-remediation-engineer.md) | Pipelines auto-réparants, SLM en air-gap, clustering sémantique | Réparer des données corrompues à grande échelle sans aucune perte |
| 🔧 [Data Engineer](engineering/engineering-data-engineer.md) | Pipelines de données, architecture lakehouse, ETL/ELT | Construire une infrastructure de données et un entrepôt fiables |
| 🔗 [Feishu Integration Developer](engineering/engineering-feishu-integration-developer.md) | Plateforme ouverte Feishu/Lark, bots, workflows | Construire des intégrations pour l'écosystème Feishu |
| 🧱 [CMS Developer](engineering/engineering-cms-developer.md) | Thèmes WordPress & Drupal, plugins/modules, architecture de contenu | Implémentation et personnalisation de CMS orientées code |
| 📧 [Email Intelligence Engineer](engineering/engineering-email-intelligence-engineer.md) | Parsing d'e-mails, extraction MIME, données structurées pour agents IA | Transformer des fils d'e-mails bruts en contexte prêt pour le raisonnement |
| 🎙️ [Voice AI Integration Engineer](engineering/engineering-voice-ai-integration-engineer.md) | Pipelines speech-to-text, Whisper, ASR, diarisation des locuteurs | Pipelines de transcription de bout en bout, prétraitement audio, livraison de transcriptions structurées |
| 🖧 [IT Service Manager](engineering/engineering-it-service-manager.md) | Gestion des services ITIL 4 | Gestion des incidents/problèmes/changements, SLA, CMDB |
| 🪡 [Minimal Change Engineer](engineering/engineering-minimal-change-engineer.md) | Diffs minimum viables | Corriger uniquement ce qui est demandé, sans dérive de périmètre |
| 📜 [OrgScript Engineer](engineering/engineering-orgscript-engineer.md) | Grammaire OrgScript & validation d'AST | Concevoir/parser des définitions de logique métier OrgScript |
| 🧬 [Prompt Engineer](engineering/engineering-prompt-engineer.md) | Conception & optimisation de prompts LLM | Transformer des instructions vagues en comportements IA fiables |
| 🕸️ [Multi-Agent Systems Architect](engineering/engineering-multi-agent-systems-architect.md) | Conception & gouvernance de pipelines multi-agents | Topologie, contexte, confiance, reprise sur erreur pour les systèmes d'agents |
| 🛒 [Drupal Shopping Cart Engineer](engineering/engineering-drupal-shopping-cart.md) | Boutiques Drupal Commerce | Catalogue, paiements, checkout, commandes sur Drupal 10/11 |
| 🛍️ [WordPress Shopping Cart Engineer](engineering/engineering-wordpress-shopping-cart.md) | Boutiques WooCommerce | Catalogue, paiements, checkout, conversion sur WordPress |

### 🎨 Division Design

Rendre le produit beau, utilisable et agréable.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🎯 [UI Designer](design/design-ui-designer.md) | Design visuel, bibliothèques de composants, design systems | Création d'interfaces, cohérence de marque, conception de composants |
| 🔍 [UX Researcher](design/design-ux-researcher.md) | Tests utilisateurs, analyse comportementale, recherche | Comprendre les utilisateurs, tests d'utilisabilité, insights de design |
| 🏛️ [UX Architect](design/design-ux-architect.md) | Architecture technique, systèmes CSS, implémentation | Fondations adaptées aux développeurs, accompagnement à l'implémentation |
| 🎭 [Brand Guardian](design/design-brand-guardian.md) | Identité de marque, cohérence, positionnement | Stratégie de marque, développement d'identité, chartes |
| 📖 [Visual Storyteller](design/design-visual-storyteller.md) | Récits visuels, contenu multimédia | Histoires visuelles percutantes, storytelling de marque |
| ✨ [Whimsy Injector](design/design-whimsy-injector.md) | Personnalité, plaisir, interactions ludiques | Ajouter de la joie, micro-interactions, easter eggs, personnalité de marque |
| 📷 [Image Prompt Engineer](design/design-image-prompt-engineer.md) | Prompts de génération d'images IA, photographie | Prompts photo pour Midjourney, DALL-E, Stable Diffusion |
| 🌈 [Inclusive Visuals Specialist](design/design-inclusive-visuals-specialist.md) | Représentation, atténuation des biais, imagerie authentique | Générer des images et vidéos IA culturellement justes |
| 🎭 [Persona Walkthrough Specialist](design/design-persona-walkthrough.md) | Parcours cognitifs guidés par persona | Simuler les réactions et les frictions des utilisateurs à chaque position de défilement |

### 💰 Division Paid Media

Transformer les dépenses publicitaires en résultats business mesurables.

| Agent | Spécialité | Quand l'utiliser |
| --- | --- | --- |
| 💰 [PPC Campaign Strategist](paid-media/paid-media-ppc-strategist.md) | Google/Microsoft/Amazon Ads, architecture de compte, enchères | Création de comptes, allocation de budget, scaling, diagnostic de performance |
| 🔍 [Search Query Analyst](paid-media/paid-media-search-query-analyst.md) | Analyse des termes de recherche, mots-clés négatifs, mapping d'intention | Audits de requêtes, élimination des dépenses gaspillées, découverte de mots-clés |
| 📋 [Paid Media Auditor](paid-media/paid-media-auditor.md) | Audits de compte à plus de 200 points, analyse concurrentielle | Reprises de compte, revues trimestrielles, pitchs concurrentiels |
| 📡 [Tracking & Measurement Specialist](paid-media/paid-media-tracking-specialist.md) | GTM, GA4, suivi de conversions, CAPI | Nouvelles implémentations, audits de tracking, migrations de plateforme |
| ✍️ [Ad Creative Strategist](paid-media/paid-media-creative-strategist.md) | Copy RSA, créa Meta, assets Performance Max | Lancements de créa, programmes de test, renouvellements anti-fatigue publicitaire |
| 📺 [Programmatic & Display Buyer](paid-media/paid-media-programmatic-buyer.md) | GDN, DSP, médias partenaires, display ABM | Planification display, prospection de partenaires, programmes ABM |
| 📱 [Paid Social Strategist](paid-media/paid-media-paid-social-strategist.md) | Meta, LinkedIn, TikTok, social multiplateforme | Programmes de pub social, choix de plateforme, stratégie d'audience |

### 💼 Division Sales

Transformer le pipeline en revenus par le métier, pas par la paperasse CRM.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🎯 [Outbound Strategist](sales/sales-outbound-strategist.md) | Prospection basée sur les signaux, séquences multicanales, ciblage ICP | Construire du pipeline par une prospection guidée par la recherche, pas par le volume |
| 🔍 [Discovery Coach](sales/sales-discovery-coach.md) | SPIN, Gap Selling, Sandler — conception des questions et structure d'appel | Préparer les appels de découverte, qualifier les opportunités, coacher les commerciaux |
| ♟️ [Deal Strategist](sales/sales-deal-strategist.md) | Qualification MEDDPICC, positionnement concurrentiel, plan de victoire | Scorer les deals, révéler les risques du pipeline, bâtir des stratégies gagnantes |
| 🛠️ [Sales Engineer](sales/sales-engineer.md) | Démos techniques, cadrage de POC, battlecards concurrentielles | Victoires techniques en avant-vente, préparation de démos, positionnement concurrentiel |
| 🏹 [Proposal Strategist](sales/sales-proposal-strategist.md) | Réponse aux appels d'offres, thèmes gagnants, structure narrative | Rédiger des propositions qui convainquent, pas qui se contentent de cocher des cases |
| 📊 [Pipeline Analyst](sales/sales-pipeline-analyst.md) | Prévisions, santé du pipeline, vélocité des deals, RevOps | Revues de pipeline, précision des prévisions, revenue operations |
| 🗺️ [Account Strategist](sales/sales-account-strategist.md) | Land-and-expand, QBR, cartographie des parties prenantes | Expansion post-vente, planification de comptes, croissance du NRR |
| 🏋️ [Sales Coach](sales/sales-coach.md) | Développement des commerciaux, coaching d'appels, animation des revues de pipeline | Améliorer chaque commercial et chaque deal grâce à un coaching structuré |
| 🎯 [Sales Outreach](specialized/sales-outreach.md) | Prospection à froid, cadences multi-touches, traitement des objections, propositions | Prospection B2B en haut de tunnel — de l'e-mail à froid au rendez-vous de découverte décroché |
| 🧲 [Offer & Lead Gen Strategist](sales/sales-offer-lead-gen-strategist.md) | Offres & lead magnets | Construction d'offres et génération de leads en haut de tunnel |

### 📢 Division Marketing

Faire grandir votre audience, une interaction authentique à la fois.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🚀 [Growth Hacker](marketing/marketing-growth-hacker.md) | Acquisition rapide d'utilisateurs, boucles virales, expérimentations | Croissance explosive, acquisition d'utilisateurs, optimisation des conversions |
| 📝 [Content Creator](marketing/marketing-content-creator.md) | Contenu multiplateforme, calendriers éditoriaux | Stratégie de contenu, copywriting, storytelling de marque |
| 🐦 [Twitter Engager](marketing/marketing-twitter-engager.md) | Engagement en temps réel, leadership d'opinion | Stratégie Twitter, campagnes LinkedIn, social professionnel |
| 🛰️ [X/Twitter Intelligence Analyst](marketing/marketing-x-twitter-intelligence-analyst.md) | Social listening, détection de tendances, surveillance de comptes | Veille sur les risques de marque, les concurrents et l'audience sur X/Twitter |
| 📱 [TikTok Strategist](marketing/marketing-tiktok-strategist.md) | Contenu viral, optimisation de l'algorithme | Croissance TikTok, contenu viral, audience Gen Z/Millennials |
| 📸 [Instagram Curator](marketing/marketing-instagram-curator.md) | Storytelling visuel, animation de communauté | Stratégie Instagram, développement esthétique, contenu visuel |
| 🤝 [Reddit Community Builder](marketing/marketing-reddit-community-builder.md) | Engagement authentique, contenu à valeur ajoutée | Stratégie Reddit, confiance de la communauté, marketing authentique |
| 📱 [App Store Optimizer](marketing/marketing-app-store-optimizer.md) | ASO, optimisation des conversions, visibilité | Marketing d'app, optimisation des stores, croissance d'app |
| 🌐 [Social Media Strategist](marketing/marketing-social-media-strategist.md) | Stratégie multiplateforme, campagnes | Stratégie social globale, campagnes multiplateformes |
| 📕 [Xiaohongshu Specialist](marketing/marketing-xiaohongshu-specialist.md) | Contenu lifestyle, stratégie portée par les tendances | Croissance Xiaohongshu, storytelling esthétique, audience Gen Z |
| 💬 [WeChat Official Account Manager](marketing/marketing-wechat-official-account.md) | Engagement des abonnés, marketing de contenu | Stratégie WeChat OA, animation de communauté, optimisation des conversions |
| 🧠 [Zhihu Strategist](marketing/marketing-zhihu-strategist.md) | Leadership d'opinion, engagement par le savoir | Construction d'autorité sur Zhihu, stratégie Q&A, génération de leads |
| 🇨🇳 [Baidu SEO Specialist](marketing/marketing-baidu-seo-specialist.md) | Optimisation Baidu, SEO Chine, conformité ICP | Se positionner sur Baidu et atteindre le marché de la recherche chinois |
| 🎬 [Bilibili Content Strategist](marketing/marketing-bilibili-content-strategist.md) | Algorithme de B站, culture du danmaku, croissance des UP主 | Construire des audiences sur Bilibili avec un contenu centré sur la communauté |
| 🎠 [Carousel Growth Engine](marketing/marketing-carousel-growth-engine.md) | Carrousels TikTok/Instagram, publication autonome | Générer et publier du contenu carrousel viral |
| 💼 [LinkedIn Content Creator](marketing/marketing-linkedin-content-creator.md) | Personal branding, leadership d'opinion, contenu professionnel | Croissance LinkedIn, construction d'audience professionnelle, contenu B2B |
| 🛒 [China E-Commerce Operator](marketing/marketing-china-ecommerce-operator.md) | Taobao, Tmall, Pinduoduo, live commerce | Piloter un e-commerce multiplateforme en Chine |
| 🎥 [Kuaishou Strategist](marketing/marketing-kuaishou-strategist.md) | Kuaishou, communauté 老铁, croissance par la base | Construire des audiences authentiques sur les marchés de tiers inférieur |
| 🔍 [SEO Specialist](marketing/marketing-seo-specialist.md) | SEO technique, stratégie de contenu, netlinking | Générer une croissance organique durable |
| 📘 [Book Co-Author](marketing/marketing-book-co-author.md) | Livres de leadership d'opinion, ghostwriting, édition | Collaboration stratégique de livre pour fondateurs et experts |
| 🌏 [Cross-Border E-Commerce Specialist](marketing/marketing-cross-border-ecommerce.md) | Amazon, Shopee, Lazada, logistique transfrontalière | Stratégie e-commerce transfrontalière sur tout le tunnel |
| 🎵 [Douyin Strategist](marketing/marketing-douyin-strategist.md) | Plateforme Douyin, marketing de vidéo courte, algorithme | Faire grandir les audiences sur la première plateforme de vidéo courte de Chine |
| 🎙️ [Livestream Commerce Coach](marketing/marketing-livestream-commerce-coach.md) | Formation des animateurs, optimisation du live, conversion | Bâtir des opérations de live commerce performantes |
| 🎧 [Podcast Strategist](marketing/marketing-podcast-strategist.md) | Stratégie de contenu podcast, optimisation des plateformes | Stratégie et opérations sur le marché chinois du podcast |
| 🔒 [Private Domain Operator](marketing/marketing-private-domain-operator.md) | WeCom, trafic privé, opérations communautaires | Construire des écosystèmes de domaine privé WeChat en entreprise |
| 🎬 [Short-Video Editing Coach](marketing/marketing-short-video-editing-coach.md) | Post-production, workflows de montage, specs des plateformes | Formation et optimisation pratiques du montage de vidéo courte |
| 🔥 [Weibo Strategist](marketing/marketing-weibo-strategist.md) | Sina Weibo, sujets tendance, engagement des fans | Opérations et croissance Weibo à 360° |
| 🎙️ [Global Podcast Strategist](marketing/marketing-global-podcast-strategist.md) | Positionnement d'émission, croissance d'audience, monétisation | Lancement de podcast, algorithmes de plateforme, sponsoring, animation de communauté |
| 🔮 [AI Citation Strategist](marketing/marketing-ai-citation-strategist.md) | AEO/GEO, visibilité dans les recommandations IA, audit de citations | Améliorer la visibilité de la marque sur ChatGPT, Claude, Gemini, Perplexity |
| 🇨🇳 [China Market Localization Strategist](marketing/marketing-china-market-localization-strategist.md) | Localisation full-stack pour le marché chinois, GTM Douyin/Xiaohongshu/WeChat | Transformer les signaux de tendance en stratégies de go-to-market actionnables en Chine |
| 🎬 [Video Optimization Specialist](marketing/marketing-video-optimization-specialist.md) | Stratégie d'algorithme YouTube, chapitrage, concepts de miniatures | Croissance de chaîne YouTube, SEO vidéo, optimisation de la rétention d'audience |
| 🏗️ [AEO Foundations Architect](marketing/marketing-aeo-foundations.md) | Infrastructure d'AI Engine Optimization | llms.txt, robots.txt compatible IA, fichiers de découverte d'agents |
| 🤖 [Agentic Search Optimizer](marketing/marketing-agentic-search-optimizer.md) | WebMCP & exécution de tâches agentiques | Rendre les sites utilisables par les agents de navigation IA |
| 📧 [Email Marketing Strategist](marketing/marketing-email-strategist.md) | E-mail de cycle de vie & délivrabilité | Campagnes CRM, automatisation, segmentation |
| 📡 [Multi-Platform Publisher](marketing/marketing-multi-platform-publisher.md) | Publication multiplateforme chinoise en un clic | Diffuser un même article vers 知乎/小红书/CSDN/B站/公众号/掘金 |
| 📣 [PR & Communications Manager](marketing/marketing-pr-communications-manager.md) | RP, relations presse & comm de crise | Communiqués de presse, leadership d'opinion, réputation |

### 📊 Division Product

Construire la bonne chose au bon moment.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🎯 [Sprint Prioritizer](product/product-sprint-prioritizer.md) | Planification agile, priorisation des fonctionnalités | Planification de sprint, allocation des ressources, gestion du backlog |
| 🔍 [Trend Researcher](product/product-trend-researcher.md) | Veille marché, analyse concurrentielle | Étude de marché, évaluation d'opportunités, identification de tendances |
| 💬 [Feedback Synthesizer](product/product-feedback-synthesizer.md) | Analyse des retours utilisateurs, extraction d'insights | Analyse des feedbacks, insights utilisateurs, priorités produit |
| 🧠 [Behavioral Nudge Engine](product/product-behavioral-nudge-engine.md) | Psychologie comportementale, conception de nudges, engagement | Maximiser la motivation des utilisateurs grâce aux sciences comportementales |
| 🧭 [Product Manager](product/product-manager.md) | Pilotage produit sur tout le cycle de vie | Discovery, PRD, planification de roadmap, GTM, mesure des résultats |

### 🎬 Division Project Management

Faire arriver les trains à l'heure (et dans le budget).

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🎬 [Studio Producer](project-management/project-management-studio-producer.md) | Orchestration de haut niveau, gestion de portefeuille | Supervision multi-projets, alignement stratégique, allocation des ressources |
| 🐑 [Project Shepherd](project-management/project-management-project-shepherd.md) | Coordination transverse, gestion des délais | Coordination de projet de bout en bout, gestion des parties prenantes |
| ⚙️ [Studio Operations](project-management/project-management-studio-operations.md) | Efficacité au quotidien, optimisation des processus | Excellence opérationnelle, soutien aux équipes, productivité |
| 🧪 [Experiment Tracker](project-management/project-management-experiment-tracker.md) | Tests A/B, validation d'hypothèses | Gestion des expérimentations, décisions data-driven, testing |
| 👔 [Senior Project Manager](project-management/project-manager-senior.md) | Cadrage réaliste, conversion en tâches | Convertir des specs en tâches, gestion du périmètre |
| 📋 [Jira Workflow Steward](project-management/project-management-jira-workflow-steward.md) | Workflow Git, stratégie de branches, traçabilité | Faire respecter une discipline Git liée à Jira et la livraison |
| 📋 [Meeting Notes Specialist](project-management/project-management-meeting-notes-specialist.md) | Comptes rendus de réunion structurés | Extraire décisions, actions à mener, questions ouvertes |

### 🧪 Division Testing

Casser les choses pour que les utilisateurs n'aient pas à le faire.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 📸 [Evidence Collector](testing/testing-evidence-collector.md) | QA par captures d'écran, preuve visuelle | Tests d'UI, vérification visuelle, documentation des bugs |
| 🔍 [Reality Checker](testing/testing-reality-checker.md) | Certification fondée sur des preuves, contrôles qualité | Prêt pour la production, validation qualité, certification de version |
| 📊 [Test Results Analyzer](testing/testing-test-results-analyzer.md) | Évaluation des tests, analyse des métriques | Analyse des résultats de tests, insights qualité, reporting de couverture |
| ⚡ [Performance Benchmarker](testing/testing-performance-benchmarker.md) | Tests de performance, optimisation | Tests de vitesse, tests de charge, tuning de performance |
| 🔌 [API Tester](testing/testing-api-tester.md) | Validation d'API, tests d'intégration | Tests d'API, vérification des endpoints, QA d'intégration |
| 🛠️ [Tool Evaluator](testing/testing-tool-evaluator.md) | Évaluation technologique, choix d'outils | Évaluer des outils, recommandations logicielles, décisions techniques |
| 🔄 [Workflow Optimizer](testing/testing-workflow-optimizer.md) | Analyse des processus, amélioration des workflows | Optimisation des processus, gains d'efficacité, opportunités d'automatisation |
| ♿ [Accessibility Auditor](testing/testing-accessibility-auditor.md) | Audit WCAG, tests avec technologies d'assistance | Conformité d'accessibilité, tests au lecteur d'écran, vérification du design inclusif |

### 🔒 Division Security

Défendre la stack — de l'architecture secure-by-design à la réponse aux intrusions.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🛡️ [Security Architect](security/security-architect.md) | Modélisation des menaces, secure-by-design, frontières de confiance | Modèles de sécurité système, revues d'architecture, défense en profondeur |
| 🔐 [Application Security Engineer](security/security-appsec-engineer.md) | Sécurité du SDLC, SAST/DAST, revue de code sécurisée | Sécuriser le cycle de développement, vulnérabilités au niveau du code |
| 🗡️ [Penetration Tester](security/security-penetration-tester.md) | Pentests autorisés, opérations red team, exploitation | Trouver les failles exploitables avant les attaquants |
| ☁️ [Cloud Security Architect](security/security-cloud-security-architect.md) | Zero trust, défense en profondeur cloud-native | Sécuriser les infrastructures et architectures cloud |
| 🚨 [Incident Responder](security/security-incident-responder.md) | DFIR, investigation d'intrusion, confinement des menaces | Intrusions en cours, forensique, gestion de crise |
| 🔍 [Threat Intelligence Analyst](security/security-threat-intelligence-analyst.md) | Suivi des adversaires, cartographie des campagnes, ATT&CK | Comprendre qui attaque et comment |
| 🎯 [Threat Detection Engineer](security/security-threat-detection-engineer.md) | Règles SIEM, threat hunting, mapping ATT&CK | Construire des couches de détection et du threat hunting |
| 🛡️ [Senior SecOps Engineer](security/security-senior-secops.md) | Scan de secrets, soumissions sécurisées par défaut | Sécurité défensive au niveau du code à chaque modification |
| 📋 [Compliance Auditor](security/security-compliance-auditor.md) | SOC 2, ISO 27001, HIPAA, PCI-DSS | Accompagner les organisations vers la certification de conformité |
| 🛡️ [Blockchain Security Auditor](security/security-blockchain-security-auditor.md) | Audits de smart contracts, analyse d'exploits | Trouver les vulnérabilités des contrats avant déploiement |

### 🛟 Division Support

La colonne vertébrale de l'opération.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 💬 [Support Responder](support/support-support-responder.md) | Service client, résolution des problèmes | Support client, expérience utilisateur, opérations de support |
| 📊 [Analytics Reporter](support/support-analytics-reporter.md) | Analyse de données, tableaux de bord, insights | Business intelligence, suivi des KPI, visualisation de données |
| 💰 [Finance Tracker](support/support-finance-tracker.md) | Planification financière, gestion budgétaire | Analyse financière, trésorerie, performance de l'entreprise |
| 🏗️ [Infrastructure Maintainer](support/support-infrastructure-maintainer.md) | Fiabilité des systèmes, optimisation des performances | Gestion d'infrastructure, opérations système, supervision |
| ⚖️ [Legal Compliance Checker](support/support-legal-compliance-checker.md) | Conformité, réglementation, revue juridique | Conformité légale, exigences réglementaires, gestion des risques |
| 📑 [Executive Summary Generator](support/support-executive-summary-generator.md) | Communication C-suite, synthèses stratégiques | Reporting de direction, communication stratégique, aide à la décision |

### 🥽 Division Spatial Computing

Construire l'avenir immersif.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🏗️ [XR Interface Architect](spatial-computing/xr-interface-architect.md) | Conception d'interaction spatiale, UX immersive | Conception d'interfaces AR/VR/XR, UX de spatial computing |
| 💻 [macOS Spatial/Metal Engineer](spatial-computing/macos-spatial-metal-engineer.md) | Swift, Metal, 3D haute performance | Spatial computing sur macOS, apps natives Vision Pro |
| 🌐 [XR Immersive Developer](spatial-computing/xr-immersive-developer.md) | WebXR, AR/VR dans le navigateur | Expériences immersives navigateur, apps WebXR |
| 🎮 [XR Cockpit Interaction Specialist](spatial-computing/xr-cockpit-interaction-specialist.md) | Contrôles de type cockpit, systèmes immersifs | Systèmes de contrôle de cockpit, interfaces de contrôle immersives |
| 🍎 [visionOS Spatial Engineer](spatial-computing/visionos-spatial-engineer.md) | Développement Apple Vision Pro | Apps Vision Pro, expériences de spatial computing |
| 🔌 [Terminal Integration Specialist](spatial-computing/terminal-integration-specialist.md) | Intégration de terminal, outils en ligne de commande | Outils CLI, workflows de terminal, outils pour développeurs |

### 🎯 Division Specialized

Les spécialistes uniques qui n'entrent dans aucune case.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🎭 [Agents Orchestrator](specialized/agents-orchestrator.md) | Coordination multi-agents, gestion de workflows | Projets complexes nécessitant la coordination de plusieurs agents |
| 🔍 [LSP/Index Engineer](specialized/lsp-index-engineer.md) | Language Server Protocol, intelligence du code | Systèmes d'intelligence du code, implémentation LSP, indexation sémantique |
| 📥 [Sales Data Extraction Agent](specialized/sales-data-extraction-agent.md) | Surveillance Excel, extraction de métriques de vente | Ingestion de données de vente, métriques MTD/YTD/fin d'année |
| 📈 [Data Consolidation Agent](specialized/data-consolidation-agent.md) | Agrégation de données de vente, rapports de tableau de bord | Synthèses par territoire, performance des commerciaux, instantanés de pipeline |
| 📬 [Report Distribution Agent](specialized/report-distribution-agent.md) | Diffusion automatisée de rapports | Distribution de rapports par territoire, envois planifiés |
| 🔐 [Agentic Identity & Trust Architect](specialized/agentic-identity-trust.md) | Identité d'agent, authentification, vérification de confiance | Systèmes d'identité multi-agents, autorisation d'agents, pistes d'audit |
| 🔗 [Identity Graph Operator](specialized/identity-graph-operator.md) | Résolution d'identité partagée pour systèmes multi-agents | Déduplication d'entités, propositions de fusion, cohérence d'identité inter-agents |
| 💸 [Accounts Payable Agent](specialized/accounts-payable-agent.md) | Traitement des paiements, gestion des fournisseurs, audit | Exécution autonome de paiements en crypto, fiat et stablecoins |
| 🌍 [Cultural Intelligence Strategist](specialized/specialized-cultural-intelligence-strategist.md) | UX mondiale, représentation, exclusion culturelle | S'assurer que le logiciel résonne d'une culture à l'autre |
| 🗣️ [Developer Advocate](specialized/specialized-developer-advocate.md) | Animation de communauté, DX, contenu pour développeurs | Faire le pont entre le produit et la communauté de développeurs |
| 🔬 [Model QA Specialist](specialized/specialized-model-qa.md) | Audits ML, analyse de features, interprétabilité | QA de bout en bout pour les modèles de machine learning |
| 🗃️ [ZK Steward](specialized/zk-steward.md) | Gestion des connaissances, Zettelkasten, notes | Construire des bases de connaissances connectées et validées |
| 🔌 [MCP Builder](specialized/specialized-mcp-builder.md) | Serveurs Model Context Protocol, outillage d'agents IA | Construire des serveurs MCP qui étendent les capacités des agents IA |
| 📄 [Document Generator](specialized/specialized-document-generator.md) | Génération de PDF, PPTX, DOCX, XLSX depuis du code | Création de documents professionnels, rapports, visualisation de données |
| ⚙️ [Automation Governance Architect](specialized/automation-governance-architect.md) | Gouvernance de l'automatisation, n8n, audit de workflows | Évaluer et gouverner les automatisations métier à grande échelle |
| 📚 [Corporate Training Designer](specialized/corporate-training-designer.md) | Formation en entreprise, conception de cursus | Concevoir des systèmes de formation et des parcours d'apprentissage |
| 🌱 [Personal Growth Mentor](specialized/personal-growth-mentor.md) | Clarté des objectifs, systèmes d'habitudes, responsabilisation, stratégie de vie | Développement personnel transverse, sans baratin motivationnel |
| 🏛️ [Government Digital Presales Consultant](specialized/government-digital-presales-consultant.md) | Avant-vente ToG en Chine, transformation numérique | Propositions et appels d'offres de transformation numérique pour le secteur public |
| ⚕️ [Healthcare Marketing Compliance](specialized/healthcare-marketing-compliance.md) | Conformité publicitaire santé en Chine | Conformité réglementaire du marketing dans la santé |
| 🎯 [Recruitment Specialist](specialized/recruitment-specialist.md) | Acquisition de talents, opérations de recrutement | Stratégie de recrutement, sourcing et processus d'embauche |
| 🎓 [Study Abroad Advisor](specialized/study-abroad-advisor.md) | Éducation internationale, planification des candidatures | Planification d'études à l'étranger aux États-Unis, au Royaume-Uni, au Canada et en Australie |
| 🔗 [Supply Chain Strategist](specialized/supply-chain-strategist.md) | Gestion de la supply chain, stratégie d'achats | Optimisation de la supply chain et planification des achats |
| 🗺️ [Workflow Architect](specialized/specialized-workflow-architect.md) | Découverte, cartographie et spécification de workflows | Cartographier chaque chemin dans un système avant d'écrire le code |
| ☁️ [Salesforce Architect](specialized/specialized-salesforce-architect.md) | Conception Salesforce multi-cloud, governor limits, intégrations | Architecture Salesforce d'entreprise, stratégie d'org, pipelines de déploiement |
| 🇫🇷 [French Consulting Market Navigator](specialized/specialized-french-consulting-market.md) | Écosystème ESN/SSII, portage salarial, positionnement tarifaire | Conseil en freelance sur le marché IT français |
| 🇰🇷 [Korean Business Navigator](specialized/specialized-korean-business-navigator.md) | Culture d'affaires coréenne, processus 품의, mécanique relationnelle | Professionnels étrangers naviguant les relations d'affaires coréennes |
| 🏗️ [Civil Engineer](specialized/specialized-civil-engineer.md) | Analyse structurelle, conception géotechnique, codes de construction internationaux | Ingénierie structurelle multi-normes : Eurocode, ACI, AISC et plus |
| 🎧 [Customer Service](specialized/customer-service.md) | Support omnicanal, traitement des réclamations, rétention, escalade | Support client tous secteurs — retail, SaaS, hôtellerie, finance, logistique |
| 🏥 [Healthcare Customer Service](specialized/healthcare-customer-service.md) | Support patient conscient des règles HIPAA, facturation, assurance, routage des urgences | Organisations de santé ayant besoin d'un support patient conforme et empathique |
| 🏨 [Hospitality Guest Services](specialized/hospitality-guest-services.md) | Réservations, conciergerie, gestion des réclamations, fidélité, événements | Hôtels, resorts, restaurants et lieux d'événements |
| 🤝 [HR Onboarding](specialized/hr-onboarding.md) | Pré-onboarding, conformité, inscription aux avantages, plans 30-60-90 jours | Toute entreprise intégrant de nouveaux collaborateurs — de la startup au grand groupe |
| 🌐 [Language Translator](specialized/language-translator.md) | Traduction espagnol ↔ anglais, prise en compte des dialectes, contexte culturel | Besoins de traduction voyage, business, médical et juridique |
| ⏱️ [Legal Billing & Time Tracking](specialized/legal-billing-time-tracking.md) | Saisie du temps, descriptifs de facturation, conformité IOLTA, recouvrements | Cabinets d'avocats maximisant le recouvrement et la précision de facturation |
| 📋 [Legal Client Intake](specialized/legal-client-intake.md) | Qualification des prospects, contrôle des conflits, prise de rendez-vous | Cabinets d'avocats convertissant les demandes en clients sous mandat |
| ⚖️ [Legal Document Review](specialized/legal-document-review.md) | Revue de contrats, signalement des risques, comparaison de versions, conformité | Première relecture prête pour l'avocat, tous domaines de pratique |
| 🏦 [Loan Officer Assistant](specialized/loan-officer-assistant.md) | Réception emprunteur, conformité TRID, suivi de pipeline, coordination de clôture | Équipes de crédit immobilier et à la consommation |
| 🏠 [Real Estate Buyer & Seller](specialized/real-estate-buyer-seller.md) | Représentation acheteur/vendeur, offres, coordination de transaction | Transactions immobilières résidentielles et d'investissement |
| 🛒 [Retail Customer Returns](specialized/retail-customer-returns.md) | Traitement des retours, prévention de la fraude, échanges, retours fournisseurs | Retail physique, e-commerce et omnicanal |
| ♟️ [Business Strategist](specialized/business-strategist.md) | Stratégie de conseil en management | Analyse concurrentielle, entrée sur un marché, plan de croissance |
| 🔄 [Change Management Consultant](specialized/change-management-consultant.md) | Conduite du changement ADKAR/Kotter/Prosci | Accompagner les organisations dans la transformation & l'adoption |
| 🧭 [Chief of Staff](specialized/specialized-chief-of-staff.md) | Coordination exécutive | Filtrer le bruit, s'approprier les processus, orienter les décisions |
| 🌟 [Customer Success Manager](specialized/customer-success-manager.md) | Onboarding, santé & rétention | QBR, prévention du churn, renouvellements & expansion |
| 📝 [Grant Writer](specialized/grant-writer.md) | Demandes de subventions & financement | LOI, propositions, budgets pour associations/recherche |
| 🏥 [Medical Billing & Coding Specialist](specialized/medical-billing-coding-specialist.md) | ICD-10/CPT/HCPCS & cycle de revenus | Réclamations, gestion des refus, optimisation du RCM |
| 💰 [Pricing Analyst](specialized/specialized-pricing-analyst.md) | Modèles de prix & optimisation des marges | Analyse concurrents/coûts, tarification à la valeur |
| 💼 [Chief Financial Officer](specialized/chief-financial-officer.md) | Allocation du capital & stratégie financière | Trésorerie, FP&A, finance M&A, reporting investisseurs & conseil |
| 🌱 [ESG & Sustainability Officer](specialized/esg-sustainability-officer.md) | Programmes ESG & reporting extra-financier | Stratégie de durabilité, décarbonation, reporting |
| 🔐 [Data Privacy Officer](specialized/data-privacy-officer.md) | Conformité RGPD/CCPA | Cartographie des données, AIPD, consentement, réponse aux violations |
| ⚙️ [Operations Manager](specialized/operations-manager.md) | Opérations Lean/Six Sigma | Cartographie des processus, planification de capacité, gouvernance des KPI |
| 🤝 [M&A Integration Manager](specialized/ma-integration-manager.md) | Intégration post-fusion | Plans Day 1/100 jours, suivi des synergies, gestion des TSA |
| 🧠 [Organizational Psychologist](specialized/organizational-psychologist.md) | Dynamique d'équipe & santé de la culture | Sécurité psychologique, risque de burnout, équipes performantes |
| ⚔️ [Strategy Duel Agent](specialized/specialized-strategy-duel-agent.md) | Théorie des jeux & les 36 stratagèmes | Duels de stratégie au tour par tour, simulation de scénarios adverses |

### 💵 Division Finance

Comptabilité, analyse financière, stratégie fiscale et recherche en investissement.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 📒 [Bookkeeper & Controller](finance/finance-bookkeeper-controller.md) | Clôture de fin de mois, rapprochements, conformité GAAP, contrôles internes | Opérations comptables quotidiennes, préparation aux audits, tenue des registres financiers |
| 📊 [Financial Analyst](finance/finance-financial-analyst.md) | Modélisation financière, prévisions, analyse de scénarios, aide à la décision | Modèles à trois états, analyse des écarts, business intelligence data-driven |
| 📈 [FP&A Analyst](finance/finance-fpa-analyst.md) | Budgétisation, prévisions glissantes, analyse des écarts, business reviews | Plans d'exploitation annuels, business reviews mensuelles, allocation stratégique des ressources |
| 🔍 [Investment Researcher](finance/finance-investment-researcher.md) | Due diligence, analyse de portefeuille, valorisation d'actifs, recherche actions | Élaboration de thèses d'investissement, évaluation des risques, étude de marché |
| 🏛️ [Tax Strategist](finance/finance-tax-strategist.md) | Optimisation fiscale, conformité multi-juridictionnelle, prix de transfert | Structuration d'entités, analyse du TEI, défense en cas d'audit, planification fiscale stratégique |

### 🎮 Division Game Development

Construire des mondes, des systèmes et des expériences sur tous les grands moteurs.

#### Agents multi-moteurs (indépendants du moteur)

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🎯 [Game Designer](game-development/game-designer.md) | Design de systèmes, rédaction de GDD, équilibrage économique, boucles de gameplay | Concevoir les mécaniques de jeu, les systèmes de progression, rédiger les documents de design |
| 🗺️ [Level Designer](game-development/level-designer.md) | Théorie du level design, rythme, design de rencontres, narration environnementale | Construire des niveaux, concevoir le flux des rencontres, narration spatiale |
| 🎨 [Technical Artist](game-development/technical-artist.md) | Shaders, VFX, pipeline LOD, optimisation art-vers-moteur | Faire le pont entre l'art et l'ingénierie, écriture de shaders, pipelines d'assets sûrs en performance |
| 🔊 [Game Audio Engineer](game-development/game-audio-engineer.md) | FMOD/Wwise, musique adaptative, audio spatial, budgets audio | Systèmes audio interactifs, musique dynamique, performance audio |
| 📖 [Narrative Designer](game-development/narrative-designer.md) | Systèmes narratifs, dialogues à embranchements, architecture de lore | Écrire des récits à embranchements, implémenter des systèmes de dialogue, lore d'univers |

#### Unity

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🏗️ [Unity Architect](game-development/unity/unity-architect.md) | ScriptableObjects, modularité data-driven, DOTS/ECS | Projets Unity à grande échelle, conception de systèmes data-driven, travail de performance ECS |
| ✨ [Unity Shader Graph Artist](game-development/unity/unity-shader-graph-artist.md) | Shader Graph, HLSL, URP/HDRP, Renderer Features | Matériaux Unity personnalisés, shaders VFX, passes de post-traitement |
| 🌐 [Unity Multiplayer Engineer](game-development/unity/unity-multiplayer-engineer.md) | Netcode for GameObjects, Unity Relay/Lobby, autorité serveur, prédiction | Jeux Unity en ligne, prédiction côté client, intégration Unity Gaming Services |
| 🛠️ [Unity Editor Tool Developer](game-development/unity/unity-editor-tool-developer.md) | EditorWindows, AssetPostprocessors, PropertyDrawers, validation de build | Outillage personnalisé de l'éditeur Unity, automatisation de pipeline, validation de contenu |

#### Unreal Engine

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| ⚙️ [Unreal Systems Engineer](game-development/unreal-engine/unreal-systems-engineer.md) | Hybride C++/Blueprint, GAS, contraintes Nanite, gestion mémoire | Systèmes de gameplay Unreal complexes, Gameplay Ability System, C++ au niveau moteur |
| 🎨 [Unreal Technical Artist](game-development/unreal-engine/unreal-technical-artist.md) | Material Editor, Niagara, PCG, Substrate | Matériaux Unreal, VFX Niagara, génération de contenu procédural |
| 🌐 [Unreal Multiplayer Architect](game-development/unreal-engine/unreal-multiplayer-architect.md) | Réplication d'acteurs, hiérarchie GameMode/GameState, serveur dédié | Jeux Unreal en ligne, replication graphs, Unreal à autorité serveur |
| 🗺️ [Unreal World Builder](game-development/unreal-engine/unreal-world-builder.md) | World Partition, Landscape, HLOD, LWC | Grands niveaux open-world Unreal, systèmes de streaming, terrain à grande échelle |

#### Godot

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 📜 [Godot Gameplay Scripter](game-development/godot/godot-gameplay-scripter.md) | GDScript 2.0, signaux, composition, typage statique | Systèmes de gameplay Godot, composition de scènes, GDScript soucieux de la performance |
| 🌐 [Godot Multiplayer Engineer](game-development/godot/godot-multiplayer-engineer.md) | MultiplayerAPI, ENet/WebRTC, RPC, modèle d'autorité | Jeux Godot en ligne, réplication de scènes, Godot à autorité serveur |
| ✨ [Godot Shader Developer](game-development/godot/godot-shader-developer.md) | Langage de shading Godot, VisualShader, RenderingDevice | Matériaux Godot personnalisés, effets 2D/3D, post-traitement, compute shaders |

#### Blender

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🧩 [Blender Addon Engineer](game-development/blender/blender-addon-engineer.md) | Python Blender (`bpy`), opérateurs/panneaux personnalisés, validateurs d'assets, exporteurs, automatisation de pipeline | Construire des add-ons Blender, des outils de préparation d'assets, des workflows d'export et de l'automatisation de pipeline DCC |

#### Roblox Studio

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| ⚙️ [Roblox Systems Scripter](game-development/roblox-studio/roblox-systems-scripter.md) | Luau, RemoteEvents/Functions, DataStore, architecture modulaire à autorité serveur | Construire des systèmes de jeu Roblox sécurisés, communication client-serveur, persistance des données |
| 🎯 [Roblox Experience Designer](game-development/roblox-studio/roblox-experience-designer.md) | Boucles d'engagement, monétisation, rétention D1/D7, flux d'onboarding | Concevoir des boucles de jeu Roblox, des Game Passes, des récompenses quotidiennes, la rétention des joueurs |
| 👗 [Roblox Avatar Creator](game-development/roblox-studio/roblox-avatar-creator.md) | Pipeline UGC, rigging d'accessoires, soumission au Creator Marketplace | Objets UGC Roblox, personnalisation HumanoidDescription, boutiques d'avatars en jeu |

### 📚 Division Academic

La rigueur universitaire au service du world-building, du storytelling et du design narratif.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🌍 [Anthropologist](academic/academic-anthropologist.md) | Systèmes culturels, parenté, rituels, systèmes de croyances | Concevoir des sociétés culturellement cohérentes dotées d'une logique interne |
| 🌐 [Geographer](academic/academic-geographer.md) | Géographie physique/humaine, climat, cartographie | Construire des mondes géographiquement cohérents avec un relief et des peuplements réalistes |
| 📚 [Historian](academic/academic-historian.md) | Analyse historique, périodisation, culture matérielle | Valider la cohérence historique, enrichir les décors de détails d'époque authentiques |
| 📜 [Narratologist](academic/academic-narratologist.md) | Théorie narrative, structure d'histoire, arcs de personnages | Analyser et améliorer la structure narrative à l'aide de cadres théoriques établis |
| 🧠 [Psychologist](academic/academic-psychologist.md) | Théorie de la personnalité, motivation, schémas cognitifs | Construire des personnages psychologiquement crédibles ancrés dans la recherche |

---

### 🌍 Division GIS

Cartographier la Terre, analyser le monde bâti et extraire de l'intelligence des données géospatiales.

| Agent | Spécialité | Quand l'utiliser |
|-------|-----------|-------------|
| 🧠 [Technical Consultant](gis/gis-technical-consultant.md) | Stratégie SIG, analyse d'écarts, roadmaps technologiques, transformation numérique | Comprendre les besoins métier, choisir la bonne stack géospatiale, planifier des programmes SIG multi-phases |
| 🔧 [Solution Engineer](gis/gis-solution-engineer.md) | Prototypage Esri + FOSS4G, livraison de PoC, faisabilité technique | Construire des démos fonctionnelles, valider des approches techniques, soutien avant-vente |
| 🖥️ [GIS Analyst](gis/gis-analyst.md) | Production cartographique, contrôle qualité des données, symbologie, mises en page, requêtes spatiales | Opérations SIG quotidiennes, cartes prêtes à publier, maintien de l'intégrité des données |
| 📦 [Spatial Data Engineer](gis/gis-spatial-data-engineer.md) | ETL géospatial, conversion de formats, reprojection de CRS, pipelines automatisés | Ingérer des données désordonnées de toute source, construire des pipelines de transformation reproductibles |
| ⚙️ [Geoprocessing Specialist](gis/gis-geoprocessing-specialist.md) | ArcPy, Python Toolbox (.pyt), Model Builder, automatisation par lots | Automatiser les workflows SIG répétitifs, construire des outils de géotraitement personnalisés |
| ✅ [GIS QA Engineer](gis/gis-qa-engineer.md) | Validation de topologie, audit de métadonnées, cohérence des CRS, évaluation de la précision | Contrôles qualité avant publication, vérification de conformité, audits d'intégrité des données |
| 🤖 [GeoAI/ML Engineer](gis/gis-geoai-ml-engineer.md) | Extraction de features, détection d'objets, segmentation sémantique, classification de l'occupation du sol | Extraire bâtiments/routes/véhicules d'imagerie, détection de changements, surveillance environnementale |
| 🏗️ [BIM/GIS Specialist](gis/gis-bim-specialist.md) | Revit/IFC vers SIG, cartographie intérieure, architecture de jumeau numérique, gestion d'installations | Campus intelligent, jumeaux numériques d'aéroports, navigation intérieure, exploitation de bâtiments |
| 🏔️ [3D & Scene Developer](gis/gis-3d-scene-developer.md) | Cesium, ArcGIS Scene Viewer, 3D Tiles, nuages de points, visualisation de terrain | Scènes de villes 3D, survols de terrain, visionneuses web de nuages de points, partage de scènes protégé par OAuth |
| 📊 [Spatial Data Scientist](gis/gis-spatial-data-scientist.md) | Statistiques spatiales, clustering, régression, interpolation, analyse de semis de points | Détection de points chauds, modélisation spatiale, analytique prédictive, analyse de niveau recherche |
| 🛸 [Drone/Reality Mapping](gis/gis-drone-reality-mapping.md) | Photogrammétrie, orthomosaïque, MNT/MNS, classification de nuages de points, maillage 3D | Traitement de levés par drone, capture du réel, suivi de chantier, cartographie environnementale |
| 🌐 [Web GIS Developer](gis/gis-web-gis-developer.md) | MapLibre GL JS, ArcGIS JS API, Leaflet, tableaux de bord temps réel, API REST | Construire des cartes web interactives, des tableaux de bord opérationnels, de la visualisation de données en temps réel |
| 🎨 [Cartography Designer](gis/gis-cartography-designer.md) | Théorie des couleurs, typographie, design de fonds de carte, hiérarchie visuelle, esthétique print et web | Rendre les cartes belles et lisibles, palettes adaptées aux daltoniens, mises en page cartographiques professionnelles |

---

## 🎯 Cas d'usage concrets

### Scénario 1 : construire le MVP d'une startup

**Votre équipe** :
1. 🎨 **Frontend Developer** - Construire l'application React
2. 🏗️ **Backend Architect** - Concevoir l'API et la base de données
3. 🚀 **Growth Hacker** - Planifier l'acquisition d'utilisateurs
4. ⚡ **Rapid Prototyper** - Cycles d'itération rapides
5. 🔍 **Reality Checker** - Garantir la qualité avant le lancement

**Résultat** : livrer plus vite avec une expertise spécialisée à chaque étape.

---

### Scénario 2 : lancement d'une campagne marketing

**Votre équipe** :
1. 📝 **Content Creator** - Développer le contenu de la campagne
2. 🐦 **Twitter Engager** - Stratégie et exécution Twitter
3. 📸 **Instagram Curator** - Contenu visuel et stories
4. 🤝 **Reddit Community Builder** - Engagement authentique de la communauté
5. 📊 **Analytics Reporter** - Suivre et optimiser la performance

**Résultat** : campagne multicanale coordonnée avec une expertise propre à chaque plateforme.

---

### Scénario 3 : développement d'une fonctionnalité en entreprise

**Votre équipe** :
1. 👔 **Senior Project Manager** - Cadrage et planification des tâches
2. 💎 **Senior Developer** - Implémentation complexe
3. 🎨 **UI Designer** - Design system et composants
4. 🧪 **Experiment Tracker** - Planification des tests A/B
5. 📸 **Evidence Collector** - Vérification de la qualité
6. 🔍 **Reality Checker** - Prêt pour la production

**Résultat** : une livraison de qualité entreprise avec des contrôles qualité et de la documentation.

---

### Scénario 4 : reprise d'un compte Paid Media

**Votre équipe** :

1. 📋 **Paid Media Auditor** - Évaluation complète du compte
2. 📡 **Tracking & Measurement Specialist** - Vérifier l'exactitude du suivi des conversions
3. 💰 **PPC Campaign Strategist** - Refondre l'architecture du compte
4. 🔍 **Search Query Analyst** - Nettoyer les dépenses gaspillées sur les termes de recherche
5. ✍️ **Ad Creative Strategist** - Renouveler toute la copy et les extensions
6. 📊 **Analytics Reporter** (Division Support) - Construire les tableaux de bord de reporting

**Résultat** : une reprise de compte systématique avec un suivi vérifié, le gaspillage éliminé, la structure optimisée et la créa renouvelée — le tout dans les 30 premiers jours.

---

### Scénario 5 : product discovery avec toute l'agence

**Votre équipe** : les 8 divisions travaillant en parallèle sur une même mission.

Voir l'**[exercice Nexus Spatial Discovery](examples/nexus-spatial-discovery.md)** -- un exemple complet où 8 agents (Product Trend Researcher, Backend Architect, Brand Guardian, Growth Hacker, Support Responder, UX Researcher, Project Shepherd et XR Interface Architect) ont été déployés simultanément pour évaluer une opportunité logicielle et produire un plan produit unifié couvrant la validation marché, l'architecture technique, la stratégie de marque, le go-to-market, les systèmes de support, la recherche UX, l'exécution projet et le design d'UI spatiale.

**Résultat** : un blueprint produit complet et transverse produit en une seule session. [Plus d'exemples](examples/).

---

### Scénario 6 : jumeau numérique de campus intelligent

**Votre équipe** :

1. 🧠 **Technical Consultant** - Définir la stratégie de jumeau numérique : BIM pour les bâtiments, SIG pour le campus, IoT pour le temps réel
2. 🏗️ **BIM/GIS Specialist** - Convertir les modèles de bâtiments Revit en couches de scène SIG, concevoir les plans d'étage intérieurs
3. 🛸 **Drone/Reality Mapping** - Survoler le campus, générer orthomosaïque et maillage 3D pour le contexte
4. 🌐 **Web GIS Developer** - Construire le tableau de bord du campus avec MapLibre, la couche bâtiments et le localisateur de salles
5. 🏔️ **3D & Scene Developer** - Créer une scène 3D immersive avec terrain, bâtiments et survol
6. 🤖 **GeoAI/ML Engineer** - Extraire les emprises de bâtiments et la canopée des arbres de l'imagerie drone
7. ✅ **GIS QA Engineer** - Valider l'exactitude des données, vérifier la topologie et la cohérence des CRS

**Résultat** : un jumeau numérique de campus qui combine le détail BIM, la capture du réel par drone, la visualisation 3D et l'accessibilité web — livré par des spécialistes coordonnés dans un seul pipeline.

---

## 🤝 Contribuer

Les contributions sont les bienvenues ! Voici comment vous pouvez aider :

### Ajouter un nouvel agent

1. Forkez le dépôt
2. Créez un nouveau fichier d'agent dans la catégorie appropriée
3. Suivez la structure du modèle d'agent :
   - Frontmatter avec name, description, color
   - Section Identity & Memory
   - Core Mission
   - Critical Rules (spécifiques au domaine)
   - Technical Deliverables avec exemples
   - Workflow Process
   - Success Metrics
4. Soumettez une PR avec votre agent

### Améliorer les agents existants

- Ajoutez des exemples concrets
- Enrichissez les exemples de code
- Mettez à jour les indicateurs de réussite
- Améliorez les workflows

### Partagez vos retours d'expérience

Vous avez utilisé ces agents avec succès ? Partagez votre histoire dans les [Discussions](https://github.com/msitarzewski/agency-agents/discussions) !

---

## 📖 Philosophie de conception des agents

Chaque agent est conçu avec :

1. **🎭 Une personnalité forte** : pas des modèles génériques — un vrai caractère et une vraie voix
2. **📋 Des livrables clairs** : des résultats concrets, pas des conseils vagues
3. **✅ Des indicateurs de réussite** : des résultats mesurables et des standards de qualité
4. **🔄 Des workflows éprouvés** : des processus étape par étape qui fonctionnent
5. **💡 Une mémoire apprenante** : reconnaissance de patterns et amélioration continue

---

## 🎁 Qu'est-ce qui rend ça spécial ?

### Contrairement aux prompts IA génériques :
- ❌ Des prompts génériques du type « Agis comme un développeur »
- ✅ Une spécialisation pointue avec personnalité et processus

### Contrairement aux bibliothèques de prompts :
- ❌ Des collections de prompts ponctuels
- ✅ Des systèmes d'agents complets avec workflows et livrables

### Contrairement aux outils IA :
- ❌ Des outils boîte noire impossibles à personnaliser
- ✅ Des personnalités d'agents transparentes, forkables et adaptables

---

## 🎨 Aperçus de la personnalité des agents

> « Je ne me contente pas de tester ton code — par défaut, je trouve 3 à 5 problèmes et j'exige une preuve visuelle pour tout. »
>
> -- **Evidence Collector** (Division Testing)

> « Tu ne fais pas du marketing sur Reddit — tu deviens un membre apprécié de la communauté qui se trouve représenter une marque. »
>
> -- **Reddit Community Builder** (Division Marketing)

> « Chaque élément ludique doit servir un but fonctionnel ou émotionnel. Conçois un plaisir qui enrichit au lieu de distraire. »
>
> -- **Whimsy Injector** (Division Design)

> « Laisse-moi ajouter une animation de célébration qui réduit de 40 % l'anxiété de fin de tâche »
>
> -- **Whimsy Injector** (pendant une revue UX)

---

## 📊 Chiffres clés

- 🎭 **232 agents spécialisés** répartis sur 16 divisions
- 📝 **Plus de 10 000 lignes** de personnalité, de processus et d'exemples de code
- ⏱️ **Des mois d'itérations** issus d'un usage réel
- 🌟 **Éprouvés** en environnement de production
- 💬 **Plus de 50 demandes** dans les 12 premières heures sur Reddit

---

## 🔌 Intégrations multi-outils

The Agency fonctionne nativement avec Claude Code et fournit des scripts de conversion + installation pour utiliser les mêmes agents sur tous les grands outils de codage agentique.

### Outils pris en charge

- **[Claude Code](https://claude.ai/code)** — agents `.md` natifs, aucune conversion nécessaire → `~/.claude/agents/`
- **[GitHub Copilot](https://github.com/copilot)** — agents `.md` natifs, aucune conversion nécessaire → `~/.github/agents/` + `~/.copilot/agents/`
- **[Antigravity](https://github.com/google-gemini/antigravity)** — un `SKILL.md` par agent → `~/.gemini/antigravity/skills/`
- **[Gemini CLI](https://github.com/google-gemini/gemini-cli)** — extension + fichiers `SKILL.md` → `~/.gemini/extensions/agency-agents/`
- **[OpenCode](https://opencode.ai)** — fichiers d'agent `.md` → `.opencode/agents/`
- **[Cursor](https://cursor.sh)** — fichiers de règles `.mdc` → `.cursor/rules/`
- **[Aider](https://aider.chat)** — un seul `CONVENTIONS.md` → `./CONVENTIONS.md`
- **[Windsurf](https://codeium.com/windsurf)** — un seul `.windsurfrules` → `./.windsurfrules`
- **[OpenClaw](https://github.com/openclaw/openclaw)** — `SOUL.md` + `AGENTS.md` + `IDENTITY.md` par agent
- **[Qwen Code](https://github.com/QwenLM/qwen-code)** — fichiers SubAgent `.md` → `~/.qwen/agents/`
- **[Kimi Code](https://github.com/MoonshotAI/kimi-cli)** — specs d'agent YAML → `~/.config/kimi/agents/`
- **[Codex](https://developers.openai.com/codex/overview)** — agents personnalisés TOML → `~/.codex/agents/`

---

### ⚡ Installation rapide

**Étape 1 -- Générer les fichiers d'intégration :**
```bash
./scripts/convert.sh
# Faster (parallel, output order may vary): ./scripts/convert.sh --parallel
```

**Étape 2 -- Installer (interactif, détecte automatiquement vos outils) :**
```bash
./scripts/install.sh
# Faster (parallel, output order may vary): ./scripts/install.sh --no-interactive --parallel
```

L'installateur analyse votre système à la recherche des outils installés, affiche une interface à cases à cocher et vous laisse choisir exactement quoi installer :

```
  +------------------------------------------------+
  |   The Agency -- Installateur d'outils          |
  +------------------------------------------------+

  Analyse du système : [*] = détecté sur cette machine

  [x]  1)  [*]  Claude Code     (claude.ai/code)
  [x]  2)  [*]  Copilot         (~/.github + ~/.copilot)
  [x]  3)  [*]  Antigravity     (~/.gemini/antigravity)
  [ ]  4)  [ ]  Gemini CLI      (~/.gemini/agents)
  [ ]  5)  [ ]  OpenCode        (opencode.ai)
  [ ]  6)  [ ]  OpenClaw        (~/.openclaw/agency-agents)
  [x]  7)  [*]  Cursor          (.cursor/rules)
  [ ]  8)  [ ]  Aider           (CONVENTIONS.md)
  [ ]  9)  [ ]  Windsurf        (.windsurfrules)
  [ ] 10)  [ ]  Qwen Code       (~/.qwen/agents)
  [ ] 11)  [ ]  Kimi Code       (~/.config/kimi/agents)
  [ ] 12)  [ ]  Codex           (~/.codex/agents)

  [1-12] basculer   [a] tout   [n] aucun   [d] détectés
  [Entrée] installer   [q] quitter
```

**Ou installer un outil précis directement :**
```bash
./scripts/install.sh --tool cursor
./scripts/install.sh --tool opencode
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool codex
```

**Non interactif (CI/scripts) :**
```bash
./scripts/install.sh --no-interactive --tool all
```

**Exécutions plus rapides (parallèle)** — Sur les machines multicœurs, utilisez `--parallel` pour que chaque outil soit traité en parallèle. L'ordre de sortie entre les outils est non déterministe. Fonctionne aussi bien en installation interactive que non interactive : par ex. `./scripts/install.sh --interactive --parallel` (choisir les outils, puis installer en parallèle) ou `./scripts/install.sh --no-interactive --parallel`. Le nombre de jobs par défaut est `nproc` (Linux), `sysctl -n hw.ncpu` (macOS) ou 4 ; à surcharger avec `--jobs N`.

```bash
./scripts/convert.sh --parallel                    # convert all tools in parallel
./scripts/convert.sh --parallel --jobs 8           # cap parallel jobs
./scripts/install.sh --no-interactive --parallel   # install all detected tools in parallel
./scripts/install.sh --interactive --parallel      # pick tools, then install in parallel
./scripts/install.sh --no-interactive --parallel --jobs 4
```

---

### Instructions par outil

<details>
<summary><strong>Claude Code</strong></summary>

Les agents sont copiés directement depuis le dépôt vers `~/.claude/agents/` -- aucune conversion nécessaire.

```bash
./scripts/install.sh --tool claude-code
```

Puis activez dans Claude Code :
```
Use the Frontend Developer agent to review this component.
```

Voir [integrations/claude-code/README.md](integrations/claude-code/README.md) pour les détails.
</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

Les agents sont copiés directement depuis le dépôt vers `~/.github/agents/` et `~/.copilot/agents/` -- aucune conversion nécessaire.

```bash
./scripts/install.sh --tool copilot
```

Puis activez dans GitHub Copilot :
```
Use the Frontend Developer agent to review this component.
```

Voir [integrations/github-copilot/README.md](integrations/github-copilot/README.md) pour les détails.
</details>

<details>
<summary><strong>Antigravity (Gemini)</strong></summary>

Chaque agent devient une skill dans `~/.gemini/antigravity/skills/agency-<slug>/`.

```bash
./scripts/install.sh --tool antigravity
```

Activez dans Gemini avec Antigravity :
```
@agency-frontend-developer review this React component
```

Voir [integrations/antigravity/README.md](integrations/antigravity/README.md) pour les détails.
</details>

<details>
<summary><strong>Gemini CLI</strong></summary>

S'installe sous forme de subagents Gemini CLI.
Sur un clone neuf, générez les fichiers d'agent Gemini avant de lancer l'installateur.

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

Voir [integrations/gemini-cli/README.md](integrations/gemini-cli/README.md) pour les détails.
</details>

<details>
<summary><strong>OpenCode</strong></summary>

Les agents sont placés dans `.opencode/agents/` à la racine de votre projet (portée projet).

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

Ou installez globalement :
```bash
mkdir -p ~/.config/opencode/agents
cp integrations/opencode/agents/*.md ~/.config/opencode/agents/
```

Activez dans OpenCode :
```
@backend-architect design this API.
```

Voir [integrations/opencode/README.md](integrations/opencode/README.md) pour les détails.
</details>

<details>
<summary><strong>Cursor</strong></summary>

Chaque agent devient un fichier de règles `.mdc` dans le `.cursor/rules/` de votre projet.

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

Les règles sont appliquées automatiquement lorsque Cursor les détecte dans le projet. Référencez-les explicitement :
```
Use the @security-engineer rules to review this code.
```

Voir [integrations/cursor/README.md](integrations/cursor/README.md) pour les détails.
</details>

<details>
<summary><strong>Aider</strong></summary>

Tous les agents sont compilés dans un unique fichier `CONVENTIONS.md` qu'Aider lit automatiquement.

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

Puis référencez les agents dans votre session Aider :
```
Use the Frontend Developer agent to refactor this component.
```

Voir [integrations/aider/README.md](integrations/aider/README.md) pour les détails.
</details>

<details>
<summary><strong>Windsurf</strong></summary>

Tous les agents sont compilés dans `.windsurfrules` à la racine de votre projet.

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

Référencez les agents dans le Cascade de Windsurf :
```
Use the Reality Checker agent to verify this is production ready.
```

Voir [integrations/windsurf/README.md](integrations/windsurf/README.md) pour les détails.
</details>

<details>
<summary><strong>OpenClaw</strong></summary>

Chaque agent devient un espace de travail avec `SOUL.md`, `AGENTS.md` et `IDENTITY.md` dans `~/.openclaw/agency-agents/`.

```bash
./scripts/convert.sh --tool openclaw
./scripts/install.sh --tool openclaw
```

Si la CLI `openclaw` est disponible, l'installateur enregistre automatiquement chaque espace de travail.
Lancez `openclaw gateway restart` après l'installation pour activer les nouveaux agents.

Voir [integrations/openclaw/README.md](integrations/openclaw/README.md) pour les détails.

</details>

<details>
<summary><strong>Qwen Code</strong></summary>

Les SubAgents sont installés dans `.qwen/agents/` à la racine de votre projet (portée projet).

```bash
# Convert and install (run from your project root)
cd /your/project
./scripts/convert.sh --tool qwen
./scripts/install.sh --tool qwen
```

**Utilisation dans Qwen Code :**
- Référence par nom : `Use the frontend-developer agent to review this component`
- Ou laissez Qwen déléguer automatiquement selon le contexte de la tâche
- Gérez via la commande `/agents` en mode interactif

> 📚 [Documentation des SubAgents Qwen](https://qwenlm.github.io/qwen-code-docs/en/users/features/sub-agents/)

</details>

<details>
<summary><strong>Kimi Code</strong></summary>

Les agents sont convertis au format CLI Kimi Code (YAML + prompt système) et installés dans `~/.config/kimi/agents/`.

```bash
# Convert and install
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

**Utilisation avec Kimi Code :**
```bash
# Use an agent
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml

# In a project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project \
     "Review this React component"
```

Voir [integrations/kimi/README.md](integrations/kimi/README.md) pour les détails.

</details>

<details>
<summary><strong>Codex</strong></summary>

Chaque agent est converti en fichier d'agent personnalisé Codex au format TOML et installé dans `~/.codex/agents/`.

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

Puis référencez l'agent personnalisé par son nom dans Codex :
```
Use the Frontend Developer agent to review this component.
```

Voir [integrations/codex/README.md](integrations/codex/README.md) pour les détails.
</details>

---

### Régénérer après des modifications

Lorsque vous ajoutez de nouveaux agents ou en modifiez d'existants, régénérez tous les fichiers d'intégration :

```bash
./scripts/convert.sh                    # regenerate all (serial)
./scripts/convert.sh --parallel         # regenerate all in parallel (faster)
./scripts/convert.sh --tool codex       # regenerate just one tool
./scripts/convert.sh --tool cursor      # regenerate just one tool
```

---

## 🗺️ Feuille de route

- [ ] Outil web interactif de sélection d'agents
- [x] Exemples de workflows multi-agents -- voir [examples/](examples/)
- [x] Scripts d'intégration multi-outils (Claude Code, GitHub Copilot, Antigravity, Gemini CLI, OpenCode, OpenClaw, Cursor, Aider, Windsurf, Qwen Code, Kimi Code, Codex)
- [ ] Tutoriels vidéo sur la conception d'agents
- [ ] Marketplace communautaire d'agents
- [ ] « Quiz de personnalité » d'agent pour le matching de projets
- [ ] Série de mises en avant « Agent de la semaine »

---

## 🌐 Traductions et localisations communautaires

Traductions et adaptations régionales maintenues par la communauté. Elles sont maintenues de façon indépendante -- consultez chaque dépôt pour la couverture et la compatibilité de version.

| Langue | Mainteneur | Lien | Notes |
|----------|-----------|------|-------|
| 🇨🇳 简体中文 (zh-CN) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-zh](https://github.com/jnMetaCode/agency-agents-zh) | 141 agents traduits + 46 originaux pour le marché chinois |
| 🇨🇳 简体中文 (zh-CN) | [@dsclca12](https://github.com/dsclca12) | [agent-teams](https://github.com/dsclca12/agent-teams) | Traduction indépendante avec localisation Bilibili, WeChat, Xiaohongshu |
| 🇧🇷 Português brasileiro (pt-BR) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-pt-BR](https://github.com/jnMetaCode/agency-agents-pt-BR) | 184 agents upstream traduits ; PR pour le marché brésilien bienvenues |
| 🇷🇺 Русский (ru) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ru](https://github.com/jnMetaCode/agency-agents-ru) | 184 agents upstream traduits ; PR pour le marché russe bienvenues |
| 🇮🇩 Bahasa Indonesia (id) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-id](https://github.com/jnMetaCode/agency-agents-id) | 184 agents upstream traduits ; PR pour le marché indonésien bienvenues |
| 🇸🇦 العربية (ar) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ar](https://github.com/jnMetaCode/agency-agents-ar) | 184 agents upstream traduits ; PR pour le marché arabe bienvenues |
| 🇰🇷 한국어 (ko) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ko](https://github.com/jnMetaCode/agency-agents-ko) | 184 agents upstream entièrement traduits ; PR spécifiques à la Corée bienvenues |
| 🇯🇵 日本語 (ja-JP) | [@sscodeai](https://github.com/sscodeai) | [agency-agents-ja](https://github.com/sscodeai/agency-agents-ja) | 281 agents localisés pour le Japon + 97 originaux pour le marché japonais + 27 workflows |

Vous voulez ajouter une traduction ? Ouvrez une issue et nous la référencerons ici.

---

## 🔗 Ressources liées

- [awesome-openclaw-agents](https://github.com/mergisi/awesome-openclaw-agents) — Collection d'agents OpenClaw maintenue par la communauté (dérivée de ce dépôt)

---

## 📜 Licence

Licence MIT - Utilisation libre, commerciale ou personnelle. Attribution appréciée mais non obligatoire.

---

## 🙏 Remerciements

Ce qui a commencé comme un fil Reddit sur la spécialisation des agents IA est devenu quelque chose de remarquable — **232 agents répartis sur 16 divisions**, soutenus par une communauté de contributeurs du monde entier. Chaque agent de ce dépôt existe parce que quelqu'un a pris la peine de l'écrire, de le tester et de le partager.

À tous ceux qui ont ouvert une PR, déposé une issue, lancé une Discussion ou simplement essayé un agent et nous ont dit ce qui marchait — merci. C'est grâce à vous que The Agency ne cesse de s'améliorer.

---

## 💬 Communauté

- **GitHub Discussions** : [Partagez vos retours d'expérience](https://github.com/msitarzewski/agency-agents/discussions)
- **Issues** : [Signalez des bugs ou demandez des fonctionnalités](https://github.com/msitarzewski/agency-agents/issues)
- **Reddit** : Rejoignez la conversation sur r/ClaudeAI
- **Twitter/X** : Partagez avec #TheAgency

---

## 🚀 Pour commencer

1. **Parcourez** les agents ci-dessus et trouvez les spécialistes adaptés à vos besoins
2. **Copiez** les agents dans `~/.claude/agents/` pour l'intégration Claude Code
3. **Activez** les agents en les référençant dans vos conversations Claude
4. **Personnalisez** la personnalité et les workflows des agents selon vos besoins
5. **Partagez** vos résultats et contribuez en retour à la communauté

---

<div align="center">

**🎭 The Agency : votre équipe de rêve IA vous attend 🎭**

[⭐ Star ce dépôt](https://github.com/msitarzewski/agency-agents) • [🍴 Forkez-le](https://github.com/msitarzewski/agency-agents/fork) • [🐛 Signalez une issue](https://github.com/msitarzewski/agency-agents/issues) • [❤️ Sponsoriser](https://github.com/sponsors/msitarzewski)

Fait avec ❤️ par la communauté, pour la communauté

</div>
