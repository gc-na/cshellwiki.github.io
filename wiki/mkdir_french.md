# [Linux] C Shell (csh) mkdir Utilisation : Créer des répertoires

## Overview
La commande `mkdir` est utilisée pour créer de nouveaux répertoires dans le système de fichiers. Elle permet aux utilisateurs d'organiser leurs fichiers en créant des dossiers.

## Usage
La syntaxe de base de la commande `mkdir` est la suivante :

```csh
mkdir [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mkdir` :

- `-p` : Crée des répertoires parents si nécessaire. Par exemple, si vous essayez de créer un répertoire dans un chemin qui n'existe pas encore, cette option créera tous les répertoires parents requis.
- `-m` : Définit les permissions du répertoire à créer. Vous pouvez spécifier les permissions en utilisant une notation octale.
- `-v` : Affiche un message pour chaque répertoire créé, ce qui peut être utile pour le débogage.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mkdir` :

1. Créer un répertoire simple :

```csh
mkdir mon_dossier
```

2. Créer plusieurs répertoires à la fois :

```csh
mkdir dossier1 dossier2 dossier3
```

3. Créer un répertoire avec des répertoires parents :

```csh
mkdir -p parent/enfant
```

4. Créer un répertoire avec des permissions spécifiques :

```csh
mkdir -m 755 mon_dossier
```

5. Créer un répertoire et afficher un message :

```csh
mkdir -v mon_dossier
```

## Tips
- Utilisez l'option `-p` lorsque vous n'êtes pas sûr que le chemin parent existe déjà, cela évite les erreurs.
- Vérifiez les permissions de votre répertoire après sa création pour vous assurer qu'elles sont correctes, surtout si vous utilisez l'option `-m`.
- N'hésitez pas à utiliser l'option `-v` pour confirmer que vos répertoires ont été créés avec succès, surtout lorsque vous créez plusieurs répertoires en une seule commande.