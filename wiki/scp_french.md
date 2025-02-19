# [Système d'exploitation] C Shell (csh) scp : Copier des fichiers de manière sécurisée

## Overview
La commande `scp` (Secure Copy Protocol) permet de copier des fichiers et des répertoires entre des hôtes sur un réseau de manière sécurisée. Elle utilise le protocole SSH pour garantir la sécurité des données pendant le transfert.

## Usage
La syntaxe de base de la commande `scp` est la suivante :

```csh
scp [options] [source] [destination]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `scp` :

- `-r` : Copie récursive des répertoires.
- `-P` : Spécifie le port à utiliser pour la connexion SSH.
- `-i` : Utilise une clé d'identification spécifique pour l'authentification.
- `-v` : Mode verbeux, affiche des informations détaillées sur le processus de copie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `scp` :

1. **Copier un fichier local vers un hôte distant :**

```csh
scp fichier.txt utilisateur@hote_distant:/chemin/vers/destination/
```

2. **Copier un fichier d'un hôte distant vers la machine locale :**

```csh
scp utilisateur@hote_distant:/chemin/vers/fichier.txt /chemin/local/
```

3. **Copier un répertoire entier vers un hôte distant :**

```csh
scp -r mon_repertoire utilisateur@hote_distant:/chemin/vers/destination/
```

4. **Copier un fichier en spécifiant un port SSH :**

```csh
scp -P 2222 fichier.txt utilisateur@hote_distant:/chemin/vers/destination/
```

## Tips
- Assurez-vous que le service SSH est en cours d'exécution sur l'hôte distant avant d'utiliser `scp`.
- Utilisez l'option `-v` pour le débogage si vous rencontrez des problèmes de connexion.
- Pour des transferts fréquents, envisagez d'utiliser des clés SSH pour éviter de saisir votre mot de passe à chaque fois.