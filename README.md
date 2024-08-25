---

## Cours Complet sur Git

### Introduction

Git est un système de contrôle de version décentralisé qui permet de suivre les modifications apportées aux fichiers et de collaborer efficacement avec d'autres développeurs. Git est très utilisé dans le développement logiciel pour gérer les versions du code source.

### Table des Matières

1. [Commandes de Base de Git](#commandes-de-base-de-git)
2. [Tableau Récapitulatif des Commandes](#tableau-récapitulatif-des-commandes)
3. [Exemple End-to-End sur Git et GitHub](#exemple-end-to-end-sur-git-et-github)

---

### Commandes de Base de Git

#### 1. `git init`

**Description :** Initialise un nouveau dépôt Git.

**Syntaxe :**
```bash
git init [chemin]
```

**Exemple :**
```bash
mkdir mon_projet
cd mon_projet
git init
```
Ce commande crée un nouveau dépôt Git dans le répertoire `mon_projet`.

#### 2. `git clone`

**Description :** Clone un dépôt distant sur votre machine locale.

**Syntaxe :**
```bash
git clone [url]
```

**Exemple :**
```bash
git clone https://github.com/mon_utilisateur/mon_repertoire.git
```
Cela crée une copie locale du dépôt `mon_repertoire`.

#### 3. `git status`

**Description :** Affiche l'état des fichiers dans le répertoire de travail.

**Syntaxe :**
```bash
git status
```

**Exemple :**
```bash
git status
```
Affiche les fichiers modifiés, les fichiers en attente de validation, etc.

#### 4. `git add`

**Description :** Ajoute des fichiers au stage (préparation pour commit).

**Syntaxe :**
```bash
git add [fichier]
```

**Exemple :**
```bash
git add index.html
```
Ajoute `index.html` à l'index pour le prochain commit.

#### 5. `git pull`

**Description :** Récupère et fusionne les modifications d'un dépôt distant.

**Syntaxe :**
```bash
git pull [origine] [branche]
```

**Exemple :**
```bash
git pull origin main
```
Récupère les modifications de la branche `main` du dépôt distant `origin`.

#### 6. `git branch`

**Description :** Liste, crée ou supprime des branches.

**Syntaxe :**
```bash
git branch [nom_br]
```

**Exemple :**
```bash
git branch feature/nouvelle-fonction
```
Crée une nouvelle branche appelée `feature/nouvelle-fonction`.

#### 7. `git checkout`

**Description :** Change de branche ou restaure des fichiers.

**Syntaxe :**
```bash
git checkout [branche]
```

**Exemple :**
```bash
git checkout feature/nouvelle-fonction
```
Bascule vers la branche `feature/nouvelle-fonction`.

#### 8. `git commit`

**Description :** Enregistre les modifications dans l'historique du dépôt.

**Syntaxe :**
```bash
git commit -m "Message de commit"
```

**Exemple :**
```bash
git commit -m "Ajout de la page d'accueil"
```
Crée un commit avec le message `Ajout de la page d'accueil`.

#### 9. `git merge`

**Description :** Fusionne les modifications d'une branche dans la branche courante.

**Syntaxe :**
```bash
git merge [branche]
```

**Exemple :**
```bash
git merge feature/nouvelle-fonction
```
Fusionne la branche `feature/nouvelle-fonction` dans la branche courante.

#### 10. `git log`

**Description :** Affiche l'historique des commits.

**Syntaxe :**
```bash
git log
```

**Exemple :**
```bash
git log
```
Affiche les commits précédents avec leurs messages, auteurs, et dates.

#### 11. `git reset`

**Description :** Réinitialise l'index ou les modifications de commit.

**Syntaxe :**
```bash
git reset [options]
```

**Exemple :**
```bash
git reset HEAD~1
```
Annule le dernier commit, mais conserve les modifications dans le répertoire de travail.

#### 12. `git push`

**Description :** Envoie les commits locaux vers un dépôt distant.

**Syntaxe :**
```bash
git push [origine] [branche]
```

**Exemple :**
```bash
git push origin main
```
Envoie les commits de la branche `main` au dépôt distant `origin`.

---

### Tableau Récapitulatif des Commandes

| Commande     | Description                                           | Syntaxe                         | Exemple                             |
|--------------|-------------------------------------------------------|---------------------------------|-------------------------------------|
| `git init`   | Initialise un dépôt Git                              | `git init [chemin]`              | `git init`                           |
| `git clone`  | Clone un dépôt distant                               | `git clone [url]`                | `git clone https://github.com/...`   |
| `git status` | Affiche l'état des fichiers                          | `git status`                     | `git status`                         |
| `git add`    | Ajoute des fichiers au stage                         | `git add [fichier]`              | `git add index.html`                 |
| `git pull`   | Récupère et fusionne les modifications                | `git pull [origine] [branche]`   | `git pull origin main`               |
| `git branch` | Liste, crée ou supprime des branches                 | `git branch [nom_br]`            | `git branch feature/nouvelle-fonction` |
| `git checkout`| Change de branche ou restaure des fichiers           | `git checkout [branche]`         | `git checkout feature/nouvelle-fonction` |
| `git commit` | Enregistre les modifications dans l'historique       | `git commit -m "Message"`        | `git commit -m "Ajout de la page d'accueil"` |
| `git merge`  | Fusionne les modifications d'une branche             | `git merge [branche]`            | `git merge feature/nouvelle-fonction` |
| `git log`    | Affiche l'historique des commits                     | `git log`                        | `git log`                            |
| `git reset`  | Réinitialise l'index ou les modifications de commit  | `git reset [options]`            | `git reset HEAD~1`                   |
| `git push`   | Envoie les commits locaux vers un dépôt distant      | `git push [origine] [branche]`   | `git push origin main`               |

---

### Exemple End-to-End sur Git et GitHub

#### Scénario : Création d'un Projet, Collaboration et Déploiement

1. **Initialisation du Projet :**

   ```bash
   mkdir mon_projet
   cd mon_projet
   git init
   ```

2. **Création du Fichier Initial :**

   ```bash
   echo "# Mon Projet" > README.md
   git add README.md
   git commit -m "Initial commit avec README"
   ```

3. **Création d'un Dépôt sur GitHub :**

   - Allez sur [GitHub](https://github.com) et créez un nouveau dépôt nommé `mon_projet`.
   - Notez l'URL du dépôt (`https://github.com/mon_utilisateur/mon_projet.git`).

4. **Ajout du Dépôt Distant et Push Initial :**

   ```bash
   git remote add origin https://github.com/mon_utilisateur/mon_projet.git
   git push -u origin main
   ```

5. **Création d'une Nouvelle Branche :**

   ```bash
   git branch feature/nouvelle-fonction
   git checkout feature/nouvelle-fonction
   ```

6. **Ajout de Fonctionnalités sur la Nouvelle Branche :**

   ```bash
   echo "Nouvelle fonctionnalité ajoutée" > fonctionnalite.txt
   git add fonctionnalite.txt
   git commit -m "Ajout de la nouvelle fonctionnalité"
   ```

7. **Fusion de la Branche dans Main :**

   ```bash
   git checkout main
   git merge feature/nouvelle-fonction
   ```

8. **Push des Modifications vers GitHub :**

   ```bash
   git push origin main
   ```

9. **Gestion des Modifications :**

   - Modifiez un fichier existant.
   - Utilisez `git status` pour voir les changements.
   - Utilisez `git add`, `git commit`, et `git push` pour enregistrer et partager les modifications.

10. **Consulter l'Historique :**

    ```bash
    git log
    ```

---

Ce cours couvre les commandes de base de Git et fournit un exemple pratique de gestion d'un projet avec Git et GitHub. Pour approfondir vos connaissances, explorez les fonctionnalités avancées telles que les rebases, les stashes, et les hooks Git. N'hésitez pas à me demander plus d'informations si nécessaire !

Bien sûr, continuons avec les commandes Git supplémentaires, de 11 à 20, avec des explications détaillées, des exemples, et un tableau récapitulatif.

---

### Commandes Avancées de Git

#### 11. `git tag`

**Description :** Crée, liste ou supprime des tags. Les tags sont souvent utilisés pour marquer des versions spécifiques de votre projet.

**Syntaxe :**
```bash
git tag [nom_tag] [commit]
```

**Exemple :**
```bash
git tag v1.0.0
```
Crée un tag `v1.0.0` sur le commit courant.

#### 12. `git stash`

**Description :** Met de côté les modifications en cours pour une utilisation ultérieure. Utile pour passer à une autre branche sans valider les modifications actuelles.

**Syntaxe :**
```bash
git stash [options]
```

**Exemple :**
```bash
git stash
```
Sauvegarde les modifications non validées dans un stash.

#### 13. `git fetch`

**Description :** Récupère les modifications du dépôt distant sans les fusionner avec la branche courante.

**Syntaxe :**
```bash
git fetch [origine]
```

**Exemple :**
```bash
git fetch origin
```
Récupère les mises à jour depuis le dépôt distant `origin`.

#### 14. `git rebase`

**Description :** Rejoue les commits d'une branche sur une autre branche. Utile pour maintenir un historique linéaire.

**Syntaxe :**
```bash
git rebase [branche]
```

**Exemple :**
```bash
git rebase main
```
Rejoue les commits de la branche courante sur la branche `main`.

#### 15. `git diff`

**Description :** Affiche les différences entre les versions de fichiers ou les commits.

**Syntaxe :**
```bash
git diff [options] [commit1] [commit2]
```

**Exemple :**
```bash
git diff HEAD~1
```
Affiche les différences entre le dernier commit et l'état actuel des fichiers.

#### 16. `git remote`

**Description :** Gère les dépôts distants. Vous pouvez ajouter, supprimer, ou modifier des dépôts distants.

**Syntaxe :**
```bash
git remote [options] [nom_distant] [url]
```

**Exemple :**
```bash
git remote add upstream https://github.com/quelquun/quelque_repertoire.git
```
Ajoute un dépôt distant nommé `upstream`.

#### 17. `git cherry-pick`

**Description :** Applique un commit spécifique d'une autre branche à la branche courante.

**Syntaxe :**
```bash
git cherry-pick [commit]
```

**Exemple :**
```bash
git cherry-pick 1a2b3c4d
```
Applique le commit avec l'ID `1a2b3c4d` à la branche courante.

#### 18. `git rm`

**Description :** Supprime des fichiers du répertoire de travail et de l'index.

**Syntaxe :**
```bash
git rm [fichier]
```

**Exemple :**
```bash
git rm fichier_a_supprimer.txt
```
Supprime `fichier_a_supprimer.txt` du répertoire de travail et de l'index.

#### 19. `git config`

**Description :** Configure les options Git, telles que les informations utilisateur et les préférences de comportement.

**Syntaxe :**
```bash
git config [options] [clé] [valeur]
```

**Exemple :**
```bash
git config --global user.name "Votre Nom"
```
Définit le nom d'utilisateur global pour les commits.

#### 20. `git blame`

**Description :** Affiche qui a modifié chaque ligne d'un fichier et dans quel commit.

**Syntaxe :**
```bash
git blame [fichier]
```

**Exemple :**
```bash
git blame index.html
```
Affiche l'auteur et le commit pour chaque ligne du fichier `index.html`.

---

### Tableau Récapitulatif des Commandes Avancées

| Commande       | Description                                           | Syntaxe                         | Exemple                                           |
|----------------|-------------------------------------------------------|---------------------------------|---------------------------------------------------|
| `git tag`      | Crée, liste ou supprime des tags                     | `git tag [nom_tag] [commit]`     | `git tag v1.0.0`                                 |
| `git stash`    | Met de côté les modifications en cours               | `git stash [options]`            | `git stash`                                      |
| `git fetch`    | Récupère les modifications du dépôt distant           | `git fetch [origine]`            | `git fetch origin`                              |
| `git rebase`   | Rejoue les commits d'une branche sur une autre       | `git rebase [branche]`           | `git rebase main`                               |
| `git diff`     | Affiche les différences entre les versions           | `git diff [options] [commit1] [commit2]` | `git diff HEAD~1`                                |
| `git remote`   | Gère les dépôts distants                              | `git remote [options] [nom_distant] [url]` | `git remote add upstream https://github.com/...` |
| `git cherry-pick`| Applique un commit spécifique d'une autre branche    | `git cherry-pick [commit]`       | `git cherry-pick 1a2b3c4d`                       |
| `git rm`       | Supprime des fichiers du répertoire de travail et de l'index | `git rm [fichier]`               | `git rm fichier_a_supprimer.txt`                 |
| `git config`   | Configure les options Git                            | `git config [options] [clé] [valeur]` | `git config --global user.name "Votre Nom"`      |
| `git blame`    | Affiche qui a modifié chaque ligne d'un fichier       | `git blame [fichier]`            | `git blame index.html
