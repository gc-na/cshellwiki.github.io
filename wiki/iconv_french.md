# [Linux] C Shell (csh) iconv : Convertir des fichiers entre différents encodages

## Overview
La commande `iconv` est utilisée pour convertir des fichiers texte d'un encodage à un autre. Cela est particulièrement utile lorsque vous travaillez avec des fichiers qui utilisent différents jeux de caractères, permettant ainsi une meilleure compatibilité entre les systèmes.

## Usage
La syntaxe de base de la commande `iconv` est la suivante :

```csh
iconv [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `iconv` :

- `-f` : Spécifie l'encodage d'entrée (par défaut UTF-8).
- `-t` : Spécifie l'encodage de sortie (par défaut UTF-8).
- `-o` : Permet de rediriger la sortie vers un fichier spécifié.
- `-c` : Ignore les caractères non valides dans le texte d'entrée.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `iconv` :

1. Convertir un fichier de l'encodage ISO-8859-1 à UTF-8 :

   ```csh
   iconv -f ISO-8859-1 -t UTF-8 fichier.txt -o fichier_utf8.txt
   ```

2. Convertir un fichier de l'encodage UTF-16 à UTF-8 :

   ```csh
   iconv -f UTF-16 -t UTF-8 fichier_utf16.txt -o fichier_utf8.txt
   ```

3. Ignorer les caractères non valides lors de la conversion :

   ```csh
   iconv -f ISO-8859-1 -t UTF-8 -c fichier.txt -o fichier_utf8.txt
   ```

## Tips
- Assurez-vous de connaître les encodages d'entrée et de sortie appropriés pour éviter des erreurs de conversion.
- Utilisez l'option `-o` pour éviter d'écraser le fichier d'origine, surtout si vous n'êtes pas sûr du résultat.
- Testez la conversion sur un petit échantillon de données avant de l'appliquer à des fichiers plus volumineux.