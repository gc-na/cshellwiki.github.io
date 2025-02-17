# [Linux] Bash mount použití: Připojení souborových systémů

## Přehled
Příkaz `mount` slouží k připojení souborových systémů k určitému místu v adresářové struktuře operačního systému. Umožňuje uživatelům přistupovat k datům na různých zařízeních, jako jsou pevné disky, USB disky nebo síťové disky.

## Použití
Základní syntaxe příkazu `mount` je následující:

```
mount [options] [arguments]
```

## Běžné možnosti
- `-t <typ>`: Určuje typ souborového systému (např. ext4, ntfs).
- `-o <možnosti>`: Umožňuje specifikovat další možnosti připojení, jako jsou `ro` (jen pro čtení) nebo `rw` (pro čtení a zápis).
- `-a`: Připojí všechny souborové systémy uvedené v souboru `/etc/fstab`.
- `-r`: Připojí souborový systém pouze pro čtení.

## Běžné příklady
1. Připojení USB disku s typem souborového systému `vfat`:
   ```bash
   mount -t vfat /dev/sdb1 /mnt/usb
   ```

2. Připojení síťového disku s možností pouze pro čtení:
   ```bash
   mount -o ro -t nfs 192.168.1.100:/data /mnt/network
   ```

3. Připojení všech souborových systémů podle `/etc/fstab`:
   ```bash
   mount -a
   ```

4. Připojení ext4 souborového systému s možností čtení a zápisu:
   ```bash
   mount -t ext4 /dev/sda1 /mnt/data
   ```

## Tipy
- Před připojením zkontrolujte, zda je cílový adresář existující a prázdný.
- Po dokončení práce nezapomeňte odpojit souborový systém pomocí příkazu `umount`.
- Ujistěte se, že máte potřebná oprávnění pro připojení souborových systémů, často je potřeba spustit příkaz jako superuživatel (root).