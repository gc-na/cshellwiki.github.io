# [Linux] C Shell (csh) unalias : Supprimer des alias

## Overview
La commande `unalias` dans C Shell (csh) est utilisée pour supprimer un ou plusieurs alias définis dans l'environnement de shell. Les alias sont des raccourcis pour des commandes plus longues, et parfois, il est nécessaire de les supprimer pour éviter des conflits ou pour revenir à des commandes par défaut.

## Usage
La syntaxe de base de la commande `unalias` est la suivante :

```csh
unalias [options] [arguments]
```

## Common Options
- `-a` : Supprime tous les alias définis.
- `-m` : Supprime les alias qui correspondent à un motif spécifique.

## Common Examples

### Supprimer un alias spécifique
Pour supprimer un alias nommé `ll`, utilisez la commande suivante :

```csh
unalias ll
```

### Supprimer tous les alias
Pour supprimer tous les alias définis dans votre session, utilisez l'option `-a` :

```csh
unalias -a
```

### Supprimer des alias correspondant à un motif
Pour supprimer tous les alias qui commencent par `g`, vous pouvez utiliser l'option `-m` :

```csh
unalias -m g*
```

## Tips
- Vérifiez vos alias actuels avec la commande `alias` avant de les supprimer pour éviter de supprimer quelque chose d'important.
- Utilisez `unalias -a` avec précaution, car cela supprimera tous les alias sans possibilité de récupération.
- Pensez à sauvegarder vos alias dans un fichier de configuration si vous souhaitez les restaurer plus tard.