# [Linux] Bash sha256sum : Calculer des sommes de contrôle SHA-256

## Overview
La commande `sha256sum` est utilisée pour calculer et vérifier les sommes de contrôle SHA-256 d'un fichier. Cela permet de garantir l'intégrité des données en s'assurant que le contenu d'un fichier n'a pas été altéré.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
sha256sum [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `sha256sum` :

- `-b` : Traite les fichiers en mode binaire.
- `-c` : Vérifie les sommes de contrôle à partir d'un fichier.
- `-o` : Spécifie un fichier de sortie pour les résultats.
- `--quiet` : Ne produit aucune sortie sauf en cas d'erreur.

## Common Examples

### Calculer la somme de contrôle d'un fichier
Pour calculer la somme de contrôle SHA-256 d'un fichier nommé `fichier.txt`, utilisez la commande suivante :

```bash
sha256sum fichier.txt
```

### Vérifier une somme de contrôle à partir d'un fichier
Si vous avez un fichier `somme.txt` contenant des sommes de contrôle, vous pouvez les vérifier avec :

```bash
sha256sum -c somme.txt
```

### Calculer la somme de contrôle de plusieurs fichiers
Pour calculer les sommes de contrôle de plusieurs fichiers à la fois, vous pouvez les lister :

```bash
sha256sum fichier1.txt fichier2.txt fichier3.txt
```

### Rediriger la sortie vers un fichier
Pour enregistrer la somme de contrôle dans un fichier, utilisez la redirection :

```bash
sha256sum fichier.txt > somme.txt
```

## Tips
- Assurez-vous de vérifier les sommes de contrôle après le téléchargement de fichiers importants pour garantir leur intégrité.
- Utilisez l'option `-c` pour vérifier plusieurs fichiers à la fois en utilisant un fichier de sommes de contrôle.
- Pensez à utiliser l'option `--quiet` si vous souhaitez réduire le bruit dans les sorties, surtout lors de vérifications de masse.