# [Linux] Bash mkfs použití: Vytváření souborových systémů

## Přehled
Příkaz `mkfs` (make filesystem) se používá k vytváření souborových systémů na diskových oddílech. Tento příkaz formátuje zvolený oddíl a připravuje ho pro ukládání dat.

## Použití
Základní syntaxe příkazu je následující:
```bash
mkfs [možnosti] [argumenty]
```

## Běžné možnosti
- `-t, --type <typ>`: Určuje typ souborového systému (např. ext4, xfs).
- `-L, --label <název>`: Přiřazuje štítek souborovému systému.
- `-n, --no-mtab`: Nezapisuje do souboru mtab.
- `-V, --verbose`: Zobrazí podrobné informace během procesu.

## Běžné příklady
1. Vytvoření souborového systému ext4 na oddílu `/dev/sdb1`:
   ```bash
   mkfs -t ext4 /dev/sdb1
   ```

2. Vytvoření souborového systému XFS s přiřazením štítku:
   ```bash
   mkfs -t xfs -L mylabel /dev/sdc1
   ```

3. Vytvoření souborového systému FAT32:
   ```bash
   mkfs -t vfat /dev/sdd1
   ```

4. Vytvoření souborového systému s podrobným výstupem:
   ```bash
   mkfs -t ext4 -V /dev/sde1
   ```

## Tipy
- Před použitím příkazu `mkfs` se ujistěte, že máte zálohovaná všechna důležitá data, protože formátování vymaže veškerý obsah oddílu.
- Používejte volbu `-L` pro snadnější identifikaci souborových systémů, zejména pokud máte více oddílů.
- Pokud nejste si jisti, jaký typ souborového systému použít, `ext4` je často dobrá volba pro většinu Linuxových distribucí.