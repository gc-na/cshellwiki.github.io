# [Linux] C Shell (csh) pr : Afficher et formater le contenu des fichiers

## Overview
La commande `pr` est utilisée pour formater le contenu des fichiers texte en vue d'une impression. Elle permet de diviser le texte en colonnes, d'ajouter des en-têtes et de gérer la pagination, ce qui facilite la lecture et l'impression des documents.

## Usage
Voici la syntaxe de base de la commande `pr` :

```csh
pr [options] [arguments]
```

## Common Options
- `-h` : Spécifie un en-tête personnalisé pour la sortie.
- `-l` : Définit le nombre de lignes par page.
- `-w` : Définit la largeur de la page en caractères.
- `-s` : Spécifie un séparateur entre les colonnes.
- `-t` : Supprime les en-têtes et les pieds de page par défaut.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `pr` :

### Exemple 1 : Formatage simple d'un fichier
Pour formater le contenu d'un fichier texte nommé `document.txt` :

```csh
pr document.txt
```

### Exemple 2 : Ajouter un en-tête personnalisé
Pour ajouter un en-tête à la sortie :

```csh
pr -h "Mon Document" document.txt
```

### Exemple 3 : Définir le nombre de lignes par page
Pour définir 50 lignes par page :

```csh
pr -l 50 document.txt
```

### Exemple 4 : Utiliser plusieurs colonnes
Pour afficher le contenu de deux fichiers en colonnes :

```csh
pr file1.txt file2.txt
```

### Exemple 5 : Supprimer les en-têtes et pieds de page
Pour afficher le contenu sans en-têtes ni pieds de page :

```csh
pr -t document.txt
```

## Tips
- Utilisez l'option `-w` pour ajuster la largeur de la page si vous imprimez sur différents formats de papier.
- Combinez plusieurs options pour personnaliser la sortie selon vos besoins spécifiques.
- Vérifiez toujours le formatage en utilisant `pr` sur un petit fichier avant de l'appliquer à des documents plus volumineux.