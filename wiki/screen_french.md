# [Linux] C Shell (csh) screen : Gérer des sessions de terminal

## Overview
La commande `screen` permet de créer des sessions de terminal détachées, ce qui signifie que vous pouvez exécuter des programmes dans un terminal et les laisser fonctionner même si vous vous déconnectez. Cela est particulièrement utile pour les tâches de longue durée ou pour travailler sur des serveurs distants.

## Usage
La syntaxe de base de la commande `screen` est la suivante :

```bash
screen [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `screen` :

- `-S <nom>` : Crée une nouvelle session avec le nom spécifié.
- `-d -r <nom>` : Détache une session et la rattache à votre terminal.
- `-list` : Affiche la liste des sessions `screen` en cours d'exécution.
- `-h <nombre>` : Définit le nombre de lignes d'historique à conserver.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `screen` :

1. **Créer une nouvelle session :**
   ```bash
   screen -S ma_session
   ```

2. **Détacher une session :**
   Pour détacher une session en cours, appuyez sur `Ctrl-a` puis `d`.

3. **Lister les sessions actives :**
   ```bash
   screen -list
   ```

4. **Rattacher une session détachée :**
   ```bash
   screen -r ma_session
   ```

5. **Créer une session avec un historique de 1000 lignes :**
   ```bash
   screen -h 1000
   ```

## Tips
- Utilisez des noms de session descriptifs pour faciliter la gestion de plusieurs sessions.
- N'oubliez pas d'utiliser `Ctrl-a` suivi de `?` pour afficher l'aide des commandes de `screen`.
- Pour quitter une session `screen`, tapez `exit` dans le terminal de la session ou détachez-la et fermez le terminal principal.