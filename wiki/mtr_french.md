# [Linux] Bash mtr Utilisation : Outil de diagnostic de réseau

## Overview
La commande `mtr` (My Traceroute) est un outil de diagnostic de réseau qui combine les fonctionnalités de `ping` et `traceroute`. Elle permet d'analyser la connectivité réseau entre votre machine et une destination, en affichant les routes empruntées par les paquets ainsi que les temps de réponse à chaque saut.

## Usage
La syntaxe de base de la commande `mtr` est la suivante :

```bash
mtr [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mtr` :

- `-r` : Exécute un rapport et quitte.
- `-c <count>` : Spécifie le nombre de paquets à envoyer.
- `-i <interval>` : Définit l'intervalle entre les envois de paquets.
- `-p` : Affiche les adresses IP au lieu des noms d'hôtes.
- `-w` : Affiche la sortie dans un format large.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `mtr` :

1. **Traceroute vers un hôte :**
   ```bash
   mtr example.com
   ```

2. **Exécuter un rapport avec un nombre limité de paquets :**
   ```bash
   mtr -r -c 10 example.com
   ```

3. **Afficher les adresses IP au lieu des noms d'hôtes :**
   ```bash
   mtr -p example.com
   ```

4. **Définir un intervalle de 2 secondes entre les paquets :**
   ```bash
   mtr -i 2 example.com
   ```

## Tips
- Utilisez l'option `-r` pour obtenir un rapport rapide et quitter automatiquement après l'envoi des paquets.
- Pour une analyse continue, exécutez `mtr` sans options, ce qui affichera les résultats en temps réel.
- Vérifiez les résultats pour identifier les sauts où le temps de réponse est élevé, ce qui peut indiquer des problèmes de réseau.