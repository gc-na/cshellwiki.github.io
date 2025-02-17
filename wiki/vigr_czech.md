# [Linux] Bash vigr použití: Úprava souborů s uživatelskými účty

## Přehled
Příkaz `vigr` slouží k bezpečné úpravě souboru `/etc/group` a `/etc/passwd`, které obsahují informace o uživatelských účtech a skupinách v systému. Tento příkaz zajišťuje, že při editaci souborů nedojde k jejich poškození, a to díky zámku souboru a kontrole syntaxe.

## Použití
Základní syntaxe příkazu `vigr` je následující:

```bash
vigr [možnosti] [soubor]
```

## Běžné možnosti
- `-s`: Spustí příkaz v režimu pouze pro čtení.
- `-f <soubor>`: Umožňuje specifikovat jiný soubor pro úpravu než výchozí `/etc/passwd`.
- `-h`: Zobrazí nápovědu k příkazu.

## Běžné příklady
1. Otevření souboru `/etc/passwd` pro úpravy:
   ```bash
   sudo vigr
   ```

2. Otevření souboru `/etc/group` pro úpravy:
   ```bash
   sudo vigr -f /etc/group
   ```

3. Otevření souboru s uživatelskými účty v režimu pouze pro čtení:
   ```bash
   sudo vigr -s
   ```

## Tipy
- Vždy používejte `sudo`, pokud potřebujete upravit systémové soubory, abyste měli potřebná oprávnění.
- Před provedením změn v souborech doporučujeme vytvořit zálohu, abyste se vyhnuli ztrátě dat.
- Po úpravě souboru zkontrolujte, zda nedošlo k syntaktickým chybám, což `vigr` provádí automaticky.