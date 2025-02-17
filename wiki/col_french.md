# [Linux] Bash col : Afficher du texte formaté

## Overview
La commande `col` est utilisée pour filtrer le texte formaté, en supprimant les caractères de contrôle et en produisant une sortie propre et lisible. Elle est souvent utilisée pour traiter des fichiers contenant des séquences de contrôle, comme ceux générés par des commandes de pagination.

## Usage
La syntaxe de base de la commande `col` est la suivante :

```bash
col [options] [arguments]
```

## Common Options
- `-b` : Ignore les séquences de contrôle de retour arrière.
- `-x` : Utilise le mode de tabulation "expansé" pour traiter les tabulations.
- `-f` : Traite les caractères de contrôle de formatage comme des espaces.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `col` :

1. **Filtrer un fichier avec des séquences de contrôle :**
   ```bash
   col < fichier_avec_formatage.txt > fichier_propre.txt
   ```

2. **Afficher le contenu d'un fichier tout en supprimant les retours arrière :**
   ```bash
   col -b < fichier_avec_retours_arriere.txt
   ```

3. **Utiliser col avec un pipe pour nettoyer la sortie d'une commande :**
   ```bash
   dmesg | col -b
   ```

4. **Traiter un fichier avec des tabulations :**
   ```bash
   col -x < fichier_avec_tabulations.txt
   ```

## Tips
- Utilisez `col` en combinaison avec d'autres commandes pour nettoyer la sortie avant de l'afficher ou de l'enregistrer.
- Vérifiez toujours le contenu de votre fichier d'entrée pour vous assurer qu'il contient des séquences de contrôle que vous souhaitez filtrer.
- Pensez à rediriger la sortie vers un nouveau fichier pour conserver l'original intact.