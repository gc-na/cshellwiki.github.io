# [Linux] Bash tcpdump utilisation : Analyse du trafic réseau

## Overview
La commande `tcpdump` est un outil puissant utilisé pour capturer et analyser le trafic réseau sur une interface donnée. Elle permet aux utilisateurs de visualiser les paquets qui transitent sur le réseau, ce qui est essentiel pour le diagnostic des problèmes de réseau et la surveillance de la sécurité.

## Usage
La syntaxe de base de la commande `tcpdump` est la suivante :

```bash
tcpdump [options] [arguments]
```

## Common Options
Voici quelques options courantes de `tcpdump` avec de courtes explications :

- `-i <interface>` : Spécifie l'interface réseau à écouter (par exemple, `eth0`, `wlan0`).
- `-n` : Ne pas résoudre les adresses IP en noms d'hôtes, ce qui accélère l'affichage.
- `-c <nombre>` : Limite le nombre de paquets à capturer.
- `-w <fichier>` : Écrit la sortie dans un fichier au lieu de l'afficher à l'écran.
- `-r <fichier>` : Lit les paquets à partir d'un fichier au lieu de l'interface réseau.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `tcpdump` :

1. **Capturer tous les paquets sur une interface spécifique :**
   ```bash
   tcpdump -i eth0
   ```

2. **Capturer un nombre limité de paquets :**
   ```bash
   tcpdump -i eth0 -c 10
   ```

3. **Écrire la sortie dans un fichier :**
   ```bash
   tcpdump -i eth0 -w capture.pcap
   ```

4. **Lire des paquets à partir d'un fichier :**
   ```bash
   tcpdump -r capture.pcap
   ```

5. **Capturer uniquement le trafic HTTP :**
   ```bash
   tcpdump -i eth0 port 80
   ```

## Tips
- Utilisez l'option `-n` pour éviter la résolution DNS, ce qui peut rendre l'analyse plus rapide.
- Pensez à filtrer le trafic pour capturer uniquement ce qui vous intéresse, par exemple en utilisant des filtres de port ou d'adresse IP.
- Pour une analyse plus approfondie, envisagez d'utiliser `tcpdump` en conjonction avec des outils comme Wireshark pour visualiser les paquets capturés.