# [Linux] C Shell (csh) tee : [rediriger et afficher la sortie]

## Overview
La commande `tee` dans C Shell (csh) permet de lire l'entrée standard et de l'écrire simultanément dans un ou plusieurs fichiers, tout en affichant également la sortie à l'écran. Cela est particulièrement utile pour enregistrer des données tout en continuant à les visualiser.

## Usage
La syntaxe de base de la commande `tee` est la suivante :

```csh
tee [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `tee` :

- `-a` : Ajoute la sortie à la fin du fichier au lieu de l'écraser.
- `-i` : Ignore les signaux d'interruption.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `tee` :

1. **Écrire la sortie d'une commande dans un fichier :**

```csh
ls -l | tee fichier.txt
```

Cela affichera la liste des fichiers dans le répertoire courant et l'écrira dans `fichier.txt`.

2. **Ajouter la sortie à un fichier existant :**

```csh
echo "Nouvelle ligne" | tee -a fichier.txt
```

Cela ajoutera "Nouvelle ligne" à la fin de `fichier.txt` tout en l'affichant à l'écran.

3. **Écrire la sortie dans plusieurs fichiers :**

```csh
echo "Bonjour" | tee fichier1.txt fichier2.txt
```

Cela écrira "Bonjour" dans `fichier1.txt` et `fichier2.txt`, tout en l'affichant à l'écran.

## Tips
- Utilisez l'option `-a` lorsque vous souhaitez conserver le contenu existant d'un fichier et y ajouter de nouvelles données.
- Combinez `tee` avec d'autres commandes pour créer des pipelines efficaces, par exemple, pour surveiller les logs tout en les sauvegardant.
- Soyez prudent avec les permissions des fichiers pour éviter les erreurs d'écriture.