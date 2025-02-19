# [Linux] C Shell (csh) mount Utilisation : Monter des systèmes de fichiers

## Overview
La commande `mount` est utilisée pour monter des systèmes de fichiers dans le système d'exploitation. Cela permet d'accéder aux fichiers et répertoires d'un périphérique de stockage, comme un disque dur ou une clé USB, en les rendant disponibles dans l'arborescence des fichiers.

## Usage
La syntaxe de base de la commande `mount` est la suivante :

```
mount [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mount` :

- `-t type` : Spécifie le type de système de fichiers à monter (par exemple, ext4, ntfs).
- `-o options` : Permet de spécifier des options de montage supplémentaires, comme `ro` pour lecture seule ou `rw` pour lecture-écriture.
- `-a` : Monte tous les systèmes de fichiers énumérés dans le fichier `/etc/fstab`.
- `-r` : Monte le système de fichiers en mode lecture seule.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mount` :

1. Monter un périphérique USB :
   ```csh
   mount -t vfat /dev/sdb1 /mnt/usb
   ```

2. Monter un disque dur avec des options de lecture-écriture :
   ```csh
   mount -o rw /dev/sda1 /mnt/disk
   ```

3. Monter tous les systèmes de fichiers définis dans `/etc/fstab` :
   ```csh
   mount -a
   ```

4. Monter un système de fichiers en lecture seule :
   ```csh
   mount -o ro /dev/sdc1 /mnt/readonly
   ```

## Tips
- Assurez-vous d'avoir les permissions nécessaires pour monter des systèmes de fichiers, souvent requises par l'utilisateur root.
- Vérifiez toujours le point de montage avant de monter un nouveau système de fichiers pour éviter les conflits.
- Utilisez la commande `umount` pour démonter un système de fichiers lorsque vous avez terminé de l'utiliser.