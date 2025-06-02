# 🌱 Exercices Git & GitHub – Niveau Débutant (Front-End)

Ce dépôt contient une série d'exercices pratiques pour apprendre à utiliser **Git** et **GitHub** dans un projet front-end.

---

## ✅ Prérequis
- Avoir Git installé
- Avoir un compte GitHub
- Avoir un éditeur de code (comme VS Code)

---

## 🧩 Exercice 1 – Initialiser un projet Git localement

1. Crée un dossier `mon-premier-projet`.

2. Initialise Git :
   ```bash
   git init
   ```

3. Crée un fichier `index.html` avec un squelette HTML.

4. Vérifie l’état :

   ```bash
   git status
   ```
5. Ajoute tous les fichiers :

   ```bash
   git add .
   ```
6. Fais un premier commit :

   ```bash
   git commit -m "Initial commit avec fichier HTML"
   ```

---

## 🧩 Exercice 2 – Se connecter à GitHub

1. Crée un dépôt vide sur GitHub.
2. Ajoute le dépôt distant :

   ```bash
   git remote add origin https://github.com/ton-utilisateur/mon-premier-projet.git
   ```
3. Envoie les fichiers :

   ```bash
   git push -u origin main
   ```

---

## 🧩 Exercice 3 – Modification et nouveaux commits

1. Ajoute `style.css` et un `<h1>` dans `index.html`.
2. Ajoute, commit et push :

   ```bash
   git add .
   git commit -m "Ajout du style et d’un titre"
   git push
   ```

---

## 🧩 Exercice 4 – Gérer les branches

1. Crée une branche :

   ```bash
   git checkout -b ajout-navbar
   ```
2. Ajoute une navbar dans `index.html` et commit.
3. Reviens sur `main` :

   ```bash
   git checkout main
   ```
4. Fusionne la branche :

   ```bash
   git merge ajout-navbar
   git push
   ```

---

## 🧩 Exercice 5 – Travailler avec les Pull Requests

1. Forke un dépôt sur GitHub.
2. Clone ton fork :

   ```bash
   git clone https://github.com/ton-utilisateur/depot-forke.git
   ```
3. Crée une branche `ajout-footer`, fais un commit.
4. Push la branche :

   ```bash
   git push origin ajout-footer
   ```
5. Crée une **Pull Request** via GitHub.

---

## 💡 Bonus : Collaboration et gestion de conflits

### 🧪 Mise en situation : travail en parallèle

Dans le fichier `index.html`, vous verrez une ligne comme celle-ci :

```html
<h1>Ceci est le fichier HTML de : [Prénom Nom]</h1>
```

Chaque apprenant doit remplacer `[Prénom Nom]` par son **propre nom et prénom**.

Ensuite :

1. Crée une branche :

   ```bash
   git checkout -b modification-nom
   ```
2. Modifie la ligne avec ton propre nom et fais un commit.
3. Reviens sur `main`, modifie aussi ce fichier (par exemple en changeant ton nom encore une fois).
4. Tente une fusion :

   ```bash
   git merge modification-nom
   ```

Git pourrait détecter un **conflit**. Résous-le en gardant la version correcte, puis :

```bash
git add .
git commit -m "Résolution de conflit dans index.html"
```

---

### 🚀 Pour aller plus loin (niveau avancé)

* Crée plusieurs branches (`ajout-navbar`, `ajout-footer`, `refacto-css`) et travaille dessus en parallèle.
* Utilise `git stash` pour mettre ton travail temporairement de côté :

  ```bash
  git stash
  git stash pop
  ```
* Visualise l'historique sous forme de graphe :

  ```bash
  git log --oneline --graph --all
  ```
* Explore un ancien commit :

  ```bash
  git checkout <id_du_commit>
  git switch main
  ```

💭 **Conseil** : pour simuler une vraie collaboration, faites cet exercice à deux, en modifiant la même ligne sur vos propres branches avant de faire une Pull Request.

---

**Bon apprentissage !**
