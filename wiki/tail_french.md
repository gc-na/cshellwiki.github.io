# [Linux] C Shell (csh) tail Utilisation : Afficher les dernières lignes d'un fichier

## Overview
La commande `tail` est utilisée pour afficher les dernières lignes d'un fichier. C'est particulièrement utile pour surveiller les fichiers de log ou pour voir les dernières entrées d'un fichier texte.

## Usage
La syntaxe de base de la commande `tail` est la suivante :

```csh
tail [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `tail` :

- `-n [nombre]` : Affiche les dernières [nombre] lignes du fichier spécifié.
- `-f` : Suivre le fichier en temps réel, affichant les nouvelles lignes au fur et à mesure qu'elles sont ajoutées.
- `-c [nombre]` : Affiche les derniers [nombre] octets du fichier.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `tail` :

1. Afficher les 10 dernières lignes d'un fichier :
   ```csh
   tail monfichier.txt
   ```

2. Afficher les 20 dernières lignes d'un fichier :
   ```csh
   tail -n 20 monfichier.txt
   ```

3. Suivre un fichier de log en temps réel :
   ```csh
   tail -f /var/log/syslog
   ```

4. Afficher les 50 derniers octets d'un fichier :
   ```csh
   tail -c 50 monfichier.txt
   ```

## Tips
- Utilisez l'option `-f` pour surveiller les fichiers de log pendant que votre application s'exécute, ce qui est très utile pour le débogage.
- Combinez `tail` avec d'autres commandes comme `grep` pour filtrer les résultats, par exemple :
  ```csh
  tail -f monfichier.txt | grep "Erreur"
  ```
- Pensez à rediriger la sortie vers un fichier si vous souhaitez conserver les dernières lignes pour une analyse ultérieure :
  ```csh
  tail -n 100 monfichier.txt > dernieres_lignes.txt
  ```