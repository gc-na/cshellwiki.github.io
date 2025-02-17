# [Linux] Bash cksum : Calculer le checksum d'un fichier

## Overview
La commande `cksum` est utilisée pour calculer et afficher le checksum (somme de contrôle) d'un fichier, ainsi que la taille du fichier en octets. Cela peut être utile pour vérifier l'intégrité des fichiers ou pour comparer des fichiers.

## Usage
La syntaxe de base de la commande `cksum` est la suivante :

```bash
cksum [options] [arguments]
```

## Common Options
- `-a, --algorithm=ALGO` : Spécifie l'algorithme de checksum à utiliser (par exemple, md5, sha256).
- `-h, --help` : Affiche l'aide et les options disponibles pour la commande.
- `-V, --version` : Affiche la version de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cksum` :

1. Calculer le checksum d'un fichier :
   ```bash
   cksum mon_fichier.txt
   ```

2. Calculer le checksum de plusieurs fichiers :
   ```bash
   cksum fichier1.txt fichier2.txt
   ```

3. Utiliser une option pour afficher l'aide :
   ```bash
   cksum --help
   ```

4. Calculer le checksum d'un fichier avec un algorithme spécifique (si supporté) :
   ```bash
   cksum -a md5 mon_fichier.txt
   ```

## Tips
- Utilisez `cksum` pour vérifier l'intégrité des fichiers après un transfert ou une sauvegarde.
- Combinez `cksum` avec d'autres commandes comme `find` pour vérifier plusieurs fichiers dans un répertoire.
- Pensez à rediriger la sortie vers un fichier si vous souhaitez conserver un enregistrement des checksums :
  ```bash
  cksum mon_fichier.txt > checksums.txt
  ```