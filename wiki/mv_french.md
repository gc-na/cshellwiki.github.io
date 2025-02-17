# [Linux] Bash mv Utilisation : Déplacer ou renommer des fichiers

## Overview
La commande `mv` est utilisée pour déplacer ou renommer des fichiers et des répertoires dans un système de fichiers. C'est un outil essentiel pour la gestion des fichiers dans un environnement Bash.

## Usage
La syntaxe de base de la commande `mv` est la suivante :

```bash
mv [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `mv` :

- `-i` : Demande confirmation avant de remplacer un fichier existant.
- `-u` : Déplace uniquement si la source est plus récente que la destination ou si la destination n'existe pas.
- `-v` : Affiche les actions effectuées par la commande, utile pour le débogage.
- `-n` : Ne remplace pas les fichiers existants.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mv` :

1. **Déplacer un fichier vers un autre répertoire :**
   ```bash
   mv fichier.txt /chemin/vers/nouveau/dossier/
   ```

2. **Renommer un fichier :**
   ```bash
   mv ancien_nom.txt nouveau_nom.txt
   ```

3. **Déplacer plusieurs fichiers vers un répertoire :**
   ```bash
   mv fichier1.txt fichier2.txt /chemin/vers/nouveau/dossier/
   ```

4. **Déplacer un fichier avec confirmation :**
   ```bash
   mv -i fichier.txt /chemin/vers/nouveau/dossier/
   ```

5. **Déplacer un fichier uniquement s'il est plus récent :**
   ```bash
   mv -u fichier.txt /chemin/vers/nouveau/dossier/
   ```

## Tips
- Utilisez l'option `-i` pour éviter de remplacer accidentellement des fichiers importants.
- Vérifiez toujours le chemin de destination pour éviter de déplacer des fichiers vers des emplacements inattendus.
- Pratiquez l'utilisation de `mv` dans un environnement de test pour vous familiariser avec son fonctionnement avant de l'utiliser sur des fichiers critiques.