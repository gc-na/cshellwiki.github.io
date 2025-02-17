# [Linux] Bash break utilisation : Interrompre une boucle

## Overview
La commande `break` en Bash est utilisée pour sortir d'une boucle. Que ce soit une boucle `for`, `while` ou `until`, `break` permet de quitter la boucle en cours d'exécution lorsque certaines conditions sont remplies.

## Usage
La syntaxe de base de la commande `break` est la suivante :

```bash
break [n]
```

Ici, `n` est un nombre optionnel qui indique le nombre de niveaux de boucle à quitter. Si `n` n'est pas spécifié, `break` sort de la boucle la plus interne.

## Common Options
- `n` : Un nombre qui spécifie le nombre de niveaux de boucle à quitter. Par défaut, il quitte la boucle la plus interne.

## Common Examples

### Exemple 1 : Sortir d'une boucle `for`
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo "Nombre : $i"
done
```
*Sortie :*
```
Nombre : 1
Nombre : 2
```

### Exemple 2 : Sortir d'une boucle `while`
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 4 ]; then
    break
  fi
  echo "Compteur : $count"
  ((count++))
done
```
*Sortie :*
```
Compteur : 1
Compteur : 2
Compteur : 3
```

### Exemple 3 : Utilisation de `break` avec un nombre
```bash
for i in {1..5}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "i : $i, j : $j"
  done
done
```
*Sortie :*
```
i : 1, j : 1
```

## Tips
- Utilisez `break` judicieusement pour éviter de sortir prématurément de boucles, ce qui pourrait entraîner des comportements inattendus.
- Si vous avez plusieurs niveaux de boucles imbriquées, spécifiez le nombre de niveaux à quitter pour un contrôle plus précis.
- Testez toujours vos conditions de sortie pour vous assurer que la boucle se termine comme prévu.