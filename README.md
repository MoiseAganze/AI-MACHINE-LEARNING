# 🤖 AI-MACHINE-LEARNING

Parcours personnel d'apprentissage du **Machine Learning, Deep Learning et des LLMs**, réalisé en collaboration avec un partenaire.

---

## 🎯 Objectif global

Construire une compréhension solide et pratique de l'IA, depuis les fondamentaux mathématiques et du Machine Learning jusqu'à la compréhension, l'entraînement et la personnalisation de modèles modernes.

À terme, être capable de :

* comprendre comment fonctionne un modèle de Machine Learning ;
* comprendre les mathématiques utilisées par les modèles ;
* implémenter les mécanismes fondamentaux soi-même ;
* entraîner des modèles ;
* comprendre les réseaux de neurones et le backpropagation ;
* comprendre les embeddings et les Transformers ;
* comprendre l'architecture et le fonctionnement des LLMs ;
* prendre un modèle open source et le personnaliser / fine-tuner ;
* évaluer correctement un modèle ;
* puis, dans une étape ultérieure, rendre ces modèles exploitables via des APIs, applications, agents, RAG, etc.

> ⚠️ L'objectif n'est pas de simplement savoir utiliser des bibliothèques d'IA.
>
> L'objectif est de **comprendre ce qui se passe sous le capot et être capable de le reproduire soi-même à petite échelle.**

---

# 🗺️ Roadmap

| Semaine | Période            | Thème                                                  | Statut      |
| ------- | ------------------ | ------------------------------------------------------ | ----------- |
| 01      | 03 → 06 sept.      | Fondamentaux : modèle, données, paramètres, prédiction | 🟡 En cours |
| 02      | 07 → 13 sept.      | Vecteurs, normes, distances, produit scalaire          | ⬜           |
| 03      | 14 → 20 sept.      | Matrices et transformations                            | ⬜           |
| 04      | 21 → 27 sept.      | Dérivées, fonction de coût, règle de chaîne            | ⬜           |
| 05      | 28 sept. → 04 oct. | Gradient Descent                                       | ⬜           |
| 06      | 05 → 11 oct.       | Régression linéaire                                    | ⬜           |
| 07      | 12 → 18 oct.       | Classification et régression logistique                | ⬜           |
| 08      | 19 → 25 oct.       | Évaluation, overfitting, underfitting, régularisation  | ⬜           |
| 09      | 26 oct. → 01 nov.  | Réseaux de neurones et forward pass                    | ⬜           |
| 10      | 02 → 08 nov.       | Backpropagation                                        | ⬜           |
| 11      | 09 → 15 nov.       | PyTorch et entraînement réel                           | ⬜           |
| 12      | 16 → 22 nov.       | Embeddings, attention et Transformers                  | ⬜           |
| 13      | 23 → 29 nov.       | Modèles open source et fine-tuning                     | ⬜           |
| 🏁      | 30 nov.            | Examen pratique final                                  | ⬜           |

### Légende

* ⬜ À faire
* 🟡 En cours
* 🟢 Validé
* 🔴 À retravailler

> Les dates sont indicatives. Le parcours est **adaptatif** : une notion non maîtrisée doit être retravaillée avant de passer à la suivante.

---

# 📚 Organisation du dépôt

Chaque semaine possède son propre espace de travail.

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
│   └── ...
│
└── ...
```

### 📌 Rôle des dossiers

**`README.md` racine**

Vue d'ensemble du parcours et suivi de progression.

**`semaine-X/README.md`**

Cours, programme, exercices et critères de validation de la semaine.

**`exercices/`**

Réponses aux exercices et raisonnements.

**`code/`**

Implémentations Python et expériences.

**`calculs/`**

Calculs réalisés sur papier, photos ou captures.

**`bilan/`**

Erreurs, difficultés, validation et score de la semaine.

---

# 🧠 Méthode d'apprentissage

Chaque notion doit être validée sur **4 niveaux** :

### 1. Comprendre

Être capable d'expliquer la notion avec ses propres mots.

### 2. Calculer

Être capable de résoudre un exercice à la main.

### 3. Implémenter

Être capable de coder le mécanisme sans copier une solution.

### 4. Expliquer

Être capable d'enseigner la notion à son partenaire et de répondre à ses questions.

Une notion n'est considérée comme **🟢 validée** que lorsque les quatre niveaux sont suffisamment maîtrisés.

---

# 💻 Règle concernant l'IA

L'IA peut être utilisée comme :

* professeur ;
* source d'explications ;
* outil de vérification ;
* générateur d'indices ;
* outil d'analyse des erreurs.

Mais elle ne doit pas remplacer le travail d'apprentissage.

### ❌ À éviter

* copier du code sans le comprendre ;
* demander directement la solution d'un exercice ;
* faire du *vibecoding* ;
* recopier une implémentation sans être capable de la refaire seul.

### ✅ À privilégier

1. réfléchir seul ;
2. écrire son raisonnement ;
3. essayer sur papier ;
4. coder soi-même ;
5. identifier son erreur ;
6. demander un indice si nécessaire ;
7. corriger ;
8. refaire l'exercice sans aide.

---

# 👥 Travail en collaboration

Le dépôt est partagé entre deux personnes :

* **Boss**
* **Collaborateur**

Chaque personne doit effectuer elle-même les exercices et implémentations importants.

Structure Git :

```text
main
├── boss
└── collaborateur
```

Avant la validation hebdomadaire :

1. chacun termine son travail ;
2. chacun relit le travail de l'autre ;
3. les erreurs sont corrigées ;
4. les notions difficiles sont discutées ;
5. le bilan est rempli ;
6. les modifications sont fusionnées dans `main`.

---

# 📊 Validation hebdomadaire

Chaque semaine est évaluée sur **20 points**.

| Critère               |  Points |
| --------------------- | ------: |
| Compréhension         |      /5 |
| Mathématiques         |      /5 |
| Programmation         |      /5 |
| Explication / défense |      /5 |
| **Total**             | **/20** |

### Interprétation

* 🟢 **16–20** → notion/semaine validée
* 🟡 **12–15** → validation partielle, remédiation nécessaire
* 🔴 **<12** → semaine à retravailler

Le score n'est pas une fin en soi : il sert à identifier les lacunes.

---

# 📅 Organisation hebdomadaire

Chaque semaine comporte :

### 🧠 4 jours d'apprentissage

Chaque journée possède :

* une notion principale ;
* une explication ;
* des exercices ;
* du calcul sur papier ;
* de la pratique de code ;
* une validation de la notion.

### 📋 Dimanche — Révision et bilan

Le dimanche est réservé à :

* révision de la semaine ;
* exercices de synthèse ;
* calculs sans aide ;
* test de code ;
* explication orale ;
* correction des erreurs ;
* score /20 ;
* décision : **continuer ou remédier**.

Aucune nouvelle notion importante ne doit être introduite le dimanche.

---

# 🧭 Principe d'adaptation

Le calendrier ne passe jamais avant la compréhension.

Si une notion est mal maîtrisée :

```text
Notion
   ↓
Exercices
   ↓
Évaluation
   ↓
❌ Lacune
   ↓
Remédiation
   ↓
Nouvelle évaluation
   ↓
🟢 Validation
   ↓
Notion suivante
```

L'objectif est de construire des bases solides plutôt que d'avancer rapidement avec des lacunes.

---

# 🚀 Objectif de fin de parcours

À la fin du parcours, l'objectif est d'être capable de partir d'un problème et de comprendre la chaîne :

```text
Données
   ↓
Features
   ↓
Modèle
   ↓
Paramètres
   ↓
Prédiction
   ↓
Loss
   ↓
Gradient
   ↓
Mise à jour des paramètres
   ↓
Entraînement
   ↓
Modèle entraîné
```

Puis de poursuivre vers :

```text
Modèle entraîné
      ↓
Embeddings
      ↓
Attention
      ↓
Transformer
      ↓
LLM
      ↓
Fine-tuning
      ↓
Évaluation
      ↓
Déploiement
      ↓
API / RAG / Agents / Applications
```

---

# 📈 Progression générale

* [ ] Semaine 01 — Fondamentaux
* [ ] Semaine 02 — Vecteurs
* [ ] Semaine 03 — Matrices
* [ ] Semaine 04 — Calcul différentiel
* [ ] Semaine 05 — Gradient Descent
* [ ] Semaine 06 — Régression linéaire
* [ ] Semaine 07 — Classification
* [ ] Semaine 08 — Évaluation et régularisation
* [ ] Semaine 09 — Réseaux de neurones
* [ ] Semaine 10 — Backpropagation
* [ ] Semaine 11 — PyTorch
* [ ] Semaine 12 — Transformers
* [ ] Semaine 13 — Fine-tuning
* [ ] Examen final

---

# 🏁 Règle finale

> **Comprendre → Calculer → Coder → Expliquer → Valider → Avancer.**

Pas l'inverse.
