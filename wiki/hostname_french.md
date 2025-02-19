# [Linux] C Shell (csh) hostname Utilisation : Afficher ou définir le nom d'hôte du système

## Overview
La commande `hostname` dans C Shell (csh) est utilisée pour afficher ou définir le nom d'hôte du système. Le nom d'hôte est un identifiant unique qui permet de reconnaître un ordinateur sur un réseau.

## Usage
La syntaxe de base de la commande `hostname` est la suivante :

```csh
hostname [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `hostname` :

- `-s` : Affiche seulement le nom d'hôte court.
- `-f` : Affiche le nom d'hôte complet (FQDN).
- `-i` : Affiche l'adresse IP associée au nom d'hôte.
- `-d` : Affiche le nom de domaine.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `hostname` :

1. Afficher le nom d'hôte actuel :
   ```csh
   hostname
   ```

2. Afficher le nom d'hôte court :
   ```csh
   hostname -s
   ```

3. Afficher le nom d'hôte complet :
   ```csh
   hostname -f
   ```

4. Afficher l'adresse IP du nom d'hôte :
   ```csh
   hostname -i
   ```

5. Définir un nouveau nom d'hôte :
   ```csh
   hostname nouveau_nom
   ```

## Tips
- Assurez-vous d'avoir les permissions nécessaires pour changer le nom d'hôte, car cela peut nécessiter des privilèges administratifs.
- Après avoir changé le nom d'hôte, il peut être nécessaire de redémarrer certains services ou le système pour que les modifications prennent effet.
- Utilisez `hostname -d` pour vérifier rapidement le nom de domaine associé à votre système, ce qui peut être utile pour la configuration réseau.