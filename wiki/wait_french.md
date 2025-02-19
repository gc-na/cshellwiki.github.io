# [Linux] C Shell (csh) wait : Attendre la fin d'un processus

## Overview
La commande `wait` dans C Shell (csh) est utilisée pour suspendre l'exécution d'un script jusqu'à ce qu'un ou plusieurs processus enfants se terminent. Cela permet de synchroniser les tâches dans un environnement shell.

## Usage
La syntaxe de base de la commande est la suivante :

```csh
wait [options] [arguments]
```

## Common Options
- `pid` : Spécifie l'identifiant du processus (PID) pour lequel vous souhaitez attendre la fin.
- `-n` : Attend la fin de n'importe quel processus enfant.

## Common Examples

### Exemple 1 : Attendre un processus spécifique
Pour attendre qu'un processus avec un PID spécifique se termine, vous pouvez utiliser :

```csh
wait 1234
```
Ici, `1234` est l'identifiant du processus que vous attendez.

### Exemple 2 : Attendre tous les processus enfants
Pour attendre que tous les processus enfants se terminent, utilisez simplement :

```csh
wait
```

### Exemple 3 : Attendre un processus en arrière-plan
Si vous avez lancé un processus en arrière-plan, par exemple :

```csh
sleep 10 &
```
Vous pouvez attendre qu'il se termine avec :

```csh
wait $!
```
Ici, `$!` fait référence au dernier processus lancé en arrière-plan.

## Tips
- Utilisez `wait` dans des scripts pour gérer l'ordre d'exécution des tâches.
- Vérifiez le statut de sortie d'un processus après `wait` en utilisant `$?` pour savoir s'il s'est terminé avec succès.
- Évitez d'utiliser `wait` sans spécifier de PID si vous avez plusieurs processus en arrière-plan, car cela peut rendre difficile le suivi de l'état de chaque processus.