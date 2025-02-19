# [Linux] C Shell (csh) basename Utilisation : Extraire le nom de fichier sans chemin

## Overview
La commande `basename` est utilisée pour extraire le nom d'un fichier à partir d'un chemin complet, en supprimant le répertoire et l'extension de fichier si nécessaire. Cela permet de travailler plus facilement avec les noms de fichiers dans des scripts ou des commandes.

## Usage
La syntaxe de base de la commande `basename` est la suivante :

```csh
basename [options] [arguments]
```

## Common Options
- `-s, --suffix`: Permet de supprimer une suffixe spécifique du nom de fichier.
- `-a, --multiple`: Traite plusieurs arguments et renvoie le nom de base pour chacun.

## Common Examples

1. **Extraire le nom de fichier d'un chemin complet :**

```csh
basename /home/user/documents/fichier.txt
```
*Sortie :* `fichier.txt`

2. **Supprimer une extension de fichier :**

```csh
basename /home/user/documents/fichier.txt .txt
```
*Sortie :* `fichier`

3. **Traiter plusieurs fichiers à la fois :**

```csh
basename -a /home/user/documents/fichier1.txt /home/user/documents/fichier2.txt
```
*Sortie :* 
```
fichier1.txt
fichier2.txt
```

4. **Supprimer un suffixe spécifique :**

```csh
basename -s .txt /home/user/documents/fichier.txt
```
*Sortie :* `fichier`

## Tips
- Utilisez `basename` dans des scripts pour simplifier la gestion des fichiers.
- Combinez `basename` avec d'autres commandes comme `find` pour manipuler efficacement les fichiers.
- Soyez attentif aux extensions de fichiers lorsque vous utilisez l'option `-s` pour éviter des suppressions inattendues.