# [Linux] C Shell (csh) sha512sum : Calculer des sommes de contrôle SHA-512

## Overview
La commande `sha512sum` est utilisée pour calculer et vérifier les sommes de contrôle SHA-512 d'un fichier. Cela permet de garantir l'intégrité des données en s'assurant qu'un fichier n'a pas été modifié.

## Usage
La syntaxe de base de la commande est la suivante :

```csh
sha512sum [options] [arguments]
```

## Common Options
- `-b` : Traite les fichiers en mode binaire.
- `-c` : Vérifie les sommes de contrôle à partir d'un fichier.
- `--help` : Affiche l'aide et les options disponibles.
- `--version` : Affiche la version de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `sha512sum` :

1. **Calculer la somme de contrôle d'un fichier :**
   ```csh
   sha512sum mon_fichier.txt
   ```

2. **Vérifier les sommes de contrôle à partir d'un fichier :**
   ```csh
   sha512sum -c sommes.txt
   ```

3. **Calculer la somme de contrôle d'un fichier en mode binaire :**
   ```csh
   sha512sum -b mon_fichier.bin
   ```

4. **Afficher l'aide de la commande :**
   ```csh
   sha512sum --help
   ```

## Tips
- Toujours vérifier les sommes de contrôle après le téléchargement de fichiers importants pour s'assurer qu'ils n'ont pas été corrompus.
- Utilisez le fichier de sommes de contrôle pour vérifier plusieurs fichiers en une seule commande.
- Pensez à rediriger la sortie vers un fichier si vous souhaitez conserver les sommes de contrôle pour une utilisation future :
  ```csh
  sha512sum mon_fichier.txt > somme.txt
  ```