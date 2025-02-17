# [Linux] Bash tmux utilisation : Gestion de sessions terminal

## Overview
Le commandement `tmux` est un multiplexeur de terminal qui permet de gérer plusieurs sessions de terminal dans une seule fenêtre. Il est particulièrement utile pour les utilisateurs qui souhaitent exécuter plusieurs tâches simultanément ou maintenir des sessions actives sur un serveur distant.

## Usage
La syntaxe de base de la commande `tmux` est la suivante :

```bash
tmux [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `tmux` :

- `new` : Crée une nouvelle session.
- `attach` : Attache une session existante.
- `list-sessions` : Liste toutes les sessions tmux en cours.
- `kill-session` : Termine une session spécifiée.
- `detach` : Détache la session active.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tmux` :

### Créer une nouvelle session
```bash
tmux new -s ma_session
```

### Attacher une session existante
```bash
tmux attach -t ma_session
```

### Lister toutes les sessions
```bash
tmux list-sessions
```

### Détacher la session active
```bash
Ctrl + b puis d
```

### Tuer une session spécifique
```bash
tmux kill-session -t ma_session
```

## Tips
- Utilisez des noms de session significatifs pour faciliter la gestion de plusieurs sessions.
- Familiarisez-vous avec les raccourcis clavier de tmux pour naviguer rapidement entre les fenêtres et les panneaux.
- Pensez à sauvegarder vos sessions pour éviter de perdre votre travail en cas de déconnexion.