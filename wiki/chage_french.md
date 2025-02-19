# [Linux] C Shell (csh) chage : Gérer les informations de changement de mot de passe

## Overview
La commande `chage` est utilisée pour modifier les informations relatives aux changements de mot de passe d'un utilisateur dans un système Linux. Elle permet de gérer la durée de vie du mot de passe, ainsi que les avertissements et les périodes d'inactivité.

## Usage
La syntaxe de base de la commande `chage` est la suivante :

```bash
chage [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `chage` :

- `-l` : Affiche les informations de changement de mot de passe pour un utilisateur.
- `-m` : Définit le nombre minimum de jours avant qu'un mot de passe puisse être changé.
- `-M` : Définit le nombre maximum de jours avant qu'un mot de passe doive être changé.
- `-I` : Définit le nombre de jours d'inactivité après l'expiration du mot de passe avant que le compte soit désactivé.
- `-E` : Définit la date d'expiration du compte utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `chage` :

1. **Afficher les informations de changement de mot de passe pour un utilisateur :**
   ```bash
   chage -l nom_utilisateur
   ```

2. **Définir un minimum de 7 jours avant qu'un mot de passe puisse être changé :**
   ```bash
   chage -m 7 nom_utilisateur
   ```

3. **Définir un maximum de 30 jours avant qu'un mot de passe doive être changé :**
   ```bash
   chage -M 30 nom_utilisateur
   ```

4. **Définir 14 jours d'inactivité avant que le compte soit désactivé :**
   ```bash
   chage -I 14 nom_utilisateur
   ```

5. **Définir une date d'expiration pour le compte utilisateur :**
   ```bash
   chage -E 2024-12-31 nom_utilisateur
   ```

## Tips
- Assurez-vous d'avoir les privilèges nécessaires (souvent en tant que super utilisateur) pour modifier les paramètres de changement de mot de passe d'autres utilisateurs.
- Utilisez l'option `-l` pour vérifier les paramètres actuels avant de faire des modifications.
- Pensez à informer les utilisateurs des changements de politique de mot de passe pour éviter toute confusion.