# Git Commit Convention

**Version:** Sprint 00  
**Status:** Approved

---

# Introduction

Project Dust utilise une convention de messages de commit inspirée des **Conventional Commits**.

Cette convention permet de :

- produire un historique Git clair et lisible ;
- faciliter les revues de code ;
- comprendre rapidement l'évolution du projet ;
- simplifier la maintenance du dépôt ;
- faciliter l'exploitation de l'historique Git.

Chaque commit doit représenter **une seule modification logique**.

---

# Format

Le format général est :

```text
<type>: <description>
```

Exemple :

```text
feat: add inventory module
```

La description est écrite :

- en anglais ;
- en minuscules (sauf noms propres) ;
- à l'impératif ;
- de manière concise.

---

# Types de commits

## feat

Ajout d'une nouvelle fonctionnalité.

Exemples :

```text
feat: add combat engine
feat: implement inventory module
feat: create quest manager
```

---

## fix

Correction d'un bug.

Exemples :

```text
fix: prevent duplicate loot
fix: resolve save loading issue
fix: correct damage calculation
```

---

## docs

Modification de la documentation uniquement.

Aucun code n'est modifié.

Exemples :

```text
docs: add architecture documentation
docs: update README
docs: document event system
```

---

## refactor

Réorganisation du code sans modifier son comportement.

Utiliser ce type lorsqu'on améliore la structure du code.

Exemples :

```text
refactor: simplify event dispatcher
refactor: split combat service into smaller classes
```

---

## test

Ajout ou modification des tests.

Exemples :

```text
test: add combat unit tests
test: improve inventory coverage
```

---

## chore

Maintenance du projet.

Exemples :

- mise à jour des dépendances ;
- configuration des outils ;
- nettoyage du dépôt ;
- scripts de développement.

Exemples :

```text
chore: update dependencies
chore: configure Ruff
chore: clean project structure
```

---

## style

Modification de la mise en forme uniquement.

Aucun changement fonctionnel.

Exemples :

```text
style: format source code
style: fix indentation
```

---

## perf

Amélioration des performances.

Exemples :

```text
perf: optimize save serialization
perf: improve combat calculations
```

---

## build

Modification du système de build ou de packaging.

Exemples :

```text
build: configure PyInstaller
build: update packaging
```

---

## ci

Modification de l'intégration continue.

Exemples :

```text
ci: add GitHub Actions workflow
ci: update release pipeline
```

---

# Bonnes pratiques

## Un commit = une modification logique

Éviter :

```text
feat: add inventory, fix combat and update README
```

Préférer plusieurs commits :

```text
feat: add inventory module

fix: correct combat damage

docs: update README
```

---

## Utiliser l'impératif

✔ Correct

```text
feat: add inventory module
docs: update architecture
fix: prevent null pointer
```

✘ À éviter

```text
added inventory
adding inventory
inventory added
```

---

## Messages courts

Le titre doit permettre de comprendre immédiatement le contenu du commit.

Éviter les descriptions longues.

---

## Granularité

Un commit doit représenter une évolution cohérente du projet.

Il doit être suffisamment petit pour être compris et relu facilement, tout en représentant une modification logique complète.

Éviter :

- les commits regroupant plusieurs sujets différents ;
- les commits excessivement petits qui fragmentent inutilement l'historique.

---

# Exemples d'historique

```text
docs: add architecture documentation

docs: add development guidelines

feat: implement character system

feat: add inventory module

feat: create combat engine

fix: resolve save loading issue

refactor: simplify game loop

test: add combat unit tests

chore: update dependencies
```

Cet historique est lisible et permet de suivre facilement l'évolution du projet.

---

# Convention adoptée par Project Dust

Le projet utilisera principalement les types suivants :

| Type | Utilisation |
|-------|-------------|
| feat | Nouvelle fonctionnalité |
| fix | Correction de bug |
| docs | Documentation |
| refactor | Réorganisation du code |
| test | Ajout ou modification des tests |
| chore | Maintenance |

Les autres types (`style`, `perf`, `build`, `ci`) seront utilisés lorsque nécessaire.

---

# Conclusion

Chaque commit doit être :

- clair ;
- concis ;
- cohérent ;
- autonome.

L'objectif est de conserver un historique Git propre, compréhensible et maintenable tout au long du développement de Project Dust.