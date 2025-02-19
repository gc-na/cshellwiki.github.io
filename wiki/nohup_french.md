# [Linux] C Shell (csh) nohup : Exécuter des commandes sans interruption

## Overview
La commande `nohup` (no hang up) permet d'exécuter des processus en arrière-plan, même si la session de terminal est fermée. Cela signifie que les commandes lancées avec `nohup` continueront à s'exécuter indépendamment de la connexion de l'utilisateur.

## Usage
La syntaxe de base de la commande `nohup` est la suivante :

```csh
nohup [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `nohup` :

- `&` : Exécute la commande en arrière-plan.
- `-o` : Permet de spécifier un fichier de sortie pour les messages.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `nohup` :

1. Exécuter un script en arrière-plan :
   ```csh
   nohup ./mon_script.sh &
   ```

2. Exécuter une commande avec redirection de la sortie :
   ```csh
   nohup ls -l > sortie.txt &
   ```

3. Exécuter un programme long sans interruption :
   ```csh
   nohup python mon_programme.py &
   ```

## Tips
- Utilisez `&` pour vous assurer que la commande s'exécute en arrière-plan.
- Vérifiez le fichier `nohup.out` pour les messages de sortie si vous n'avez pas redirigé la sortie.
- Pensez à utiliser des gestionnaires de processus comme `screen` ou `tmux` pour une gestion plus avancée des sessions.