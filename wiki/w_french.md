# [Linux] C Shell (csh) w : Afficher les utilisateurs connectés

## Overview
La commande `w` dans C Shell (csh) est utilisée pour afficher une liste des utilisateurs actuellement connectés à la machine, ainsi que des informations sur leur activité. Cela inclut des détails tels que le temps d'activité, l'heure de connexion et l'activité en cours.

## Usage
La syntaxe de base de la commande est la suivante :

```
w [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `w` :

- `-h` : Supprime l'en-tête de la sortie.
- `-s` : Affiche la sortie dans un format plus compact.
- `-u` : Affiche les utilisateurs qui ont été inactifs pendant une période prolongée.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `w` :

1. Afficher la liste des utilisateurs connectés :
   ```csh
   w
   ```

2. Afficher la liste sans l'en-tête :
   ```csh
   w -h
   ```

3. Afficher la liste dans un format compact :
   ```csh
   w -s
   ```

4. Afficher les utilisateurs inactifs :
   ```csh
   w -u
   ```

## Tips
- Utilisez `w` régulièrement pour surveiller l'activité des utilisateurs sur le système.
- Combinez `w` avec d'autres commandes comme `grep` pour filtrer les résultats selon des critères spécifiques.
- Familiarisez-vous avec les options pour personnaliser la sortie selon vos besoins.