# [Linux] Bash chage Utilisation : Gérer les informations de mot de passe des utilisateurs

## Overview
La commande `chage` est utilisée pour modifier les paramètres d'expiration des mots de passe des utilisateurs sur un système Linux. Elle permet aux administrateurs de gérer la durée de vie des mots de passe, d'imposer des délais d'avertissement avant l'expiration et de définir des périodes d'inactivité.

## Usage
La syntaxe de base de la commande `chage` est la suivante :

```bash
chage [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `chage` :

- `-l, --list`: Affiche les informations d'expiration du mot de passe pour un utilisateur.
- `-m, --mindays`: Définit le nombre minimum de jours avant qu'un mot de passe puisse être changé.
- `-M, --maxdays`: Définit le nombre maximum de jours avant qu'un mot de passe doive être changé.
- `-I, --inactive`: Définit le nombre de jours d'inactivité après l'expiration du mot de passe avant que le compte ne soit désactivé.
- `-W, --warndays`: Définit le nombre de jours avant l'expiration du mot de passe pendant lesquels un avertissement sera donné à l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `chage` :

1. **Afficher les informations d'expiration du mot de passe d'un utilisateur :**
   ```bash
   chage -l nom_utilisateur
   ```

2. **Définir un maximum de 90 jours avant que le mot de passe doive être changé :**
   ```bash
   chage -M 90 nom_utilisateur
   ```

3. **Définir un minimum de 7 jours avant que le mot de passe puisse être changé :**
   ```bash
   chage -m 7 nom_utilisateur
   ```

4. **Configurer un avertissement de 14 jours avant l'expiration du mot de passe :**
   ```bash
   chage -W 14 nom_utilisateur
   ```

5. **Définir une période d'inactivité de 30 jours après l'expiration du mot de passe :**
   ```bash
   chage -I 30 nom_utilisateur
   ```

## Tips
- Assurez-vous de toujours vérifier les paramètres actuels d'un utilisateur avec `chage -l` avant de faire des modifications.
- Utilisez des valeurs raisonnables pour les jours d'expiration afin de ne pas perturber les utilisateurs.
- Pensez à informer les utilisateurs des changements de politique concernant les mots de passe pour éviter toute confusion.