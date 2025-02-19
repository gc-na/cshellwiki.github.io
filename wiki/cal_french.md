# [Linux] C Shell (csh) cal <Utilisation équivalente en français> : Afficher un calendrier

## Overview
La commande `cal` dans C Shell (csh) est utilisée pour afficher un calendrier dans le terminal. Elle permet de visualiser le calendrier d'un mois ou d'une année spécifique, facilitant ainsi la planification et la gestion du temps.

## Usage
La syntaxe de base de la commande `cal` est la suivante :

```csh
cal [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `cal` :

- `-m` : Affiche le calendrier en commençant par le lundi.
- `-3` : Affiche le calendrier du mois précédent, du mois actuel et du mois suivant.
- `-y` : Affiche le calendrier de l'année en cours.
- `-j` : Affiche le calendrier avec les jours de l'année.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cal` :

- Afficher le calendrier du mois actuel :
  ```csh
  cal
  ```

- Afficher le calendrier d'un mois spécifique, par exemple, mars 2023 :
  ```csh
  cal 03 2023
  ```

- Afficher le calendrier de l'année 2023 :
  ```csh
  cal -y 2023
  ```

- Afficher le calendrier des trois mois consécutifs :
  ```csh
  cal -3
  ```

## Tips
- Utilisez l'option `-m` si vous préférez que la semaine commence par le lundi.
- Pour une vue d'ensemble de l'année, l'option `-y` est très utile.
- N'hésitez pas à combiner les options pour personnaliser l'affichage selon vos besoins.