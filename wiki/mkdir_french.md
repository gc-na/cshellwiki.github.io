# [Linux] Bash mkdir Utilisation : Créer des répertoires

## Overview
La commande `mkdir` est utilisée pour créer de nouveaux répertoires dans le système de fichiers. Elle permet aux utilisateurs d'organiser leurs fichiers en créant des dossiers selon leurs besoins.

## Usage
La syntaxe de base de la commande `mkdir` est la suivante :

```bash
mkdir [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mkdir` :

- `-p` : Crée des répertoires parents si nécessaire. Par exemple, si le répertoire parent n'existe pas, il sera créé.
- `-v` : Affiche un message pour chaque répertoire créé, ce qui peut être utile pour le débogage.
- `-m` : Définit les permissions du répertoire créé, en utilisant une notation octale.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mkdir` :

1. **Créer un répertoire simple :**

   ```bash
   mkdir mon_dossier
   ```

2. **Créer plusieurs répertoires à la fois :**

   ```bash
   mkdir dossier1 dossier2 dossier3
   ```

3. **Créer un répertoire avec des répertoires parents :**

   ```bash
   mkdir -p parent/enfant
   ```

4. **Créer un répertoire avec des permissions spécifiques :**

   ```bash
   mkdir -m 755 mon_dossier
   ```

5. **Créer un répertoire et afficher un message :**

   ```bash
   mkdir -v mon_dossier
   ```

## Tips
- Utilisez l'option `-p` pour éviter les erreurs lorsque vous essayez de créer un répertoire dans un chemin où certains répertoires parents n'existent pas.
- Pensez à vérifier les permissions de votre répertoire après sa création, surtout si vous utilisez l'option `-m`.
- Utilisez l'option `-v` pour avoir un retour visuel sur ce que vous créez, ce qui peut être utile lors de la création de plusieurs répertoires.