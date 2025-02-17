# [Linux] Bash time utilisation : mesurer le temps d'exécution d'une commande

## Overview
La commande `time` permet de mesurer le temps d'exécution d'une autre commande dans un terminal Bash. Elle fournit des informations sur le temps écoulé, le temps CPU utilisé et d'autres statistiques pertinentes.

## Usage
La syntaxe de base de la commande `time` est la suivante :

```bash
time [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `time` :

- `-p` : Affiche le temps au format POSIX.
- `-o <file>` : Redirige la sortie vers un fichier spécifié.
- `-v` : Affiche des informations détaillées sur l'utilisation des ressources.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `time` :

1. Mesurer le temps d'exécution d'une commande simple :
   ```bash
   time ls -l
   ```

2. Mesurer le temps d'exécution d'un script :
   ```bash
   time ./mon_script.sh
   ```

3. Rediriger la sortie vers un fichier :
   ```bash
   time -o temps.txt sleep 3
   ```

4. Afficher des informations détaillées :
   ```bash
   time -v find / -name "*.txt"
   ```

## Tips
- Utilisez l'option `-p` pour obtenir un format de sortie plus simple et standardisé.
- Pensez à rediriger la sortie vers un fichier si vous souhaitez conserver les résultats pour une analyse ultérieure.
- Pour des scripts complexes, utilisez `time` avec `bash -c` pour mesurer le temps d'exécution de plusieurs commandes en une seule ligne.