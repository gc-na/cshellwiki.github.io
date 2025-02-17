# [Linux] Bash batch utilisation : Exécuter des commandes en arrière-plan

## Overview
La commande `batch` permet d'exécuter des commandes en arrière-plan lorsque le système est moins chargé. Elle est utile pour planifier des tâches qui ne nécessitent pas d'interaction immédiate avec l'utilisateur.

## Usage
La syntaxe de base de la commande `batch` est la suivante :

```bash
batch [options] [arguments]
```

## Common Options
- `-f` : Spécifie un fichier contenant des commandes à exécuter.
- `-q` : Exécute les commandes en mode silencieux, sans afficher de messages.
- `-l` : Affiche la liste des commandes en attente.

## Common Examples

### Exécuter une commande simple
Pour exécuter une commande simple comme `echo`, vous pouvez utiliser :

```bash
echo "Hello, World!" | batch
```

### Exécuter un script
Pour exécuter un script shell nommé `script.sh`, utilisez :

```bash
batch < script.sh
```

### Utiliser un fichier de commandes
Si vous avez un fichier `commands.txt` contenant plusieurs commandes, vous pouvez l'exécuter comme suit :

```bash
batch < commands.txt
```

### Exécuter en mode silencieux
Pour exécuter une commande sans afficher de messages, utilisez l'option `-q` :

```bash
echo "Backup started" | batch -q
```

## Tips
- Assurez-vous que les commandes que vous planifiez n'ont pas besoin d'interaction utilisateur, car elles s'exécuteront en arrière-plan.
- Vérifiez régulièrement la file d'attente des commandes en attente avec `atq` pour gérer vos tâches.
- Utilisez des scripts pour regrouper plusieurs commandes et faciliter leur exécution en une seule fois.