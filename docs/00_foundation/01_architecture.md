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

## Indépendance

Le moteur doit rester indépendant :

- de l'interface utilisateur ;
- du fournisseur d'intelligence artificielle.

## Conséquence recherchée

Chaque décision d'architecture doit permettre au projet d'évoluer avec un impact minimal sur les systèmes existants.

---

# 3. Principes d'architecture

Les principes suivants guident toutes les décisions d'architecture de Project Dust.

Ils constituent les critères de référence lors de la conception de nouveaux systèmes ou de l'évolution de l'existant.

## Modularité

Chaque module possède une responsabilité clairement définie et peut évoluer indépendamment des autres.

---

## Séparation des responsabilités

Chaque couche possède une responsabilité clairement définie.

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

# 4. Le cœur du moteur

Le cœur de Project Dust est le **Game Engine**.

Il agit comme orchestrateur du système.

Il est responsable de :

- coordonner les systèmes ;
- gérer le cycle de jeu ;
- acheminer les demandes vers le module approprié ;
- poursuivre le déroulement de la partie selon les résultats obtenus.

Le Game Engine ne contient jamais les règles métier.

---

# 5. Répartition des responsabilités

Le Game Engine sait **quand** les choses doivent se produire.

Les modules savent **comment** elles se produisent.

Le Game Engine exprime les intentions du système.

Chaque module applique les règles de son propre domaine et retourne le résultat de son traitement.

Cette séparation constitue l'une des règles fondamentales de l'architecture de Project Dust.

---

# 6. Dépendances

Les modules métier ne communiquent jamais directement entre eux.

Toute interaction entre deux modules transite par le Game Engine, qui agit comme orchestrateur du système.

Cette règle garantit un faible couplage entre les différents domaines métier.

---

# 7. Intelligence Artificielle

L'intelligence artificielle est considérée comme un service externe.

Le moteur ne dépend d'aucun fournisseur particulier.

Il doit être possible de remplacer un fournisseur d'IA sans modifier la logique métier.

---

# 8. Interface utilisateur

L'interface utilisateur est indépendante du moteur.

Le moteur doit pouvoir fonctionner avec différentes interfaces sans modifier les systèmes métier.

---

# 9. Évolutivité

L'ajout d'un nouveau système doit avoir un impact minimal sur les systèmes existants.

L'architecture doit favoriser :

- l'ajout de fonctionnalités ;
- la maintenance ;
- les tests ;
- la réutilisation du code.

---

# 10. Structure du dépôt

La structure du dépôt est documentée séparément.

Elle pourra évoluer tant que les principes définis dans ce document sont respectés.

---

# 11. Conclusion

Toutes les décisions prises durant le développement devront respecter les principes définis dans ce document.

Ce document constitue la référence architecturale de Project Dust.