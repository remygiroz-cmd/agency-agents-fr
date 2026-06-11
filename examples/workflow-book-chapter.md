# Exemple de workflow : développement d'un chapitre de livre

> Un workflow mono-agent ciblé pour transformer une matière source brute en un brouillon de chapitre stratégique à la première personne, avec des boucles de révision explicites.

## Quand l'utiliser

Utilisez ce workflow lorsqu'un auteur dispose de notes vocales, de fragments ou de notes stratégiques, mais pas encore d'un brouillon de chapitre propre. L'objectif n'est pas du ghostwriting générique. L'objectif est de produire un chapitre qui renforce le positionnement de catégorie, préserve la voix de l'auteur et expose clairement les décisions éditoriales ouvertes.

## Agent utilisé

| Agent | Rôle |
|-------|------|
| Book Co-Author | Convertit la matière source en un brouillon de chapitre versionné avec notes éditoriales et questions pour l'étape suivante |

## Exemple d'activation

```text
Activate Book Co-Author.

Book goal: Build authority around practical AI adoption for Mittelstand companies.
Target audience: Owners and operational leaders of 20-200 person businesses.
Chapter topic: Why most AI projects fail before implementation starts.
Desired draft maturity: First substantial draft.

Raw material:
- Voice memo: "The real failure happens in expectation setting, not tooling."
- Notes: Leaders buy software before defining the operational bottleneck.
- Story fragment: We nearly rolled out the wrong automation in a cabinetmaking workflow because the actual problem was quoting delays, not production throughput.
- Positioning angle: Practical realism over hype.

Produce:
1. Chapter objective and strategic role in the book
2. Any clarification questions you need
3. Chapter 2 - Version 1 - ready for review
4. Editorial notes on assumptions and proof gaps
5. Specific next-step revision requests
```

## Forme attendue de la sortie

Le Book Co-Author devrait répondre en cinq parties :

1. `Target Outcome`
2. `Chapter Draft`
3. `Editorial Notes`
4. `Feedback Loop`
5. `Next Step`

## Exigence de qualité

- Le brouillon reste à la première personne
- Le chapitre a une promesse claire et une logique interne
- Les affirmations sont rattachées à la matière source ou signalées comme des hypothèses
- Le langage motivationnel générique est supprimé
- La sortie se termine par des questions de révision explicites, et non par une transmission vague
