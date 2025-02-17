# [Linux] Bash strace Utilisation : Suivre les appels système d'un programme

## Overview
La commande `strace` est un outil puissant utilisé pour suivre les appels système et les signaux d'un programme en cours d'exécution. Elle permet aux développeurs et aux administrateurs système de déboguer des applications en fournissant des informations détaillées sur les interactions entre un programme et le noyau du système d'exploitation.

## Usage
La syntaxe de base de la commande `strace` est la suivante :

```bash
strace [options] [arguments]
```

## Common Options
Voici quelques options courantes de `strace` avec de courtes explications :

- `-o <fichier>` : Redirige la sortie vers le fichier spécifié au lieu de la sortie standard.
- `-e <expression>` : Filtre les appels système à tracer selon l'expression donnée.
- `-p <pid>` : Attache `strace` à un processus existant identifié par son PID (identifiant de processus).
- `-c` : Résume les statistiques des appels système effectués.
- `-f` : Suit les processus fils créés par le programme traqué.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `strace` :

1. **Tracer un programme simple :**
   ```bash
   strace ls
   ```

2. **Rediriger la sortie vers un fichier :**
   ```bash
   strace -o sortie.txt ls
   ```

3. **Tracer un processus existant :**
   ```bash
   strace -p 1234
   ```

4. **Filtrer les appels système :**
   ```bash
   strace -e trace=open,close ls
   ```

5. **Obtenir un résumé des appels système :**
   ```bash
   strace -c ls
   ```

## Tips
- Utilisez l'option `-o` pour enregistrer la sortie dans un fichier, ce qui facilite l'analyse ultérieure.
- Combinez `strace` avec d'autres outils comme `grep` pour filtrer les résultats et se concentrer sur des appels spécifiques.
- Faites attention à la quantité de données générées, surtout avec des programmes qui effectuent de nombreux appels système, car cela peut rendre l'analyse difficile.