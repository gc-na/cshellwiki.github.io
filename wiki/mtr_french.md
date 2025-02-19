# [Système d'exploitation] C Shell (csh) mtr utilisation : outil de diagnostic réseau

## Overview
La commande `mtr` (My Traceroute) est un outil de diagnostic réseau qui combine les fonctionnalités de `traceroute` et `ping`. Elle permet d'analyser le chemin emprunté par les paquets de données vers une destination spécifique et de mesurer la latence à chaque étape.

## Usage
La syntaxe de base de la commande est la suivante :

```csh
mtr [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mtr` :

- `-r` : Exécute un rapport et sort les résultats dans un format lisible.
- `-c <count>` : Spécifie le nombre de paquets à envoyer à chaque saut.
- `-i <interval>` : Définit l'intervalle entre les paquets envoyés.
- `-p` : Affiche les numéros de port dans les résultats.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mtr` :

1. Pour effectuer un test de connectivité vers un hôte :

   ```csh
   mtr example.com
   ```

2. Pour exécuter un rapport avec un nombre spécifique de paquets :

   ```csh
   mtr -r -c 10 example.com
   ```

3. Pour définir un intervalle de 1 seconde entre les paquets :

   ```csh
   mtr -i 1 example.com
   ```

4. Pour afficher les numéros de port dans les résultats :

   ```csh
   mtr -p example.com
   ```

## Tips
- Utilisez l'option `-r` pour obtenir un rapport clair et concis lorsque vous partagez des résultats avec d'autres.
- Augmentez le nombre de paquets avec `-c` pour obtenir des résultats plus fiables, surtout si vous rencontrez des pertes de paquets.
- Pensez à exécuter `mtr` avec des privilèges d'administrateur si vous avez besoin d'informations plus détaillées sur les routes réseau.