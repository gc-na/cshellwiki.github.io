# [Linux] Bash last commande : afficher les connexions des utilisateurs

## Overview
La commande `last` est utilisée pour afficher les connexions des utilisateurs sur un système Linux. Elle lit le fichier `/var/log/wtmp` pour afficher une liste des connexions, des déconnexions et des redémarrages du système.

## Usage
La syntaxe de base de la commande `last` est la suivante :

```bash
last [options] [arguments]
```

## Common Options
- `-a` : Affiche l'adresse IP ou le nom d'hôte de l'utilisateur connecté.
- `-n [nombre]` : Limite le nombre d'entrées affichées à `[nombre]`.
- `-R` : Ne pas afficher le nom d'hôte.
- `-x` : Affiche les connexions de tous les utilisateurs, y compris les redémarrages et les arrêts.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `last` :

1. Afficher toutes les connexions des utilisateurs :
   ```bash
   last
   ```

2. Afficher les 5 dernières connexions :
   ```bash
   last -n 5
   ```

3. Afficher les connexions avec les adresses IP :
   ```bash
   last -a
   ```

4. Afficher les connexions sans les noms d'hôte :
   ```bash
   last -R
   ```

5. Afficher les connexions ainsi que les redémarrages :
   ```bash
   last -x
   ```

## Tips
- Utilisez `last -n 10` pour obtenir rapidement les 10 dernières connexions, ce qui peut être utile pour un aperçu rapide.
- Combinez `last` avec d'autres commandes comme `grep` pour filtrer les résultats par utilisateur spécifique.
- Consultez le fichier `/var/log/wtmp` directement avec `last -f /chemin/vers/wtmp` si vous souhaitez analyser un fichier de journal spécifique.