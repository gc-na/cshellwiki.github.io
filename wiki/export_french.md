# [Linux] Bash export : Gérer les variables d'environnement

## Overview
La commande `export` en Bash est utilisée pour définir des variables d'environnement qui peuvent être accessibles par les processus enfants. Cela permet de partager des informations entre différents programmes exécutés dans le même environnement.

## Usage
La syntaxe de base de la commande `export` est la suivante :

```bash
export [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `export` :

- `-p` : Affiche toutes les variables d'environnement exportées.
- `-n` : Supprime l'exportation d'une variable, la rendant non disponible pour les processus enfants.

## Common Examples

### Exporter une variable
Pour créer une variable d'environnement et l'exporter, vous pouvez utiliser la commande suivante :

```bash
export NOM_VARIABLE="valeur"
```

### Vérifier les variables exportées
Pour afficher toutes les variables d'environnement exportées, utilisez :

```bash
export -p
```

### Supprimer l'exportation d'une variable
Pour supprimer l'exportation d'une variable, utilisez l'option `-n` :

```bash
export -n NOM_VARIABLE
```

### Utiliser une variable exportée dans un script
Si vous avez exporté une variable, vous pouvez l'utiliser dans un script Bash comme ceci :

```bash
#!/bin/bash
export MON_VARIABLE="Bonjour"
bash -c 'echo $MON_VARIABLE'
```

## Tips
- Assurez-vous d'exporter les variables dont vous avez besoin dans les sous-processus pour éviter les erreurs.
- Pour rendre une variable persistante à travers les sessions, ajoutez l'exportation dans votre fichier `~/.bashrc` ou `~/.bash_profile`.
- Évitez d'utiliser des noms de variables qui pourraient entrer en conflit avec les variables d'environnement système.