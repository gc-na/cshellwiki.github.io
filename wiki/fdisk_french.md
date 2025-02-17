# [Linux] Bash fdisk : Gérer les partitions de disque

## Overview
La commande `fdisk` est un utilitaire en ligne de commande utilisé pour gérer les partitions de disque sur les systèmes Linux. Elle permet de créer, supprimer, redimensionner et afficher les informations sur les partitions d'un disque dur.

## Usage
La syntaxe de base de la commande `fdisk` est la suivante :

```bash
fdisk [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `fdisk` :

- `-l` : Liste toutes les partitions sur tous les disques.
- `-u` : Utilise des unités de secteurs pour afficher les tailles de partition.
- `-s` : Affiche la taille d'une partition spécifiée.
- `-n` : Crée une nouvelle partition.
- `-d` : Supprime une partition existante.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `fdisk` :

1. **Lister toutes les partitions :**
   ```bash
   fdisk -l
   ```

2. **Créer une nouvelle partition :**
   ```bash
   fdisk /dev/sda
   ```
   Ensuite, suivez les instructions à l'écran pour créer une nouvelle partition.

3. **Supprimer une partition :**
   ```bash
   fdisk /dev/sda
   ```
   Ensuite, utilisez l'option `d` pour supprimer la partition souhaitée.

4. **Afficher la taille d'une partition :**
   ```bash
   fdisk -s /dev/sda1
   ```

## Tips
- **Sauvegarde des données** : Avant de modifier les partitions, assurez-vous de sauvegarder toutes les données importantes.
- **Utilisation avec précaution** : `fdisk` peut entraîner la perte de données si mal utilisé. Soyez prudent lors de la suppression ou de la modification des partitions.
- **Vérification des partitions** : Après avoir effectué des modifications, utilisez `partprobe` ou `lsblk` pour vérifier que les changements ont été appliqués correctement.