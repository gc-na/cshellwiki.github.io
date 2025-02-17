# [Linux] Bash vigr Usage : Éditeur de fichiers de configuration des utilisateurs

## Overview
La commande `vigr` est un éditeur de texte spécialisé pour modifier les fichiers de configuration des utilisateurs, tels que `/etc/passwd` et `/etc/group`. Elle est conçue pour éviter les erreurs de syntaxe en verrouillant le fichier pendant l'édition et en vérifiant la validité du fichier avant de le sauvegarder.

## Usage
La syntaxe de base de la commande `vigr` est la suivante :

```bash
vigr [options] [fichier]
```

## Common Options
- `-c` : Vérifie la syntaxe du fichier après modification.
- `-s` : Affiche le fichier dans un format sécurisé.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `vigr` :

1. **Éditer le fichier `/etc/passwd` :**
   ```bash
   sudo vigr /etc/passwd
   ```

2. **Éditer le fichier `/etc/group` :**
   ```bash
   sudo vigr /etc/group
   ```

3. **Vérifier la syntaxe après modification :**
   ```bash
   sudo vigr -c /etc/passwd
   ```

4. **Utiliser l'option sécurisée :**
   ```bash
   sudo vigr -s /etc/group
   ```

## Tips
- Toujours utiliser `sudo` pour éditer des fichiers système afin d'avoir les permissions nécessaires.
- Vérifiez toujours la syntaxe du fichier après modification avec l'option `-c` pour éviter des erreurs de configuration.
- Familiarisez-vous avec les commandes de l'éditeur de texte utilisé par `vigr`, généralement `vi` ou `vim`, pour une édition efficace.