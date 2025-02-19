# [Linux] C Shell (csh) xz : Compression de fichiers

## Overview
La commande `xz` est utilisée pour compresser et décompresser des fichiers en utilisant l'algorithme de compression LZMA. Elle est particulièrement efficace pour réduire la taille des fichiers, ce qui facilite le stockage et le transfert.

## Usage
La syntaxe de base de la commande `xz` est la suivante :

```bash
xz [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `xz` :

- `-d` ou `--decompress` : Décompresse un fichier.
- `-k` ou `--keep` : Garde le fichier d'origine après compression.
- `-f` ou `--force` : Force la compression ou la décompression, même si cela écrase des fichiers existants.
- `-9` : Utilise le niveau de compression maximum (1 à 9, où 9 est le plus élevé).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `xz` :

1. **Compresser un fichier :**
   ```bash
   xz fichier.txt
   ```

2. **Décompresser un fichier :**
   ```bash
   xz -d fichier.txt.xz
   ```

3. **Compresser en gardant le fichier d'origine :**
   ```bash
   xz -k fichier.txt
   ```

4. **Compresser avec le niveau de compression maximum :**
   ```bash
   xz -9 fichier.txt
   ```

5. **Forcer la compression :**
   ```bash
   xz -f fichier.txt
   ```

## Tips
- Utilisez l'option `-k` si vous souhaitez conserver le fichier original après compression.
- Pour des fichiers très volumineux, envisagez d'utiliser le niveau de compression `-9` pour obtenir une taille de fichier plus réduite, mais cela peut prendre plus de temps.
- Vérifiez toujours l'espace disque disponible avant de compresser de gros fichiers, car la compression peut temporairement nécessiter plus d'espace.