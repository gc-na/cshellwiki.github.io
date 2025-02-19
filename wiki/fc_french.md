# [Linux] C Shell (csh) fc <Utilisation équivalente en français>: [modifier l'historique des commandes]

## Overview
La commande `fc` dans le C Shell (csh) est utilisée pour modifier et réexécuter des commandes précédemment exécutées. Elle permet aux utilisateurs de rechercher dans l'historique des commandes, d'éditer des commandes spécifiques et de les exécuter à nouveau.

## Usage
La syntaxe de base de la commande `fc` est la suivante :

```csh
fc [options] [arguments]
```

## Common Options
- `-l` : Liste les commandes de l'historique.
- `-s` : Exécute la commande sans l'afficher dans le terminal.
- `-n` : Ne pas afficher les numéros de ligne lors de la liste des commandes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `fc` :

1. **Lister les commandes de l'historique :**
   ```csh
   fc -l
   ```

2. **Modifier la dernière commande exécutée :**
   ```csh
   fc
   ```

3. **Exécuter la dernière commande sans l'afficher :**
   ```csh
   fc -s
   ```

4. **Modifier une commande spécifique dans l'historique (par exemple, la commande 5) :**
   ```csh
   fc 5
   ```

5. **Lister les 10 dernières commandes :**
   ```csh
   fc -l -10
   ```

## Tips
- Utilisez `fc` régulièrement pour corriger rapidement des erreurs dans les commandes précédentes sans avoir à les retaper.
- Familiarisez-vous avec les numéros de commande de votre historique pour un accès rapide.
- Combinez `fc` avec un éditeur de texte comme `vi` pour des modifications plus complexes.