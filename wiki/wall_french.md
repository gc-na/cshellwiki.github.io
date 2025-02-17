# [Linux] Bash wall : envoyer des messages à tous les utilisateurs connectés

## Overview
La commande `wall` (write to all) permet d'envoyer un message à tous les utilisateurs connectés à un système Linux. C'est un outil utile pour les administrateurs système qui souhaitent communiquer des informations importantes à tous les utilisateurs simultanément.

## Usage
La syntaxe de base de la commande `wall` est la suivante :

```bash
wall [options] [arguments]
```

## Common Options
- `-n` : Ne pas envoyer le message aux utilisateurs qui ne sont pas connectés à un terminal.
- `-s` : Utiliser un format de message court, sans retour à la ligne.
- `-f` : Lire le message à partir d'un fichier au lieu de l'entrée standard.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `wall` :

1. **Envoyer un message simple :**
   ```bash
   wall "Attention, le système sera hors ligne pour maintenance à 22h."
   ```

2. **Envoyer un message à partir d'un fichier :**
   ```bash
   wall -f message.txt
   ```

3. **Envoyer un message court :**
   ```bash
   wall -s "Rappel : réunion à 15h."
   ```

4. **Envoyer un message sans le transmettre aux utilisateurs non connectés :**
   ```bash
   wall -n "Mise à jour du système en cours, veuillez patienter."
   ```

## Tips
- Utilisez `wall` avec précaution, car les messages peuvent interrompre le travail des utilisateurs.
- Pour des messages importants, envisagez d'utiliser `wall` pendant des heures creuses pour minimiser les interruptions.
- Vous pouvez combiner `wall` avec d'autres commandes pour automatiser l'envoi de messages, par exemple, en utilisant un script cron.