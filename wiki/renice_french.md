# [Linux] C Shell (csh) renice : Modifier la priorité d'un processus

## Overview
La commande `renice` permet de modifier la priorité d'un ou plusieurs processus en cours d'exécution. Cela peut être utile pour augmenter ou diminuer la quantité de ressources système qu'un processus utilise, ce qui peut améliorer les performances d'autres processus.

## Usage
La syntaxe de base de la commande `renice` est la suivante :

```csh
renice [options] [arguments]
```

## Common Options
- `-n` : Spécifie la nouvelle valeur de priorité à appliquer. La valeur peut être positive (pour diminuer la priorité) ou négative (pour augmenter la priorité).
- `-p` : Permet de spécifier les identifiants de processus (PID) à modifier.
- `-g` : Modifie la priorité de tous les processus d'un groupe de processus spécifié.
- `-u` : Modifie la priorité de tous les processus appartenant à un utilisateur spécifié.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `renice` :

1. **Modifier la priorité d'un processus spécifique :**
   Pour augmenter la priorité d'un processus avec le PID 1234 :
   ```csh
   renice -n -5 -p 1234
   ```

2. **Modifier la priorité de plusieurs processus :**
   Pour diminuer la priorité de plusieurs processus avec les PIDs 1234 et 5678 :
   ```csh
   renice -n 10 -p 1234 5678
   ```

3. **Modifier la priorité de tous les processus d'un utilisateur :**
   Pour diminuer la priorité de tous les processus de l'utilisateur "alice" :
   ```csh
   renice -n 5 -u alice
   ```

4. **Modifier la priorité de tous les processus d'un groupe :**
   Pour augmenter la priorité de tous les processus du groupe de processus 1001 :
   ```csh
   renice -n -3 -g 1001
   ```

## Tips
- Vérifiez toujours la priorité actuelle d'un processus avec la commande `ps` avant d'utiliser `renice`.
- Utilisez des valeurs de priorité judicieusement ; une priorité trop élevée pour un processus peut nuire à la réactivité du système.
- Vous devez avoir les permissions appropriées pour modifier la priorité des processus d'autres utilisateurs.