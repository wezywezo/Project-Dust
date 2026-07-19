# Documentation — Project Dust

Bienvenue dans la documentation de **Project Dust**.

Cette documentation constitue la mémoire durable du projet. Elle décrit non seulement ce qui est développé, mais également les principes, les décisions et les choix de conception qui guident son évolution.

Avant de consulter un document particulier, il est recommandé de comprendre l'organisation générale de la documentation.

---

# Vision d'ensemble

```text
                 PROJECT DUST
                      │
                      ▼
               Connaissance
                      │
      ┌───────────────┼───────────────┐
      │               │               │
      ▼               ▼               ▼
 Fondations        Design           ADR
                      │
                      ▼
                 Exécution
                      │
             ┌────────┴────────┐
             ▼                 ▼
         Roadmap           Sprints
                                 │
                                 ▼
                               Code
```

La documentation distingue deux dimensions complémentaires.

## Connaissance

La connaissance représente tout ce qui permet de comprendre le projet indépendamment de son implémentation.

Elle regroupe :

- les **Fondations**, qui définissent les principes et les règles du projet ;
- les documents de **Design**, qui décrivent la conception des différentes parties du logiciel ;
- les **ADR** (*Architecture Decision Records*), qui expliquent les décisions importantes et leur justification.

## Exécution

L'exécution représente la réalisation concrète du projet.

Elle comprend :

- la **Roadmap**, qui définit la direction du projet ;
- les **Sprints**, qui organisent le travail de développement ;
- le **Code**, qui constitue le résultat de cette exécution.

> **La connaissance guide l'exécution. L'exécution produit le logiciel.**

---

# Organisation de la documentation

## `00_foundation`

Les documents de fondation définissent les principes permanents du projet.

Ils constituent la référence utilisée lors de chaque décision importante.

Ce dossier contient notamment :

- la Charte du projet ;
- l'Architecture générale ;
- les règles de développement ;
- le workflow ;
- les conventions Git ;
- la collaboration avec l'IA ;
- le cycle de vie des sprints.

---

## `01_design`

Le dossier **Design** regroupe les documents décrivant la conception des différentes parties du logiciel.

Chaque document explique notamment :

- les responsabilités d'un système ;
- son architecture ;
- les composants impliqués ;
- leurs interactions ;
- les règles métier.

Ces documents évoluent avec le logiciel.

---

## `02_sprints`

Chaque sprint possède son propre document.

Il constitue la mémoire du sprint et documente notamment :

- les objectifs ;
- l'état d'avancement ;
- les décisions importantes ;
- les travaux réalisés ;
- les difficultés rencontrées ;
- les enseignements ;
- la Sprint Review ;
- la Sprint Retrospective.

---

## `03_adr`

Les **Architecture Decision Records (ADR)** documentent les décisions importantes prises durant le développement.

Chaque ADR répond notamment aux questions suivantes :

- Pourquoi cette décision était-elle nécessaire ?
- Quelles alternatives ont été étudiées ?
- Pourquoi cette solution a-t-elle été retenue ?
- Quelles sont ses conséquences ?

Les ADR constituent la mémoire des décisions d'architecture du projet.

---

## `04_roadmap`

La Roadmap décrit la vision du projet à moyen et long terme.

Elle présente les objectifs des prochains sprints ainsi que les grandes étapes du développement sans entrer dans les détails de leur implémentation.

---

# Convention générale

La documentation est rédigée principalement en français.

Le code source, les noms de classes, les méthodes, les variables et les éléments techniques utilisent l'anglais.

---

# Philosophie

La documentation fait partie intégrante du projet.

Chaque document doit permettre à un nouveau développeur de comprendre rapidement :

- le fonctionnement du projet ;
- les choix qui ont été réalisés ;
- les raisons qui ont conduit à ces choix.

Le dépôt Git et la documentation constituent ensemble la mémoire durable de Project Dust.

À tout moment, il doit être possible de reprendre le développement sans dépendre de l'historique d'une conversation particulière.