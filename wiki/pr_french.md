# [Linux] Bash pr : afficher des fichiers formatés

## Overview
La commande `pr` est utilisée pour formater des fichiers texte pour une impression ou une visualisation plus claire. Elle divise le texte en colonnes et ajoute des en-têtes, ce qui facilite la lecture des données.

## Usage
La syntaxe de base de la commande `pr` est la suivante :

```bash
pr [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `pr` :

- `-h` : spécifie un en-tête personnalisé pour la sortie.
- `-l` : définit le nombre de lignes par page.
- `-t` : supprime les numéros de page et les en-têtes.
- `-s` : définit un séparateur personnalisé entre les colonnes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `pr` :

1. **Afficher un fichier avec des colonnes par défaut :**
   ```bash
   pr mon_fichier.txt
   ```

2. **Afficher un fichier avec un en-tête personnalisé :**
   ```bash
   pr -h "Mon En-tête Personnalisé" mon_fichier.txt
   ```

3. **Afficher un fichier avec 50 lignes par page :**
   ```bash
   pr -l 50 mon_fichier.txt
   ```

4. **Supprimer les en-têtes et numéros de page :**
   ```bash
   pr -t mon_fichier.txt
   ```

5. **Afficher deux fichiers côte à côte avec un séparateur :**
   ```bash
   pr -s ' | ' fichier1.txt fichier2.txt
   ```

## Tips
- Utilisez l'option `-h` pour rendre vos sorties plus claires et personnalisées.
- Expérimentez avec le nombre de lignes par page pour adapter la sortie à votre imprimante ou à votre écran.
- Combinez `pr` avec d'autres commandes comme `cat` ou `less` pour une visualisation améliorée.