# [Linux] Bash traceroute6 : Suivre le chemin des paquets IPv6

## Overview
La commande `traceroute6` est utilisée pour suivre le chemin qu'un paquet IPv6 prend à travers un réseau. Elle permet d'identifier les différents nœuds (routeurs) que le paquet traverse avant d'atteindre sa destination, ce qui est utile pour diagnostiquer des problèmes de connectivité réseau.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
traceroute6 [options] [arguments]
```

## Common Options
- `-m <max_ttl>` : Définit le nombre maximum de sauts (TTL) à utiliser.
- `-p <port>` : Spécifie le port à utiliser pour l'envoi des paquets.
- `-q <nqueries>` : Définit le nombre de requêtes à envoyer par saut.
- `-w <timeout>` : Définit le délai d'attente pour chaque réponse.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `traceroute6` :

1. **Traceroute vers une adresse IPv6 spécifique :**
   ```bash
   traceroute6 google.com
   ```

2. **Traceroute avec un nombre maximum de sauts de 15 :**
   ```bash
   traceroute6 -m 15 google.com
   ```

3. **Traceroute en utilisant un port spécifique (par exemple, le port 80) :**
   ```bash
   traceroute6 -p 80 google.com
   ```

4. **Traceroute avec un délai d'attente de 2 secondes :**
   ```bash
   traceroute6 -w 2 google.com
   ```

## Tips
- Utilisez `traceroute6` avec des adresses IPv6 pour obtenir des résultats précis, car cette commande est spécifiquement conçue pour le protocole IPv6.
- Vérifiez que votre réseau et votre système prennent en charge IPv6 avant d'utiliser cette commande.
- Combinez les options pour affiner vos résultats, par exemple, en ajustant le TTL et le délai d'attente pour une analyse plus approfondie.