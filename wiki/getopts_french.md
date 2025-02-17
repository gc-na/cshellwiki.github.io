# [Linux] Bash getopts Utilisation : Gérer les options de ligne de commande

## Overview
La commande `getopts` est utilisée dans les scripts Bash pour analyser les options de ligne de commande. Elle permet de gérer les arguments passés à un script de manière structurée, facilitant ainsi la création de scripts plus interactifs et conviviaux.

## Usage
La syntaxe de base de la commande `getopts` est la suivante :

```bash
getopts [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `getopts` :

- `-a` : Active le mode d'analyse des options.
- `-d` : Définit un délimiteur personnalisé pour les options.
- `-n` : Spécifie le nom du script pour les messages d'erreur.

## Common Examples

### Exemple 1 : Analyse d'options simples
Voici un exemple de script qui utilise `getopts` pour analyser des options simples :

```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a) echo "Option A activée" ;;
    b) echo "Option B avec argument : $OPTARG" ;;
    c) echo "Option C avec argument : $OPTARG" ;;
    *) echo "Option invalide" ;;
  esac
done
```

### Exemple 2 : Utilisation avec des arguments
Dans cet exemple, nous allons passer des arguments avec les options :

```bash
#!/bin/bash

while getopts "x:y:" opt; do
  case $opt in
    x) echo "Valeur de X : $OPTARG" ;;
    y) echo "Valeur de Y : $OPTARG" ;;
    *) echo "Option invalide" ;;
  esac
done

# Exécution : ./script.sh -x 10 -y 20
```

### Exemple 3 : Gestion des options multiples
Cet exemple montre comment gérer plusieurs options :

```bash
#!/bin/bash

while getopts "abc" opt; do
  case $opt in
    a) echo "Option A activée" ;;
    b) echo "Option B activée" ;;
    c) echo "Option C activée" ;;
    *) echo "Option invalide" ;;
  esac
done

# Exécution : ./script.sh -a -b
```

## Tips
- Utilisez des options courtes et significatives pour améliorer la convivialité de votre script.
- Pensez à gérer les erreurs pour informer l'utilisateur en cas d'options invalides.
- Documentez toujours les options disponibles dans votre script pour faciliter son utilisation.