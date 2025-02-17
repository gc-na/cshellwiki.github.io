# [Linux] Bash nslookup Utilisation : Résoudre des noms de domaine en adresses IP

## Overview
La commande `nslookup` est un outil de ligne de commande utilisé pour interroger les serveurs DNS afin de résoudre les noms de domaine en adresses IP. Elle permet également d'obtenir des informations sur les enregistrements DNS associés à un domaine.

## Usage
La syntaxe de base de la commande `nslookup` est la suivante :

```bash
nslookup [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `nslookup` :

- `-type=TYPE` : Spécifie le type d'enregistrement DNS à interroger (par exemple, A, AAAA, MX).
- `-timeout=SEC` : Définit le délai d'attente en secondes pour une réponse du serveur DNS.
- `-retry=NUM` : Définit le nombre de tentatives de requête en cas d'échec.
- `server` : Permet de spécifier un serveur DNS différent pour la requête.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `nslookup` :

1. **Résoudre un nom de domaine en adresse IP :**
   ```bash
   nslookup example.com
   ```

2. **Obtenir des enregistrements MX d'un domaine :**
   ```bash
   nslookup -type=MX example.com
   ```

3. **Interroger un serveur DNS spécifique :**
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. **Changer le type d'enregistrement à AAAA pour obtenir l'adresse IPv6 :**
   ```bash
   nslookup -type=AAAA example.com
   ```

## Tips
- Utilisez `nslookup` en mode interactif en tapant simplement `nslookup` sans arguments pour entrer dans le mode de requête, où vous pouvez effectuer plusieurs recherches sans redémarrer la commande.
- Vérifiez toujours les enregistrements DNS avec plusieurs serveurs pour confirmer la validité des résultats.
- Pensez à utiliser l'option `-timeout` pour ajuster le délai d'attente si vous interrogez des serveurs DNS lents.