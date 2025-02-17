# [Linux] Bash stty utilisation : Configurer les paramètres du terminal

## Overview
La commande `stty` est utilisée pour modifier et afficher les paramètres du terminal. Elle permet de configurer des options telles que le contrôle de flux, les caractères spéciaux, et d'autres comportements du terminal.

## Usage
La syntaxe de base de la commande `stty` est la suivante :

```bash
stty [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `stty` :

- `-a` : Affiche tous les paramètres du terminal.
- `-g` : Affiche les paramètres sous forme de chaîne que vous pouvez utiliser pour restaurer la configuration.
- `erase` : Définit le caractère utilisé pour supprimer un caractère (généralement `^H` ou `Backspace`).
- `kill` : Définit le caractère utilisé pour supprimer la ligne entière (généralement `^U`).
- `intr` : Définit le caractère utilisé pour interrompre un processus (généralement `^C`).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `stty` :

1. **Afficher les paramètres actuels du terminal :**

   ```bash
   stty -a
   ```

2. **Changer le caractère d'effacement à `^H` :**

   ```bash
   stty erase ^H
   ```

3. **Modifier le caractère d'interruption à `^X` :**

   ```bash
   stty intr ^X
   ```

4. **Restaurer les paramètres du terminal à partir d'une chaîne :**

   ```bash
   stty -g
   # Copiez la chaîne affichée, puis utilisez-la comme suit :
   stty $(<votre_chaine)
   ```

## Tips
- Utilisez `stty -a` pour vérifier les paramètres avant d'apporter des modifications, afin de savoir ce qui a été modifié.
- Faites attention lorsque vous changez des caractères spéciaux, car cela peut affecter votre capacité à contrôler le terminal.
- Si vous travaillez sur un script, envisagez d'utiliser `stty -g` pour sauvegarder les paramètres avant de les modifier, afin de pouvoir les restaurer facilement.