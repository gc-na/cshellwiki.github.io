# [Linux] C Shell (csh) sftp : Transférer des fichiers en toute sécurité

## Overview
La commande `sftp` (SSH File Transfer Protocol) permet de transférer des fichiers de manière sécurisée entre un ordinateur local et un serveur distant. Elle utilise le protocole SSH pour garantir la sécurité des données pendant le transfert.

## Usage
La syntaxe de base de la commande `sftp` est la suivante :

```csh
sftp [options] [user@]host
```

## Common Options
Voici quelques options courantes pour la commande `sftp` :

- `-b batchfile` : Utiliser un fichier batch pour exécuter des commandes `sftp` en mode non interactif.
- `-C` : Activer la compression des données pendant le transfert.
- `-P port` : Spécifier un port différent pour la connexion au serveur.
- `-r` : Permet de transférer des répertoires de manière récursive.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `sftp` :

1. **Se connecter à un serveur SFTP :**
   ```csh
   sftp user@hostname
   ```

2. **Télécharger un fichier depuis le serveur :**
   ```csh
   sftp> get fichier.txt
   ```

3. **Télécharger un répertoire entier :**
   ```csh
   sftp> get -r mon_repertoire
   ```

4. **Téléverser un fichier vers le serveur :**
   ```csh
   sftp> put fichier.txt
   ```

5. **Lister les fichiers sur le serveur :**
   ```csh
   sftp> ls
   ```

## Tips
- Utilisez l'option `-C` pour accélérer le transfert de fichiers volumineux grâce à la compression.
- Pensez à utiliser des clés SSH pour une connexion sans mot de passe, ce qui facilite l'automatisation des transferts.
- Vérifiez toujours les permissions des fichiers sur le serveur après un transfert pour vous assurer qu'elles sont correctes.