# [Linux] C Shell (csh) tcpdump : Analyse de paquets réseau

## Overview
La commande `tcpdump` est un outil puissant utilisé pour capturer et analyser le trafic réseau. Il permet aux utilisateurs de surveiller les paquets qui transitent par un réseau, ce qui est essentiel pour le dépannage et la sécurité.

## Usage
La syntaxe de base de la commande `tcpdump` est la suivante :

```csh
tcpdump [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `tcpdump` :

- `-i <interface>` : Spécifie l'interface réseau à écouter.
- `-n` : Ne pas résoudre les noms d'hôtes ou les ports, affichant les adresses IP et les numéros de port au lieu des noms.
- `-c <nombre>` : Limite le nombre de paquets à capturer.
- `-w <fichier>` : Écrit la sortie dans un fichier au lieu de l'afficher sur la console.
- `-r <fichier>` : Lit les paquets à partir d'un fichier enregistré.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tcpdump` :

1. **Capturer des paquets sur une interface spécifique :**
   ```csh
   tcpdump -i eth0
   ```

2. **Capturer un nombre limité de paquets :**
   ```csh
   tcpdump -i eth0 -c 10
   ```

3. **Écrire la sortie dans un fichier :**
   ```csh
   tcpdump -i eth0 -w capture.pcap
   ```

4. **Lire des paquets à partir d'un fichier :**
   ```csh
   tcpdump -r capture.pcap
   ```

5. **Capturer uniquement le trafic HTTP :**
   ```csh
   tcpdump -i eth0 port 80
   ```

## Tips
- Utilisez l'option `-n` pour éviter la résolution DNS, ce qui peut rendre la capture plus rapide.
- Pensez à filtrer le trafic pour ne capturer que ce qui vous intéresse, afin de réduire le bruit dans les résultats.
- Vérifiez régulièrement les permissions de votre interface réseau, car certaines peuvent nécessiter des privilèges élevés pour être écoutées.