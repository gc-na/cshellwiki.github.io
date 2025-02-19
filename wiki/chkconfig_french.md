# [Linux] C Shell (csh) chkconfig : Gérer les services système

## Overview
La commande `chkconfig` est utilisée pour gérer les services système sur les systèmes basés sur Linux. Elle permet d'activer ou de désactiver des services au démarrage, facilitant ainsi la gestion des processus qui s'exécutent automatiquement lors du démarrage du système.

## Usage
La syntaxe de base de la commande `chkconfig` est la suivante :

```csh
chkconfig [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `chkconfig` :

- `--list` : Affiche la liste de tous les services et leur statut.
- `--add <service>` : Ajoute un service à la gestion de `chkconfig`.
- `--remove <service>` : Supprime un service de la gestion de `chkconfig`.
- `--level <niveau>` : Définit le niveau d'exécution pour lequel le service doit être activé ou désactivé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `chkconfig` :

1. **Lister tous les services :**
   ```csh
   chkconfig --list
   ```

2. **Activer un service au démarrage :**
   ```csh
   chkconfig httpd on
   ```

3. **Désactiver un service au démarrage :**
   ```csh
   chkconfig httpd off
   ```

4. **Ajouter un nouveau service :**
   ```csh
   chkconfig --add myservice
   ```

5. **Supprimer un service existant :**
   ```csh
   chkconfig --remove myservice
   ```

## Tips
- Assurez-vous d'exécuter `chkconfig` avec des privilèges d'administrateur pour apporter des modifications aux services.
- Utilisez `chkconfig --list` régulièrement pour vérifier l'état des services et éviter les démarrages inutiles.
- Lorsque vous ajoutez un nouveau service, vérifiez que le script d'initialisation est correctement configuré pour éviter des erreurs au démarrage.