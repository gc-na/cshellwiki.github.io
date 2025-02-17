# [Linux] Bash vgs : Afficher des informations sur les groupes de volumes

## Overview
La commande `vgs` est utilisée pour afficher des informations sur les groupes de volumes dans un système utilisant LVM (Logical Volume Manager). Elle permet de visualiser des détails tels que la taille, l'état et le nombre de volumes logiques associés à chaque groupe de volumes.

## Usage
La syntaxe de base de la commande `vgs` est la suivante :

```bash
vgs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `vgs` :

- `-o` : Spécifie les colonnes à afficher.
- `--units` : Définit les unités d'affichage (par exemple, Mo, Go).
- `-h` : Affiche l'aide et les informations sur les options disponibles.
- `-n` : Affiche uniquement les noms des groupes de volumes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `vgs` :

1. **Afficher tous les groupes de volumes :**
   ```bash
   vgs
   ```

2. **Afficher des informations détaillées sur les groupes de volumes avec des colonnes spécifiques :**
   ```bash
   vgs -o +pv_count,lv_count
   ```

3. **Afficher les groupes de volumes avec des unités spécifiques :**
   ```bash
   vgs --units g
   ```

4. **Afficher uniquement les noms des groupes de volumes :**
   ```bash
   vgs -n
   ```

## Tips
- Utilisez l'option `-o` pour personnaliser les informations affichées selon vos besoins.
- Combinez `vgs` avec d'autres commandes LVM comme `lvdisplay` ou `pvdisplay` pour obtenir une vue complète de votre configuration LVM.
- Pensez à exécuter `vgs` avec des privilèges administratifs si vous ne voyez pas tous les groupes de volumes, car certaines informations peuvent nécessiter des autorisations élevées.