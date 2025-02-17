# [Linux] Bash vgextend použití: Rozšíření skupiny svazků

## Přehled
Příkaz `vgextend` se používá v systému Linux pro rozšíření skupiny svazků (Volume Group) o nové fyzické svazky (Physical Volumes). Tento příkaz je součástí systému LVM (Logical Volume Manager), který umožňuje flexibilní správu diskového prostoru.

## Použití
Základní syntaxe příkazu `vgextend` je následující:

```
vgextend [možnosti] [argumenty]
```

## Běžné možnosti
- `-l, --extents <rozsah>`: Určuje počet rozšíření, která mají být přidána do skupiny svazků.
- `-n, --noheadings`: Potlačuje hlavičky v výstupu.
- `-f, --force`: Vynutí akci, i když by mohla být nebezpečná.
- `--test`: Provádí testovací běh bez skutečné aplikace změn.

## Běžné příklady
1. **Rozšíření skupiny svazků o jeden fyzický svazek:**
   ```bash
   vgextend moje_skupina /dev/sdb1
   ```

2. **Rozšíření skupiny svazků o více fyzických svazků:**
   ```bash
   vgextend moje_skupina /dev/sdb1 /dev/sdc1
   ```

3. **Rozšíření skupiny svazků s určením počtu rozšíření:**
   ```bash
   vgextend -l +5 moje_skupina /dev/sdb1
   ```

4. **Testovací běh příkazu bez aplikace změn:**
   ```bash
   vgextend --test moje_skupina /dev/sdb1
   ```

## Tipy
- Před použitím příkazu `vgextend` se ujistěte, že fyzické svazky, které chcete přidat, jsou správně inicializovány jako LVM.
- Vždy je dobré provést zálohu dat před prováděním změn v diskovém uspořádání.
- Používejte možnost `--test`, abyste se ujistili, že příkaz provede požadované akce, než jej skutečně spustíte.