# [Linux] Bash mkfifo Utilisation : Créer des tubes nommés

## Overview
La commande `mkfifo` est utilisée pour créer des tubes nommés, également appelés FIFO (First In, First Out). Ces tubes permettent la communication entre différents processus en permettant à un processus d'écrire des données dans le tube, tandis qu'un autre processus peut lire ces données.

## Usage
La syntaxe de base de la commande `mkfifo` est la suivante :

```bash
mkfifo [options] [arguments]
```

## Common Options
- `-m, --mode=MODE` : Définit les permissions du tube créé, en utilisant la notation octale.
- `-Z, --context=CONTEXT` : Définit le contexte de sécurité SELinux pour le tube créé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mkfifo` :

1. **Créer un tube nommé simple :**
   ```bash
   mkfifo mon_tube
   ```

2. **Créer un tube nommé avec des permissions spécifiques :**
   ```bash
   mkfifo -m 644 mon_tube
   ```

3. **Utiliser un tube nommé dans un script :**
   ```bash
   mkfifo mon_tube
   echo "Bonjour, monde!" > mon_tube &
   cat < mon_tube
   ```

4. **Créer plusieurs tubes nommés à la fois :**
   ```bash
   mkfifo tube1 tube2 tube3
   ```

## Tips
- Assurez-vous de supprimer le tube nommé après utilisation avec `rm mon_tube` pour éviter d'encombrer votre système de fichiers.
- Utilisez des tubes nommés pour synchroniser des processus lorsque vous avez besoin de passer des données entre eux de manière ordonnée.
- Vérifiez les permissions du tube avec `ls -l mon_tube` pour vous assurer qu'elles sont correctes pour vos besoins.