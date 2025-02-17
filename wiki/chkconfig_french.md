# [Linux] Bash chkconfig : Gérer les services système

## Overview
La commande `chkconfig` est utilisée pour gérer les services système sur les distributions Linux basées sur SysVinit. Elle permet d'activer ou de désactiver des services au démarrage du système, facilitant ainsi la gestion des processus qui s'exécutent automatiquement.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
chkconfig [options] [arguments]
```

## Common Options
- `--list` : Affiche la liste des services et leur statut.
- `--add` : Ajoute un service à la gestion de `chkconfig`.
- `--del` : Supprime un service de la gestion de `chkconfig`.
- `--level` : Spécifie les niveaux d'exécution pour lesquels le service doit être activé ou désactivé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `chkconfig` :

1. **Lister tous les services et leur statut :**
   ```bash
   chkconfig --list
   ```

2. **Activer un service au démarrage :**
   ```bash
   chkconfig httpd on
   ```

3. **Désactiver un service au démarrage :**
   ```bash
   chkconfig httpd off
   ```

4. **Ajouter un nouveau service :**
   ```bash
   chkconfig --add myservice
   ```

5. **Supprimer un service de la gestion :**
   ```bash
   chkconfig --del myservice
   ```

## Tips
- Toujours vérifier l'état des services après les modifications avec `chkconfig --list`.
- Utiliser `service [nom_du_service] start|stop|restart` pour gérer les services manuellement.
- Soyez prudent lorsque vous modifiez les services au démarrage, car cela peut affecter la stabilité de votre système.