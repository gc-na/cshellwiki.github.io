# [Linux] Bash fsck : Vérification et réparation des systèmes de fichiers

## Overview
La commande `fsck` (File System Consistency Check) est utilisée pour vérifier et réparer les systèmes de fichiers sous Linux. Elle permet de s'assurer que le système de fichiers est en bon état et de corriger les erreurs qui pourraient affecter la stabilité et la performance du système.

## Usage
La syntaxe de base de la commande `fsck` est la suivante :

```bash
fsck [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `fsck` :

- `-a` : Répare automatiquement les erreurs sans demander confirmation.
- `-n` : Effectue une vérification sans apporter de modifications (mode "lecture seule").
- `-y` : Répond "oui" à toutes les questions posées pendant la vérification.
- `-t` : Affiche le temps pris pour chaque étape de la vérification.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fsck` :

1. Vérifier un système de fichiers spécifique :
   ```bash
   fsck /dev/sda1
   ```

2. Vérifier tous les systèmes de fichiers dans `/etc/fstab` :
   ```bash
   fsck -A
   ```

3. Réparer automatiquement les erreurs sur un système de fichiers :
   ```bash
   fsck -a /dev/sda1
   ```

4. Effectuer une vérification sans apporter de modifications :
   ```bash
   fsck -n /dev/sda1
   ```

5. Répondre "oui" à toutes les questions lors de la réparation :
   ```bash
   fsck -y /dev/sda1
   ```

## Tips
- Toujours effectuer une sauvegarde des données importantes avant d'utiliser `fsck`, car des erreurs peuvent survenir lors de la réparation.
- Utilisez `fsck` sur un système de fichiers démonté pour éviter des problèmes supplémentaires.
- Pour les systèmes de fichiers très endommagés, il peut être préférable d'utiliser des outils spécifiques au système de fichiers, comme `e2fsck` pour les systèmes ext2/ext3/ext4.