# [Linux] Bash sftp Utilisation : Transférer des fichiers de manière sécurisée

## Overview
La commande `sftp` (SSH File Transfer Protocol) permet de transférer des fichiers de manière sécurisée entre un client et un serveur via une connexion SSH. Elle offre une interface interactive similaire à celle de FTP, mais avec la sécurité supplémentaire fournie par SSH.

## Usage
La syntaxe de base de la commande `sftp` est la suivante :

```bash
sftp [options] [user@]host
```

## Common Options
Voici quelques options courantes pour la commande `sftp` :

- `-b batchfile` : Exécute les commandes SFTP à partir d'un fichier batch.
- `-C` : Active la compression des données.
- `-i identity_file` : Spécifie un fichier de clé d'identité pour l'authentification.
- `-P port` : Spécifie le port à utiliser pour la connexion.
- `-v` : Active le mode verbeux pour afficher des informations de débogage.

## Common Examples

### Connexion à un serveur SFTP
Pour se connecter à un serveur SFTP :

```bash
sftp user@hostname
```

### Transférer un fichier vers le serveur
Pour envoyer un fichier vers le serveur :

```bash
put localfile.txt
```

### Télécharger un fichier depuis le serveur
Pour récupérer un fichier depuis le serveur :

```bash
get remotefile.txt
```

### Lister les fichiers dans le répertoire distant
Pour afficher les fichiers dans le répertoire actuel du serveur :

```bash
ls
```

### Changer de répertoire sur le serveur
Pour naviguer vers un autre répertoire sur le serveur :

```bash
cd /path/to/directory
```

## Tips
- Utilisez l'option `-v` pour le débogage si vous rencontrez des problèmes de connexion.
- Pensez à utiliser des clés SSH pour une authentification plus sécurisée plutôt que des mots de passe.
- Vérifiez toujours les permissions des fichiers après un transfert pour vous assurer qu'elles sont correctes.