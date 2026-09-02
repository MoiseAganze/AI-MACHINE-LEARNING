# 🧠 AI / Machine Learning — Semaine 01

> **Période : 3 → 6 septembre 2026**
> **Dimanche 6 septembre : bilan hebdomadaire**
> **Objectif de la semaine : comprendre ce qu'est réellement un modèle de Machine Learning et être capable d'en construire un premier très simple.**

---

# 🗂️ STRUCTURE DU DÉPÔT GITHUB

Nous allons volontairement garder une structure **simple et facile à maintenir**.

Le dépôt sera organisé par semaines.

```text
AI-MACHINE-LEARNING/
│
├── README.md
│
├── semaine-01/
│   ├── README.md
│   ├── exercices/
│   ├── code/
│   ├── calculs/
│   └── bilan/
│
├── semaine-02/
│   ├── README.md
│   ├── exercices/
│   ├── code/
│   ├── calculs/
│   └── bilan/
│
├── semaine-03/
│   ├── README.md
│   ├── exercices/
│   ├── code/
│   ├── calculs/
│   └── bilan/
│
└── ...
```

### Principe

Chaque semaine possède donc :

```text
semaine-X/
│
├── README.md      ← plan + cours + exercices + validation
├── exercices/     ← réponses aux exercices
├── code/          ← code écrit pendant la semaine
├── calculs/       ← calculs papier / captures
└── bilan/         ← bilan du dimanche
```

Le **README.md est le document principal**.

Tout ce que nous faisons pendant la semaine doit pouvoir être retrouvé depuis celui-ci.

---

# 📂 QUE METTRE DANS CHAQUE DOSSIER ?

## `README.md`

C'est le fichier que nous sommes en train de lire.

Il contient :

* les objectifs ;
* les notions à apprendre ;
* le programme de chaque jour ;
* les exercices ;
* les questions ;
* le niveau attendu ;
* les critères de validation ;
* la checklist du dimanche.

---

## `exercices/`

On y place les réponses aux exercices.

Exemple :

```text
exercices/
├── EX-01.md
├── EX-02.md
└── EX-03.md
```

Chaque exercice doit contenir :

```markdown
# EX-01

## Énoncé

...

## Mon raisonnement

...

## Ma réponse

...

## Vérification

...

## Erreur éventuelle

...

## Ce que j'ai appris

...
```

### Règle

**Le raisonnement doit apparaître avant la réponse.**

Même si la réponse est fausse.

Cela nous permettra d'identifier précisément nos erreurs.

---

# ✏️ `calculs/`

Tous les calculs réalisés sur papier sont conservés ici.

Exemple :

```text
calculs/
├── CALC-01.jpg
├── CALC-02.jpg
└── CALC-03.jpg
```

Une photo/capture est parfaitement acceptable.

Il n'est pas nécessaire de retaper tous les calculs dans Markdown.

### Exemple

```text
calculs/
└── CALC-01-prediction.jpg
```

Si un calcul est réalisé directement dans le README, on peut également l'écrire.

Mais pour les exercices importants :

> **on garde une trace du travail papier.**

---

# 💻 `code/`

Tous les programmes écrits pendant la semaine.

Exemple :

```text
code/
├── CODE-01-model.py
├── CODE-02-experiment.py
└── CODE-03-test.py
```

Pour chaque exercice de code, le README indique quel fichier correspond à l'exercice.

Exemple :

```markdown
## CODE-01

Fichier : `code/CODE-01-model.py`
```

---

# 📋 `bilan/`

Ce dossier contient le compte rendu du dimanche.

```text
bilan/
├── README.md
├── erreurs.md
└── validation.md
```

### `bilan/README.md`

Il contient :

* ce que nous avons appris ;
* ce que nous savons faire ;
* nos difficultés ;
* nos erreurs ;
* nos questions restantes ;
* notre score ;
* les notions validées ;
* les notions à revoir ;
* l'objectif de la semaine suivante.

---

# 👥 TRAVAIL À DEUX

Nous sommes deux.

Le dépôt doit permettre de savoir qui a produit quoi, mais sans créer une structure compliquée.

Pour les exercices individuels, nous utiliserons simplement le nom/prénom ou un identifiant.

Exemple :

```text
exercices/
├── EX-01-boss.md
├── EX-01-collaborateur.md
```

Pour le code :

```text
code/
├── CODE-01-boss.py
└── CODE-01-collaborateur.py
```

Pour les calculs :

```text
calculs/
├── CALC-01-boss.jpg
└── CALC-01-collaborateur.jpg
```

Cela permet de comparer les raisonnements sans multiplier les dossiers.

---

# 🔀 GIT

Nous utiliserons également Git de manière simple.

```text
main
│
├── boss
│
└── collaborateur
```

Chacun travaille sur sa branche.

À la fin de la semaine :

1. chacun pousse son travail ;
2. chacun regarde le travail de l'autre ;
3. on corrige les éventuelles erreurs ;
4. le travail validé rejoint `main`.

---

# 📝 CONVENTION DES COMMITS

Utiliser des messages simples et explicites.

```text
feat: add first model
docs: add exercise answers
docs: add weekly questions
test: validate prediction
fix: correct calculation
review: validate week 01
```

Éviter :

```text
update
test
final
new
aaa
final-final
```

---

# 🎯 OBJECTIF GÉNÉRAL DE LA SEMAINE

À la fin de cette première semaine, nous devons être capables de répondre clairement à cette question :

> **Qu'est-ce qu'un modèle de Machine Learning et comment apprend-il à partir de données ?**

Nous ne cherchons pas encore à utiliser des bibliothèques complexes.

Nous voulons comprendre le mécanisme **de l'intérieur**.

---

# 📚 À LA FIN DE LA SEMAINE, NOUS DEVONS COMPRENDRE

* ce qu'est une donnée ;
* ce qu'est une feature ;
* ce qu'est une cible (`target`) ;
* ce qu'est un paramètre ;
* ce qu'est une prédiction ;
* ce qu'est un modèle ;
* la différence entre programmation classique et Machine Learning ;
* ce que signifie entraîner un modèle ;
* ce que signifie faire une prédiction ;
* comment un modèle peut apprendre une relation à partir d'exemples ;
* pourquoi les paramètres du modèle sont importants.

---

# 📅 ORGANISATION

| Jour                | Travail                  | Validation                       |
| ------------------- | ------------------------ | -------------------------------- |
| 🟢 Jeudi 03/09      | Qu'est-ce qu'un modèle ? | Compréhension fondamentale       |
| 🟢 Samedi 05/09     | Premier modèle apprenant | Implémentation + expérimentation |
| 🔵 Dimanche 06/09   | Bilan                    | Examen + validation              |
| ⚪ Mercredi/Vendredi | Repos / rattrapage       | Facultatif                       |

---

# 🟢 JOUR 1 — 03 SEPTEMBRE

# 🧠 Notion : modèle, données et apprentissage

## Objectif

Comprendre la différence entre :

```text
Programme classique
        ↓
Règles écrites par le programmeur
        ↓
Résultat
```

et :

```text
Machine Learning
        ↓
Données + résultats connus
        ↓
Apprentissage
        ↓
Modèle
        ↓
Prédiction
```

---

# 📚 À APPRENDRE

## 1. Donnée

Comprendre ce qu'est une donnée utilisée par un modèle.

Exemple :

```text
surface = 100 m²
chambres = 3
prix = 200 000 €
```

Identifier :

* les informations disponibles ;
* l'information que nous cherchons à prédire.

---

## 2. Feature

Une **feature** est une caractéristique utilisée comme entrée du modèle.

Exemple :

```text
surface
nombre de chambres
distance au centre-ville
```

Ces informations constituent les entrées `X`.

---

## 3. Target

La cible est ce que le modèle doit apprendre à prédire.

Exemple :

```text
X = [100, 3, 5]
y = 200000
```

---

## 4. Paramètres

Comprendre qu'un modèle possède des paramètres internes qui déterminent son comportement.

Nous introduirons notamment :

```text
w
b
```

où :

* `w` représente un poids ;
* `b` représente un biais.

---

## 5. Prédiction

Le modèle reçoit une entrée :

```text
X
```

et produit :

```text
ŷ
```

où `ŷ` représente la prédiction.

---

# ✏️ EXERCICES — JOUR 1

## EX-01 — Identifier les éléments

On possède les données suivantes :

| Surface | Chambres | Prix |
| ------: | -------: | ---: |
|      50 |        2 |  100 |
|      80 |        3 |  150 |
|     120 |        4 |  230 |

Sur papier, identifier :

1. `X`
2. `y`
3. les features
4. la target

### Fichier attendu

```text
calculs/CALC-01-identification.jpg
```

et :

```text
exercices/EX-01-boss.md
exercices/EX-01-collaborateur.md
```

---

## EX-02 — Raisonnement

Un modèle reçoit :

```text
surface = 100
```

et prédit :

```text
ŷ = 180
```

alors que la vraie valeur est :

```text
y = 200
```

Questions :

1. Quelle est l'entrée ?
2. Quelle est la prédiction ?
3. Quelle est la vraie valeur ?
4. Le modèle a-t-il fait une erreur ?
5. De combien ?

### Fichier attendu

```text
exercices/EX-02-boss.md
exercices/EX-02-collaborateur.md
```

---

# 🧠 QUESTIONS DE VALIDATION — JOUR 1

Vous devez répondre **sans regarder les notes**.

### Niveau 1 — Comprendre

* Qu'est-ce qu'une donnée ?
* Qu'est-ce qu'une feature ?
* Qu'est-ce qu'une target ?
* Quelle différence entre `y` et `ŷ` ?
* Qu'est-ce qu'un paramètre ?

### Niveau 2 — Expliquer

Expliquez avec vos propres mots :

> Pourquoi dit-on qu'un modèle de Machine Learning "apprend" ?

Puis :

> Quelle différence entre écrire une règle permettant de calculer un prix et entraîner un modèle à prédire ce prix ?

### Niveau 3 — Défendre

Votre partenaire doit vous poser au minimum **3 questions imprévues**.

Vous devez être capables de défendre votre réponse sans consulter ChatGPT.

---

# 📁 TRACES ATTENDUES — JOUR 1

À la fin de la séance :

```text
semaine-01/
│
├── README.md
│
├── exercices/
│   ├── EX-01-boss.md
│   ├── EX-01-collaborateur.md
│   ├── EX-02-boss.md
│   └── EX-02-collaborateur.md
│
├── code/
│
├── calculs/
│   └── CALC-01-identification.jpg
│
└── bilan/
```

---

# ✅ NIVEAU ATTENDU EN FIN DE JOURNÉE

### 🟢 VALIDÉ

Vous êtes capables de :

* identifier `X` et `y` ;
* distinguer feature et target ;
* expliquer `w`, `b`, `y`, `ŷ` ;
* expliquer ce qu'est un modèle ;
* expliquer pourquoi un modèle possède des paramètres ;
* expliquer la différence entre programmation classique et ML.

### 🟡 PARTIEL

Vous connaissez les définitions mais avez besoin d'aide pour les relier.

### 🔴 NON VALIDÉ

Vous récitez les définitions sans comprendre les relations entre elles.

---

# 🟢 JOUR 2 — 05 SEPTEMBRE

# 🚀 Construire notre premier modèle

## Objectif

Nous allons construire un modèle extrêmement simple :

```text
ŷ = wx + b
```

Il s'agit d'un modèle linéaire.

⚠️ **Important : nous ne cherchons pas encore à faire du Machine Learning sophistiqué.**

Le but est de comprendre :

```text
entrée
   ↓
modèle
   ↓
prédiction
```

puis :

```text
prédiction
   ↓
comparaison avec la vraie valeur
   ↓
erreur
```

---

# 📚 À APPRENDRE

## 1. Poids `w`

Comprendre comment `w` influence la prédiction.

Question fondamentale :

> Que se passe-t-il lorsque `w` augmente ?

---

## 2. Biais `b`

Comprendre le rôle du biais.

Question :

> Que se passe-t-il lorsque `b` augmente sans modifier `w` ?

---

## 3. Fonction de prédiction

Notre modèle :

```text
ŷ = wx + b
```

Nous devons être capables de calculer `ŷ` à la main.

---

# ✏️ EXERCICE PAPIER

Prenons :

```text
x = 5
w = 2
b = 3
```

Calculer :

```text
ŷ
```

Puis modifier :

```text
w = 3
```

et recalculer.

### Questions

1. Pourquoi la prédiction a-t-elle changé ?
2. Quelle variable a provoqué ce changement ?
3. Que représente intuitivement `w` ?

### Fichiers attendus

```text
calculs/
├── CALC-01-first-prediction-boss.jpg
├── CALC-01-first-prediction-collaborateur.jpg
├── CALC-02-weight-change-boss.jpg
└── CALC-02-weight-change-collaborateur.jpg
```

---

# 🔬 EXPÉRIENCE

Tester plusieurs valeurs :

```text
w = 0
w = 1
w = 2
w = 5
```

en conservant :

```text
x = 5
b = 3
```

Créer un tableau :

|  w |  x |  b |  ŷ |
| -: | -: | -: | -: |
|  0 |  5 |  3 |  ? |
|  1 |  5 |  3 |  ? |
|  2 |  5 |  3 |  ? |
|  5 |  5 |  3 |  ? |

---

# 💻 CODAGE

Nous allons implémenter nous-mêmes le modèle.

### Contraintes

❌ Pas de scikit-learn
❌ Pas de PyTorch
❌ Pas de fonction ML toute faite
❌ Pas de code copié depuis ChatGPT

✅ Python uniquement.

Vous devez être capables d'écrire vous-mêmes la logique :

```text
x
↓
w
↓
b
↓
ŷ
```

### Fichiers attendus

```text
code/
├── CODE-01-basic-model-boss.py
└── CODE-01-basic-model-collaborateur.py
```

---

# 🧪 EXPÉRIENCE 2 — Modifier le modèle

Faire varier :

```text
x
w
b
```

et observer les prédictions.

Chercher expérimentalement :

> Quelle combinaison de `w` et `b` permet de se rapprocher le plus d'une valeur cible ?

### Fichiers attendus

```text
code/
├── CODE-02-experiment-boss.py
└── CODE-02-experiment-collaborateur.py
```

et éventuellement :

```text
exercices/
├── EXP-01-results-boss.md
└── EXP-01-results-collaborateur.md
```

---

# 🧠 QUESTIONS DE VALIDATION — JOUR 2

### Niveau 1

* Que représente `x` ?
* Que représente `w` ?
* Que représente `b` ?
* Que représente `ŷ` ?

### Niveau 2

Sans ordinateur :

```text
x = 4
w = 3
b = 2
```

Calculer la prédiction.

Puis :

```text
w = 5
```

Calculer à nouveau.

---

### Niveau 3

Expliquez :

> Pourquoi modifier `w` modifie-t-il la prédiction ?

Puis :

> Pourquoi modifier `b` modifie-t-il la prédiction ?

---

### Niveau 4 — Challenge

Votre partenaire vous donne :

```text
x = 10
```

et vous demande :

> "Trouve `w` et `b` permettant d'obtenir une prédiction de 25."

Vous devez raisonner **sans chercher sur Internet et sans demander à ChatGPT**.

Plusieurs solutions peuvent exister.

Le but est de comprendre la relation entre les paramètres et la sortie.

---

# 📁 TRACES ATTENDUES — JOUR 2

```text
semaine-01/
│
├── README.md
│
├── exercices/
│   ├── EX-01-boss.md
│   ├── EX-01-collaborateur.md
│   ├── EX-02-boss.md
│   ├── EX-02-collaborateur.md
│   ├── EXP-01-results-boss.md
│   └── EXP-01-results-collaborateur.md
│
├── code/
│   ├── CODE-01-basic-model-boss.py
│   ├── CODE-01-basic-model-collaborateur.py
│   ├── CODE-02-experiment-boss.py
│   └── CODE-02-experiment-collaborateur.py
│
├── calculs/
│   ├── CALC-01-first-prediction-boss.jpg
│   ├── CALC-01-first-prediction-collaborateur.jpg
│   ├── CALC-02-weight-change-boss.jpg
│   └── CALC-02-weight-change-collaborateur.jpg
│
└── bilan/
```

---

# ✅ NIVEAU ATTENDU EN FIN DE JOURNÉE

Vous devez être capables de :

* calculer `ŷ = wx + b` sans aide ;
* expliquer le rôle de `w` ;
* expliquer le rôle de `b` ;
* coder le modèle vous-mêmes ;
* modifier les paramètres ;
* observer leur impact ;
* expliquer pourquoi le modèle peut produire différentes prédictions.

---

# 🔵 DIMANCHE 06 SEPTEMBRE — BILAN

# 📋 WEEKLY REVIEW

Le dimanche est consacré au **compte rendu, aux cases et au bilan**.

Aucune nouvelle notion obligatoire.

---

# 1️⃣ CHECKLIST

### Compréhension

* [ ] Je sais définir un modèle ML.
* [ ] Je sais expliquer ce qu'est une donnée.
* [ ] Je sais identifier une feature.
* [ ] Je sais identifier une target.
* [ ] Je comprends `y`.
* [ ] Je comprends `ŷ`.
* [ ] Je comprends le rôle de `w`.
* [ ] Je comprends le rôle de `b`.

### Mathématiques

* [ ] Je peux calculer `ŷ = wx + b`.
* [ ] Je peux modifier `w` et prévoir son effet.
* [ ] Je peux modifier `b` et prévoir son effet.

### Programmation

* [ ] Je peux coder le modèle sans assistance.
* [ ] Je peux modifier ses paramètres.
* [ ] Je peux tester plusieurs entrées.
* [ ] Je comprends mon propre code.

### Explication

* [ ] Je peux expliquer le fonctionnement du modèle à mon partenaire.
* [ ] Je peux répondre à une question imprévue.
* [ ] Je peux expliquer sans lire mes notes.

---

# 2️⃣ EXAMEN PAPIER ✏️

## Question 1

On possède :

```text
x = 7
w = 3
b = 2
```

Calculer `ŷ`.

---

## Question 2

On obtient :

```text
ŷ = 23
y = 25
```

Quelle est l'erreur ?

---

## Question 3

Si `w` augmente :

> Quel effet cela peut-il avoir sur `ŷ` ?

Expliquez **pourquoi**, pas seulement le résultat.

---

## Question 4

Quelle différence fondamentale existe entre :

```text
ŷ
```

et :

```text
y
```

---

## Question 5 — Conceptuelle

Expliquez cette phrase :

> "Un modèle de Machine Learning apprend des paramètres à partir de données."

Votre réponse doit expliquer :

```text
données
   ↓
modèle
   ↓
paramètres
   ↓
prédiction
```

---

# 3️⃣ EXAMEN ORAL 🗣️

Chaque personne dispose de **5 minutes**.

Le partenaire joue le rôle du professeur.

Il peut demander :

> Pourquoi `w` existe ?

> Pourquoi `b` existe ?

> Pourquoi avons-nous besoin de données ?

> Pourquoi la prédiction n'est-elle pas forcément correcte ?

> Est-ce que changer `w` change toujours la prédiction ?

> Est-ce qu'un modèle est une simple formule ?

> Quelle différence entre programmer une règle et entraîner un modèle ?

---

# 4️⃣ EXAMEN CODE 💻

### Mission

Repartir d'un fichier Python vide.

Sans ChatGPT :

1. créer une entrée `x` ;
2. créer `w` ;
3. créer `b` ;
4. calculer `ŷ` ;
5. afficher le résultat ;
6. modifier `w` ;
7. observer le changement.

### Règle

Si vous bloquez :

**10 minutes de réflexion → notes → nouvelle tentative → seulement ensuite demander de l'aide.**

L'objectif est de développer votre capacité à coder **sans dépendre de l'IA**.

---

# 📊 SCORE DE LA SEMAINE

Attribuer une note sur 20 :

| Domaine               |  Points |
| --------------------- | ------: |
| Compréhension         |      /5 |
| Mathématiques         |      /5 |
| Programmation         |      /5 |
| Explication / défense |      /5 |
| **TOTAL**             | **/20** |

### 🟢 16–20

Notion validée.

### 🟡 12–15

Compréhension correcte mais une faiblesse doit être identifiée.

### 🔴 <12

La notion n'est pas suffisamment maîtrisée.

➡️ La semaine suivante commence par une **remédiation** avant de poursuivre.

---

# 📝 COMPTE RENDU DU DIMANCHE

À remplir dans :

```text
bilan/
```

## `bilan/README.md`

```markdown
# 📋 Bilan — Semaine 01

## 🎯 Objectif de la semaine

...

## 🧠 Ce que j'ai appris

- ...
- ...
- ...

## 💻 Ce que je sais coder seul

- ...
- ...
- ...

## ✏️ Ce que je sais calculer

- ...
- ...
- ...

## ⚠️ Mes difficultés

- ...
- ...
- ...

## ❌ Mes principales erreurs

- ...
- ...
- ...

## ❓ Questions encore ouvertes

- ...
- ...
- ...

## 🟢 Notions validées

- [ ] Modèle
- [ ] Données
- [ ] Features
- [ ] Target
- [ ] Paramètres
- [ ] Poids
- [ ] Biais
- [ ] Prédiction

## 📊 Score

### Boss

__/20

### Collaborateur

__/20

## 🎯 Remédiation

...

## 🚀 Objectif de la semaine suivante

...
```

---

# `bilan/erreurs.md`

Conserver uniquement les erreurs importantes.

```markdown
# ❌ Erreurs importantes

## Erreur 01

### Ce que j'ai fait

...

### Pourquoi c'était faux

...

### Correction

...

### Ce que je retiens

...
```

---

# `bilan/validation.md`

```markdown
# 🟢 Validation — Semaine 01

## Boss

- [ ] Niveau 1 — Comprendre
- [ ] Niveau 2 — Calculer
- [ ] Niveau 3 — Coder
- [ ] Niveau 4 — Défendre

### Résultat

🟢 VALIDÉ / 🟡 PARTIEL / 🔴 NON VALIDÉ

---

## Collaborateur

- [ ] Niveau 1 — Comprendre
- [ ] Niveau 2 — Calculer
- [ ] Niveau 3 — Coder
- [ ] Niveau 4 — Défendre

### Résultat

🟢 VALIDÉ / 🟡 PARTIEL / 🔴 NON VALIDÉ
```

---

# 🏆 CRITÈRE DE RÉUSSITE DE LA SEMAINE 01

La semaine est considérée comme réussie si chacun des deux membres peut, **individuellement et sans IA**, expliquer et implémenter :

```text
X
↓
modèle
↓
w, b
↓
ŷ
↓
comparaison avec y
```

Le but n'est pas encore de connaître beaucoup de concepts.

Le but est de construire la première brique de notre compréhension :

> **Un modèle est une structure paramétrée qui transforme des entrées en prédictions, et l'apprentissage consistera ensuite à trouver de meilleurs paramètres à partir des données.**

---

# 🔒 RÈGLES DU PROJET

## 1. Pas de vibecoding

Pendant les exercices :

**Nous essayons d'abord nous-mêmes.**

L'IA peut servir à :

* expliquer une notion ;
* poser des questions ;
* donner un indice ;
* analyser une erreur après tentative.

Elle ne doit pas devenir :

> "Donne-moi le code."

---

## 2. Chaque membre doit coder

Même si une personne comprend mieux :

```text
Personne A → implémente
Personne B → explique/review
```

puis on inverse.

---

## 3. Comprendre > mémoriser

Une formule récitée mais non comprise = ❌ non validée.

---

## 4. Une notion non maîtrisée bloque la progression

Nous ne poursuivons pas simplement parce que le calendrier dit d'avancer.

**Compréhension insuffisante → remédiation → nouvelle validation.**

---

# 🚀 PROCHAINE ÉTAPE

Si la semaine 01 est validée, nous attaquerons :

**Semaine 02 → vecteurs, normes, distances et produit scalaire.**

Ces notions seront directement reliées aux représentations numériques que nous utiliserons ensuite en Machine Learning.
