# [Linux] C Shell (csh) script : Enregistrer une session de terminal

## Overview
La commande `script` permet d'enregistrer une session de terminal dans un fichier. Cela peut être utile pour garder une trace des commandes exécutées et de leurs sorties, facilitant ainsi la documentation ou le partage d'une session de travail.

## Usage
La syntaxe de base de la commande est la suivante :

```csh
script [options] [arguments]
```

## Common Options
- `-a` : Ajoute la sortie au fichier existant au lieu de l'écraser.
- `-f` : Écrit la sortie immédiatement dans le fichier, ce qui peut être utile pour suivre l'activité en temps réel.
- `-q` : Exécute la commande en mode silencieux, sans afficher les messages d'information.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `script` :

1. **Enregistrer une session par défaut :**
   ```csh
   script
   ```
   Cela crée un fichier nommé `typescript` dans le répertoire courant et enregistre la session.

2. **Enregistrer une session avec un nom de fichier spécifique :**
   ```csh
   script mon_fichier.txt
   ```
   Cela enregistre la session dans `mon_fichier.txt`.

3. **Ajouter à un fichier existant :**
   ```csh
   script -a mon_fichier.txt
   ```
   Cela ajoute la sortie de la session actuelle à `mon_fichier.txt`.

4. **Mode silencieux :**
   ```csh
   script -q
   ```
   Cela enregistre la session sans afficher de messages d'information.

## Tips
- Pensez à vérifier le contenu du fichier généré après avoir terminé votre session pour vous assurer que tout a été enregistré correctement.
- Utilisez l'option `-f` si vous souhaitez voir les résultats en temps réel, ce qui peut être utile lors de l'exécution de longues commandes.
- N'oubliez pas de quitter la session enregistrée en tapant `exit` ou `Ctrl+D` pour finaliser l'enregistrement.