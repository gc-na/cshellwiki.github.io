# [Linux] Bash tar použití: Komprimace a archivace souborů

## Přehled
Příkaz `tar` slouží k archivaci a komprimaci souborů a adresářů v systému Linux. Umožňuje vytvářet soubory s příponou `.tar`, které mohou obsahovat více souborů a adresářů, a také je možné je komprimovat pro úsporu místa.

## Použití
Základní syntaxe příkazu `tar` je následující:

```bash
tar [možnosti] [argumenty]
```

## Běžné možnosti
- `-c`: Vytvoření nového archivu.
- `-x`: Rozbalení archivu.
- `-f`: Určení názvu archivu.
- `-v`: Zobrazit podrobnosti o procesu (verbose).
- `-z`: Komprimace pomocí gzip.
- `-j`: Komprimace pomocí bzip2.

## Běžné příklady
1. **Vytvoření archivu:**
   Vytvoření archivu `moje_soubory.tar` z adresáře `soubory`.
   ```bash
   tar -cvf moje_soubory.tar soubory/
   ```

2. **Rozbalení archivu:**
   Rozbalení archivu `moje_soubory.tar`.
   ```bash
   tar -xvf moje_soubory.tar
   ```

3. **Vytvoření komprimovaného archivu:**
   Vytvoření komprimovaného archivu `moje_soubory.tar.gz`.
   ```bash
   tar -czvf moje_soubory.tar.gz soubory/
   ```

4. **Rozbalení komprimovaného archivu:**
   Rozbalení archivu `moje_soubory.tar.gz`.
   ```bash
   tar -xzvf moje_soubory.tar.gz
   ```

## Tipy
- Při vytváření archivu použijte volbu `-v`, abyste viděli, které soubory jsou přidávány.
- Pro úsporu místa zvažte použití komprese (`-z` nebo `-j`) při vytváření archivu.
- Před rozbalením archivu si ověřte jeho obsah pomocí `tar -tvf archiv.tar`, abyste zjistili, co obsahuje.