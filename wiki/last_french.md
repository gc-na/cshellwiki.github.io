# [Linux] C Shell (csh) last : afficher les connexions précédentes

## Overview
La commande `last` dans C Shell (csh) est utilisée pour afficher les connexions précédentes des utilisateurs sur le système. Elle lit le fichier `/var/log/wtmp` pour fournir un historique des connexions et des déconnexions.

## Usage
La syntaxe de base de la commande `last` est la suivante :

```csh
last [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `last` :

- `-n [nombre]` : Affiche les [nombre] dernières connexions.
- `-R` : N'affiche pas le nom d'hôte.
- `-x` : Affiche également les événements de démarrage et d'arrêt du système.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `last` :

1. Afficher toutes les connexions précédentes :
   ```csh
   last
   ```

2. Afficher les 5 dernières connexions :
   ```csh
   last -n 5
   ```

3. Afficher les connexions sans le nom d'hôte :
   ```csh
   last -R
   ```

4. Afficher les connexions avec les événements de démarrage et d'arrêt :
   ```csh
   last -x
   ```

## Tips
- Utilisez `last` régulièrement pour surveiller l'activité des utilisateurs sur votre système.
- Combinez `last` avec d'autres commandes comme `grep` pour filtrer les résultats selon des utilisateurs spécifiques.
- Pensez à vérifier les permissions d'accès au fichier `/var/log/wtmp` si vous ne voyez pas les résultats attendus.