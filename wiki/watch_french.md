# [Linux] C Shell (csh) watch utilisation : surveiller les commandes en temps réel

## Overview
La commande `watch` permet d'exécuter périodiquement une autre commande et d'afficher sa sortie dans le terminal. Cela est particulièrement utile pour surveiller les changements dans les fichiers ou les processus en cours d'exécution.

## Usage
La syntaxe de base de la commande `watch` est la suivante :

```csh
watch [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `watch` :

- `-n <seconds>` : définit l'intervalle de temps en secondes entre chaque exécution de la commande.
- `-d` : met en surbrillance les différences entre les sorties successives.
- `-t` : supprime l'affichage de l'horodatage en haut de l'écran.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `watch` :

1. Surveiller l'utilisation de l'espace disque toutes les 2 secondes :

   ```csh
   watch -n 2 df -h
   ```

2. Afficher les processus en cours d'exécution et mettre en surbrillance les changements :

   ```csh
   watch -d ps aux
   ```

3. Vérifier les modifications dans un fichier texte toutes les 5 secondes :

   ```csh
   watch -n 5 cat /path/to/file.txt
   ```

4. Surveiller l'état d'un service (par exemple, Apache) sans horodatage :

   ```csh
   watch -t systemctl status apache2
   ```

## Tips
- Utilisez l'option `-d` pour mieux visualiser les changements, surtout lorsque vous surveillez des informations qui changent fréquemment.
- Choisissez un intervalle de temps approprié avec `-n` pour éviter de surcharger votre terminal avec des mises à jour trop fréquentes.
- Combinez `watch` avec d'autres commandes pour des tâches de surveillance plus complexes, comme `grep` ou `awk`, pour filtrer les résultats.