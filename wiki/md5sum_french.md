# [Linux] Bash md5sum : Calculer des sommes de contrôle MD5

## Overview
La commande `md5sum` est utilisée pour calculer et vérifier les sommes de contrôle MD5 d'un fichier. Cela permet de garantir l'intégrité des données en vérifiant si le contenu d'un fichier a été modifié.

## Usage
La syntaxe de base de la commande `md5sum` est la suivante :

```bash
md5sum [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `md5sum` :

- `-b` : Traite les fichiers en mode binaire.
- `-c` : Vérifie les sommes de contrôle à partir d'un fichier.
- `-t` : Calcule la somme de contrôle pour les fichiers texte.
- `--help` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `md5sum` :

1. **Calculer la somme de contrôle d'un fichier :**

   ```bash
   md5sum mon_fichier.txt
   ```

2. **Enregistrer la somme de contrôle dans un fichier :**

   ```bash
   md5sum mon_fichier.txt > somme.md5
   ```

3. **Vérifier les sommes de contrôle à partir d'un fichier :**

   ```bash
   md5sum -c somme.md5
   ```

4. **Calculer la somme de contrôle d'un fichier binaire :**

   ```bash
   md5sum -b mon_fichier_binaire.bin
   ```

## Tips
- Utilisez `md5sum` pour vérifier les fichiers téléchargés afin de vous assurer qu'ils n'ont pas été corrompus.
- Gardez une copie des sommes de contrôle dans un fichier pour une vérification future.
- Évitez d'utiliser MD5 pour des applications de sécurité critiques, car il est considéré comme vulnérable aux collisions.