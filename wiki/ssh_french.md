# [Linux] C Shell (csh) ssh utilisation : Établir une connexion sécurisée à distance

## Overview
La commande `ssh` (Secure Shell) permet d'établir une connexion sécurisée à un autre ordinateur sur un réseau. Elle est principalement utilisée pour accéder à des serveurs à distance et exécuter des commandes de manière sécurisée.

## Usage
La syntaxe de base de la commande `ssh` est la suivante :

```csh
ssh [options] [utilisateur@]hôte
```

## Common Options
Voici quelques options courantes pour la commande `ssh` :

- `-p [port]` : Spécifie le port à utiliser pour la connexion SSH.
- `-i [clé]` : Utilise une clé d'authentification spécifique.
- `-v` : Active le mode verbeux pour le débogage.
- `-X` : Active le transfert X11 pour exécuter des applications graphiques à distance.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ssh` :

1. Connexion à un serveur distant :
   ```csh
   ssh utilisateur@serveur.com
   ```

2. Connexion à un serveur sur un port spécifique :
   ```csh
   ssh -p 2222 utilisateur@serveur.com
   ```

3. Utilisation d'une clé d'authentification :
   ```csh
   ssh -i ~/.ssh/ma_cle_rsa utilisateur@serveur.com
   ```

4. Activation du mode verbeux pour le débogage :
   ```csh
   ssh -v utilisateur@serveur.com
   ```

5. Exécution d'une commande à distance :
   ```csh
   ssh utilisateur@serveur.com 'ls -l /var/www'
   ```

## Tips
- Utilisez des clés SSH pour une authentification plus sécurisée au lieu de mots de passe.
- Gardez votre clé privée sécurisée et ne la partagez jamais.
- Pensez à configurer votre fichier `~/.ssh/config` pour simplifier les connexions fréquentes à différents hôtes.