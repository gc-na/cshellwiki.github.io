# [Linux] Bash foreach : Exécuter des commandes pour chaque élément d'une liste

## Overview
La commande `foreach` est utilisée dans certains shells, comme `csh` et `tcsh`, pour exécuter une série de commandes pour chaque élément d'une liste. Bien que `foreach` ne soit pas une commande Bash native, son équivalent en Bash est souvent réalisé avec une boucle `for`.

## Usage
La syntaxe de base de la commande `foreach` est la suivante :

```bash
foreach variable ( liste )
    commande
end
```

Cependant, en Bash, vous utiliseriez une syntaxe similaire avec une boucle `for` :

```bash
for variable in liste; do
    commande
done
```

## Common Options
La commande `foreach` en tant que telle n'a pas d'options spécifiques, mais voici quelques éléments à considérer lors de l'utilisation de la boucle `for` en Bash :

- `-n` : Exécute la commande sans afficher la sortie.
- `-v` : Affiche les commandes avant leur exécution.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `foreach` en Bash avec une boucle `for` :

### Exemple 1 : Afficher des noms de fichiers
```bash
for fichier in *.txt; do
    echo "Fichier trouvé : $fichier"
done
```

### Exemple 2 : Exécuter une commande sur plusieurs serveurs
```bash
for serveur in serveur1 serveur2 serveur3; do
    ssh $serveur 'uptime'
done
```

### Exemple 3 : Calculer le carré des nombres
```bash
for i in {1..5}; do
    echo "Le carré de $i est $((i * i))"
done
```

## Tips
- Utilisez des guillemets autour des variables pour éviter des erreurs avec des noms de fichiers contenant des espaces.
- Préférez utiliser des boucles `for` en Bash pour plus de flexibilité et de compatibilité.
- Testez vos commandes dans un environnement sécurisé avant de les exécuter sur des systèmes de production.