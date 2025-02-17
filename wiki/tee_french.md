# [Linux] Bash tee Utilisation : Rediriger la sortie vers un fichier et l'afficher

## Overview
La commande `tee` est utilisée dans Bash pour lire l'entrée standard et écrire à la fois sur la sortie standard et dans un ou plusieurs fichiers. Cela permet de visualiser les données tout en les enregistrant simultanément.

## Usage
La syntaxe de base de la commande `tee` est la suivante :

```bash
tee [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `tee` :

- `-a` : Ajoute la sortie au fichier au lieu de le remplacer.
- `-i` : Ignore les signaux d'interruption.
- `-p` : Écrit la sortie dans le fichier tout en affichant les erreurs.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tee` :

1. **Écrire la sortie d'une commande dans un fichier :**
   ```bash
   echo "Bonjour, monde!" | tee fichier.txt
   ```

2. **Ajouter la sortie à un fichier existant :**
   ```bash
   echo "Nouvelle ligne" | tee -a fichier.txt
   ```

3. **Utiliser tee avec une commande :**
   ```bash
   ls -l | tee liste_fichiers.txt
   ```

4. **Écrire la sortie d'une commande dans plusieurs fichiers :**
   ```bash
   echo "Données importantes" | tee fichier1.txt fichier2.txt
   ```

## Tips
- Utilisez l'option `-a` si vous souhaitez conserver le contenu existant d'un fichier et y ajouter de nouvelles données.
- Combinez `tee` avec d'autres commandes pour créer des pipelines efficaces.
- Faites attention aux permissions des fichiers lorsque vous utilisez `tee`, surtout si vous écrivez dans des fichiers système ou protégés.