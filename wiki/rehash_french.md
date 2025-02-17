# [Linux] Bash rehash utilisation : Met à jour la liste des commandes disponibles

## Overview
La commande `rehash` dans Bash est utilisée pour mettre à jour le cache des commandes disponibles dans le shell. Cela est particulièrement utile lorsque de nouveaux exécutables ont été ajoutés à un répertoire qui est déjà dans le chemin d'accès, permettant ainsi à l'utilisateur d'accéder à ces nouveaux exécutables sans redémarrer le shell.

## Usage
La syntaxe de base de la commande `rehash` est la suivante :

```bash
rehash [options] [arguments]
```

## Common Options
La commande `rehash` n'a pas d'options spécifiques, elle est généralement utilisée sans arguments. 

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `rehash` :

1. **Mettre à jour le cache des commandes** :
   ```bash
   rehash
   ```

2. **Après avoir ajouté un nouvel exécutable dans un répertoire** :
   Supposons que vous ayez ajouté un script nommé `myscript.sh` dans `/usr/local/bin`, vous pouvez exécuter :
   ```bash
   rehash
   ```
   Ensuite, vous pourrez exécuter `myscript.sh` directement.

3. **Utilisation après l'installation d'un nouveau logiciel** :
   Si vous avez installé un nouveau logiciel qui a ajouté des commandes dans votre chemin, utilisez :
   ```bash
   rehash
   ```

## Tips
- Utilisez `rehash` régulièrement si vous installez fréquemment de nouveaux outils ou scripts.
- Si vous ne voyez pas un nouvel exécutable dans votre terminal, essayez d'abord `rehash` avant de vérifier votre chemin d'accès.
- Notez que certains shells, comme `zsh`, utilisent `rehash` automatiquement, donc cette commande peut ne pas être nécessaire dans ces environnements.