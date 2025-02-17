# [Linux] Bash vgcreate použití: Vytváření svazků v Logical Volume Management

## Přehled
Příkaz `vgcreate` se používá k vytváření nových svazků (volume groups) v systému správy logických svazků (LVM). Tento příkaz umožňuje uživatelům organizovat fyzické svazky do logických skupin, což usnadňuje správu a alokaci úložného prostoru.

## Použití
Základní syntaxe příkazu `vgcreate` je následující:

```bash
vgcreate [možnosti] [název_svazku] [fyzické_svazky]
```

## Běžné možnosti
- `-s, --stripes <n>`: Určuje počet pruhů pro svazek.
- `-l, --maxlogicalextents <n>`: Nastavuje maximální počet logických rozšíření pro svazek.
- `-p, --maxphysicalextents <n>`: Nastavuje maximální počet fyzických rozšíření pro svazek.
- `-f, --force`: Přepíše existující svazek bez potvrzení.

## Běžné příklady
1. Vytvoření nového svazku s názvem `myvg` z fyzického svazku `/dev/sda1`:

    ```bash
    vgcreate myvg /dev/sda1
    ```

2. Vytvoření svazku `datavg` z více fyzických svazků:

    ```bash
    vgcreate datavg /dev/sdb1 /dev/sdc1
    ```

3. Vytvoření svazku s určeným počtem pruhů:

    ```bash
    vgcreate -s 64k myvg /dev/sda1
    ```

## Tipy
- Před použitím `vgcreate` se ujistěte, že fyzické svazky, které chcete použít, nejsou již součástí jiného svazku.
- Je dobré mít zálohu důležitých dat, protože operace s LVM mohou mít vliv na úložný prostor.
- Používejte volbu `--force` opatrně, abyste neztratili důležitá data.