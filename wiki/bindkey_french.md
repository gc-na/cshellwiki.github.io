# [Linux] Bash bindkey Utilisation : Gérer les raccourcis clavier dans l'interface de ligne de commande

## Overview
La commande `bindkey` est utilisée dans les environnements de ligne de commande, comme Zsh, pour gérer les raccourcis clavier. Elle permet de lier des combinaisons de touches à des commandes spécifiques, facilitant ainsi l'interaction avec le terminal.

## Usage
La syntaxe de base de la commande `bindkey` est la suivante :

```bash
bindkey [options] [arguments]
```

## Common Options
- `-l` : Liste toutes les liaisons de touches actuelles.
- `-e` : Active le mode Emacs pour les liaisons de touches.
- `-v` : Active le mode Vi pour les liaisons de touches.
- `-s` : Permet de lier une séquence de touches à une chaîne de caractères.

## Common Examples

### Lister les liaisons de touches
Pour afficher toutes les liaisons de touches actuelles, utilisez :

```bash
bindkey -l
```

### Passer en mode Emacs
Pour activer le mode Emacs, exécutez :

```bash
bindkey -e
```

### Passer en mode Vi
Pour activer le mode Vi, exécutez :

```bash
bindkey -v
```

### Lier une touche à une commande
Pour lier la combinaison de touches `Ctrl + x` à la commande `ls`, utilisez :

```bash
bindkey '^x' 'ls'
```

### Lier une séquence de touches
Pour lier `Ctrl + g` à la chaîne de caractères "Hello, World!", utilisez :

```bash
bindkey -s '^g' 'Hello, World!'
```

## Tips
- Pensez à sauvegarder vos liaisons de touches dans votre fichier de configuration (`.zshrc`) pour qu'elles soient disponibles à chaque démarrage du terminal.
- Utilisez des combinaisons de touches qui ne sont pas déjà utilisées par d'autres commandes pour éviter les conflits.
- Testez vos liaisons de touches après les avoir définies pour vous assurer qu'elles fonctionnent comme prévu.