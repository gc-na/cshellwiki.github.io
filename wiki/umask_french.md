# [Linux] C Shell (csh) umask : [définir les permissions par défaut des fichiers]

## Overview
La commande `umask` dans C Shell (csh) permet de définir les permissions par défaut pour les nouveaux fichiers et répertoires créés par l'utilisateur. Elle détermine les permissions qui seront retirées des fichiers et répertoires nouvellement créés.

## Usage
La syntaxe de base de la commande `umask` est la suivante :

```csh
umask [options] [arguments]
```

## Common Options
- `-S` : Affiche les permissions sous forme symbolique.
- `-p` : Affiche la valeur actuelle de umask en mode symbolique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `umask` :

1. **Afficher la valeur actuelle de umask :**
   ```csh
   umask
   ```

2. **Définir umask pour retirer les permissions d'écriture pour le groupe et les autres :**
   ```csh
   umask 022
   ```

3. **Définir umask pour retirer toutes les permissions pour les autres :**
   ```csh
   umask 007
   ```

4. **Afficher umask en mode symbolique :**
   ```csh
   umask -S
   ```

5. **Définir umask pour permettre uniquement les permissions de lecture et d'exécution :**
   ```csh
   umask 133
   ```

## Tips
- Pensez à vérifier la valeur de `umask` avant de créer des fichiers sensibles pour vous assurer que les permissions sont appropriées.
- Utilisez `umask -S` pour comprendre facilement les permissions actuelles sous forme symbolique.
- Modifiez `umask` dans votre fichier de configuration de shell (comme `.cshrc`) pour appliquer vos préférences de manière persistante.