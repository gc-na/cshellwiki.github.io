# [Linux] C Shell (csh) hexdump : Afficher le contenu binaire d'un fichier

## Overview
La commande `hexdump` permet d'afficher le contenu binaire d'un fichier sous forme hexadécimale. Cela est particulièrement utile pour analyser les fichiers non textuels ou pour le débogage.

## Usage
La syntaxe de base de la commande `hexdump` est la suivante :

```csh
hexdump [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `hexdump` :

- `-C` : Affiche le contenu en hexadécimal et en ASCII.
- `-n N` : Limite la sortie aux premiers N octets du fichier.
- `-s N` : Ignore les premiers N octets du fichier avant de commencer à afficher.
- `-v` : Affiche tous les octets, y compris les répétitions.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `hexdump` :

1. Afficher le contenu d'un fichier en hexadécimal :
   ```csh
   hexdump fichier.bin
   ```

2. Afficher le contenu en hexadécimal et ASCII :
   ```csh
   hexdump -C fichier.bin
   ```

3. Limiter l'affichage aux 16 premiers octets :
   ```csh
   hexdump -n 16 fichier.bin
   ```

4. Ignorer les 10 premiers octets et afficher le reste :
   ```csh
   hexdump -s 10 fichier.bin
   ```

5. Afficher tous les octets, y compris les répétitions :
   ```csh
   hexdump -v fichier.bin
   ```

## Tips
- Utilisez l'option `-C` pour obtenir une vue plus lisible avec les valeurs ASCII correspondantes.
- Pour les fichiers volumineux, combinez `-n` et `-s` pour cibler des sections spécifiques du fichier.
- Pensez à rediriger la sortie vers un fichier si vous travaillez avec de grandes quantités de données :
  ```csh
  hexdump fichier.bin > sortie.txt
  ```