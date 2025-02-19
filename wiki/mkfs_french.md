# [Linux] C Shell (csh) mkfs : Créer un système de fichiers

## Overview
La commande `mkfs` (make filesystem) est utilisée pour créer un système de fichiers sur un périphérique de stockage. Cela permet de préparer un disque ou une partition pour y stocker des données de manière organisée.

## Usage
La syntaxe de base de la commande `mkfs` est la suivante :

```csh
mkfs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mkfs` :

- `-t <type>` : Spécifie le type de système de fichiers à créer (par exemple, ext4, vfat).
- `-L <label>` : Attribue une étiquette au système de fichiers créé.
- `-n` : Crée un système de fichiers sans le formater (mode dry-run).
- `-V` : Affiche des informations détaillées sur le processus de création.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `mkfs` :

1. Créer un système de fichiers ext4 sur une partition :
   ```csh
   mkfs -t ext4 /dev/sda1
   ```

2. Créer un système de fichiers vfat avec une étiquette :
   ```csh
   mkfs -t vfat -L "MonDisque" /dev/sdb1
   ```

3. Créer un système de fichiers ext3 sans formater (simulation) :
   ```csh
   mkfs -n -t ext3 /dev/sdc1
   ```

4. Afficher des informations détaillées lors de la création d'un système de fichiers :
   ```csh
   mkfs -V -t ext4 /dev/sdd1
   ```

## Tips
- Assurez-vous de sauvegarder toutes les données importantes avant d'utiliser `mkfs`, car cela effacera toutes les informations sur le périphérique.
- Vérifiez le périphérique cible avec `lsblk` ou `fdisk -l` pour éviter de formater le mauvais disque.
- Utilisez l'option `-n` pour tester la commande sans effectuer de modifications réelles, ce qui est utile pour vérifier les paramètres avant l'exécution.