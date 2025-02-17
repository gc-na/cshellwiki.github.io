# [Linux] Bash source usage : Exécuter des scripts dans le shell courant

## Overview
La commande `source` est utilisée dans les environnements Bash pour exécuter des scripts dans le contexte du shell courant. Cela signifie que les variables et les fonctions définies dans le script restent disponibles après son exécution, contrairement à l'exécution d'un script en tant que processus séparé.

## Usage
La syntaxe de base de la commande `source` est la suivante :

```bash
source [options] [arguments]
```

## Common Options
- `-h`, `--help` : Affiche l'aide et les options disponibles pour la commande.
- `-V`, `--version` : Affiche la version de la commande `source`.

## Common Examples

### Exemple 1 : Exécuter un script
Pour exécuter un script nommé `script.sh`, vous pouvez utiliser la commande suivante :

```bash
source script.sh
```

### Exemple 2 : Charger un fichier de configuration
Si vous avez un fichier de configuration nommé `config.sh`, vous pouvez le charger dans votre session actuelle :

```bash
source config.sh
```

### Exemple 3 : Utiliser un alias défini dans un script
Supposons que `alias.sh` définit un alias. Après avoir exécuté :

```bash
source alias.sh
```
Vous pouvez utiliser l'alias défini dans votre shell.

## Tips
- Utilisez `source` pour charger des fichiers de configuration ou des scripts qui définissent des variables d'environnement ou des fonctions que vous souhaitez utiliser dans votre session actuelle.
- Évitez d'utiliser `source` avec des scripts qui modifient l'état de votre système de manière permanente, à moins que vous ne soyez sûr de ce que vous faites.
- Pour une meilleure lisibilité, commentez vos scripts afin que vous sachiez ce que chaque section fait lorsque vous les chargez avec `source`.