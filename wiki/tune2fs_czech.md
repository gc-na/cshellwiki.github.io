# [Linux] Bash tune2fs použití: Správa parametrů souborového systému ext2/ext3/ext4

## Přehled
Příkaz `tune2fs` slouží k úpravě parametrů souborového systému ext2, ext3 a ext4. Umožňuje uživatelům měnit různé vlastnosti souborového systému, jako jsou časové intervaly pro kontrolu, maximální počet připojení a další.

## Použití
Základní syntaxe příkazu je následující:
```bash
tune2fs [možnosti] [argumenty]
```

## Běžné možnosti
- `-c <max_count>`: Nastaví maximální počet připojení před provedením kontroly souborového systému.
- `-i <interval>`: Určuje interval mezi kontrolami souborového systému.
- `-m <reserved_blocks_percentage>`: Nastaví procento rezervovaných bloků pro uživatele root.
- `-L <label>`: Změní štítek souborového systému.
- `-O <feature>`: Přidá nebo odebere funkce souborového systému.

## Běžné příklady
1. **Nastavení maximálního počtu připojení:**
   ```bash
   tune2fs -c 20 /dev/sda1
   ```
   Tento příkaz nastaví maximální počet připojení na 20 pro souborový systém na `/dev/sda1`.

2. **Nastavení intervalu mezi kontrolami:**
   ```bash
   tune2fs -i 2w /dev/sda1
   ```
   Tento příkaz nastaví interval mezi kontrolami na 2 týdny.

3. **Změna štítku souborového systému:**
   ```bash
   tune2fs -L novy_stitek /dev/sda1
   ```
   Tento příkaz změní štítek souborového systému na `novy_stitek`.

4. **Nastavení procenta rezervovaných bloků:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```
   Tento příkaz rezervuje 5 % bloků pro uživatele root.

## Tipy
- Před provedením změn na souborovém systému doporučujeme provést zálohu důležitých dat.
- Používejte příkaz `tune2fs` s opatrností, zejména při změně parametrů, které mohou ovlivnit stabilitu souborového systému.
- Je dobré pravidelně kontrolovat souborový systém pomocí příkazu `fsck`, aby se zajistila jeho integrita.