# [Linux] Bash scp Utilisation : Transférer des fichiers de manière sécurisée

## Overview
La commande `scp` (Secure Copy Protocol) permet de transférer des fichiers et des répertoires entre des machines sur un réseau de manière sécurisée. Elle utilise le protocole SSH pour garantir la sécurité des données pendant le transfert.

## Usage
La syntaxe de base de la commande `scp` est la suivante :

```bash
scp [options] [source] [destination]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `scp` :

- `-r` : Copie récursive des répertoires.
- `-P` : Spécifie le port à utiliser pour la connexion SSH.
- `-i` : Utilise une clé d'identification spécifique pour l'authentification.
- `-v` : Affiche des informations détaillées sur le processus de transfert (mode verbeux).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `scp` :

1. **Transférer un fichier local vers un serveur distant :**
   ```bash
   scp /chemin/vers/fichier.txt utilisateur@serveur:/chemin/vers/destination/
   ```

2. **Transférer un fichier d'un serveur distant vers votre machine locale :**
   ```bash
   scp utilisateur@serveur:/chemin/vers/fichier.txt /chemin/vers/destination/
   ```

3. **Copier un répertoire entier vers un serveur distant :**
   ```bash
   scp -r /chemin/vers/répertoire utilisateur@serveur:/chemin/vers/destination/
   ```

4. **Transférer un fichier en spécifiant un port SSH différent :**
   ```bash
   scp -P 2222 /chemin/vers/fichier.txt utilisateur@serveur:/chemin/vers/destination/
   ```

## Tips
- Assurez-vous que le service SSH est actif sur le serveur distant avant d'utiliser `scp`.
- Utilisez l'option `-v` pour diagnostiquer les problèmes de connexion ou de transfert.
- Pour des transferts fréquents, envisagez d'utiliser une clé SSH pour éviter de saisir votre mot de passe à chaque fois.