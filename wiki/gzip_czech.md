# [Linux] Bash gzip použití: Komprimace souborů

## Přehled
Příkaz `gzip` slouží k komprimaci souborů pomocí algoritmu DEFLATE. Tento nástroj je široce používán pro zmenšení velikosti souborů, což usnadňuje jejich přenos a ukládání.

## Použití
Základní syntaxe příkazu `gzip` je následující:

```bash
gzip [možnosti] [argumenty]
```

## Běžné možnosti
- `-d` nebo `--decompress`: Rozbalí komprimovaný soubor.
- `-k` nebo `--keep`: Zachová původní soubor po komprimaci.
- `-v` nebo `--verbose`: Zobrazí podrobnosti o komprimaci.
- `-f` nebo `--force`: Přepíše existující soubory bez dotazu.

## Běžné příklady
1. Komprimace souboru:
   ```bash
   gzip soubor.txt
   ```

2. Rozbalení komprimovaného souboru:
   ```bash
   gzip -d soubor.txt.gz
   ```

3. Komprimace souboru a zachování původního souboru:
   ```bash
   gzip -k soubor.txt
   ```

4. Zobrazení podrobností o komprimaci:
   ```bash
   gzip -v soubor.txt
   ```

5. Přepsání existujícího komprimovaného souboru:
   ```bash
   gzip -f soubor.txt
   ```

## Tipy
- Při komprimaci více souborů najednou můžete použít zástupné znaky, například `gzip *.txt`.
- Pokud potřebujete komprimovat adresář, zvažte použití `tar` v kombinaci s `gzip`, například `tar -czf archiv.tar.gz adresář/`.
- Vždy se ujistěte, že máte zálohu důležitých souborů před jejich komprimací, zejména pokud používáte možnost `-f`.