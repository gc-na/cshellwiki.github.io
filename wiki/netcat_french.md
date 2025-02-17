# [Linux] Bash netcat utilisation : Outil de communication réseau

## Overview
Le commandement `netcat`, souvent abrégé en `nc`, est un outil polyvalent utilisé pour lire et écrire des données à travers des connexions réseau en utilisant le protocole TCP ou UDP. Il est souvent décrit comme le "couteau suisse" des outils réseau en raison de sa flexibilité et de sa capacité à établir des connexions entre des machines.

## Usage
La syntaxe de base de la commande `netcat` est la suivante :

```
netcat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `netcat` :

- `-l` : Écoute sur un port pour les connexions entrantes.
- `-p [port]` : Spécifie le port à utiliser.
- `-u` : Utilise le protocole UDP au lieu de TCP.
- `-v` : Mode verbeux, affiche des informations supplémentaires.
- `-z` : Mode "scan", vérifie si un port est ouvert sans établir de connexion.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `netcat` :

1. **Écouter sur un port spécifique :**
   ```
   netcat -l -p 1234
   ```
   Cela démarre `netcat` en mode écoute sur le port 1234.

2. **Envoyer un message à un serveur :**
   ```
   echo "Bonjour, serveur!" | netcat 192.168.1.10 1234
   ```
   Cela envoie le message "Bonjour, serveur!" à l'adresse IP 192.168.1.10 sur le port 1234.

3. **Transférer un fichier :**
   Sur la machine réceptrice, exécutez :
   ```
   netcat -l -p 1234 > fichier_recu.txt
   ```
   Sur la machine émettrice, exécutez :
   ```
   netcat 192.168.1.10 1234 < fichier_a_envoyer.txt
   ```
   Cela transfère `fichier_a_envoyer.txt` à la machine réceptrice.

4. **Scanner les ports d'une machine :**
   ```
   netcat -z -v 192.168.1.10 1-1000
   ```
   Cela vérifie les ports de 1 à 1000 sur l'adresse IP 192.168.1.10 pour voir lesquels sont ouverts.

## Tips
- Utilisez le mode verbeux (`-v`) pour obtenir des informations supplémentaires lors du débogage.
- Soyez prudent lorsque vous utilisez `netcat` pour écouter sur des ports, car cela peut exposer votre machine à des connexions non sécurisées.
- Pour des transferts de fichiers sécurisés, envisagez d'utiliser `netcat` en conjonction avec `ssh` pour chiffrer la connexion.