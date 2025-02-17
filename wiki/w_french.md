# [Linux] Bash w : afficher les utilisateurs connectés

## Overview
La commande `w` affiche une liste des utilisateurs actuellement connectés au système, ainsi que des informations sur ce qu'ils font. Cela inclut des détails tels que l'heure de connexion, le temps d'inactivité, et l'activité en cours.

## Usage
La syntaxe de base de la commande `w` est la suivante :

```bash
w [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `w` :

- `-h` : Affiche la sortie sans l'en-tête.
- `-s` : Affiche une sortie plus concise, sans les informations sur le temps d'inactivité.
- `-f` : Affiche le nom d'hôte complet des utilisateurs.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `w` :

1. **Afficher tous les utilisateurs connectés :**
   ```bash
   w
   ```

2. **Afficher les utilisateurs sans l'en-tête :**
   ```bash
   w -h
   ```

3. **Afficher une sortie concise :**
   ```bash
   w -s
   ```

4. **Afficher les utilisateurs avec le nom d'hôte complet :**
   ```bash
   w -f
   ```

## Tips
- Utilisez la commande `w` régulièrement pour surveiller l'activité des utilisateurs sur votre système.
- Combinez `w` avec d'autres commandes comme `grep` pour filtrer les résultats selon des critères spécifiques.
- Pensez à utiliser l'option `-s` pour obtenir une vue d'ensemble rapide sans trop de détails si vous n'en avez pas besoin.