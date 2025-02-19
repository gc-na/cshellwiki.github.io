# [Linux] C Shell (csh) strace Utilisation : Suivre les appels système d'un programme

## Overview
La commande `strace` est un outil puissant utilisé pour suivre les appels système et les signaux d'un programme en cours d'exécution. Elle permet aux développeurs et aux administrateurs système de déboguer et d'analyser le comportement des applications en montrant les interactions entre le programme et le noyau du système d'exploitation.

## Usage
La syntaxe de base de la commande `strace` est la suivante :

```csh
strace [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `strace` :

- `-c` : Résume les statistiques des appels système effectués.
- `-e` : Filtre les appels système à tracer (par exemple, `-e trace=open` pour tracer uniquement les appels `open`).
- `-o <fichier>` : Redirige la sortie vers un fichier au lieu de l'afficher sur la console.
- `-p <pid>` : Attache `strace` à un processus existant en spécifiant son identifiant de processus (PID).
- `-f` : Suit les processus fils créés par le programme traqué.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `strace` :

1. Suivre un programme simple :
   ```csh
   strace ls
   ```

2. Rediriger la sortie vers un fichier :
   ```csh
   strace -o sortie.txt ls
   ```

3. Analyser les appels système avec un résumé :
   ```csh
   strace -c ls
   ```

4. Suivre un processus existant :
   ```csh
   strace -p 1234
   ```

5. Filtrer pour ne tracer que les appels `open` :
   ```csh
   strace -e trace=open ls
   ```

## Tips
- Utilisez l'option `-o` pour enregistrer les résultats dans un fichier, ce qui facilite l'analyse ultérieure.
- Combinez `-c` avec d'autres options pour obtenir un résumé des performances des appels système.
- Soyez prudent lors de l'utilisation de `strace` sur des programmes critiques, car cela peut affecter leur performance.