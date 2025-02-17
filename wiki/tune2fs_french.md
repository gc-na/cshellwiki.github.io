# [Linux] Bash tune2fs : Modifier les paramètres d'un système de fichiers ext2/ext3/ext4

## Overview
La commande `tune2fs` est utilisée pour modifier les paramètres d'un système de fichiers ext2, ext3 ou ext4. Elle permet d'ajuster divers aspects du système de fichiers, tels que les options de montage, les journaux, et d'autres paramètres de performance.

## Usage
La syntaxe de base de la commande `tune2fs` est la suivante :

```bash
tune2fs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `tune2fs` :

- `-c <nombre>` : Définit le nombre maximum de montages avant que le système de fichiers ne soit vérifié.
- `-i <intervalle>` : Définit l'intervalle entre les vérifications du système de fichiers.
- `-m <pourcentage>` : Définit le pourcentage d'espace réservé pour l'utilisateur root.
- `-o <options>` : Modifie les options de montage du système de fichiers.
- `-L <label>` : Change le label du système de fichiers.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tune2fs` :

1. **Définir le nombre maximum de montages avant vérification :**
   ```bash
   tune2fs -c 30 /dev/sda1
   ```

2. **Définir l'intervalle de vérification à 2 mois :**
   ```bash
   tune2fs -i 2m /dev/sda1
   ```

3. **Réserver 5% de l'espace pour l'utilisateur root :**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Modifier les options de montage :**
   ```bash
   tune2fs -o journal_data /dev/sda1
   ```

5. **Changer le label du système de fichiers :**
   ```bash
   tune2fs -L MonDisque /dev/sda1
   ```

## Tips
- Toujours effectuer une sauvegarde des données avant de modifier les paramètres du système de fichiers.
- Utilisez la commande `dumpe2fs` pour afficher les informations actuelles du système de fichiers avant d'apporter des modifications.
- Soyez prudent avec les options qui peuvent affecter la sécurité et la performance du système de fichiers.