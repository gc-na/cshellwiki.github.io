# [Linux] Bash unsetopt : Désactiver des options de shell

## Overview
La commande `unsetopt` est utilisée dans les shells compatibles avec `zsh` pour désactiver certaines options qui modifient le comportement du shell. Cela permet aux utilisateurs de personnaliser leur environnement de travail selon leurs besoins.

## Usage
La syntaxe de base de la commande `unsetopt` est la suivante :

```bash
unsetopt [options]
```

## Common Options
Voici quelques options courantes que vous pouvez désactiver avec `unsetopt` :

- `allexport` : Désactive l'exportation automatique des variables.
- `braceexpand` : Désactive l'expansion des accolades.
- `emacs` : Désactive le mode d'édition de ligne Emacs.
- `noclobber` : Permet d'écraser des fichiers existants lors de la redirection.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `unsetopt` :

1. Désactiver l'exportation automatique des variables :

   ```bash
   unsetopt allexport
   ```

2. Désactiver l'expansion des accolades :

   ```bash
   unsetopt braceexpand
   ```

3. Désactiver le mode d'édition de ligne Emacs :

   ```bash
   unsetopt emacs
   ```

4. Permettre d'écraser des fichiers existants :

   ```bash
   unsetopt noclobber
   ```

## Tips
- Vérifiez toujours les options actuellement activées avec `set` avant de désactiver une option pour éviter des comportements inattendus.
- Utilisez `setopt` pour activer à nouveau une option si nécessaire.
- Pensez à ajouter vos commandes `unsetopt` dans votre fichier de configuration `.zshrc` pour qu'elles soient appliquées à chaque démarrage de votre shell.