# [Linux] Bash true : Exécute une commande qui réussit toujours

## Overview
La commande `true` en Bash est une commande simple qui ne fait rien mais renvoie toujours un code de sortie de 0, indiquant un succès. Elle est souvent utilisée dans des scripts pour représenter une opération réussie ou pour remplir des conditions.

## Usage
La syntaxe de base de la commande `true` est la suivante :

```bash
true [options] [arguments]
```

Cependant, `true` n'accepte généralement pas d'options ou d'arguments.

## Common Options
La commande `true` ne possède pas d'options courantes à proprement parler, car son fonctionnement est très simple. Elle est conçue pour être utilisée sans options.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `true` :

1. **Utiliser true dans un script :**
   ```bash
   #!/bin/bash
   if true; then
       echo "Cette condition est toujours vraie."
   fi
   ```

2. **Utiliser true dans une boucle :**
   ```bash
   while true; do
       echo "Cette boucle tourne indéfiniment."
       sleep 1
   done
   ```

3. **Combiner true avec d'autres commandes :**
   ```bash
   command1 && true && command2
   ```

4. **Utiliser true pour créer un fichier vide :**
   ```bash
   true > fichier_vide.txt
   ```

## Tips
- Utilisez `true` pour créer des boucles infinies ou des scripts qui doivent continuer à s'exécuter sans condition d'arrêt.
- `true` peut être utile dans des scripts pour remplacer des commandes qui ne sont pas encore implémentées, permettant ainsi de tester la structure du script.
- Évitez d'utiliser `true` dans des contextes où une condition réelle doit être évaluée, car cela pourrait mener à des comportements inattendus.