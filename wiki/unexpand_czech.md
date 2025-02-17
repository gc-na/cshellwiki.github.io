# [Linux] Bash unexpand použití: Převod tabulátorů na mezery

## Přehled
Příkaz `unexpand` se používá k převodu tabulátorů na mezery v textových souborech. Tento příkaz je užitečný, když potřebujete zajistit, aby text byl formátován konzistentně, zejména při práci s programy, které preferují mezery místo tabulátorů.

## Použití
Základní syntaxe příkazu `unexpand` je následující:

```bash
unexpand [možnosti] [argumenty]
```

## Běžné možnosti
- `-t, --tabs=N` : Určuje šířku tabulátorů v počtu mezer. Výchozí hodnota je 8.
- `-a, --all` : Převádí všechny tabulátory na mezery, nejen ty, které jsou na začátku řádků.
- `-h, --help` : Zobrazí nápovědu k příkazu.

## Běžné příklady
Pár praktických příkladů použití příkazu `unexpand`:

1. Převod tabulátorů na mezery v souboru `soubor.txt` s výchozí šířkou tabulátorů:
   ```bash
   unexpand soubor.txt
   ```

2. Uložení výsledku do nového souboru `novy_soubor.txt`:
   ```bash
   unexpand soubor.txt > novy_soubor.txt
   ```

3. Převod tabulátorů na mezery s vlastní šířkou tabulátorů (např. 4 mezery):
   ```bash
   unexpand -t 4 soubor.txt
   ```

4. Převod všech tabulátorů v souboru, včetně těch na začátku řádků:
   ```bash
   unexpand -a soubor.txt
   ```

## Tipy
- Před použitím `unexpand` si vždy udělejte zálohu původního souboru, abyste předešli ztrátě dat.
- Pokud pracujete s kódem, zkontrolujte, zda je formátování konzistentní, aby nedošlo k chybám při kompilaci nebo spuštění.
- Používejte `unexpand` v kombinaci s dalšími příkazy, jako je `grep` nebo `sed`, pro efektivnější zpracování textu.