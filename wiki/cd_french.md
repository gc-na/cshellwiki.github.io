# [Linux] C Shell (csh) cd : Changer de répertoire

## Overview
La commande `cd` (change directory) permet de naviguer entre les répertoires dans le système de fichiers. Elle est essentielle pour se déplacer dans l'arborescence des fichiers et accéder aux fichiers et dossiers souhaités.

## Usage
La syntaxe de base de la commande `cd` est la suivante :

```csh
cd [options] [arguments]
```

## Common Options
- `..` : Permet de remonter d'un niveau dans l'arborescence des répertoires.
- `-` : Retourne au dernier répertoire visité.
- `~` : Accède au répertoire personnel de l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cd` :

1. **Accéder à un répertoire spécifique :**
   ```csh
   cd /chemin/vers/le/répertoire
   ```

2. **Remonter d'un niveau :**
   ```csh
   cd ..
   ```

3. **Retourner au dernier répertoire :**
   ```csh
   cd -
   ```

4. **Accéder au répertoire personnel :**
   ```csh
   cd ~
   ```

5. **Accéder à un sous-répertoire :**
   ```csh
   cd mon_dossier/sous_dossier
   ```

## Tips
- Utilisez `cd -` pour naviguer rapidement entre deux répertoires.
- Pour éviter les erreurs, utilisez des chemins absolus lorsque vous n'êtes pas sûr de votre position actuelle dans l'arborescence.
- N'oubliez pas que les chemins sont sensibles à la casse, donc `Dossier` et `dossier` sont considérés comme différents.