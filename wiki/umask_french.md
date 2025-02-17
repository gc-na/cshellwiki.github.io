# [Linux] Bash umask Utilisation : Gérer les permissions par défaut des fichiers

## Overview
La commande `umask` est utilisée pour définir les permissions par défaut des fichiers et des répertoires créés par un utilisateur. Elle détermine les permissions qui ne seront pas attribuées lors de la création de nouveaux fichiers.

## Usage
La syntaxe de base de la commande `umask` est la suivante :

```bash
umask [options] [arguments]
```

## Common Options
- `-S` : Affiche les permissions sous forme symbolique.
- `-p` : Affiche la valeur actuelle de umask dans un format qui peut être utilisé dans le script.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `umask` :

1. **Afficher la valeur actuelle de umask :**
   ```bash
   umask
   ```

2. **Définir umask pour interdire l'écriture pour le groupe et les autres :**
   ```bash
   umask 022
   ```

3. **Définir umask pour interdire toutes les permissions pour le groupe et les autres :**
   ```bash
   umask 077
   ```

4. **Afficher les permissions sous forme symbolique :**
   ```bash
   umask -S
   ```

## Tips
- Vérifiez régulièrement la valeur de umask pour vous assurer que les fichiers créés ont les bonnes permissions.
- Utilisez des valeurs de umask plus restrictives (comme 077) pour des fichiers sensibles.
- N'oubliez pas que la valeur de umask est appliquée à chaque nouvelle session, donc il peut être utile de la définir dans votre fichier de configuration de shell (comme `.bashrc`).