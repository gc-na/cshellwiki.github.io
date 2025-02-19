# [Linux] C Shell (csh) vgs : [afficher des groupes de volumes]

## Overview
La commande `vgs` est utilisée pour afficher des informations sur les groupes de volumes dans un système de gestion de volumes logiques (LVM). Elle fournit des détails sur les groupes de volumes, tels que leur nom, leur taille, et l'espace utilisé.

## Usage
La syntaxe de base de la commande `vgs` est la suivante :

```csh
vgs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `vgs` :

- `-o` : Spécifie les colonnes à afficher.
- `--units` : Définit les unités d'affichage pour les tailles.
- `-h` : Affiche l'aide et les options disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `vgs` :

1. **Afficher tous les groupes de volumes :**
   ```csh
   vgs
   ```

2. **Afficher des colonnes spécifiques (nom et taille) :**
   ```csh
   vgs -o vg_name,size
   ```

3. **Afficher les groupes de volumes avec des unités spécifiques :**
   ```csh
   vgs --units g
   ```

4. **Afficher l'aide pour la commande :**
   ```csh
   vgs -h
   ```

## Tips
- Utilisez l'option `-o` pour personnaliser les informations affichées selon vos besoins.
- Pensez à utiliser `--units` pour faciliter la lecture des tailles, surtout si vous travaillez avec de grands volumes.
- Vérifiez régulièrement l'état de vos groupes de volumes pour éviter des problèmes de gestion d'espace.