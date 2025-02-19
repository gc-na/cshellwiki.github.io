# [Linux] C Shell (csh) dig : interroger des serveurs DNS

## Overview
La commande `dig` (Domain Information Groper) est un outil puissant utilisé pour interroger les serveurs DNS. Elle permet aux utilisateurs de récupérer des informations sur les enregistrements DNS d'un domaine, tels que les adresses IP, les enregistrements MX, et bien plus encore.

## Usage
La syntaxe de base de la commande `dig` est la suivante :

```bash
dig [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `dig` :

- `@server` : Spécifie le serveur DNS à interroger.
- `-t type` : Définit le type d'enregistrement à rechercher (par exemple, A, MX, TXT).
- `+short` : Affiche une sortie simplifiée, ne montrant que les résultats pertinents.
- `+trace` : Suit la chaîne de résolution DNS pour un nom de domaine donné.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `dig` :

1. **Interroger l'enregistrement A d'un domaine :**
   ```bash
   dig example.com A
   ```

2. **Obtenir l'enregistrement MX d'un domaine :**
   ```bash
   dig example.com MX
   ```

3. **Utiliser un serveur DNS spécifique :**
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Afficher une sortie simplifiée :**
   ```bash
   dig example.com +short
   ```

5. **Suivre la chaîne de résolution DNS :**
   ```bash
   dig example.com +trace
   ```

## Tips
- Utilisez l'option `+short` pour obtenir des résultats plus lisibles, surtout si vous ne souhaitez que l'adresse IP.
- Pour des diagnostics approfondis, l'option `+trace` peut être très utile pour comprendre comment un nom de domaine est résolu.
- Pensez à vérifier plusieurs types d'enregistrements (A, AAAA, MX, TXT) pour obtenir une vue complète des informations DNS d'un domaine.