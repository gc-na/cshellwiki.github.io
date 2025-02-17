# [Linux] Bash cal <Utilisation équivalente en français>: Afficher un calendrier

## Overview
La commande `cal` permet d'afficher un calendrier dans le terminal. Elle peut afficher le calendrier d'un mois spécifique ou d'une année entière, et elle est très utile pour visualiser rapidement les dates.

## Usage
La syntaxe de base de la commande `cal` est la suivante :

```bash
cal [options] [arguments]
```

## Common Options
- `-m` : Affiche le calendrier en commençant par le mois actuel.
- `-y` : Affiche le calendrier de l'année actuelle.
- `-3` : Affiche le mois précédent, le mois actuel et le mois suivant.
- `-j` : Affiche les jours de l'année au lieu des numéros de mois.
- `-h` : Affiche le calendrier sans les jours de la semaine.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cal` :

1. Afficher le calendrier du mois actuel :
   ```bash
   cal
   ```

2. Afficher le calendrier d'un mois spécifique (par exemple, mars 2023) :
   ```bash
   cal 03 2023
   ```

3. Afficher le calendrier de l'année actuelle :
   ```bash
   cal -y
   ```

4. Afficher le calendrier des trois mois (précédent, actuel et suivant) :
   ```bash
   cal -3
   ```

5. Afficher le calendrier avec les jours de l'année :
   ```bash
   cal -j
   ```

## Tips
- Utilisez l'option `-m` pour commencer le calendrier par le mois actuel, ce qui peut être plus intuitif.
- Pensez à combiner les options pour obtenir le format de calendrier qui vous convient le mieux.
- Pour une vue rapide des jours fériés, vous pouvez utiliser `cal` en conjonction avec d'autres commandes pour filtrer les dates importantes.