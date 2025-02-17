# [Linux] Bash env : [afficher ou modifier l'environnement d'exécution]

## Overview
La commande `env` est utilisée pour afficher ou modifier l'environnement d'exécution des programmes. Elle permet de lancer des programmes avec un environnement spécifique, ce qui peut être utile pour tester des configurations ou exécuter des scripts avec des variables d'environnement personnalisées.

## Usage
La syntaxe de base de la commande `env` est la suivante :

```bash
env [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `env` :

- `-i` : Exécute la commande dans un environnement vide, sans variables d'environnement héritées.
- `-u` : Supprime une variable d'environnement spécifique avant d'exécuter la commande.
- `VAR=value` : Définit une variable d'environnement pour la commande qui suit.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `env` :

1. **Afficher toutes les variables d'environnement :**

   ```bash
   env
   ```

2. **Exécuter un programme avec un environnement vide :**

   ```bash
   env -i bash
   ```

3. **Supprimer une variable d'environnement avant d'exécuter une commande :**

   ```bash
   env -u PATH command
   ```

4. **Définir une variable d'environnement temporaire :**

   ```bash
   env MY_VAR=value command
   ```

5. **Lancer un script avec des variables d'environnement spécifiques :**

   ```bash
   env VAR1=value1 VAR2=value2 ./myscript.sh
   ```

## Tips
- Utilisez `env` pour tester des scripts dans un environnement contrôlé sans interférences d'autres variables d'environnement.
- Soyez prudent lorsque vous utilisez l'option `-u`, car cela peut empêcher certaines commandes de fonctionner correctement si elles dépendent de la variable supprimée.
- Pour vérifier les variables d'environnement d'un processus en cours, vous pouvez utiliser `env` en combinaison avec d'autres commandes comme `grep`.