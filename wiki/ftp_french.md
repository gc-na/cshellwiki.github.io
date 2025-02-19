# [Système d'exploitation] C Shell (csh) ftp : Transférer des fichiers entre ordinateurs

## Overview
La commande `ftp` (File Transfer Protocol) permet de transférer des fichiers entre un client et un serveur sur un réseau. Elle est largement utilisée pour télécharger ou téléverser des fichiers sur des serveurs distants.

## Usage
La syntaxe de base de la commande `ftp` est la suivante :

```csh
ftp [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `ftp` :

- `-i` : Désactive le mode interactif, ce qui permet de transférer des fichiers sans demander confirmation.
- `-v` : Active le mode verbeux, affichant des informations détaillées sur le transfert.
- `-n` : Empêche l'auto-connexion au serveur FTP à l'ouverture de la commande.
- `-g` : Permet d'ignorer les commandes de globbing (expansion de caractères génériques).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ftp` :

1. **Se connecter à un serveur FTP :**
   ```csh
   ftp ftp.example.com
   ```

2. **Télécharger un fichier depuis le serveur :**
   ```csh
   get fichier.txt
   ```

3. **Téléverser un fichier vers le serveur :**
   ```csh
   put fichier_local.txt
   ```

4. **Télécharger plusieurs fichiers :**
   ```csh
   mget *.jpg
   ```

5. **Téléverser plusieurs fichiers :**
   ```csh
   mput *.txt
   ```

## Tips
- Assurez-vous d'utiliser un mot de passe fort pour protéger vos connexions FTP.
- Utilisez le mode passif (avec la commande `passive`) si vous rencontrez des problèmes de connexion derrière un pare-feu.
- Pensez à vérifier les permissions des fichiers sur le serveur après le transfert pour vous assurer qu'ils sont accessibles comme prévu.