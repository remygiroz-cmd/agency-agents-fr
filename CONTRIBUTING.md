# 🤝 Contribuer à The Agency

Tout d'abord, merci d'envisager de contribuer à The Agency ! Ce sont des personnes comme vous qui rendent cette collection d'agents IA meilleure pour tout le monde.

## 📋 Table des matières

- [Code de conduite](#code-of-conduct)
- [Comment puis-je contribuer ?](#how-can-i-contribute)
- [Principes de conception des agents](#agent-design-guidelines)
- [Processus de pull request](#pull-request-process)
- [Guide de style](#style-guide)
- [Communauté](#community)

---

## 📜 Code de conduite

Ce projet et toutes les personnes qui y participent sont régis par notre code de conduite. En participant, vous vous engagez à respecter ce code :

- **Soyez respectueux** : traitez chacun avec respect. Un débat sain est encouragé, mais les attaques personnelles ne sont pas tolérées.
- **Soyez inclusif** : accueillez et soutenez les personnes de tous horizons et de toutes identités.
- **Soyez collaboratif** : ce que nous créons ensemble est meilleur que ce que nous créons seuls.
- **Soyez professionnel** : gardez les discussions centrées sur l'amélioration des agents et de la communauté.

---

## 🎯 Comment puis-je contribuer ?

### 1. Créer un nouvel agent

Vous avez une idée d'agent spécialisé ? Parfait ! Voici comment en ajouter un :

1. **Forkez le dépôt**
2. **Choisissez la catégorie appropriée** (ou proposez-en une nouvelle) :
   - `engineering/` - Spécialistes du développement logiciel
   - `design/` - Spécialistes UX/UI et créatifs
   - `finance/` - Spécialistes de la planification financière, de la comptabilité et de l'investissement
   - `game-development/` - Spécialistes de la conception et du développement de jeux
   - `marketing/` - Spécialistes de la croissance et du marketing
   - `paid-media/` - Spécialistes de l'acquisition payante et des médias
   - `product/` - Spécialistes de la gestion de produit
   - `project-management/` - Spécialistes de la gestion de projet et de la coordination
   - `testing/` - Spécialistes de l'assurance qualité et des tests
   - `security/` - Architecture de sécurité, AppSec, pentest, threat intel et réponse aux incidents
   - `support/` - Spécialistes des opérations et du support
   - `spatial-computing/` - Spécialistes AR/VR/XR
   - `specialized/` - Spécialistes uniques qui ne rentrent dans aucune autre catégorie

3. **Créez le fichier de votre agent** en suivant le modèle ci-dessous
4. **Testez votre agent** dans des scénarios réels
5. **Soumettez une pull request** avec votre agent

### 2. Améliorer les agents existants

Vous avez trouvé un moyen d'améliorer un agent ? Les contributions sont les bienvenues :

- Ajoutez des exemples concrets et des cas d'usage
- Enrichissez les exemples de code avec des patterns modernes
- Mettez à jour les workflows en fonction des nouvelles bonnes pratiques
- Ajoutez des métriques de réussite et des benchmarks
- Corrigez les fautes de frappe, améliorez la clarté, enrichissez la documentation

### 3. Partager vos retours d'expérience

Vous avez utilisé ces agents avec succès ? Partagez votre histoire :

- Publiez dans les [GitHub Discussions](https://github.com/msitarzewski/agency-agents/discussions)
- Ajoutez une étude de cas au README
- Rédigez un article de blog et partagez le lien
- Créez un tutoriel vidéo

### 4. Signaler des problèmes

Vous avez trouvé un problème ? Faites-le-nous savoir :

- Vérifiez si le problème existe déjà
- Fournissez des étapes de reproduction claires
- Donnez du contexte sur votre cas d'usage
- Suggérez des solutions potentielles si vous avez des idées

---

## 🎨 Principes de conception des agents

### Structure d'un fichier d'agent

Chaque agent doit suivre cette structure :

```markdown
---
name: Agent Name
description: One-line description of the agent's specialty and focus
color: colorname or "#hexcode"
emoji: 🎯
vibe: One-line personality hook — what makes this agent memorable
services:                              # optional — only if the agent requires external services
  - name: Service Name
    url: https://service-url.com
    tier: free                         # free, freemium, or paid
---

# Agent Name

## 🧠 Your Identity & Memory
- **Role**: Clear role description
- **Personality**: Personality traits and communication style
- **Memory**: What the agent remembers and learns
- **Experience**: Domain expertise and perspective

## 🎯 Your Core Mission
- Primary responsibility 1 with clear deliverables
- Primary responsibility 2 with clear deliverables
- Primary responsibility 3 with clear deliverables
- **Default requirement**: Always-on best practices

## 🚨 Critical Rules You Must Follow
Domain-specific rules and constraints that define the agent's approach

## 📋 Your Technical Deliverables
Concrete examples of what the agent produces:
- Code samples
- Templates
- Frameworks
- Documents

## 🔄 Your Workflow Process
Step-by-step process the agent follows:
1. Phase 1: Discovery and research
2. Phase 2: Planning and strategy
3. Phase 3: Execution and implementation
4. Phase 4: Review and optimization

## 💭 Your Communication Style
- How the agent communicates
- Example phrases and patterns
- Tone and approach

## 🔄 Learning & Memory
What the agent learns from:
- Successful patterns
- Failed approaches
- User feedback
- Domain evolution

## 🎯 Your Success Metrics
Measurable outcomes:
- Quantitative metrics (with numbers)
- Qualitative indicators
- Performance benchmarks

## 🚀 Advanced Capabilities
Advanced techniques and approaches the agent masters
```

### Structure d'un agent

Les fichiers d'agent sont organisés en deux groupes sémantiques qui correspondent au format d'espace de travail d'OpenClaw et aident les autres outils à analyser votre agent :

#### Persona (qui est l'agent)
- **Identity & Memory** — rôle, personnalité, parcours
- **Communication Style** — ton, voix, approche
- **Critical Rules** — limites et contraintes

#### Operations (ce que fait l'agent)
- **Core Mission** — responsabilités principales
- **Technical Deliverables** — livrables concrets et modèles
- **Workflow Process** — méthodologie étape par étape
- **Success Metrics** — résultats mesurables
- **Advanced Capabilities** — techniques spécialisées

Aucun formatage particulier n'est requis — gardez simplement les sections liées au persona (identité, communication, règles) groupées séparément des sections opérationnelles (mission, livrables, workflow, métriques). Le script `convert.sh` utilise ces en-têtes de section pour répartir automatiquement les agents dans des formats spécifiques à chaque outil.

### Principes de conception des agents

1. **🎭 Une personnalité forte**
   - Donnez à l'agent une voix et un caractère distincts
   - Pas de « Je suis un assistant serviable » — soyez spécifique et mémorable
   - Exemple : « Je trouve par défaut 3 à 5 problèmes et j'exige une preuve visuelle » (Evidence Collector)

2. **📋 Des livrables clairs**
   - Fournissez des exemples de code concrets
   - Incluez des modèles et des frameworks
   - Montrez de vrais résultats, pas des descriptions vagues

3. **✅ Des métriques de réussite**
   - Incluez des métriques précises et mesurables
   - Exemple : « Temps de chargement des pages sous les 3 secondes en 3G »
   - Exemple : « Plus de 10 000 points de karma cumulés sur l'ensemble des comptes »

4. **🔄 Des workflows éprouvés**
   - Des processus étape par étape
   - Des approches testées en conditions réelles
   - Pas de théorie — du concret éprouvé sur le terrain

5. **💡 Une mémoire d'apprentissage**
   - Les patterns que l'agent reconnaît
   - Comment il s'améliore au fil du temps
   - Ce dont il se souvient d'une session à l'autre

### Services externes

Les agents peuvent dépendre de services externes (API, plateformes, outils SaaS) lorsque ces services sont essentiels au fonctionnement de l'agent. Dans ce cas :

1. **Déclarez les dépendances** dans le frontmatter à l'aide du champ `services`
2. **L'agent doit tenir debout seul** — en retirant les appels d'API, il doit rester en dessous un persona, un workflow et une expertise utiles
3. **Ne dupliquez pas la documentation du fournisseur** — référencez-la, ne la reproduisez pas. Le fichier d'agent doit se lire comme un agent, pas comme un guide de démarrage
4. **Privilégiez les services dotés d'offres gratuites** afin que les contributeurs puissent tester l'agent

Le test : *cet agent est-il pour l'utilisateur ou pour le fournisseur ?* Un agent qui résout le problème de l'utilisateur à l'aide d'un service a sa place ici. Le guide de démarrage rapide d'un service déguisé en agent, non.

### Compatibilité avec des outils spécifiques

**Compatibilité Qwen Code** : le corps des agents prend en charge le templating `${variable}` pour le contexte dynamique (par exemple `${project_name}`, `${task_description}`). Les SubAgents Qwen utilisent un frontmatter minimal : seuls `name` et `description` sont requis ; les champs `color`, `emoji` et `version` sont omis car Qwen ne les utilise pas.

**Compatibilité Codex** : les agents personnalisés Codex sont générés sous forme de fichiers TOML autonomes. L'intégration Codex conserve une correspondance 1:1 minimale : `name` et `description` sont copiés depuis le frontmatter, et le corps Markdown devient `developer_instructions`. Les métadonnées propres à la source telles que `color`, `emoji`, `vibe` et les autres champs de frontmatter non pris en charge sont omises.

### Qu'est-ce qui fait un bon agent ?

**Les bons agents ont** :
- ✅ Une spécialisation étroite et approfondie
- ✅ Une personnalité et une voix distinctes
- ✅ Des exemples concrets de code/modèles
- ✅ Des métriques de réussite mesurables
- ✅ Des workflows étape par étape
- ✅ Des tests et itérations en conditions réelles

**À éviter** :
- ❌ La personnalité générique d'un « assistant serviable »
- ❌ Les descriptions vagues du type « Je vais vous aider à... »
- ❌ L'absence d'exemples de code ou de livrables
- ❌ Une portée trop large (touche-à-tout)
- ❌ Des approches théoriques non testées

---

## 🔄 Processus de pull request

### Ce qui a sa place dans une PR (et ce qui n'y a pas sa place)

Le chemin le plus rapide vers une PR fusionnée, c'est **un seul fichier markdown** — un agent nouveau ou amélioré. C'est le format idéal.

Pour tout le reste, voici comment garder les choses fluides :

#### Toujours bienvenu sous forme de PR
- Ajouter un nouvel agent (un seul fichier `.md`)
- Améliorer le contenu, les exemples ou la personnalité d'un agent existant
- Corriger des fautes de frappe ou clarifier la documentation

#### Ouvrez d'abord une Discussion
- Nouveaux outils, systèmes de build ou workflows CI
- Changements d'architecture (nouveaux répertoires, nouveaux scripts, générateurs de site)
- Changements qui touchent de nombreux fichiers à travers le dépôt
- Nouveaux formats d'intégration ou plateformes

Nous adorons les idées ambitieuses — une [Discussion](https://github.com/msitarzewski/agency-agents/discussions) donne simplement à la communauté l'occasion de s'aligner sur l'approche avant que le code ne soit écrit. Cela fait gagner du temps à tout le monde, et surtout à vous.

#### Ce que nous fermerons systématiquement
- **Sorties de build commitées** : les fichiers générés (`_site/`, assets compilés, fichiers d'agent convertis) ne doivent jamais être versionnés. Les utilisateurs exécutent `convert.sh` localement ; toutes les sorties sont gitignorées.
- **Les PR qui modifient en masse des agents existants** sans discussion préalable — même un reformatage bien intentionné peut créer des conflits de merge pour les autres contributeurs.
- **Les quasi-doublons « relookés »** : les nouveaux agents qui sont des copies par chercher-remplacer d'un agent existant (par exemple en remplaçant un nom de pays ou de plateforme) plutôt que de véritables nouveaux spécialistes. Exécutez `scripts/check-agent-originality.sh` avant de soumettre — la CI le lance automatiquement.

### Avant de soumettre

1. **Testez votre agent** : utilisez-le dans des scénarios réels, itérez selon les retours
2. **Suivez le modèle** : respectez la structure des agents existants
3. **Ajoutez des exemples** : incluez au moins 2 à 3 exemples de code/modèles
4. **Définissez des métriques** : incluez des critères de réussite précis et mesurables
5. **Relisez** : vérifiez les fautes de frappe, les problèmes de formatage, la clarté
6. **Vérifiez l'originalité** : exécutez `./scripts/check-agent-originality.sh path/to/your-agent.md`. Il compare votre agent à l'ensemble du catalogue et signale les quasi-doublons (un nom de pays/plateforme remplacé ne le trompera pas). Un nouvel agent doit être réellement nouveau — si vous localisez pour un marché, faites en sorte que les plateformes, les tactiques et les exemples soient réellement différents, pas un simple chercher-remplacer.

### Soumettre votre PR

1. **Forkez** le dépôt
2. **Créez une branche** : `git checkout -b add-agent-name`
3. **Effectuez vos modifications** : ajoutez le ou les fichiers de votre agent
4. **Commitez** : `git commit -m "Add [Agent Name] specialist"`
5. **Poussez** : `git push origin add-agent-name`
6. **Ouvrez une pull request** avec :
   - Un titre clair : « Add [Agent Name] - [Category] »
   - Une description de ce que fait l'agent
   - La raison pour laquelle cet agent est nécessaire (cas d'usage)
   - Les tests que vous avez effectués

### Processus de revue de la PR

1. **Revue par la communauté** : d'autres contributeurs peuvent donner leur avis
2. **Itération** : prenez en compte les retours et apportez des améliorations
3. **Approbation** : les mainteneurs approuveront lorsque ce sera prêt
4. **Merge** : votre contribution intègre The Agency !

### Modèle de PR

```markdown
## Agent Information
**Agent Name**: [Name]
**Category**: [engineering/design/marketing/etc.]
**Specialty**: [One-line description]

## Motivation
[Why is this agent needed? What gap does it fill?]

## Testing
[How have you tested this agent? Real-world use cases?]

## Checklist
- [ ] Original — not a near-duplicate (ran `scripts/check-agent-originality.sh`)
- [ ] Follows agent template structure
- [ ] Includes personality and voice
- [ ] Has concrete code/template examples
- [ ] Defines success metrics
- [ ] Includes step-by-step workflow
- [ ] Proofread and formatted correctly
- [ ] Tested in real scenarios
```

---

## 📐 Guide de style

### Style d'écriture

- **Soyez spécifique** : « Réduire le temps de chargement des pages de 60 % » et non « Rendre ça plus rapide »
- **Soyez concret** : « Créer des composants React en TypeScript » et non « Construire des interfaces »
- **Soyez mémorable** : donnez de la personnalité aux agents, pas du jargon corporate générique
- **Soyez pratique** : incluez du vrai code, pas du pseudo-code

### Formatage

- Utilisez le **formatage Markdown** de manière cohérente
- Incluez des **emojis** pour les en-têtes de section (la lecture en diagonale est plus facile)
- Utilisez des **blocs de code** pour tous les exemples de code, avec une coloration syntaxique adaptée
- Utilisez des **tableaux** pour comparer des options ou présenter des métriques
- Utilisez le **gras** pour la mise en valeur, et `code` pour les termes techniques

### Exemples de code

```markdown
## Example Code Block

\`\`\`typescript
// Always include:
// 1. Language specification for syntax highlighting
// 2. Comments explaining key concepts
// 3. Real, runnable code (not pseudo-code)
// 4. Modern best practices

interface AgentExample {
  name: string;
  specialty: string;
  deliverables: string[];
}
\`\`\`
```

### Ton

- **Professionnel mais accessible** : ni trop formel ni trop décontracté
- **Confiant mais pas arrogant** : « Voici la meilleure approche » et non « Vous pourriez peut-être essayer... »
- **Utile sans materner** : présumez la compétence, apportez de la profondeur
- **Porté par la personnalité** : chaque agent doit avoir une voix unique

---

## 🌟 Reconnaissance

Les contributeurs qui apportent des contributions significatives seront :

- Cités dans la section des remerciements du README
- Mis en avant dans les notes de version
- Présentés dans les vitrines « Agent of the Week » (le cas échéant)
- Crédités directement dans le fichier de l'agent

---

## 🤔 Des questions ?

- **Questions générales** : [GitHub Discussions](https://github.com/msitarzewski/agency-agents/discussions)
- **Rapports de bug** : [GitHub Issues](https://github.com/msitarzewski/agency-agents/issues)
- **Demandes de fonctionnalités** : [GitHub Issues](https://github.com/msitarzewski/agency-agents/issues)
- **Discussion communautaire** : [Rejoignez nos discussions](https://github.com/msitarzewski/agency-agents/discussions)

---

## 📚 Ressources

### Pour les nouveaux contributeurs

- [README.md](README.md) - Vue d'ensemble et catalogue d'agents
- [Développeur Frontend](engineering/developpeur-frontend.md) - Exemple d'agent bien structuré
- [Bâtisseur de Communauté Reddit](marketing/batisseur-de-communaute-reddit.md) - Excellent exemple de personnalité
- [Injecteur de Fantaisie](design/injecteur-de-fantaisie.md) - Exemple de spécialiste créatif

### Pour la conception d'agents

- Lisez les agents existants pour vous inspirer
- Étudiez les patterns qui fonctionnent bien
- Testez vos agents dans des scénarios réels
- Itérez en fonction des retours

---

## 🎉 Merci !

Vos contributions rendent The Agency meilleure pour tout le monde. Que vous soyez en train de :

- Ajouter un nouvel agent
- Améliorer la documentation
- Corriger des bugs
- Partager des retours d'expérience
- Aider d'autres contributeurs

**Vous faites la différence. Merci !**

---

<div align="center">

**Des questions ? Des idées ? Des retours ?**

[Ouvrir une Issue](https://github.com/msitarzewski/agency-agents/issues) • [Lancer une Discussion](https://github.com/msitarzewski/agency-agents/discussions) • [Soumettre une PR](https://github.com/msitarzewski/agency-agents/pulls)

Fait avec ❤️ par la communauté

</div>
