# [Linux] Bash continue : Poursuit l'exécution de la boucle

## Overview
La commande `continue` en Bash est utilisée pour sauter le reste des instructions dans une boucle et passer à l'itération suivante. Cela est particulièrement utile lorsque certaines conditions sont remplies et que vous souhaitez ignorer certaines itérations sans sortir complètement de la boucle.

## Usage
La syntaxe de base de la commande `continue` est la suivante :

```bash
continue [n]
```

Ici, `n` est un nombre optionnel qui indique combien d'itérations de la boucle doivent être ignorées. Si `n` n'est pas spécifié, la commande passe simplement à l'itération suivante.

## Common Options
- `n` : Un nombre qui indique combien d'itérations de la boucle doivent être ignorées. Par défaut, il est égal à 1.

## Common Examples

### Exemple 1 : Ignorer les nombres pairs
Dans cet exemple, nous allons imprimer les nombres de 1 à 10, en ignorant les nombres pairs.

```bash
for i in {1..10}; do
    if (( i % 2 == 0 )); then
        continue
    fi
    echo $i
done
```

### Exemple 2 : Sauter les fichiers cachés
Voici comment vous pouvez utiliser `continue` pour ignorer les fichiers cachés dans un répertoire.

```bash
for file in *; do
    if [[ $file == .* ]]; then
        continue
    fi
    echo "Traitement de $file"
done
```

### Exemple 3 : Sauter une itération spécifique
Dans cet exemple, nous allons sauter l'itération 3 d'une boucle.

```bash
for i in {1..5}; do
    if [[ $i -eq 3 ]]; then
        continue
    fi
    echo "Itération $i"
done
```

## Tips
- Utilisez `continue` pour rendre votre code plus lisible en évitant des instructions imbriquées complexes.
- Soyez prudent avec l'utilisation de `continue` dans des boucles imbriquées ; il ne s'applique qu'à la boucle la plus proche.
- Testez toujours vos conditions avant d'utiliser `continue` pour vous assurer que le comportement est celui que vous attendez.