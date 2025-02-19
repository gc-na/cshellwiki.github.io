# [Linux] C Shell (csh) while : Exécute une commande tant qu'une condition est vraie

## Overview
La commande `while` dans C Shell (csh) permet d'exécuter une série de commandes tant qu'une condition spécifiée est vraie. Cela est particulièrement utile pour les boucles qui nécessitent une répétition jusqu'à ce qu'un certain critère soit atteint.

## Usage
La syntaxe de base de la commande `while` est la suivante :

```csh
while (condition)
    commande1
    commande2
    ...
end
```

## Common Options
La commande `while` n'a pas d'options spécifiques, mais elle fonctionne avec des conditions qui peuvent inclure des expressions logiques et des comparaisons. Voici quelques exemples de conditions que vous pouvez utiliser :

- `-e fichier` : Vérifie si le fichier existe.
- `-d répertoire` : Vérifie si le répertoire existe.
- `expr` : Évalue une expression arithmétique.

## Common Examples

### Exemple 1 : Compter jusqu'à 5
```csh
set i = 1
while ($i <= 5)
    echo $i
    @ i++
end
```

### Exemple 2 : Lire des fichiers jusqu'à ce qu'un fichier soit trouvé
```csh
set fichier = "fichier.txt"
while (! -e $fichier)
    echo "Recherche de $fichier..."
    sleep 1
end
echo "$fichier trouvé !"
```

### Exemple 3 : Boucle infinie avec une condition d'arrêt
```csh
set i = 0
while (1)
    echo "Boucle numéro $i"
    @ i++
    if ($i >= 10) break
end
```

## Tips
- Assurez-vous que la condition de la boucle finisse par devenir fausse pour éviter les boucles infinies.
- Utilisez `break` pour sortir d'une boucle lorsque vous atteignez une condition spécifique.
- Testez vos conditions avant de les utiliser dans une boucle pour garantir qu'elles fonctionnent comme prévu.