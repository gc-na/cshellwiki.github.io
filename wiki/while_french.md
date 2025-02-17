# [Linux] Bash while utilisation : Exécuter des commandes en boucle

## Overview
La commande `while` en Bash permet d'exécuter une série de commandes tant qu'une condition spécifiée est vraie. C'est un outil puissant pour automatiser des tâches répétitives dans des scripts.

## Usage
La syntaxe de base de la commande `while` est la suivante :

```bash
while [condition]
do
    # commandes à exécuter
done
```

## Common Options
- Aucun option spécifique n'est généralement utilisée avec `while`, mais il est important de bien formuler la condition pour éviter des boucles infinies.

## Common Examples

### Exemple 1 : Compter jusqu'à 5
```bash
count=1
while [ $count -le 5 ]
do
    echo "Compteur : $count"
    ((count++))
done
```

### Exemple 2 : Lire des lignes d'un fichier
```bash
while IFS= read -r line
do
    echo "Ligne : $line"
done < fichier.txt
```

### Exemple 3 : Boucle infinie avec condition d'arrêt
```bash
while true
do
    echo "Appuyez sur [CTRL+C] pour quitter."
    sleep 1
done
```

## Tips
- Assurez-vous que la condition finisse par devenir fausse pour éviter des boucles infinies.
- Utilisez `break` pour sortir d'une boucle `while` prématurément si nécessaire.
- Pensez à utiliser `sleep` pour éviter une utilisation excessive des ressources CPU dans des boucles rapides.