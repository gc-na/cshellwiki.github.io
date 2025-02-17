# [Linux] Bash script utilisation : Enregistrer des sessions de terminal

## Overview
La commande `script` permet d'enregistrer une session de terminal dans un fichier. Cela peut être utile pour créer des journaux de commandes ou pour documenter des étapes spécifiques lors de l'utilisation de la ligne de commande.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
script [options] [arguments]
```

## Common Options
- `-a` : Ajoute la sortie à un fichier existant au lieu de le remplacer.
- `-c` : Exécute une commande spécifique et enregistre sa sortie.
- `-f` : Affiche la sortie en temps réel dans le terminal pendant l'enregistrement.
- `-q` : Exécute la commande en mode silencieux, sans afficher de messages d'état.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `script` :

1. **Enregistrer une session dans un fichier :**
   ```bash
   script session.txt
   ```
   Cela démarre l'enregistrement de la session dans le fichier `session.txt`.

2. **Ajouter à un fichier existant :**
   ```bash
   script -a session.txt
   ```
   Cela ajoute la nouvelle session à `session.txt` sans écraser le contenu précédent.

3. **Exécuter une commande et enregistrer sa sortie :**
   ```bash
   script -c "ls -l" output.txt
   ```
   Cela exécute la commande `ls -l` et enregistre la sortie dans `output.txt`.

4. **Enregistrer une session en temps réel :**
   ```bash
   script -f session.txt
   ```
   Cela enregistre la session dans `session.txt` tout en affichant la sortie en temps réel.

## Tips
- Utilisez l'option `-q` si vous souhaitez éviter les messages de statut pendant l'enregistrement.
- Pensez à utiliser `-a` si vous voulez conserver un historique de plusieurs sessions dans un même fichier.
- N'oubliez pas de terminer la session d'enregistrement en tapant `exit` ou en utilisant `Ctrl+D`.