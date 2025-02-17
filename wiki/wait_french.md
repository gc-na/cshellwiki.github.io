# [Linux] Bash wait : Attendre la fin des processus

## Overview
La commande `wait` en Bash est utilisée pour attendre la fin d'un ou plusieurs processus en arrière-plan. Elle est particulièrement utile lorsque vous lancez des tâches en parallèle et que vous souhaitez synchroniser leur achèvement avant de continuer l'exécution d'un script.

## Usage
La syntaxe de base de la commande `wait` est la suivante :

```bash
wait [options] [arguments]
```

## Common Options
- `-n` : Attend la fin du prochain processus en arrière-plan.
- `PID` : Spécifiez l'identifiant du processus (PID) pour lequel vous souhaitez attendre la fin.

## Common Examples

### Exemple 1 : Attendre tous les processus en arrière-plan
```bash
sleep 5 &
sleep 3 &
wait
echo "Tous les processus sont terminés."
```
Dans cet exemple, le script attend que les deux commandes `sleep` se terminent avant d'afficher le message.

### Exemple 2 : Attendre un processus spécifique
```bash
sleep 5 &
PID=$!
echo "Attente du processus avec PID $PID..."
wait $PID
echo "Le processus $PID est terminé."
```
Ici, le script attend spécifiquement que le processus `sleep` avec l'identifiant `$PID` se termine.

### Exemple 3 : Utiliser l'option -n
```bash
sleep 2 &
sleep 4 &
wait -n
echo "Un des processus en arrière-plan est terminé."
```
Cet exemple montre comment utiliser l'option `-n` pour attendre la fin du prochain processus en arrière-plan.

## Tips
- Utilisez `wait` dans des scripts pour gérer des tâches parallèles et éviter les conflits de ressources.
- Vérifiez les codes de sortie des processus en utilisant `wait` pour une gestion d'erreurs plus efficace.
- Combinez `wait` avec des structures de contrôle comme `if` pour exécuter des actions conditionnelles basées sur le succès ou l'échec des processus.