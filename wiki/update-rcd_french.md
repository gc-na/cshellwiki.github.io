# [Linux] C Shell (csh) update-rc.d : Gérer les scripts de démarrage

## Overview
La commande `update-rc.d` est utilisée pour ajouter, supprimer ou gérer les scripts de démarrage dans les systèmes basés sur Debian. Elle permet de configurer comment et quand les services doivent être lancés ou arrêtés lors du démarrage ou de l'arrêt du système.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
update-rc.d [options] [arguments]
```

## Common Options
- `defaults` : Installe les scripts avec les niveaux d'exécution par défaut.
- `remove` : Supprime le script de démarrage du système.
- `enable` : Active le script pour qu'il soit exécuté au démarrage.
- `disable` : Désactive le script pour qu'il ne soit pas exécuté au démarrage.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `update-rc.d` :

1. **Ajouter un script de démarrage avec les paramètres par défaut :**
   ```bash
   update-rc.d mon-service defaults
   ```

2. **Supprimer un script de démarrage :**
   ```bash
   update-rc.d mon-service remove
   ```

3. **Activer un script de démarrage :**
   ```bash
   update-rc.d mon-service enable
   ```

4. **Désactiver un script de démarrage :**
   ```bash
   update-rc.d mon-service disable
   ```

## Tips
- Assurez-vous que le script de démarrage est exécutable avant de l'ajouter avec `update-rc.d`.
- Utilisez `ls /etc/rc*.d/` pour vérifier les scripts de démarrage existants et leur ordre d'exécution.
- Pour des modifications plus avancées, consultez la documentation de votre système pour comprendre les niveaux d'exécution et leur impact sur le démarrage des services.