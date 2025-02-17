# [Linux] Bash depmod použití: Správa modulů jádra

## Přehled
Příkaz `depmod` se používá k vytváření a aktualizaci souboru závislostí pro moduly jádra v Linuxu. Tento příkaz analyzuje moduly a vytváří soubor, který informuje jádro o tom, které moduly jsou závislé na jiných modulech.

## Použití
Základní syntaxe příkazu `depmod` je následující:

```bash
depmod [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`, `--all`: Zpracuje všechny moduly v aktuálním adresáři.
- `-n`, `--show`: Zobrazí, co by bylo provedeno, ale nevytvoří žádné soubory.
- `-F`, `--file`: Umožňuje specifikovat alternativní soubor pro moduly.
- `-r`, `--remove`: Odstraní staré soubory závislostí.

## Běžné příklady
1. **Vytvoření závislostí pro všechny moduly:**
   ```bash
   depmod
   ```

2. **Zobrazení, co by bylo provedeno bez skutečného provedení:**
   ```bash
   depmod -n
   ```

3. **Vytvoření závislostí pro specifický adresář:**
   ```bash
   depmod -F /path/to/modules
   ```

4. **Odstranění starých souborů závislostí:**
   ```bash
   depmod -r
   ```

## Tipy
- Před provedením příkazu `depmod` se ujistěte, že máte potřebná oprávnění, obvykle jako uživatel root.
- Pravidelně spouštějte `depmod` po instalaci nových modulů jádra, aby se zajistilo, že závislosti jsou aktuální.
- Použijte volbu `-n` pro testování, zda příkaz funguje správně, než provedete skutečné změny.