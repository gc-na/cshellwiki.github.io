# [Linux] Bash lsmod použití: Zobrazí seznam načtených modulů jádra

## Přehled
Příkaz `lsmod` slouží k zobrazení seznamu aktuálně načtených modulů jádra v systému Linux. Tento příkaz je užitečný pro správu a diagnostiku modulů, které ovlivňují chování jádra.

## Použití
Základní syntaxe příkazu je následující:

```bash
lsmod [options] [arguments]
```

## Běžné možnosti
- **-h, --help**: Zobrazí nápovědu k příkazu.
- **-v, --verbose**: Zobrazí podrobnější informace o načtených modulech.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `lsmod`:

1. **Zobrazení všech načtených modulů**:
   ```bash
   lsmod
   ```

2. **Zobrazení nápovědy k příkazu**:
   ```bash
   lsmod --help
   ```

3. **Zobrazení podrobnějších informací o modulech**:
   ```bash
   lsmod --verbose
   ```

## Tipy
- Používejte `lsmod` společně s dalšími příkazy, jako je `modinfo`, pro získání více informací o konkrétních modulech.
- Pokud potřebujete zjistit, které moduly závisí na jiných, použijte příkaz `modprobe` s volbou `-r` pro odstranění modulů a následně `lsmod` pro kontrolu aktuálního stavu.
- Pravidelně kontrolujte načtené moduly, zejména po instalaci nového hardwaru nebo aktualizaci systému, abyste zajistili správnou funkčnost.