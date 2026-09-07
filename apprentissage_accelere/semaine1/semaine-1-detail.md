# Semaine 1 — Détail jour par jour
**Objectif de la semaine** : comprendre concrètement ce qui se passe quand un modèle "s'entraîne" — tensors, autograd, boucle d'entraînement — en codant tout toi-même, pas en copiant-collant.

Budget : ~7h sur la semaine (adapte selon tes 5-10h dispo). Découpage en 5 jours de ~1h15-1h30, mais libre à toi de fusionner des jours si ton emploi du temps est irrégulier.

Setup unique avant de commencer : Python + `torch` + `matplotlib` + `numpy` installés (Colab gratuit fonctionne très bien aussi, zéro install).

---

## Jour 1 — Tensors : le Lego de base (1h15)

**Théorie (20 min)**
Un tensor = un tableau de nombres à N dimensions (scalaire, vecteur, matrice, cube...). Tout ce qu'un réseau de neurones manipule — images, texte, audio, poids — est encodé en tensors. Regarde la doc rapide "Tensors" de PyTorch (les bases : création, shape, dtype, device).

**Exercice 1 — "Le détective de shapes" (20 min)**
Sans exécuter le code, prédis sur papier le `.shape` résultant de chaque opération, puis vérifie :
```python
import torch
a = torch.rand(3, 4)
b = torch.rand(4, 5)
c = a @ b                    # shape ?
d = a.unsqueeze(0)           # shape ?
e = a.T                      # shape ?
f = torch.cat([a, a], dim=0) # shape ?
g = a.view(2, 6)             # shape ?
```
C'est un jeu que tu peux rejouer chaque fois que tu es perdu plus tard : la plupart des bugs en deep learning sont des erreurs de shape.

**Exercice 2 — Image = tensor (25 min)**
Charge une image (une photo de ton choix) avec PIL, convertis-la en tensor, affiche son `.shape` (tu devrais voir channels × hauteur × largeur). Puis :
- Mets tous les pixels du canal rouge à 0 → réaffiche l'image
- Fais une transposition pour tourner l'image de 90° juste avec des opérations tensor (`torch.rot90` puis essaie de le refaire "à la main" avec `.transpose` et `.flip`)

**Exercice 3 bonus — GPU ou CPU ? (10 min)**
Crée deux grosses matrices aléatoires (2000x2000), multiplie-les, chronomètre sur CPU. Si tu as accès à un GPU (Colab gratuit), refais le test avec `.to("cuda")` et compare le temps. Premier contact concret avec "pourquoi on a besoin de GPU".

---

## Jour 2 — Autograd : la magie du calcul de gradient (1h15)

**Théorie (15 min)**
`requires_grad=True` + `.backward()` = PyTorch calcule automatiquement la dérivée de n'importe quelle fonction par rapport à n'importe quelle variable. C'est LE mécanisme qui permet à un modèle d'apprendre.

**Exercice 1 — Calculer un gradient à la main, puis avec autograd (25 min)**
Prends une fonction simple : `y = x**2 + 3*x`. Calcule à la main la dérivée en `x=2` (sur papier, 2 minutes de maths). Puis vérifie avec PyTorch :
```python
x = torch.tensor(2.0, requires_grad=True)
y = x**2 + 3*x
y.backward()
print(x.grad)  # doit matcher ton calcul manuel
```
Refais avec une fonction plus tordue de ton choix (ex : `sin(x) * x**3`) pour voir qu'autograd gère n'importe quoi.

**Exercice 2 — "Descends la montagne" : gradient descent à la main (30 min)**
Sans utiliser `torch.optim`, code une boucle de descente de gradient manuelle pour trouver le minimum de `f(x) = (x - 5)**2 + 3` en partant de `x = 0` :
```python
x = torch.tensor(0.0, requires_grad=True)
lr = 0.1
for step in range(50):
    y = (x - 5)**2 + 3
    y.backward()
    with torch.no_grad():
        x -= lr * x.grad
    x.grad.zero_()
    # affiche x et y tous les 10 steps
```
Joue avec le learning rate (`lr = 0.01`, puis `lr = 1.5`) et observe : convergence lente, ou divergence totale. Note ce que tu observes — c'est exactement le genre de bug que tu rencontreras en fine-tuning.

**Exercice 3 bonus — Visualisation (10 min)**
Utilise `matplotlib` pour tracer la courbe de `f(x)` et place un point à chaque étape de ta descente de gradient, pour *voir* la bille rouler vers le minimum.

---

## Jour 3 — Ton premier neurone, puis ton premier petit réseau (1h30)

**Théorie (15 min)**
Un neurone = `y = activation(w·x + b)`. Un réseau = plusieurs neurones empilés en couches. `nn.Linear` fait le `w·x + b` pour toi, `nn.Module` organise l'ensemble.

**Exercice 1 — Un seul neurone qui apprend une droite (25 min)**
Génère des données synthétiques bruitées suivant `y = 2x + 1 + bruit`. Crée un unique `nn.Linear(1, 1)`, entraîne-le à retrouver la pente (2) et l'ordonnée à l'origine (1) avec une boucle d'entraînement simple (loss MSE, `torch.optim.SGD`). Affiche les poids appris à la fin — sont-ils proches de 2 et 1 ?

**Exercice 2 — Le problème XOR : pourquoi il faut des couches cachées (35 min)**
Le classique qui fait vraiment comprendre pourquoi la profondeur compte. Données XOR :
```python
X = torch.tensor([[0.,0.], [0.,1.], [1.,0.], [1.,1.]])
Y = torch.tensor([[0.], [1.], [1.], [0.]])
```
1. Essaie d'abord avec UN seul `nn.Linear(2, 1)` + sigmoid → entraîne 500 steps → constate que ça ne converge jamais bien (le XOR n'est pas linéairement séparable)
2. Puis construit un petit MLP : `Linear(2,4) → ReLU → Linear(4,1) → Sigmoid` → entraîne → ça doit converger cette fois
3. Note dans un commentaire pourquoi, à ton avis, la version 2 fonctionne et pas la version 1

**Exercice 3 bonus — Visualise la frontière de décision (15 min)**
Pour ton MLP entraîné sur XOR, trace une grille 2D et colorie chaque point selon la prédiction du modèle. Tu devrais voir une frontière non-linéaire qui sépare correctement les 4 points.

---

## Jour 4 — Boucle d'entraînement complète sur un vrai dataset : MNIST (1h30)

**Théorie (10 min)**
MNIST = 70000 images de chiffres manuscrits (28x28 pixels). C'est le "hello world" du deep learning, mais le refaire toi-même sans copier-coller passif enseigne toute la mécanique : DataLoader, batchs, epochs, train/eval.

**Exercice 1 — Construire le pipeline complet (45 min)**
Étapes à coder toi-même (résiste à l'envie de copier un tutoriel entier — regarde la doc au fur et à mesure si bloqué) :
1. Charger MNIST via `torchvision.datasets.MNIST` + `DataLoader` (batch_size=64)
2. Définir un petit MLP : `Flatten → Linear(784,128) → ReLU → Linear(128,10)`
3. Boucle d'entraînement : 3 epochs, `CrossEntropyLoss`, `Adam`
4. Après chaque epoch, calcule l'accuracy sur le test set

**Exercice 2 — Casser volontairement ton modèle pour comprendre (20 min)**
Sur des copies de ton script, teste 3 "sabotages" et observe l'effet :
- Enlève le `ReLU` (garde juste 2 couches linéaires empilées) → que se passe-t-il sur l'accuracy ?
- Mets un learning rate énorme (`lr=10`) → observe la loss exploser
- Oublie `optimizer.zero_grad()` dans la boucle → observe le comportement bizarre

Comprendre *pourquoi* chaque sabotage casse l'entraînement est plus formateur que n'importe quel cours théorique.

**Exercice 3 bonus — Erreurs du modèle (15 min)**
Affiche 5 images que ton modèle a mal classées, avec la vraie étiquette et la prédiction. Est-ce que ce sont des chiffres ambigus même pour un humain ?

---

## Jour 5 — Consolidation : ton propre mini-projet (1h30)

Pas de nouvel exercice guidé aujourd'hui — c'est le jour où tu appliques seul, condition indispensable pour vérifier que tu as vraiment compris (pas juste suivi des instructions).

**Mini-projet libre (1h)**
Choisis UNE des options suivantes (ou invente la tienne) :
- **Option A** : entraîne ton MLP MNIST sur Fashion-MNIST (vêtements au lieu de chiffres) — dataset dispo directement dans `torchvision`, aucun changement de code nécessaire à part le nom du dataset
- **Option B** : ajoute une 3e couche cachée à ton MLP MNIST et compare l'accuracy avant/après
- **Option C** : entraîne ton modèle avec seulement 1000 images d'entraînement (au lieu de 60000) et observe l'overfitting (bonne accuracy sur train, mauvaise sur test)

**Bilan écrit (30 min)**
Rédige (dans un fichier texte ou un notebook, 10-15 lignes) tes réponses à :
1. Explique avec tes propres mots ce que fait `.backward()`
2. Pourquoi a-t-on besoin d'une fonction d'activation non-linéaire (ReLU, sigmoid) entre les couches ?
3. Quelle est la différence entre une epoch et un batch ?
4. Qu'est-ce que tu as trouvé le plus contre-intuitif cette semaine ?

Ce bilan n'est pas de la paperasse : le fait de reformuler avec tes mots est ce qui transforme une notion vue en une notion sue. Tu réutiliseras ce réflexe (mini-projet libre + bilan écrit) chaque fin de semaine du plan global.

---

## Livrable final de la semaine
Un notebook unique (ou dossier de scripts) contenant :
- Les exercices des jours 1 à 4
- Ton mini-projet du jour 5
- Ton bilan écrit de 4 questions

Garde ce notebook — semaine 3 tu le pousseras sur ton repo GitHub perso, qui deviendra ton portfolio au fil des 12 semaines.

## Si tu bloques
- Erreur de shape → reviens à l'exercice "détective de shapes" du jour 1, imprime `.shape` partout
- Loss qui ne descend pas → vérifie learning rate, vérifie que `optimizer.zero_grad()` est bien appelé
- Pas de GPU dispo pour les tests de vitesse → Google Colab (gratuit, GPU T4 inclus) suffit largement pour toute cette semaine
