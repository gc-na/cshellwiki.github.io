# [Linux] C Shell (csh) netstat : Afficher les connexions réseau

## Overview
La commande `netstat` est utilisée pour afficher des informations sur les connexions réseau, les tables de routage, et les statistiques d'interface. Elle est très utile pour diagnostiquer les problèmes de réseau et pour surveiller l'état des connexions.

## Usage
La syntaxe de base de la commande est la suivante :

```csh
netstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `netstat` :

- `-a` : Affiche toutes les connexions et les ports d'écoute.
- `-n` : Affiche les adresses et numéros de port sous forme numérique.
- `-r` : Affiche la table de routage.
- `-i` : Affiche les statistiques des interfaces réseau.
- `-s` : Affiche les statistiques par protocole.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `netstat` :

1. Afficher toutes les connexions et ports d'écoute :
   ```csh
   netstat -a
   ```

2. Afficher les connexions avec des adresses numériques :
   ```csh
   netstat -n
   ```

3. Afficher la table de routage :
   ```csh
   netstat -r
   ```

4. Afficher les statistiques des interfaces réseau :
   ```csh
   netstat -i
   ```

5. Afficher les statistiques par protocole :
   ```csh
   netstat -s
   ```

## Tips
- Utilisez l'option `-n` pour accélérer l'affichage des résultats, surtout sur des réseaux avec de nombreux noms d'hôtes.
- Combinez plusieurs options pour obtenir des informations plus détaillées, par exemple `netstat -an` pour voir toutes les connexions avec des adresses numériques.
- Pensez à exécuter `netstat` avec des privilèges d'administrateur pour accéder à des informations complètes sur les connexions réseau.