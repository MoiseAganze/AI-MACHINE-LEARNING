# Plan d'apprentissage Machine Learning & Deep Learning

> **Période : 3 septembre → 30 novembre 2026**  
> **Objectif :** construire progressivement les bases mathématiques, comprendre les mécanismes fondamentaux du Machine Learning et du Deep Learning, puis être capable d'entraîner, évaluer et adapter un modèle moderne sur un problème réel.

---

## 1. Vision générale

Le parcours repose sur trois livres complémentaires :

1. **Math for ML** — construire les fondations mathématiques nécessaires au ML.
2. **Hands-On Machine Learning** — apprendre à transformer les concepts en modèles et expérimentations concrètes.
3. **Deep Learning — Goodfellow, Bengio & Courville** — comprendre les fondements théoriques du Deep Learning.

---

# 2. Plan hebdomadaire

## Semaine 1 — 3 → 6 septembre
### Fondamentaux du Machine Learning

**Objectif**

Comprendre ce qu'est un modèle de Machine Learning, ce que représentent les données, les paramètres, les prédictions, la fonction de coût et l'entraînement.


### Critère de validation

Tu dois pouvoir répondre clairement à :

> Qu'est-ce qu'un modèle ?  
> Qu'est-ce qu'un paramètre ?  
> Qu'est-ce qu'une prédiction ?  
> Pourquoi entraîne-t-on un modèle ?

---

# Semaine 2 — 7 → 13 septembre
## Vecteurs, normes, distances et produit scalaire

**Objectif**

Comprendre comment les données numériques sont représentées mathématiquement et comment mesurer leur position, leur longueur et leur similarité.

### Critère de validation

Être capable d'expliquer pourquoi un exemple de données ML peut être représenté par un vecteur.

---

# Semaine 3 — 14 → 20 septembre
## Matrices et transformations

**Objectif**

Passer des vecteurs aux matrices et comprendre les matrices comme des opérateurs capables de transformer les données.

### Critère de validation

Comprendre :

```text
vecteur → matrice → vecteur transformé
```

et savoir expliquer ce que fait chaque dimension.

---

# Semaine 4 — 21 → 27 septembre
## Fonctions, dérivées et règle de chaîne

**Objectif**

Comprendre le calcul différentiel nécessaire pour optimiser un modèle.

### Critère de validation

Comprendre intuitivement :

> Le gradient indique dans quelle direction une fonction augmente le plus rapidement.

---

# Semaine 5 — 28 septembre → 4 octobre
## Optimisation et Gradient Descent

**Objectif**

Comprendre comment un modèle apprend ses paramètres.


### Critère de validation

Pouvoir expliquer précisément :

```text
θ ← θ - η ∇J(θ)
```

où `θ` représente les paramètres, `η` le learning rate et `J` la fonction de coût.

---

# Semaine 6 — 5 → 11 octobre
## Régression linéaire

**Objectif**

Construire le premier véritable modèle ML de bout en bout.

### Critère de validation

Être capable d'expliquer la différence entre :

- apprendre les paramètres analytiquement ;
- apprendre les paramètres avec Gradient Descent ;
- utiliser une implémentation de bibliothèque.

---

# Semaine 7 — 12 → 18 octobre
## Classification et régression logistique

**Objectif**

Passer de la prédiction d'une valeur continue à la prédiction d'une classe.

### Critère de validation

Comprendre pourquoi :

> Une bonne accuracy ne signifie pas forcément qu'un classifieur est bon.

---

# Semaine 8 — 19 → 25 octobre
## Évaluation, surapprentissage et régularisation

**Objectif**

Comprendre comment savoir si un modèle apprend réellement et comment contrôler sa capacité à généraliser.

### Critère de validation

Pouvoir diagnostiquer :

```text
Underfitting
     vs
Good fit
     vs
Overfitting
```

et proposer une correction.

---

# Semaine 9 — 26 octobre → 1er novembre
## Réseaux de neurones et Forward Pass

**Objectif**

Comprendre la structure interne d'un réseau de neurones et calculer une prédiction couche par couche.

### Critère de validation

Être capable de calculer à la main le résultat d'un petit réseau comportant quelques neurones.

---

# Semaine 10 — 2 → 8 novembre
## Backpropagation

**Objectif**

Comprendre comment un réseau de neurones calcule les gradients de ses paramètres.


### Critère de validation

Pouvoir expliquer :

> Comment l'erreur calculée à la sortie influence les poids situés plusieurs couches plus tôt ?

---

# Semaine 11 — 9 → 15 novembre
## PyTorch et entraînement réel

**Objectif**

Passer de l'implémentation pédagogique à un framework moderne de Deep Learning.

### Critère de validation

Être capable d'écrire sans tutoriel un training loop PyTorch simple.

---

# Semaine 12 — 16 → 22 novembre
## Embeddings, attention et Transformers

**Objectif**

Comprendre le passage des réseaux classiques aux architectures modernes utilisées notamment en NLP et dans les modèles de langage.

### Critère de validation

Pouvoir répondre à :

> Pourquoi l'attention permet-elle à un modèle de relier des éléments éloignés dans une séquence ?

---

# Semaine 13 — 23 → 29 novembre
## Modèles open source et Fine-Tuning

**Objectif**

Passer de la compréhension des architectures à l'utilisation de modèles pré-entraînés.

### Critère de validation

Être capable d'expliquer la différence entre :

- entraîner un modèle from scratch ;
- utiliser un modèle pré-entraîné ;
- faire du transfer learning ;
- faire du fine-tuning.

---

# 3. 30 novembre — Examen pratique final

## Objectif

Réaliser un mini-projet ML/DL complet sans suivre un tutoriel étape par étape.

### Sujet

Choisir un problème réel de :

- régression ;
- classification ;
- traitement de texte ;
- ou autre problème adapté au niveau atteint.

### Pipeline attendu

```text
1. Définition du problème
          ↓
2. Collecte / chargement des données
          ↓
3. Exploration
          ↓
4. Préprocessing
          ↓
5. Séparation train / validation / test
          ↓
6. Baseline
          ↓
7. Modèle
          ↓
8. Fonction de coût
          ↓
9. Entraînement
          ↓
10. Évaluation
          ↓
11. Analyse des erreurs
          ↓
12. Amélioration
          ↓
13. Résultat final
```

### Livrables finaux

Le projet doit contenir :

```text
project/
├── README.md
├── data/
├── notebooks/
├── src/
├── models/
├── requirements.txt
└── results/
```

Le `README.md` doit expliquer le projet de manière reproductible.

---

# 4. Progression des livrables

| Semaine | Livrable principal |
|---|---|
| W1 | Comprendre et expliquer un modèle ML |
| W2 | Module vecteurs / normes / distances |
| W3 | Transformations matricielles |
| W4 | Dérivées et gradients |
| W5 | Gradient Descent from scratch |
| W6 | Régression linéaire |
| W7 | Classification + métriques |
| W8 | Diagnostic overfitting / underfitting |
| W9 | Réseau de neurones + forward pass |
| W10 | Backpropagation from scratch |
| W11 | Réseau entraîné avec PyTorch |
| W12 | Attention + utilisation d'un Transformer |
| W13 | Adaptation / fine-tuning d'un modèle pré-entraîné |
| 30 nov. | Projet ML/DL complet |

---

# 5. Architecture pédagogique du parcours

Le parcours suit volontairement cette chaîne :

```text
MATHÉMATIQUES
     │
     ├── Vecteurs
     ├── Matrices
     ├── Fonctions
     ├── Dérivées
     ├── Gradients
     └── Optimisation
             │
             ▼
     MACHINE LEARNING
             │
     ├── Régression
     ├── Classification
     ├── Évaluation
     ├── Généralisation
     └── Régularisation
             │
             ▼
      DEEP LEARNING
             │
     ├── Neurones
     ├── Forward pass
     ├── Backpropagation
     ├── Optimisation
     └── Régularisation
             │
             ▼
      MODÈLES MODERNES
             │
     ├── Embeddings
     ├── Attention
     ├── Transformers
     ├── Modèles pré-entraînés
     └── Fine-tuning
```

L'idée centrale est de ne pas apprendre ces sujets comme des chapitres indépendants. Chaque nouvelle notion doit répondre à une question apparue précédemment.

Par exemple :

**Pourquoi les dérivées ?**

→ Parce qu'il faut calculer comment modifier les paramètres.

**Pourquoi le gradient ?**

→ Parce qu'un modèle possède plusieurs paramètres.

**Pourquoi Gradient Descent ?**

→ Parce qu'on veut minimiser une fonction de coût.

**Pourquoi Backpropagation ?**

→ Parce qu'un réseau contient de nombreuses couches et qu'il faut calculer efficacement les gradients.

**Pourquoi les Transformers ?**

→ Parce que les représentations et mécanismes d'attention permettent de traiter efficacement les dépendances dans des séquences et ont conduit à de nombreuses architectures modernes.

---

# 6. Règle de validation hebdomadaire

Une semaine n'est pas considérée comme terminée simplement parce que les chapitres ont été lus.

Elle est validée lorsque les trois niveaux suivants sont atteints :

### Niveau 1 — Compréhension

> Je peux expliquer le concept avec mes propres mots.

### Niveau 2 — Mathématiques

> Je peux comprendre ou reproduire les équations essentielles.

### Niveau 3 — Implémentation

> Je peux écrire ou utiliser le mécanisme dans un programme.

Pour les semaines centrales, ajouter un quatrième niveau :

### Niveau 4 — Analyse

> Je peux interpréter les résultats et expliquer pourquoi le modèle fonctionne ou échoue.

---

# 7. Priorité entre les trois livres

En cas de manque de temps, suivre cette priorité :

### Pour les mathématiques

**Math for ML > Deep Learning**

Math for ML sert de référence principale pour les bases mathématiques.

### Pour le Machine Learning classique

**Hands-On ML > Deep Learning**

Hands-On ML est plus directement orienté vers l'implémentation et l'expérimentation.

### Pour le Deep Learning théorique

**Deep Learning > Hands-On ML**

Goodfellow fournit le cadre théorique permettant de comprendre les mécanismes fondamentaux.

### Pour les Transformers

**Hands-On ML Ch. 16 > autres livres**

Le livre de Goodfellow est fondamental pour le Deep Learning, mais il ne constitue pas une référence moderne sur les Transformers. Le chapitre 16 de Hands-On ML est donc la lecture principale pour cette partie.

### Pour PyTorch

Les trois livres ne constituent pas une ressource PyTorch dédiée.

Le plan utilise Hands-On ML et Deep Learning pour les concepts, mais **PyTorch doit être complété par une ressource pratique dédiée**.

---

# 8. Résultat attendu au 30 novembre

À la fin du parcours, l'objectif n'est pas de connaître tous les algorithmes de Machine Learning.

L'objectif est d'être capable de passer de :

```text
"J'ai un problème et des données"
```

à :

```text
"J'ai défini le problème,
préparé les données,
choisi une baseline,
construit un modèle,
compris sa fonction de coût,
entraîné le modèle,
évalué ses performances,
analysé ses erreurs
et amélioré son comportement."
```

Et, pour le Deep Learning :

```text
Je comprends
    ↓
le neurone
    ↓
le forward pass
    ↓
la loss
    ↓
le gradient
    ↓
la backpropagation
    ↓
l'optimisation
    ↓
la régularisation
    ↓
les embeddings
    ↓
l'attention
    ↓
les Transformers
    ↓
le fine-tuning
```

C'est cette chaîne de compréhension et de pratique qui constitue l'objectif réel du parcours.
