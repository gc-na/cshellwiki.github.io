# [Linux] Bash exec usage : Exécute une commande dans le contexte du shell actuel

## Overview
La commande `exec` dans Bash est utilisée pour exécuter une commande en remplaçant le shell actuel par le processus de la commande spécifiée. Cela signifie que, après l'exécution de la commande, le shell ne revient pas à l'état précédent. C'est utile pour lancer des programmes sans créer de nouveaux processus.

## Usage
La syntaxe de base de la commande `exec` est la suivante :

```bash
exec [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `exec` :

- `-a` : Permet de spécifier un nom de programme différent pour le processus exécuté.
- `-l` : Lance le programme comme un shell de connexion.
- `-p` : Préserve l'environnement du shell actuel.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `exec` :

1. **Remplacer le shell actuel par un autre programme :**
   ```bash
   exec /bin/ls
   ```
   Cela exécutera `ls` et remplacera le shell actuel par ce processus.

2. **Utiliser `exec` pour rediriger la sortie :**
   ```bash
   exec > output.txt
   ```
   Cela redirige toute la sortie standard vers le fichier `output.txt`.

3. **Lancer un script avec `exec` :**
   ```bash
   exec ./mon_script.sh
   ```
   Cela exécutera `mon_script.sh` et remplacera le shell courant.

4. **Exécuter un programme avec un nom différent :**
   ```bash
   exec -a nouveau_nom /bin/bash
   ```
   Cela lancera un nouveau shell Bash sous le nom `nouveau_nom`.

## Tips
- Utilisez `exec` lorsque vous souhaitez remplacer le shell actuel par un programme, surtout dans des scripts où vous ne voulez pas revenir au shell après l'exécution.
- Soyez prudent avec `exec` car une fois exécuté, vous ne pourrez pas revenir au shell précédent.
- Pensez à rediriger les sorties si vous exécutez des commandes qui produisent beaucoup de texte, pour éviter de saturer votre terminal.