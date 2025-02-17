# [Linux] Bash hostnamectl : Gérer les paramètres d'hôte du système

## Overview
La commande `hostnamectl` est utilisée pour afficher et modifier les paramètres d'hôte du système, tels que le nom d'hôte, le nom d'icône, et d'autres informations liées à l'identité du système.

## Usage
La syntaxe de base de la commande `hostnamectl` est la suivante :

```bash
hostnamectl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `hostnamectl` :

- `set-hostname` : Définit le nom d'hôte du système.
- `set-icon-name` : Définit le nom de l'icône du système.
- `set-chassis` : Définit le type de châssis du système (ex. : desktop, laptop).
- `status` : Affiche l'état actuel des paramètres d'hôte.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `hostnamectl` :

1. **Afficher l'état actuel des paramètres d'hôte :**
   ```bash
   hostnamectl status
   ```

2. **Définir un nouveau nom d'hôte :**
   ```bash
   hostnamectl set-hostname mon-nouveau-nom
   ```

3. **Définir le nom de l'icône :**
   ```bash
   hostnamectl set-icon-name mon-icone
   ```

4. **Définir le type de châssis :**
   ```bash
   hostnamectl set-chassis laptop
   ```

## Tips
- Assurez-vous d'exécuter `hostnamectl` avec des privilèges administratifs (par exemple, en utilisant `sudo`) pour modifier les paramètres d'hôte.
- Vérifiez toujours l'état actuel après avoir effectué des modifications pour vous assurer qu'elles ont été appliquées correctement.
- Utilisez des noms d'hôte significatifs qui reflètent la fonction ou l'emplacement du système pour faciliter la gestion des réseaux.