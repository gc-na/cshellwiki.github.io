# [Linux] Bash bzip2 použití: Komprimace a dekomprimace souborů

## Přehled
Bzip2 je nástroj pro kompresi souborů, který využívá algoritmus Burrows-Wheeler a je známý svou vysokou kompresní účinností. Tento příkaz se často používá k zmenšení velikosti souborů, což usnadňuje jejich ukládání a přenos.

## Použití
Základní syntaxe příkazu bzip2 je následující:
```bash
bzip2 [možnosti] [argumenty]
```

## Běžné možnosti
- `-d`, `--decompress`: Dekompresuje soubor.
- `-k`, `--keep`: Zachová původní soubor po kompresi.
- `-f`, `--force`: Přepíše existující soubory bez dotazu.
- `-z`, `--compress`: Komprimuje soubor (toto je výchozí chování).
- `-v`, `--verbose`: Zobrazí podrobnosti o procesu komprese.

## Běžné příklady
1. **Kompresní soubor**:
   ```bash
   bzip2 soubor.txt
   ```
   Tento příkaz vytvoří komprimovaný soubor `soubor.txt.bz2`.

2. **Dekompresní soubor**:
   ```bash
   bzip2 -d soubor.txt.bz2
   ```
   Tento příkaz obnoví původní soubor `soubor.txt`.

3. **Kompresní soubor a zachování původního**:
   ```bash
   bzip2 -k soubor.txt
   ```
   Původní soubor `soubor.txt` zůstane zachován a vytvoří se komprimovaný soubor `soubor.txt.bz2`.

4. **Kompresní více souborů**:
   ```bash
   bzip2 soubor1.txt soubor2.txt
   ```
   Tento příkaz komprimuje oba soubory a vytvoří `soubor1.txt.bz2` a `soubor2.txt.bz2`.

## Tipy
- Při kompresi velkých souborů můžete použít možnost `-v`, abyste sledovali průběh komprese.
- Pokud často pracujete s bzip2, zvažte použití skriptů pro automatizaci běžných úloh.
- Pamatujte, že bzip2 je efektivní, ale může být pomalejší než jiné kompresní nástroje, jako je gzip, takže zvažte vaše potřeby při výběru nástroje.