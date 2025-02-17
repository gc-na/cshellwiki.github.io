# [Linux] Bash screen utilisation : Gestion des sessions terminal

## Overview
La commande `screen` permet de créer des sessions terminal virtuelles qui peuvent être détachées et réattachées. Cela est particulièrement utile pour exécuter des programmes à long terme ou pour gérer plusieurs sessions dans un seul terminal.

## Usage
La syntaxe de base de la commande `screen` est la suivante :

```bash
screen [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `screen` :

- `-S <nom>` : Crée une nouvelle session avec le nom spécifié.
- `-d -r <nom>` : Détache et réattache une session existante avec le nom spécifié.
- `-list` : Affiche la liste des sessions `screen` en cours.
- `-X <commande>` : Envoie une commande à une session `screen` existante.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `screen` :

1. **Créer une nouvelle session `screen` :**
   ```bash
   screen -S ma_session
   ```

2. **Détacher une session :**
   Pour détacher la session en cours, appuyez sur `Ctrl + A`, puis `D`.

3. **Lister les sessions `screen` en cours :**
   ```bash
   screen -list
   ```

4. **Réattacher une session détachée :**
   ```bash
   screen -r ma_session
   ```

5. **Envoyer une commande à une session `screen` :**
   ```bash
   screen -S ma_session -X quit
   ```

## Tips
- Utilisez des noms de session significatifs pour faciliter la gestion de plusieurs sessions.
- N'oubliez pas que vous pouvez détacher une session à tout moment, ce qui vous permet de continuer à travailler sur d'autres tâches.
- Pour quitter complètement une session `screen`, tapez `exit` dans la session ou utilisez `Ctrl + D`.