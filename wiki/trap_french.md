# [Linux] Bash trap usage : Gérer les signaux et les événements

## Overview
La commande `trap` en Bash permet de spécifier des actions à exécuter lorsqu'un script reçoit certains signaux ou événements. Cela est particulièrement utile pour gérer le nettoyage ou pour intercepter des erreurs avant que le script ne se termine.

## Usage
La syntaxe de base de la commande `trap` est la suivante :

```bash
trap [options] [arguments]
```

## Common Options
- `SIGINT` : Intercepte l'interruption du script (généralement Ctrl+C).
- `SIGTERM` : Intercepte la demande de terminaison du script.
- `EXIT` : Exécute une commande lorsque le script se termine, que ce soit normalement ou par erreur.
- `DEBUG` : Exécute une commande avant chaque ligne de code dans le script.

## Common Examples

### Exemple 1 : Intercepter SIGINT
```bash
trap 'echo "Script interrompu"; exit' SIGINT
while true; do
    echo "Exécution en cours... (appuyez sur Ctrl+C pour interrompre)"
    sleep 2
done
```
Dans cet exemple, lorsque l'utilisateur appuie sur Ctrl+C, le message "Script interrompu" est affiché et le script se termine proprement.

### Exemple 2 : Nettoyage à la sortie
```bash
trap 'rm -f /tmp/tempfile; echo "Fichier temporaire supprimé."' EXIT
touch /tmp/tempfile
echo "Fichier temporaire créé."
```
Ici, le fichier temporaire est supprimé lorsque le script se termine, qu'il se termine normalement ou par une erreur.

### Exemple 3 : Intercepter plusieurs signaux
```bash
trap 'echo "Signal reçu"; exit' SIGINT SIGTERM
while true; do
    echo "En attente d'un signal..."
    sleep 5
done
```
Cet exemple montre comment intercepter plusieurs signaux, permettant au script de répondre à différents types d'interruptions.

## Tips
- Utilisez `trap` pour garantir que les ressources sont libérées correctement, même en cas d'erreur.
- Testez vos scripts avec des signaux pour vous assurer que le comportement est conforme à vos attentes.
- Évitez d'utiliser des commandes complexes dans `trap`, car cela peut rendre le débogage difficile.