# [Linux] Bash blkid Utilisation : Identifier les systèmes de fichiers

## Overview
La commande `blkid` est utilisée pour afficher les informations sur les périphériques de bloc, notamment les systèmes de fichiers et les UUID (identifiants uniques universels) associés. C'est un outil essentiel pour gérer les disques et les partitions sur un système Linux.

## Usage
La syntaxe de base de la commande `blkid` est la suivante :

```bash
blkid [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `blkid` :

- `-o` : Spécifie le format de sortie (par exemple, `value`, `full`, `list`).
- `-s` : Sélectionne un attribut spécifique à afficher (par exemple, `UUID`, `TYPE`).
- `-p` : Ignore les périphériques qui ne sont pas montés.
- `-c` : Spécifie un fichier de cache à utiliser.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `blkid` :

1. **Afficher toutes les informations sur les périphériques de bloc :**
   ```bash
   blkid
   ```

2. **Afficher uniquement les UUID des systèmes de fichiers :**
   ```bash
   blkid -s UUID
   ```

3. **Afficher les informations au format de valeur :**
   ```bash
   blkid -o value
   ```

4. **Afficher les informations d'un périphérique spécifique :**
   ```bash
   blkid /dev/sda1
   ```

5. **Utiliser un fichier de cache pour accélérer la recherche :**
   ```bash
   blkid -c /tmp/blkid.cache
   ```

## Tips
- Utilisez `blkid` avec des privilèges d'administrateur (par exemple, avec `sudo`) pour obtenir des informations complètes sur tous les périphériques.
- Pensez à utiliser l'option `-o` pour formater la sortie selon vos besoins, ce qui peut être utile pour les scripts.
- Vérifiez régulièrement les UUID de vos partitions, surtout si vous modifiez la configuration de votre système ou si vous ajoutez de nouveaux disques.