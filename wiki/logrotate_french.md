# [Linux] Bash logrotate : Gérer la rotation des fichiers journaux

## Overview
La commande `logrotate` est utilisée pour gérer la rotation des fichiers journaux sur un système Linux. Elle permet de compresser, supprimer ou archiver les fichiers journaux afin de libérer de l'espace disque et de maintenir une organisation efficace des logs.

## Usage
La syntaxe de base de la commande `logrotate` est la suivante :

```bash
logrotate [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `logrotate` :

- `-f` : Force la rotation des journaux, même si cela n'est pas nécessaire.
- `-s` : Spécifie le fichier d'état à utiliser pour suivre les rotations.
- `-d` : Exécute en mode "débogage", affichant ce qui serait fait sans effectuer de changements.
- `-v` : Active le mode verbeux pour afficher des informations détaillées sur le processus de rotation.

## Common Examples

### Exemple 1 : Rotation manuelle d'un fichier journal
Pour forcer la rotation d'un fichier journal spécifique, utilisez la commande suivante :

```bash
logrotate -f /etc/logrotate.conf
```

### Exemple 2 : Exécution en mode débogage
Pour voir ce que `logrotate` ferait sans effectuer de changements, utilisez :

```bash
logrotate -d /etc/logrotate.conf
```

### Exemple 3 : Rotation avec un fichier d'état personnalisé
Pour utiliser un fichier d'état différent, vous pouvez spécifier :

```bash
logrotate -s /var/lib/logrotate/status /etc/logrotate.conf
```

### Exemple 4 : Rotation quotidienne des journaux
Si vous souhaitez configurer une rotation quotidienne pour un fichier journal, vous pouvez ajouter une entrée dans le fichier de configuration :

```bash
/var/log/example.log {
    daily
    rotate 7
    compress
    missingok
    notifempty
}
```

## Tips
- **Planifiez des rotations régulières** : Utilisez `cron` pour exécuter `logrotate` à intervalles réguliers.
- **Surveillez l'espace disque** : Assurez-vous que vos fichiers journaux ne consomment pas trop d'espace disque.
- **Testez vos configurations** : Utilisez le mode débogage pour tester vos configurations avant de les appliquer.
- **Gardez une copie des logs importants** : Si certains journaux sont critiques, envisagez de les sauvegarder avant la rotation.