# [Linux] C Shell (csh) whoami : [affiche le nom de l'utilisateur courant]

## Overview
La commande `whoami` dans C Shell (csh) est utilisée pour afficher le nom de l'utilisateur actuellement connecté au système. Cela peut être utile pour vérifier sous quel compte vous travaillez, surtout si vous avez plusieurs sessions ouvertes ou si vous utilisez des comptes différents.

## Usage
La syntaxe de base de la commande est la suivante :

```
whoami [options] [arguments]
```

## Common Options
La commande `whoami` n'a généralement pas d'options spécifiques, mais il est important de noter qu'elle peut être utilisée dans des scripts ou avec d'autres commandes pour obtenir le nom de l'utilisateur.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `whoami` :

1. **Afficher le nom de l'utilisateur courant :**
   ```csh
   whoami
   ```

2. **Utiliser `whoami` dans un script :**
   ```csh
   echo "Vous êtes connecté en tant que : $(whoami)"
   ```

3. **Vérifier l'utilisateur avant d'exécuter une commande :**
   ```csh
   if ( `whoami` == "admin" ) then
       echo "Vous avez les droits d'administrateur."
   else
       echo "Vous n'êtes pas administrateur."
   endif
   ```

## Tips
- Utilisez `whoami` pour confirmer votre identité avant d'exécuter des commandes sensibles.
- Intégrez `whoami` dans vos scripts pour personnaliser les messages ou les actions en fonction de l'utilisateur.
- Si vous travaillez avec des sessions SSH, `whoami` peut vous aider à vérifier que vous êtes connecté avec le bon compte.