# [Linux] Bash lvextend : Étendre un volume logique

## Overview
La commande `lvextend` est utilisée pour augmenter la taille d'un volume logique dans un système de gestion de volumes logiques (LVM). Cela permet d'allouer plus d'espace à un volume existant sans avoir à le recréer.

## Usage
La syntaxe de base de la commande `lvextend` est la suivante :

```bash
lvextend [options] [arguments]
```

## Common Options
- `-L +size` : Ajoute une taille spécifique au volume logique.
- `-l +size` : Ajoute un nombre de blocs au volume logique.
- `-r` : Redimensionne le système de fichiers automatiquement après l'extension du volume.
- `-n` : Change le nom du volume logique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `lvextend` :

1. **Étendre un volume logique de 10 Go :**
   ```bash
   lvextend -L +10G /dev/vg01/lv01
   ```

2. **Étendre un volume logique en utilisant des blocs :**
   ```bash
   lvextend -l +100 /dev/vg01/lv01
   ```

3. **Étendre un volume logique et redimensionner le système de fichiers automatiquement :**
   ```bash
   lvextend -r -L +5G /dev/vg01/lv01
   ```

4. **Changer le nom d'un volume logique :**
   ```bash
   lvextend -n new_lv_name /dev/vg01/lv01
   ```

## Tips
- Avant d'étendre un volume logique, assurez-vous que l'espace disponible dans le groupe de volumes est suffisant.
- Utilisez l'option `-r` pour redimensionner automatiquement le système de fichiers, ce qui simplifie le processus.
- Vérifiez toujours l'état du volume logique après l'extension avec `lvdisplay` pour confirmer les modifications.