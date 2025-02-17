# [Linux] Bash bunzip2 použití: Rozbalení souborů ve formátu bzip2

## Přehled
Příkaz `bunzip2` slouží k dekompresi souborů, které byly komprimovány pomocí algoritmu bzip2. Tento příkaz odstraní kompresi z cílového souboru a vytvoří původní soubor.

## Použití
Základní syntaxe příkazu `bunzip2` je následující:

```bash
bunzip2 [možnosti] [argumenty]
```

## Běžné možnosti
- `-k`, `--keep`: Zachová původní komprimovaný soubor po dekompresi.
- `-f`, `--force`: Přepíše existující soubory bez dotazu.
- `-v`, `--verbose`: Zobrazí podrobnosti o procesu dekomprese.

## Běžné příklady
1. **Dekomprimace souboru**:
   ```bash
   bunzip2 soubor.bz2
   ```
   Tento příkaz dekomprimuje soubor `soubor.bz2` a vytvoří `soubor`.

2. **Dekomprimace souboru a zachování původního**:
   ```bash
   bunzip2 -k soubor.bz2
   ```
   Tento příkaz dekomprimuje `soubor.bz2`, ale ponechá původní soubor.

3. **Dekomprimace s přepsáním existujícího souboru**:
   ```bash
   bunzip2 -f soubor.bz2
   ```
   Tento příkaz dekomprimuje `soubor.bz2` a přepíše existující soubor, pokud je to potřeba.

4. **Zobrazit podrobnosti o dekompresi**:
   ```bash
   bunzip2 -v soubor.bz2
   ```
   Tento příkaz dekomprimuje soubor a zároveň zobrazí informace o procesu.

## Tipy
- Před použitím `bunzip2` se ujistěte, že máte zálohu důležitých souborů, zejména pokud používáte možnost `-f`.
- Pokud často pracujete se soubory bzip2, zvažte použití `bzip2` pro kompresi a `bunzip2` pro dekompresi, abyste optimalizovali úložiště.
- Používejte možnost `-k`, pokud si nejste jisti, zda potřebujete původní soubor, dokud si neověříte, že dekomprese proběhla úspěšně.