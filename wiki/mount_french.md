# [Linux] Bash mount utilisation : Monter des systèmes de fichiers

## Overview
La commande `mount` est utilisée pour monter des systèmes de fichiers dans le système d'exploitation Linux. Elle permet d'accéder à des partitions, des disques externes ou des systèmes de fichiers réseau en les intégrant dans l'arborescence des fichiers.

## Usage
La syntaxe de base de la commande `mount` est la suivante :

```bash
mount [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec la commande `mount` :

- `-t type` : Spécifie le type de système de fichiers (par exemple, ext4, ntfs).
- `-o options` : Permet de spécifier des options de montage supplémentaires (comme `ro` pour lecture seule).
- `-a` : Monte tous les systèmes de fichiers énumérés dans `/etc/fstab`.
- `-r` : Monte le système de fichiers en mode lecture seule.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mount` :

1. Monter une partition ext4 :
   ```bash
   mount -t ext4 /dev/sda1 /mnt/mon_part
   ```

2. Monter un disque USB automatiquement :
   ```bash
   mount /dev/sdb1 /media/usb
   ```

3. Monter un système de fichiers en lecture seule :
   ```bash
   mount -o ro /dev/sdc1 /mnt/lecture_seule
   ```

4. Monter tous les systèmes de fichiers définis dans `/etc/fstab` :
   ```bash
   mount -a
   ```

## Tips
- Assurez-vous d'avoir les permissions nécessaires pour monter des systèmes de fichiers, souvent requises pour l'utilisateur root.
- Vérifiez toujours que le point de montage est vide avant de monter un nouveau système de fichiers pour éviter de perdre des données.
- Utilisez la commande `umount` pour démonter un système de fichiers lorsque vous avez terminé de l'utiliser.