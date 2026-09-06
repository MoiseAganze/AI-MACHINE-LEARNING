# Plan ML — README de suivi

## Règle de progression

Le parcours est organisé en semaines avec un système de **validation + rattrapage cumulatif**.

À la fin de chaque semaine :
1. Test des notions de la semaine.
2. Évaluation des réponses et de la pratique.
3. Les notions mal maîtrisées ou les pratiques non réalisées sont ajoutées à la **liste de rattrapage**.
4. La semaine suivante commence normalement.
5. À la fin de la semaine suivante : test de la nouvelle semaine + rattrapage des éléments précédemment échoués ou non réalisés.

### Statuts
- 🟢 Maîtrisé
- 🟡 Partiellement maîtrisé — rattrapage nécessaire
- 🔴 Non maîtrisé / non réalisé — rattrapage obligatoire

---

# Semaine 1 — Jargon & concepts fondamentaux

## 1. Machine Learning
**Question :** Qu'est-ce que le Machine Learning ? Différence avec un programme classique ?

**Ma réponse :**
> le machine learning est un domaine d'etude qui confere aux ordinateurs la capacité d'apprendre une tache données d'une serie d'experience sans etre explicitement programmé.
>
> la difference avec la programmation classique reside dans le fait que contrairement au machine learning, dans la programmation classique toute les regles relative à la réalisation d'une tache doivent etre explicitement programmé.

**Évaluation : 🟢 Maîtrisé**

**Correction :** Bonne définition. Le ML apprend une relation à partir de données/expériences au lieu de recevoir toutes les règles explicitement. Plus précisément, on parle souvent d'une fonction paramétrée dont les paramètres sont ajustés pendant l'entraînement.

---

## 2. Features, target, dataset et modèle
**Question :** Pour prédire le prix d'une maison à partir de sa surface, son nombre de chambres et sa localisation, identifier features, target, dataset et modèle.

**Ma réponse :**
> les features sont les differente caracteristiques commune à toute les maison par exemple le nombre des chambres, possession d'un parking ou non, etc
>
> le data set c'est l'ensemble des données de maison regroupé
>
> le modele est l'ensemble des regles que la machine va apprendre explicitement en fonction des l'ensemble des données(constituant l'experience) dans le but de realiser la tache(ici predire une maison)

**Évaluation : 🟡 Partiellement maîtrisé**

**Correction :**
- Features (`X`) : surface, chambres, localisation, parking...
- Target (`y`) : prix de la maison.
- Dataset : ensemble des exemples.
- Modèle : fonction paramétrée transformant les features en prédiction.

**Rattrapage :** target + définition précise du modèle.

---

## 3. Training vs inference
**Question :** Différence entre entraînement et prédiction ?

**Ma réponse :**
> l'entrainement c'est le processus qui permet de creer cette ensembles des regles(model)
>
> la prediction c'est la teche qu'effectue le model, une fois qu'on lui donne une nouvelle entrée

**Évaluation : 🟢 Maîtrisé**

**Correction :** Le training ajuste les paramètres du modèle à partir des données. L'inference utilise le modèle entraîné pour produire une prédiction.

---

## 4. Supervisé vs non supervisé
**Question :** Différence entre apprentissage supervisé et non supervisé ?

**Ma réponse :**
> l'apprentissage supervisé consiste à fournir au model des données d'entrainement étiqueté avec les bonne reponses et non supervicé c'est l'inverse

**Évaluation : 🟡 Partiellement maîtrisé**

**Correction :**
- Supervisé : les données ont des labels/targets pour la tâche.
- Non supervisé : aucune target n'est fournie pour la tâche ; l'algorithme cherche notamment des structures ou regroupements.

**Rattrapage :** définition du non supervisé.

---

## 5. Auto-supervisé
**Question :** Qu'est-ce que l'apprentissage auto-supervisé ?

**Ma réponse :**
> l'apprentissage auto supervisé consiste à generer un ensemble des données etiqueté partant d'un ensemble non etiqueté(d'où le nom auto-apprentissage car le model apprend seul à octroyer des reponse aux donnée sans intervention humaine)

**Évaluation : 🟡 Partiellement maîtrisé**

**Correction :** Le modèle construit automatiquement un signal/une tâche d'apprentissage à partir des données elles-mêmes. Exemple : masquer un mot dans une phrase et demander au modèle de le prédire.

**Rattrapage :** distinction supervisé / auto-supervisé / non supervisé.

---

## 6. Paramètres et hyperparamètres
**Question :** Qu'est-ce qu'un paramètre ? Différence avec un hyperparamètre ?

**Ma réponse :**
> un parametre d'un model est une variable interne qui permet aux models d'effectuer des nouvelles prediction

**Évaluation : 🟡 Partiellement maîtrisé**

**Correction :**
- Paramètre : valeur interne apprise/ajustée pendant le training.
- Hyperparamètre : valeur choisie par le praticien pour contrôler l'apprentissage ou la structure du modèle.
- Exemples : poids/biais = paramètres ; learning rate/profondeur d'arbre = hyperparamètres.

**Rattrapage :** paramètres vs hyperparamètres.

---

## 7. Fonction de perte
**Question :** À quoi sert une fonction de perte ? Si prédiction = 250 000 € et valeur réelle = 300 000 €, que cherche à faire l'entraînement ?

**Ma réponse :**
> une fonction de perte sert à quantifier l'erreur que commet un modele sur une entrée lors de l'entrainement
>
> l'entrainement cherche à minimiser le plus possible cet ecart

**Évaluation : 🟢 Maîtrisé**

**Correction :** Exact. La loss mesure l'écart entre prédiction et valeur attendue ; l'entraînement cherche à la minimiser en ajustant les paramètres.

---

## 8. Overfitting
**Question :** Qu'est-ce que l'overfitting ?

**Ma réponse :**
> on parle d'overfitting lorsqu'un model apprend tres parfaitement des ses données d'netrainement mais a du mal sur des nouvelles données

**Évaluation : 🟢 Maîtrisé**

**Correction :** Correct. Le modèle s'adapte excessivement aux données d'entraînement et généralise mal.

---

## 9. Underfitting vs overfitting
**Question :** Quelle différence ?

**Ma réponse :**
> overfitting: modele trop complexe pour la structure des données
>
> underfitting: modele trop simple pour la structure des donnée

**Évaluation : 🟢 Maîtrisé, avec précision**

**Correction :**
- Underfitting : modèle trop simple ou insuffisamment entraîné ; il capture mal les relations importantes.
- Overfitting : modèle trop adapté aux données d'entraînement et qui généralise mal.
La complexité excessive peut provoquer l'overfitting, mais n'en constitue pas la définition.

---

## 10. Train / validation / test
**Question :** Pourquoi séparer les données en train / validation / test ? Quel rôle pour chacun ?

**Ma réponse :** Pas de réponse.

**Évaluation : 🔴 Non maîtrisé / non répondu**

**Correction :**
- Train : apprendre les paramètres.
- Validation : comparer des configurations/modèles et régler les hyperparamètres.
- Test : évaluation finale sur des données gardées à part.

**Rattrapage obligatoire.**

---

## 11. Data snooping
**Question :** Pourquoi calculer moyenne et écart-type sur les 10 000 maisons avant la séparation train/test peut-il poser problème ?

**Ma réponse :** Pas de réponse.

**Évaluation : 🔴 Non maîtrisé / non répondu**

**Correction :** Les données de test influencent indirectement la préparation. Les statistiques de normalisation doivent être calculées sur le train uniquement, puis appliquées au train et au test.

**Rattrapage obligatoire.**

---

## 12. Data leakage
**Question :** Qu'est-ce que le data leakage ? Donne un exemple.

**Ma réponse :** Pas de réponse.

**Évaluation : 🔴 Non maîtrisé / non répondu**

**Correction :** Une information qui ne devrait pas être disponible au moment de la prédiction influence l'apprentissage ou l'évaluation. Exemple : utiliser une information obtenue après la sortie d'un patient pour prédire sa réadmission.

**Rattrapage obligatoire.**

---

## 13. Diagnostic
**Question :** Train accuracy = 99 %, Test accuracy = 68 %. Que suspectes-tu ?

**Ma réponse :** Pas de réponse.

**Évaluation : 🔴 Non maîtrisé / non répondu**

**Correction :** On suspecte fortement un **overfitting** : très bonne performance sur les données vues, mauvaise généralisation sur les données nouvelles.

**Rattrapage obligatoire.**

---

## 14. Pipeline ML
**Question :** Remettre dans l'ordre : définition du problème, collecte, séparation train/test, nettoyage/préparation, entraînement, prédictions, évaluation, déploiement.

**Ma réponse :** Pas de réponse.

**Évaluation : 🔴 Non maîtrisé / non répondu**

**Correction :**
1. Définition du problème
2. Collecte des données
3. Séparation train/test
4. Nettoyage / préparation
5. Entraînement
6. Prédictions
7. Évaluation
8. Déploiement

Le pipeline réel est itératif : après l'évaluation, on peut revenir modifier les données, features, modèle ou hyperparamètres.

**Rattrapage obligatoire.**

---

# État Semaine 1

## Maîtrisé
- Machine Learning
- Programmation classique vs ML
- Features / dataset (hors target)
- Training / inference
- Loss
- Overfitting
- Underfitting / overfitting

## Rattrapage à faire fin Semaine 2
1. Target
2. Non supervisé
3. Auto-supervisé
4. Paramètres vs hyperparamètres
5. Train / validation / test
6. Data snooping / fuite d'information
7. Data leakage
8. Diagnostic train/test
9. Pipeline ML

La Semaine 1 reste **non totalement validée** jusqu'au rattrapage.