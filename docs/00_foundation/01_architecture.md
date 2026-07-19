# Project Dust - Architecture

**Version:** Sprint 00  
**Status:** Draft  
**Last Updated:** YYYY-MM-DD

---

# 1. Vision

Project Dust est un moteur de campagne Fallout 2d20 assisté par Intelligence Artificielle.

Son objectif est de permettre à un joueur de vivre une campagne solo où l'IA remplit le rôle de Game Master tout en respectant les règles du système Fallout 2d20.

Project Dust n'est pas conçu comme un jeu codé en dur, mais comme un moteur modulaire capable de faire évoluer les règles, les campagnes et les interfaces sans remettre en cause son architecture.

---

# 2. Objectifs

Les objectifs principaux du projet sont :

- architecture modulaire
- faible couplage entre les systèmes
- forte cohésion des modules
- extensibilité
- maintenabilité
- testabilité
- indépendance de l'interface utilisateur
- indépendance du fournisseur d'IA
- facilité d'ajout de nouvelles fonctionnalités

---

# 3. Principes d'architecture

Le développement repose sur plusieurs principes fondamentaux.

## Modularité

Chaque système possède une responsabilité unique.

Exemples :

- Character
- Combat
- Inventory
- Quest
- Exploration
- Dialogue
- Settlement

Chaque module doit pouvoir évoluer indépendamment des autres.

---

## Séparation des responsabilités

Chaque couche possède un rôle précis.

Aucune couche ne doit contenir la logique d'une autre.

---

## Faible couplage

Les modules métier ne communiquent jamais directement entre eux.

Toute communication passe par le moteur principal.

---

## Forte cohésion

Chaque module regroupe uniquement les éléments liés à son domaine.

---

## Testabilité

Chaque système doit pouvoir être testé indépendamment.

---

# 4. Architecture générale

Project Dust est organisé en plusieurs couches.

```
UI
│
Application
│
Game Engine
│
Domain
│
Infrastructure
```

Chaque couche ne dépend que de la couche située sous elle.

---

# 5. Le cœur du moteur

Le cœur du projet est le Game Engine.

Il est responsable de :

- coordonner les systèmes
- gérer le cycle de jeu
- transmettre les événements
- appliquer les règles globales
- orchestrer les interactions entre les modules

Le Game Engine ne contient pas les règles métier.

---

# 6. Modules

Le moteur est composé de plusieurs modules indépendants.

Modules actuellement prévus :

- Core
- Character
- Inventory
- Combat
- Exploration
- Dialogue
- Quest
- Settlement
- AI
- Database
- Save
- UI

Cette liste pourra évoluer au cours du projet.

---

# 7. Dépendances

Les modules métier ne doivent jamais dépendre directement les uns des autres.

Exemple :

❌ Combat → Inventory

✔ Combat → Game Engine → Inventory

Le Game Engine agit comme orchestrateur.

---

# 8. Intelligence Artificielle

L'IA est considérée comme un service.

Le moteur ne dépend d'aucun fournisseur spécifique.

Il doit être possible de remplacer :

- OpenAI
- Ollama
- LM Studio
- tout autre fournisseur compatible

sans modifier la logique métier.

---

# 9. Interface utilisateur

L'interface utilisateur est indépendante du moteur.

Le projet doit pouvoir fonctionner avec :

- interface console
- interface graphique
- interface Web

sans modifier les systèmes métier.

---

# 10. Évolutivité

L'ajout d'un nouveau système doit avoir un impact minimal sur les systèmes existants.

L'architecture doit favoriser :

- l'ajout de fonctionnalités
- la maintenance
- les tests
- la réutilisation du code

---

# 11. Structure du dépôt

La structure générale du dépôt est décrite dans la documentation du projet.

Elle pourra évoluer tant que les principes d'architecture sont respectés.

---

# 12. Conclusion

Toutes les décisions prises durant le développement devront respecter les principes définis dans ce document.

Ce document constitue la référence architecturale de Project Dust.