# [Linux] C Shell (csh) blkid : Identifier les systèmes de fichiers

## Overview
La commande `blkid` est utilisée pour identifier les systèmes de fichiers sur les périphériques de stockage. Elle affiche des informations sur les partitions, y compris leur type et leur UUID (Identifiant Universel Unique).

## Usage
La syntaxe de base de la commande `blkid` est la suivante :

```csh
blkid [options] [arguments]
```

## Common Options
- `-o` : Spécifie le format de sortie (par exemple, `value`, `full`, `list`).
- `-s` : Sélectionne les attributs à afficher (par exemple, `UUID`, `TYPE`).
- `-p` : Ignore les périphériques qui ne sont pas montés.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `blkid` :

1. **Afficher toutes les partitions et leurs informations :**
   ```csh
   blkid
   ```

2. **Afficher uniquement le type de système de fichiers et l'UUID :**
   ```csh
   blkid -s TYPE -s UUID
   ```

3. **Afficher les informations d'un périphérique spécifique :**
   ```csh
   blkid /dev/sda1
   ```

4. **Afficher les informations au format "value" :**
   ```csh
   blkid -o value -s UUID /dev/sda1
   ```

## Tips
- Utilisez `sudo` si vous rencontrez des problèmes d'autorisation lors de l'exécution de `blkid`.
- Combinez `blkid` avec d'autres commandes comme `grep` pour filtrer les résultats.
- Vérifiez régulièrement les UUID de vos partitions, surtout après des changements de configuration ou de matériel.