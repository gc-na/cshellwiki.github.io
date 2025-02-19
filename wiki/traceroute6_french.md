# [Linux] C Shell (csh) traceroute6 : [tracer le chemin des paquets IPv6]

## Overview
La commande `traceroute6` est utilisée pour tracer le chemin que prennent les paquets IPv6 à travers un réseau. Elle permet d'identifier les différents nœuds (routeurs) que les paquets traversent pour atteindre leur destination, ce qui est utile pour diagnostiquer des problèmes de connectivité.

## Usage
La syntaxe de base de la commande `traceroute6` est la suivante :

```csh
traceroute6 [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `traceroute6` :

- `-m <max_ttl>` : Définit le nombre maximum de sauts (TTL) à suivre.
- `-p <port>` : Spécifie le port à utiliser pour les paquets envoyés.
- `-w <timeout>` : Définit le délai d'attente pour chaque réponse.
- `-q <nqueries>` : Définit le nombre de requêtes à envoyer par saut.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `traceroute6` :

1. Traceroute vers une adresse IPv6 spécifique :
   ```csh
   traceroute6 2001:db8::1
   ```

2. Traceroute avec un nombre maximum de sauts de 15 :
   ```csh
   traceroute6 -m 15 2001:db8::1
   ```

3. Traceroute en spécifiant un port :
   ```csh
   traceroute6 -p 80 2001:db8::1
   ```

4. Traceroute avec un délai d'attente de 2 secondes :
   ```csh
   traceroute6 -w 2 2001:db8::1
   ```

## Tips
- Assurez-vous que votre réseau prend en charge IPv6 avant d'utiliser `traceroute6`.
- Utilisez l'option `-m` pour éviter de dépasser le nombre de sauts, ce qui peut être utile dans des réseaux complexes.
- Vérifiez les permissions nécessaires, car certaines options peuvent nécessiter des privilèges d'administrateur.