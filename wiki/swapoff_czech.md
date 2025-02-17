# [Linux] Bash swapoff použití: Deaktivace swap prostoru

## Přehled
Příkaz `swapoff` se používá k deaktivaci swap prostoru v systému. Swap prostor je část disku, která se používá jako virtuální paměť, když fyzická paměť (RAM) není dostatečná. Deaktivace swapu může být užitečná při optimalizaci výkonu systému nebo při provádění údržby.

## Použití
Základní syntaxe příkazu `swapoff` je následující:

```bash
swapoff [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Deaktivuje všechny swap soubory a oddíly uvedené v souboru `/etc/fstab`.
- `-e`: Ignoruje chyby při deaktivaci swapu.
- `-h`: Zobrazí nápovědu k příkazu.

## Běžné příklady
1. Deaktivace všech swap prostorů uvedených v `/etc/fstab`:

    ```bash
    swapoff -a
    ```

2. Deaktivace konkrétního swap souboru:

    ```bash
    swapoff /path/to/swapfile
    ```

3. Deaktivace swapu s ignorováním chyb:

    ```bash
    swapoff -e /path/to/swapfile
    ```

## Tipy
- Před deaktivací swapu se ujistěte, že máte dostatečnou fyzickou paměť, aby systém mohl fungovat bez swapu.
- Po deaktivaci swapu můžete použít příkaz `free -h` pro kontrolu stavu paměti.
- Pokud plánujete trvale deaktivovat swap, zvažte úpravu souboru `/etc/fstab`, abyste odstranili příslušné záznamy.