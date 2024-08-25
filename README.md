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
