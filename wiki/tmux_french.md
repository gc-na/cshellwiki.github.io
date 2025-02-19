# [Linux] C Shell (csh) tmux : Gestion des sessions terminal

## Overview
La commande `tmux` est un multiplexeur de terminal qui permet de créer, gérer et naviguer entre plusieurs sessions de terminal dans une seule fenêtre. Cela facilite le travail sur plusieurs tâches simultanément sans avoir à ouvrir plusieurs fenêtres de terminal.

## Usage
La syntaxe de base de la commande `tmux` est la suivante :

```bash
tmux [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `tmux` :

- `new`: Crée une nouvelle session tmux.
- `attach`: Attache une session existante.
- `list-sessions`: Liste toutes les sessions tmux en cours.
- `kill-session`: Termine une session tmux spécifiée.
- `detach`: Détache la session actuelle.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tmux` :

1. **Créer une nouvelle session tmux :**
   ```bash
   tmux new -s ma_session
   ```

2. **Attacher une session existante :**
   ```bash
   tmux attach -t ma_session
   ```

3. **Lister toutes les sessions :**
   ```bash
   tmux list-sessions
   ```

4. **Détacher la session actuelle :**
   ```bash
   Ctrl + b, d
   ```

5. **Terminer une session spécifique :**
   ```bash
   tmux kill-session -t ma_session
   ```

## Tips
- Utilisez des noms de session descriptifs pour faciliter la gestion de plusieurs sessions.
- Familiarisez-vous avec les raccourcis clavier de tmux pour améliorer votre efficacité.
- Pensez à sauvegarder votre travail avant de détacher ou de fermer une session pour éviter toute perte de données.