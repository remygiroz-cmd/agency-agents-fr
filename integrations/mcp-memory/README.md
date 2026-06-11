# Intégration MCP Memory

> Donnez à n'importe quel agent une mémoire persistante d'une session à l'autre grâce au Model Context Protocol (MCP).

## Ce que ça fait

Par défaut, les agents de The Agency démarrent chaque session de zéro. Le contexte est transmis manuellement par copier-coller entre agents et sessions. Un serveur de mémoire MCP change la donne :

- **Mémoire inter-session** : un agent se souvient des décisions, des livrables et du contexte des sessions précédentes
- **Continuité des passations** : lorsqu'un agent passe la main à un autre, l'agent qui reçoit peut se remémorer exactement ce qui a été fait — aucun copier-coller requis
- **Rollback en cas d'échec** : lorsqu'un contrôle QA échoue ou qu'une décision d'architecture s'avère mauvaise, revenez à un état sain connu plutôt que de tout recommencer

## Mise en place

Vous avez besoin d'un serveur MCP qui fournit des outils de mémoire : `remember`, `recall`, `rollback` et `search`. Ajoutez-le à la config de votre client MCP (Claude Code, Cursor, etc.) :

```json
{
  "mcpServers": {
    "memory": {
      "command": "your-mcp-memory-server",
      "args": []
    }
  }
}
```

Tout serveur MCP qui expose les outils `remember`, `recall`, `rollback` et `search` fonctionnera. Consultez l'[écosystème MCP](https://modelcontextprotocol.io) pour les implémentations disponibles.

## Comment ajouter une mémoire à n'importe quel agent

Pour enrichir un agent existant d'une mémoire persistante, ajoutez une section **Memory Integration** au prompt de l'agent. Cette section indique à l'agent d'utiliser les outils de mémoire MCP aux moments clés.

### Le motif

```markdown
## Memory Integration

When you start a session:
- Recall relevant context from previous sessions using your role and the current project as search terms
- Review any memories tagged with your agent name to pick up where you left off

When you make key decisions or complete deliverables:
- Remember the decision or deliverable with descriptive tags (your agent name, the project, the topic)
- Include enough context that a future session — or a different agent — can understand what was done and why

When handing off to another agent:
- Remember your deliverables tagged for the receiving agent
- Include the handoff metadata: what you completed, what's pending, and what the next agent needs to know

When something fails and you need to recover:
- Search for the last known-good state
- Use rollback to restore to that point rather than rebuilding from scratch
```

### Ce que l'agent fait de cela

Le LLM utilisera automatiquement les outils de mémoire MCP quand on lui donne ces instructions :

- `remember` — stocke une décision, un livrable ou un instantané de contexte avec des tags
- `recall` — recherche les mémoires pertinentes par mot-clé, tag ou similarité sémantique
- `rollback` — revient à un état antérieur lorsque quelque chose tourne mal
- `search` — retrouve des mémoires spécifiques à travers les sessions et les agents

Aucune modification de code dans les fichiers d'agent. Aucun appel API à écrire. Les outils MCP gèrent tout.

## Exemple : enrichir le Backend Architect

Voir [architecte-backend.md](architecte-backend.md) pour un exemple complet — l'agent Backend Architect standard auquel a été ajoutée une section Memory Integration.

## Exemple : workflow propulsé par la mémoire

Voir [../../examples/workflow-with-memory.md](../../examples/workflow-with-memory.md) pour le workflow Startup MVP enrichi d'une mémoire persistante, montrant comment les agents se transmettent le contexte via la mémoire plutôt que par copier-coller.

## Conseils

- **Taguez de façon cohérente** : utilisez le nom de l'agent et le nom du projet comme tags sur chaque mémoire. Cela rend la remémoration fiable.
- **Laissez le LLM décider de ce qui est important** : les instructions de mémoire sont des indications, pas des règles rigides. Le LLM saura quand mémoriser et quoi se remémorer.
- **Le rollback est la fonctionnalité phare** : lorsqu'un Reality Checker recale un livrable, l'agent d'origine peut revenir à son dernier point de contrôle au lieu d'essayer d'annuler manuellement les changements.
