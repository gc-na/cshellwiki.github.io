# [Linux] Bash ssh Utilisation : Connexion sécurisée à un serveur distant

## Overview
La commande `ssh` (Secure Shell) est utilisée pour établir une connexion sécurisée à un serveur distant. Elle permet aux utilisateurs d'exécuter des commandes sur un autre ordinateur via un réseau, tout en assurant la confidentialité et l'intégrité des données échangées.

## Usage
La syntaxe de base de la commande `ssh` est la suivante :

```bash
ssh [options] [utilisateur@]hôte
```

## Common Options
Voici quelques options courantes pour la commande `ssh` :

- `-p PORT` : Spécifie le port à utiliser pour la connexion (par défaut, c'est le port 22).
- `-i FICHIER` : Utilise une clé d'authentification spécifique (fichier de clé privée).
- `-v` : Active le mode verbeux pour afficher des informations de débogage.
- `-X` : Active le transfert X11, permettant d'exécuter des applications graphiques à distance.
- `-C` : Active la compression des données pour réduire la bande passante utilisée.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ssh` :

1. **Connexion à un serveur distant :**
   ```bash
   ssh utilisateur@192.168.1.1
   ```

2. **Connexion à un serveur distant sur un port spécifique :**
   ```bash
   ssh -p 2222 utilisateur@192.168.1.1
   ```

3. **Utilisation d'une clé d'authentification spécifique :**
   ```bash
   ssh -i ~/.ssh/id_rsa utilisateur@192.168.1.1
   ```

4. **Exécution d'une commande à distance :**
   ```bash
   ssh utilisateur@192.168.1.1 'ls -l /var/www'
   ```

5. **Transfert de fichiers avec SCP (Secure Copy) :**
   ```bash
   scp fichier.txt utilisateur@192.168.1.1:/chemin/destination/
   ```

## Tips
- **Utiliser des clés SSH** : Pour une sécurité accrue, utilisez des clés SSH plutôt que des mots de passe pour vous authentifier.
- **Configurer le fichier `~/.ssh/config`** : Simplifiez vos connexions en configurant des alias pour vos serveurs dans ce fichier.
- **Vérifier les connexions** : Utilisez l'option `-v` pour diagnostiquer les problèmes de connexion.
- **Désactiver l'authentification par mot de passe** : Pour renforcer la sécurité, envisagez de désactiver l'authentification par mot de passe sur vos serveurs.