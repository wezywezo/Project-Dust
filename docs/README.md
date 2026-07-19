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

- les **Fondations**, qui définissent les principes permanents du projet ;
- les documents de **Design**, qui décrivent la conception des différentes parties du logiciel ;
- les **ADR** (*Architecture Decision Records*), qui expliquent les décisions importantes et leur justification.

## Exécution

L'exécution représente la réalisation concrète du projet.

Elle comprend :

- les **Ideas**, qui permettent d'explorer des idées, des recherches et des preuves de concept avant toute décision ;
- la **Roadmap**, qui définit la direction du projet ;
- les **Sprints**, qui organisent le travail de développement ;
- le **Code**, qui constitue le résultat de cette exécution.

> **La connaissance guide l'exécution. L'exécution produit le logiciel.**

---

# Organisation de la documentation

## `00_foundation`

Les documents de fondation définissent les principes permanents du projet.

Ils constituent la référence utilisée lors des décisions importantes.

| Document | Description |
|----------|-------------|
| `00_project_charter.md` | Vision, objectifs et périmètre de Project Dust. |
| `01_architecture.md` | Architecture générale du projet. |
| `02_development_guidelines.md` | Principes et bonnes pratiques de développement. |
| `03_project_workflow.md` | Workflow de développement du projet. |
| `04_git_commit_conventions.md` | Conventions de commits Git. |
| `05_ai_collaboration.md` | Règles de collaboration avec l'IA. |
| `06_sprint_lifecycle.md` | Cycle de vie des sprints. |
| `07_documentation_standards.md` | Conventions de rédaction et de présentation de la documentation. |

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

## `02_adr`

Les **Architecture Decision Records (ADR)** documentent les décisions importantes prises durant le développement.

Chaque ADR répond notamment aux questions suivantes :

- Pourquoi cette décision était-elle nécessaire ?
- Quelles alternatives ont été étudiées ?
- Pourquoi cette solution a-t-elle été retenue ?
- Quelles sont ses conséquences ?

Les ADR constituent la mémoire des décisions d'architecture du projet.

---

## `03_roadmap`

La Roadmap présente la vision du projet à moyen et long terme.

Elle décrit les différentes phases du projet, leur objectif, leur état d'avancement ainsi que les sprints associés.

Elle permet de suivre la progression globale du projet sans entrer dans le détail de l'implémentation.

---

## `04_sprints`

Chaque sprint possède son propre document.

Il constitue la mémoire du sprint et documente notamment :

- son objectif ;
- sa portée ;
- ses livrables ;
- les critères de fin du sprint ;
- la rétrospective.

Le détail de l'implémentation reste dans le code et les documents de conception lorsque nécessaire.

---

## `05_ideas`

Le dossier **Ideas** regroupe les idées, recherches, expérimentations et preuves de concept (POC) qui ne font pas encore partie de la roadmap.

Il permet d'explorer de nouvelles pistes avant qu'une décision soit prise.

Une idée validée pourra ensuite être intégrée à la roadmap puis planifiée dans un sprint.

---

# Convention générale

La documentation est rédigée principalement en français.

Le code source, les noms de classes, les méthodes, les variables et les éléments techniques utilisent l'anglais.

---

# Philosophie

La documentation fait partie intégrante du projet.

Chaque document possède une responsabilité clairement définie et complète les autres sans les remplacer.

L'objectif est de permettre à tout développeur de comprendre rapidement :

- le fonctionnement du projet ;
- les choix réalisés ;
- les raisons ayant conduit à ces choix.

Le dépôt Git et la documentation constituent ensemble la mémoire durable de Project Dust.

À tout moment, il doit être possible de reprendre le développement sans dépendre de l'historique d'une conversation particulière.