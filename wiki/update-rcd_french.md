# [Linux] Bash update-rc.d : Gérer les scripts de démarrage

## Overview
La commande `update-rc.d` est utilisée pour gérer les scripts de démarrage dans les systèmes basés sur Debian. Elle permet d'ajouter, de supprimer ou de modifier des scripts d'initialisation pour les services, facilitant ainsi leur gestion au démarrage et à l'arrêt du système.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
update-rc.d [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `update-rc.d` :

- `defaults` : Installe les liens symboliques par défaut pour le script spécifié.
- `remove` : Supprime les liens symboliques associés au script d'initialisation.
- `enable` : Active le script pour qu'il soit exécuté au démarrage.
- `disable` : Désactive le script pour qu'il ne soit pas exécuté au démarrage.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `update-rc.d` :

1. **Ajouter un script de démarrage par défaut :**
   ```bash
   sudo update-rc.d mon-service defaults
   ```

2. **Supprimer un script de démarrage :**
   ```bash
   sudo update-rc.d mon-service remove
   ```

3. **Activer un script pour le démarrage :**
   ```bash
   sudo update-rc.d mon-service enable
   ```

4. **Désactiver un script pour le démarrage :**
   ```bash
   sudo update-rc.d mon-service disable
   ```

## Tips
- Assurez-vous d'exécuter `update-rc.d` avec les privilèges administratifs (utilisez `sudo`) pour éviter les erreurs de permission.
- Vérifiez toujours l'état des services après avoir modifié les scripts de démarrage pour vous assurer qu'ils fonctionnent comme prévu.
- Utilisez `ls /etc/rc*.d/` pour voir les scripts de démarrage actuellement configurés et leur ordre d'exécution.