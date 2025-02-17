# [Linux] Bash tail usage : Afficher les dernières lignes d'un fichier

## Overview
La commande `tail` est utilisée pour afficher les dernières lignes d'un fichier. Elle est particulièrement utile pour surveiller les fichiers de log ou pour examiner les dernières entrées d'un fichier texte.

## Usage
La syntaxe de base de la commande `tail` est la suivante :

```bash
tail [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `tail` :

- `-n [nombre]` : Affiche le nombre spécifié de lignes à partir de la fin du fichier.
- `-f` : Suivre le fichier en temps réel, affichant les nouvelles lignes au fur et à mesure qu'elles sont ajoutées.
- `-c [nombre]` : Affiche le nombre spécifié d'octets à partir de la fin du fichier.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `tail` :

1. Afficher les 10 dernières lignes d'un fichier :
   ```bash
   tail mon_fichier.txt
   ```

2. Afficher les 20 dernières lignes d'un fichier :
   ```bash
   tail -n 20 mon_fichier.txt
   ```

3. Suivre un fichier de log en temps réel :
   ```bash
   tail -f /var/log/syslog
   ```

4. Afficher les 50 derniers octets d'un fichier :
   ```bash
   tail -c 50 mon_fichier.txt
   ```

## Tips
- Utilisez l'option `-f` pour surveiller les fichiers de log pendant qu'ils sont mis à jour, ce qui est très utile pour le débogage.
- Combinez `tail` avec d'autres commandes comme `grep` pour filtrer les résultats. Par exemple :
  ```bash
  tail -f /var/log/syslog | grep erreur
  ```
- Pensez à rediriger la sortie de `tail` vers un fichier si vous souhaitez conserver les dernières lignes pour une consultation ultérieure :
  ```bash
  tail -n 100 mon_fichier.txt > dernieres_lignes.txt
  ```