# [Linux] Bash killall Utilisation : Terminer tous les processus d'un nom donné

## Overview
La commande `killall` est utilisée pour terminer tous les processus qui correspondent à un nom spécifique. Cela permet de gérer facilement plusieurs instances d'un programme sans avoir à identifier chaque processus individuellement.

## Usage
La syntaxe de base de la commande `killall` est la suivante :

```bash
killall [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `killall` :

- `-u <utilisateur>` : Terminer uniquement les processus appartenant à un utilisateur spécifique.
- `-i` : Demander confirmation avant de tuer chaque processus.
- `-q` : Ne pas afficher de messages d'erreur pour les processus qui n'existent pas.
- `-s <signal>` : Spécifier le signal à envoyer (par défaut, c'est SIGTERM).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `killall` :

1. Terminer tous les processus nommés `firefox` :
   ```bash
   killall firefox
   ```

2. Terminer tous les processus `gedit` en demandant une confirmation :
   ```bash
   killall -i gedit
   ```

3. Terminer tous les processus d'un utilisateur spécifique, par exemple `alice` :
   ```bash
   killall -u alice
   ```

4. Envoyer un signal spécifique, comme SIGKILL, à tous les processus `myapp` :
   ```bash
   killall -s SIGKILL myapp
   ```

## Tips
- Utilisez l'option `-q` pour éviter les messages d'erreur si vous essayez de tuer des processus qui ne sont pas en cours d'exécution.
- Soyez prudent avec `killall`, car il peut terminer plusieurs processus en une seule commande, ce qui peut entraîner une perte de données si des applications ne sont pas sauvegardées.
- Pour vérifier quels processus sont en cours d'exécution avant de les terminer, utilisez la commande `ps` ou `pgrep`.