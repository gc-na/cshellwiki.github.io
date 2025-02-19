# [Unix] C Shell (csh) bg : Mettre un processus en arrière-plan

## Overview
La commande `bg` dans C Shell (csh) permet de reprendre un processus suspendu et de l'exécuter en arrière-plan. Cela est particulièrement utile lorsque vous souhaitez continuer à utiliser le terminal tout en laissant un programme s'exécuter.

## Usage
La syntaxe de base de la commande `bg` est la suivante :

```csh
bg [options] [arguments]
```

## Common Options
- **%job_id** : Spécifie le numéro de job du processus que vous souhaitez mettre en arrière-plan. Par exemple, `%1` pour le premier job.
- **-l** : Affiche les jobs en arrière-plan avec des informations supplémentaires.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `bg` :

1. **Mettre un job en arrière-plan** :
   Si vous avez suspendu un job (par exemple, en appuyant sur `Ctrl+Z`), vous pouvez le mettre en arrière-plan avec :
   ```csh
   bg %1
   ```

2. **Mettre tous les jobs suspendus en arrière-plan** :
   Pour mettre tous les jobs suspendus en arrière-plan, utilisez :
   ```csh
   bg
   ```

3. **Vérifier l'état des jobs** :
   Avant de mettre un job en arrière-plan, vous pouvez vérifier l'état des jobs avec :
   ```csh
   jobs
   ```

## Tips
- Utilisez la commande `jobs` pour voir tous les jobs en cours et leur état avant de décider lequel mettre en arrière-plan.
- N'oubliez pas que les processus en arrière-plan peuvent continuer à s'exécuter même si vous fermez le terminal, selon la manière dont ils sont lancés.
- Pour ramener un processus en avant-plan, utilisez la commande `fg` suivie du numéro de job, par exemple :
  ```csh
  fg %1
  ```