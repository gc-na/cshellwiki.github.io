# [Linux] C Shell (csh) stty : Configurer les paramètres du terminal

## Overview
La commande `stty` est utilisée pour modifier et afficher les paramètres du terminal dans le shell C. Elle permet de configurer des options telles que le contrôle de flux, les caractères spéciaux, et d'autres réglages liés à l'entrée et à la sortie du terminal.

## Usage
La syntaxe de base de la commande `stty` est la suivante :

```csh
stty [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `stty` :

- `-a` : Affiche tous les paramètres actuels du terminal.
- `-g` : Affiche les paramètres sous forme de chaîne, pouvant être réutilisés.
- `erase` : Définit le caractère utilisé pour effacer le dernier caractère.
- `kill` : Définit le caractère utilisé pour supprimer la ligne en cours.
- `intr` : Définit le caractère d'interruption (habituellement Ctrl+C).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `stty` :

1. **Afficher tous les paramètres du terminal :**
   ```csh
   stty -a
   ```

2. **Changer le caractère d'effacement à `^H` (backspace) :**
   ```csh
   stty erase ^H
   ```

3. **Définir le caractère d'interruption à `^C` :**
   ```csh
   stty intr ^C
   ```

4. **Sauvegarder les paramètres actuels dans une variable :**
   ```csh
   set params = `stty -g`
   ```

5. **Restaurer les paramètres à partir d'une variable :**
   ```csh
   stty $params
   ```

## Tips
- Utilisez `stty -g` pour sauvegarder les paramètres avant de faire des modifications, afin de pouvoir les restaurer facilement.
- Vérifiez les paramètres du terminal après des modifications pour vous assurer qu'ils sont configurés comme prévu.
- Soyez prudent lors de la modification des caractères spéciaux, car cela peut affecter le comportement de votre terminal.