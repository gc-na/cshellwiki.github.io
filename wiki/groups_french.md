# [Linux] Bash groups : Afficher les groupes d'un utilisateur

## Overview
La commande `groups` permet d'afficher les groupes auxquels un utilisateur appartient. Cela peut être utile pour vérifier les permissions d'accès et les rôles d'un utilisateur dans un système.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
groups [options] [arguments]
```

## Common Options
- `-h`, `--help` : Affiche l'aide et quitte.
- `-v`, `--version` : Affiche la version de la commande et quitte.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `groups` :

1. **Afficher les groupes de l'utilisateur courant :**
   ```bash
   groups
   ```

2. **Afficher les groupes d'un utilisateur spécifique :**
   ```bash
   groups nom_utilisateur
   ```

3. **Afficher les groupes d'un utilisateur avec des options :**
   ```bash
   groups -h
   ```

## Tips
- Utilisez `groups` sans arguments pour rapidement vérifier les groupes de l'utilisateur connecté.
- Pour des scripts, vous pouvez rediriger la sortie de `groups` vers un fichier pour une analyse ultérieure.
- Vérifiez régulièrement les groupes des utilisateurs pour maintenir une bonne gestion des permissions dans votre système.