# [Linux] C Shell (csh) du : Afficher l'utilisation de l'espace disque

## Overview
La commande `du` (disk usage) est utilisée pour estimer et afficher l'utilisation de l'espace disque des fichiers et des répertoires. Elle permet aux utilisateurs de comprendre combien d'espace est occupé par leurs fichiers et dossiers, ce qui est essentiel pour la gestion de l'espace disque.

## Usage
La syntaxe de base de la commande `du` est la suivante :

```csh
du [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `du` :

- `-h` : Affiche les tailles dans un format lisible par l'homme (par exemple, Ko, Mo, Go).
- `-s` : Affiche uniquement le total pour chaque argument, sans lister les sous-répertoires.
- `-a` : Inclut les fichiers dans la sortie, pas seulement les répertoires.
- `-c` : Affiche un total cumulatif à la fin de la sortie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `du` :

1. Afficher l'utilisation de l'espace disque pour le répertoire courant :

   ```csh
   du
   ```

2. Afficher l'utilisation de l'espace disque dans un format lisible par l'homme :

   ```csh
   du -h
   ```

3. Afficher uniquement le total de l'utilisation de l'espace pour un répertoire spécifique :

   ```csh
   du -sh /chemin/vers/repertoire
   ```

4. Inclure les fichiers dans la sortie :

   ```csh
   du -ah
   ```

5. Afficher un total cumulatif pour plusieurs répertoires :

   ```csh
   du -ch /chemin/vers/repertoire1 /chemin/vers/repertoire2
   ```

## Tips
- Utilisez l'option `-h` pour rendre les chiffres plus compréhensibles, surtout lorsque vous travaillez avec de grandes quantités de données.
- Combinez `-s` avec d'autres options pour obtenir des résumés clairs de l'utilisation de l'espace.
- Pensez à rediriger la sortie vers un fichier si vous avez besoin de conserver un rapport sur l'utilisation de l'espace disque :

  ```csh
  du -h > rapport_utilisation_espace.txt
  ```