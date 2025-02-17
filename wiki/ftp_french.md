# [Linux] Bash ftp Utilisation : Transférer des fichiers via le protocole FTP

## Overview
La commande `ftp` (File Transfer Protocol) est utilisée pour transférer des fichiers entre un client et un serveur via le protocole FTP. Elle permet de se connecter à un serveur FTP, de naviguer dans les répertoires et de télécharger ou téléverser des fichiers.

## Usage
La syntaxe de base de la commande `ftp` est la suivante :

```bash
ftp [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `ftp` :

- `-v` : Mode verbeux, affiche des informations détaillées sur les opérations en cours.
- `-n` : Ne pas tenter de se connecter automatiquement au serveur.
- `-g` : Désactive l'expansion des caractères génériques (wildcards).
- `-i` : Désactive le mode interactif, ce qui permet de transférer des fichiers sans confirmation.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ftp` :

1. **Se connecter à un serveur FTP :**
   ```bash
   ftp ftp.example.com
   ```

2. **Télécharger un fichier depuis le serveur :**
   ```bash
   ftp> get nom_du_fichier.txt
   ```

3. **Téléverser un fichier vers le serveur :**
   ```bash
   ftp> put nom_du_fichier.txt
   ```

4. **Lister les fichiers dans le répertoire courant du serveur :**
   ```bash
   ftp> ls
   ```

5. **Changer de répertoire sur le serveur :**
   ```bash
   ftp> cd nom_du_répertoire
   ```

## Tips
- Assurez-vous d'utiliser un mot de passe fort pour sécuriser votre connexion FTP.
- Utilisez le mode passif (`passive`) si vous rencontrez des problèmes de connexion, surtout derrière un pare-feu.
- Pensez à utiliser `sftp` (SSH File Transfer Protocol) pour une sécurité accrue lors du transfert de fichiers.