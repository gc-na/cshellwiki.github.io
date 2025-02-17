# [Linux] Bash traceroute : Suivre le chemin des paquets réseau

## Overview
La commande `traceroute` est utilisée pour afficher le chemin que prennent les paquets de données pour atteindre une destination spécifique sur un réseau. Elle permet d'identifier les routeurs intermédiaires et de mesurer le temps de réponse à chaque saut.

## Usage
La syntaxe de base de la commande `traceroute` est la suivante :

```bash
traceroute [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `traceroute` :

- `-m <max_ttl>` : Définit le nombre maximum de sauts (TTL) à suivre.
- `-p <port>` : Spécifie le port à utiliser pour les requêtes.
- `-n` : N'affiche pas les noms d'hôtes, seulement les adresses IP.
- `-I` : Utilise des paquets ICMP Echo au lieu de paquets UDP.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `traceroute` :

1. **Traceroute vers un site web :**
   ```bash
   traceroute www.example.com
   ```

2. **Traceroute avec un nombre maximum de sauts :**
   ```bash
   traceroute -m 10 www.example.com
   ```

3. **Traceroute en utilisant des paquets ICMP :**
   ```bash
   traceroute -I www.example.com
   ```

4. **Traceroute sans résolution de noms :**
   ```bash
   traceroute -n www.example.com
   ```

## Tips
- Utilisez l'option `-n` si vous souhaitez une sortie plus rapide sans résolution de noms d'hôtes.
- Vérifiez les permissions de votre réseau, car certaines configurations peuvent bloquer les paquets ICMP ou UDP.
- Combinez `traceroute` avec d'autres outils comme `ping` pour obtenir une vue d'ensemble de la connectivité réseau.