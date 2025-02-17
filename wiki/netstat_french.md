# [Linux] Bash netstat Utilisation : Afficher les connexions réseau

## Overview
La commande `netstat` est un outil puissant qui permet d'afficher des informations sur les connexions réseau, les tables de routage, et les statistiques d'interface. Elle est souvent utilisée pour diagnostiquer des problèmes de réseau et surveiller l'activité réseau sur un système.

## Usage
La syntaxe de base de la commande `netstat` est la suivante :

```bash
netstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `netstat` :

- `-a` : Affiche toutes les connexions et ports d'écoute.
- `-t` : Affiche uniquement les connexions TCP.
- `-u` : Affiche uniquement les connexions UDP.
- `-n` : Affiche les adresses et numéros de port sous forme numérique, sans tenter de résoudre les noms d'hôte.
- `-l` : Affiche uniquement les ports d'écoute.
- `-p` : Affiche le PID et le nom du programme associé à chaque connexion.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `netstat` :

1. **Afficher toutes les connexions et ports d'écoute :**
   ```bash
   netstat -a
   ```

2. **Afficher uniquement les connexions TCP :**
   ```bash
   netstat -t
   ```

3. **Afficher les connexions UDP avec des adresses numériques :**
   ```bash
   netstat -u -n
   ```

4. **Afficher les ports d'écoute :**
   ```bash
   netstat -l
   ```

5. **Afficher les connexions avec le PID et le nom du programme :**
   ```bash
   netstat -p
   ```

## Tips
- Utilisez `netstat -tuln` pour obtenir une vue d'ensemble des ports TCP et UDP en écoute sans résolution de nom, ce qui peut accélérer l'affichage.
- Combinez plusieurs options pour obtenir des informations plus détaillées, par exemple `netstat -tulpan` pour voir les connexions avec les détails des processus.
- Pensez à exécuter `netstat` avec des privilèges d'administrateur pour voir toutes les connexions, y compris celles qui appartiennent à d'autres utilisateurs.