# Documentation Standards

## Objectif

Ce document définit les conventions de rédaction utilisées dans la documentation de Project Dust.

Son objectif est d'assurer une documentation cohérente, homogène et facile à maintenir.

---

## Statuts

Les statuts permettent d'indiquer l'état d'avancement d'un élément dans la documentation.

| Icône | Signification |
|-------|---------------|
| ⚪ | Planifié |
| 🟡 | En cours |
| ✅ | Terminé |
| 🔴 | Bloqué |

Ces statuts sont utilisés dans les roadmaps, les sprints et tout autre document de suivi.

---

## Liens

Les liens entre les documents doivent être relatifs afin de garantir leur portabilité.

Exemple :

```markdown
[Roadmap](../03_roadmap/roadmap.md)
```

---

## Langue

Toute la documentation du projet est rédigée en français.

Les noms techniques (classes, méthodes, variables, concepts de programmation) peuvent rester en anglais lorsqu'ils correspondent au langage utilisé dans le code.

---

## Source de vérité

Chaque information importante du projet doit posséder une **source de vérité unique**.

Les autres documents doivent faire référence à cette source plutôt que de dupliquer son contenu.

Exemples :

- Le `README.md` présente le projet et renvoie vers la documentation.
- `docs/README.md` présente la documentation et renvoie vers les documents spécialisés.
- La Roadmap décrit l'avancement global du projet.
- Les Sprints décrivent le travail en cours.

Cette approche limite les incohérences, simplifie la maintenance et garantit que chaque information n'est mise à jour qu'à un seul endroit.

---

## Niveau de détail

La documentation doit être suffisamment détaillée pour expliquer le raisonnement, sans devenir verbeuse.

Privilégier des explications courtes et précises.

Si un sujet nécessite plusieurs paragraphes pour être expliqué, il mérite probablement son propre document ou une section dédiée.

Chaque document doit rester facile à parcourir tout en permettant de comprendre le "pourquoi" des décisions importantes.

---

## Évolution

Ce document est évolutif.

Toute nouvelle convention de documentation validée durant le projet doit être ajoutée ici.

