# [Linux] Bash logout : Déconnexion de la session

## Overview
La commande `logout` est utilisée dans les environnements de terminal pour terminer une session de shell. Elle permet à l'utilisateur de se déconnecter proprement d'une session interactive, que ce soit dans un terminal local ou à distance.

## Usage
La syntaxe de base de la commande `logout` est la suivante :

```bash
logout [options]
```

## Common Options
La commande `logout` ne dispose pas de nombreuses options, mais voici quelques points à considérer :

- `-f` : Force la déconnexion sans demander de confirmation.
- `-n` : Ne pas exécuter les scripts de déconnexion.

## Common Examples

### Exemple 1 : Déconnexion simple
Pour se déconnecter d'une session de terminal, il suffit de taper :

```bash
logout
```

### Exemple 2 : Déconnexion forcée
Si vous souhaitez vous déconnecter sans confirmation, utilisez l'option `-f` :

```bash
logout -f
```

### Exemple 3 : Déconnexion sans exécuter les scripts
Pour vous déconnecter sans exécuter les scripts de déconnexion, utilisez l'option `-n` :

```bash
logout -n
```

## Tips
- Assurez-vous d'avoir enregistré tout votre travail avant de taper `logout`, car cela fermera votre session.
- Utilisez `exit` comme alternative à `logout` dans les shells non interactifs ou dans des scripts.
- Si vous êtes connecté à distance, vérifiez que vous n'avez pas de processus en cours d'exécution qui pourraient être affectés par la déconnexion.