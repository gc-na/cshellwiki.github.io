# [Linux] Bash mesg : Contrôle des messages de terminal

## Overview
La commande `mesg` permet de contrôler la réception de messages sur un terminal. Elle est souvent utilisée pour permettre ou interdire aux autres utilisateurs d'envoyer des messages via la commande `write`.

## Usage
La syntaxe de base de la commande `mesg` est la suivante :

```bash
mesg [options] [arguments]
```

## Common Options
- `y` : Autorise la réception de messages.
- `n` : Interdit la réception de messages.
- `--help` : Affiche l'aide sur l'utilisation de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mesg` :

1. **Autoriser la réception de messages :**
   ```bash
   mesg y
   ```

2. **Interdire la réception de messages :**
   ```bash
   mesg n
   ```

3. **Vérifier l'état actuel de la réception de messages :**
   ```bash
   mesg
   ```

## Tips
- Utilisez `mesg n` si vous ne souhaitez pas être dérangé par des messages pendant que vous travaillez.
- Pensez à réactiver la réception de messages avec `mesg y` lorsque vous êtes prêt à recevoir des communications.
- Vérifiez régulièrement l'état de votre terminal avec `mesg` pour vous assurer que vos préférences sont respectées.