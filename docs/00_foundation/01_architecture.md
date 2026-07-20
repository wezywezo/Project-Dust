# Architecture — Project Dust
 
**Status:** Vivant  

---

# 1. Vision

L'architecture de Project Dust est conçue pour privilégier la modularité, l'évolutivité et la maintenabilité.

Project Dust n'est pas pensé comme un jeu codé en dur, mais comme un moteur capable de faire évoluer indépendamment les règles, les campagnes, les interfaces et les services qui le composent.

Chaque décision d'architecture vise à faciliter l'évolution du projet sans remettre en cause ses fondations.

---

# 2. Objectifs

Les principaux objectifs de l'architecture sont :

## Qualités de conception

- **Modularité** : chaque système possède une responsabilité claire et peut évoluer indépendamment.
- **Faible couplage** : limiter les dépendances entre les modules pour faciliter leur évolution.
- **Forte cohésion** : regrouper dans un même module uniquement les responsabilités liées à son domaine.
- **Extensibilité** : permettre l'ajout de nouvelles fonctionnalités sans modifier l'existant.
- **Maintenabilité** : favoriser un code simple à comprendre, corriger et faire évoluer.
- **Testabilité** : permettre de tester chaque système de manière isolée.

### Indépendance

- indépendance de l'interface utilisateur
- indépendance du fournisseur d'IA

### Conséquence recherchée

- faciliter l'ajout de nouvelles fonctionnalités sans remettre en cause l'architecture existante

---

# 3. Principes d'architecture

Les principes suivants guident toutes les décisions d'architecture de Project Dust.

Ils constituent les critères de référence lors de la conception de nouveaux systèmes ou de l'évolution de l'existant.

## Modularité

Chaque module possède une responsabilité clairement définie et peut évoluer indépendamment des autres, tant que ses interfaces restent respectées.

Chaque module doit pouvoir évoluer indépendamment des autres.

---

## Séparation des responsabilités

CChaque couche possède une responsabilité clairement définie.

Aucune couche ne doit contenir la logique d'une autre.

---

## Faible couplage

Les dépendances entre les modules doivent être limitées afin que chacun puisse évoluer avec un impact minimal sur les autres systèmes.

---

## Forte cohésion

Chaque module regroupe uniquement les responsabilités liées à son domaine.

---

## Testabilité

Chaque système doit pouvoir être testé de manière isolée afin de valider son comportement indépendamment des autres modules.

---

# 4. Architecture générale

Project Dust est organisé autour d'un Game Engine qui orchestre plusieurs modules spécialisés.

```
    UI
    │
Game Engine
├── Character
├── Combat
├── Inventory
├── Quest
├── Exploration
├── Dialogue
├── Settlement
├── Save
└── AI
```

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