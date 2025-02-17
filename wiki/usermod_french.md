# [Linux] Bash usermod : Gérer les utilisateurs

## Overview
La commande `usermod` est utilisée pour modifier les comptes d'utilisateurs sur un système Linux. Elle permet d'ajuster divers paramètres d'un utilisateur, tels que le groupe, le nom, le répertoire personnel, et bien plus encore.

## Usage
La syntaxe de base de la commande `usermod` est la suivante :

```bash
usermod [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `usermod` :

- `-aG` : Ajoute l'utilisateur à un ou plusieurs groupes supplémentaires sans le retirer des groupes existants.
- `-d` : Change le répertoire personnel de l'utilisateur.
- `-l` : Modifie le nom de l'utilisateur.
- `-s` : Change le shell par défaut de l'utilisateur.
- `-u` : Change l'UID de l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `usermod` :

1. **Ajouter un utilisateur à un groupe** :
   ```bash
   usermod -aG sudo nom_utilisateur
   ```
   Cet exemple ajoute `nom_utilisateur` au groupe `sudo`, lui permettant d'exécuter des commandes avec des privilèges élevés.

2. **Changer le répertoire personnel d'un utilisateur** :
   ```bash
   usermod -d /nouveau/chemin nom_utilisateur
   ```
   Cela modifie le répertoire personnel de `nom_utilisateur` vers `/nouveau/chemin`.

3. **Modifier le nom d'un utilisateur** :
   ```bash
   usermod -l nouveau_nom ancien_nom
   ```
   Cet exemple change le nom d'utilisateur de `ancien_nom` à `nouveau_nom`.

4. **Changer le shell par défaut d'un utilisateur** :
   ```bash
   usermod -s /bin/zsh nom_utilisateur
   ```
   Cela définit le shell par défaut de `nom_utilisateur` à Zsh.

## Tips
- Toujours faire une sauvegarde des fichiers de configuration avant de modifier les comptes d'utilisateurs.
- Utiliser `usermod` avec précaution, surtout lors du changement de l'UID ou du nom d'utilisateur, car cela peut affecter les permissions des fichiers.
- Vérifiez les groupes d'un utilisateur après modification avec la commande `groups nom_utilisateur` pour vous assurer que les changements ont été appliqués correctement.