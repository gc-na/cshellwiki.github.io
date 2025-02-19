# [Linux] C Shell (csh) mkfifo : Créer des fichiers FIFO

## Overview
La commande `mkfifo` est utilisée pour créer des fichiers FIFO (First In, First Out) dans le système de fichiers. Ces fichiers permettent la communication entre différents processus en utilisant un mécanisme de file d'attente.

## Usage
La syntaxe de base de la commande `mkfifo` est la suivante :

```csh
mkfifo [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `mkfifo` :

- `-m` : Définit les permissions du fichier FIFO créé. Par exemple, `-m 644` donnera des permissions de lecture et d'écriture au propriétaire, et de lecture aux autres.
- `--help` : Affiche l'aide et les options disponibles pour la commande.
- `--version` : Affiche la version de la commande `mkfifo`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `mkfifo` :

1. **Créer un fichier FIFO simple :**
   ```csh
   mkfifo mon_fifo
   ```

2. **Créer un fichier FIFO avec des permissions spécifiques :**
   ```csh
   mkfifo -m 666 mon_fifo
   ```

3. **Créer plusieurs fichiers FIFO à la fois :**
   ```csh
   mkfifo fifo1 fifo2 fifo3
   ```

4. **Vérifier la création du fichier FIFO :**
   ```csh
   ls -l mon_fifo
   ```

## Tips
- Assurez-vous de supprimer le fichier FIFO après utilisation avec `rm mon_fifo` pour éviter de laisser des fichiers inutiles dans le système.
- Utilisez des noms de fichiers descriptifs pour vos FIFOs afin de faciliter leur identification dans des scripts ou des programmes.
- Testez toujours les permissions de votre fichier FIFO pour vous assurer que les processus peuvent y accéder comme prévu.