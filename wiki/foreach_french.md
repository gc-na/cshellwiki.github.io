# [Linux] C Shell (csh) foreach : Exécute une commande pour chaque élément d'une liste

## Overview
La commande `foreach` dans C Shell (csh) permet d'exécuter une série de commandes pour chaque élément d'une liste. C'est un outil puissant pour automatiser des tâches répétitives en itérant sur des éléments.

## Usage
La syntaxe de base de la commande `foreach` est la suivante :

```csh
foreach variable (liste)
    commande
end
```

## Common Options
La commande `foreach` n'a pas de nombreuses options, mais voici quelques éléments à considérer :

- `variable` : Nom de la variable qui prendra la valeur de chaque élément de la liste à chaque itération.
- `liste` : Une série d'éléments séparés par des espaces ou des parenthèses.

## Common Examples

### Exemple 1 : Afficher des noms de fichiers
```csh
foreach file (*.txt)
    echo $file
end
```
Cet exemple affiche tous les fichiers avec l'extension `.txt` dans le répertoire courant.

### Exemple 2 : Compresser des fichiers
```csh
foreach file (*.log)
    gzip $file
end
```
Ici, tous les fichiers avec l'extension `.log` sont compressés en utilisant `gzip`.

### Exemple 3 : Exécuter une commande sur plusieurs serveurs
```csh
foreach server (server1 server2 server3)
    ssh $server 'uptime'
end
```
Cet exemple se connecte à plusieurs serveurs et exécute la commande `uptime` sur chacun d'eux.

## Tips
- Utilisez des parenthèses pour définir clairement la liste des éléments.
- Faites attention aux espaces dans les noms de fichiers ; utilisez des guillemets si nécessaire.
- Testez vos commandes avec un petit sous-ensemble de données avant de les exécuter sur de grandes listes pour éviter des erreurs coûteuses.