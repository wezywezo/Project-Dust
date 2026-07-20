# Cycle de vie d'un Sprint

## Objectif

Chaque sprint représente une étape cohérente du développement.

Un sprint constitue une unité de travail, indépendamment du nombre de conversations nécessaires pour le réaliser.

Afin de conserver un contexte clair et facilement consultable, les discussions sont organisées en une ou plusieurs conversations dédiées au sprint en cours.

Le document `SprintXX.md` constitue la mémoire du sprint et sert de point de reprise entre les conversations.

---

# Début d'un Sprint

Avant de commencer un nouveau sprint :

1. créer une nouvelle conversation dédiée au sprint;
2. fournir une archive ZIP du dépôt dans son état actuel;
3. préciser le numéro du sprint;
4. créer le document `SprintXX.md`;
5. définir les objectifs du sprint;
6. laisser l'IA analyser la documentation et la structure du projet;
7. valider ensemble le résumé du contexte avant de commencer les travaux.

Le dépôt Git constitue la source de vérité du projet.

---

# Analyse initiale

En début de sprint, l'IA doit prendre connaissance notamment de :

- la Charte du projet;
- l'Architecture;
- les ADR;
- la Roadmap;
- le dernier Sprint;
- les documents modifiés depuis le sprint précédent.

Cette étape garantit une compréhension commune avant toute nouvelle décision.

---

# Reprise d'un Sprint

Lorsqu'un sprint se poursuit dans une nouvelle conversation, la procédure suivante est appliquée :

1. créer une nouvelle conversation;
2. fournir une archive ZIP du dépôt dans son état actuel;
3. préciser le numéro du sprint et le numéro de la conversation (ex. : Sprint 03 — Conversation 2);
4. laisser l'IA relire le document `SprintXX.md`;
5. laisser l'IA analyser le dépôt ainsi que les documents mis à jour depuis le début du sprint;
6. valider ensemble le résumé avant de reprendre les travaux.

Cette procédure garantit qu'aucune information importante n'est perdue lors d'un changement de conversation.

---

# Déroulement d'un Sprint

Le développement suit le cycle suivant :

1. Compréhension du besoin.
2. Discussion.
3. Pause Café.
4. Conception.
5. Implémentation.
6. Revue technique.
7. Documentation.

Le code n'est jamais la première étape.

La compréhension précède toujours l'implémentation.

---

# Documentation continue

Le document `SprintXX.md` est maintenu tout au long du sprint.

Il constitue le journal de bord et la mémoire du sprint.

Les objectifs, l'état d'avancement, les décisions importantes, les travaux réalisés et les enseignements sont documentés progressivement afin d'éviter toute perte d'information.

À chaque début de séance de travail, il convient de vérifier si le document du sprint doit être mis à jour avant de poursuivre le développement.

---

# Fin d'un Sprint

Avant de clôturer un sprint :

- vérifier que la documentation est à jour;
- effectuer une Sprint Review;
- réaliser une Sprint Retrospective;
- documenter les leçons apprises;
- définir les objectifs du sprint suivant.

Une fois le sprint terminé :

- créer un commit propre;
- créer une archive ZIP du dépôt;
- utiliser cette archive comme point de départ du sprint suivant.

---

# Sprint Review

La Sprint Review permet de valider le travail réalisé.

Elle répond notamment aux questions suivantes :

- Les objectifs du sprint sont-ils atteints ?
- Les décisions prises sont-elles toujours pertinentes ?
- La documentation reflète-t-elle correctement l'état du projet ?
- Le projet est-il prêt pour le sprint suivant ?

---

# Sprint Retrospective

La Sprint Retrospective vise à améliorer notre manière de travailler.

Elle permet d'identifier :

- ce qui a bien fonctionné;
- ce qui pourrait être amélioré;
- les difficultés rencontrées;
- les enseignements tirés du sprint.

L'objectif est d'améliorer continuellement notre processus de développement.

---

# Critère de reprise

À tout moment, il doit être possible de reprendre le développement uniquement à partir :

- du dépôt Git;
- de la documentation;
- du document `SprintXX.md`.

Les conversations servent de support aux échanges.

Le dépôt Git et la documentation constituent la mémoire durable du projet.

---
