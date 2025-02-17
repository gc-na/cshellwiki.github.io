# [Linux] Bash parted použití: Správa diskových oddílů

## Přehled
Příkaz `parted` slouží k vytváření, mazání a úpravě diskových oddílů. Umožňuje uživatelům spravovat diskové oddíly na různých typech disků a souborových systémů.

## Použití
Základní syntaxe příkazu `parted` je následující:

```bash
parted [možnosti] [argumenty]
```

## Běžné možnosti
- `-l` : Zobrazí seznam všech dostupných disků a jejich oddílů.
- `mkpart` : Vytvoří nový oddíl.
- `rm` : Odstraní existující oddíl.
- `resizepart` : Změní velikost existujícího oddílu.
- `print` : Zobrazí informace o aktuálních oddílech na disku.

## Běžné příklady
1. **Zobrazení seznamu disků a oddílů:**
   ```bash
   parted -l
   ```

2. **Vytvoření nového oddílu:**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Odstranění oddílu:**
   ```bash
   parted /dev/sda rm 1
   ```

4. **Změna velikosti oddílu:**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **Zobrazení informací o oddílech:**
   ```bash
   parted /dev/sda print
   ```

## Tipy
- Před prováděním změn na oddílech si vždy zálohujte důležitá data.
- Používejte příkaz `print` k ověření aktuálního stavu oddílů před jakýmikoli změnami.
- Při práci s `parted` buďte opatrní, protože nesprávné příkazy mohou vést ke ztrátě dat.