# [Linux] C Shell (csh) dirname : [obtenir le nom de répertoire d'un chemin]

## Overview
La commande `dirname` est utilisée pour extraire le nom du répertoire d'un chemin donné. Elle renvoie la partie du chemin qui précède le dernier séparateur de répertoire, permettant ainsi d'isoler le répertoire parent d'un fichier ou d'un autre répertoire.

## Usage
La syntaxe de base de la commande `dirname` est la suivante :

```csh
dirname [options] [arguments]
```

## Common Options
- `-z` : Traite les chemins vides comme des chemins valides.
- `--help` : Affiche l'aide et les options disponibles pour la commande.
- `--version` : Affiche la version de la commande `dirname`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `dirname` :

1. **Obtenir le répertoire d'un fichier :**
   ```csh
   dirname /home/utilisateur/documents/fichier.txt
   ```
   Cela renverra :
   ```
   /home/utilisateur/documents
   ```

2. **Utiliser dirname avec un chemin relatif :**
   ```csh
   dirname ./projets/codage/script.sh
   ```
   Cela renverra :
   ```
   ./projets/codage
   ```

3. **Traiter un chemin vide :**
   ```csh
   dirname ""
   ```
   Cela renverra :
   ```
   .
   ```

4. **Obtenir le répertoire d'un chemin avec des espaces :**
   ```csh
   dirname "/home/utilisateur/mes fichiers/rapport.doc"
   ```
   Cela renverra :
   ```
   /home/utilisateur/mes fichiers
   ```

## Tips
- Utilisez `dirname` en combinaison avec d'autres commandes comme `basename` pour manipuler les chemins de fichiers de manière efficace.
- Soyez attentif aux chemins relatifs et absolus pour éviter des résultats inattendus.
- Pensez à utiliser l'option `-z` si vous devez gérer des chemins qui peuvent être vides dans vos scripts.