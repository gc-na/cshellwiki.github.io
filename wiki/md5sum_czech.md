# [Linux] Bash md5sum použití: Výpočet MD5 kontrolních součtů

## Přehled
Příkaz `md5sum` slouží k výpočtu a kontrole MD5 kontrolních součtů souborů. Tento příkaz je užitečný pro ověření integrity dat a zajištění, že soubory nebyly poškozeny nebo změněny.

## Použití
Základní syntaxe příkazu je následující:

```bash
md5sum [možnosti] [argumenty]
```

## Běžné možnosti
- `-b`: Zpracovává binární soubory.
- `-c`: Kontroluje MD5 kontrolní součty z uvedeného souboru.
- `-t`: Zpracovává textové soubory.
- `--quiet`: Potlačuje výstup, pokud je kontrolní součet správný.

## Běžné příklady
1. Výpočet MD5 kontrolního součtu pro soubor:
   ```bash
   md5sum soubor.txt
   ```

2. Uložení kontrolního součtu do souboru:
   ```bash
   md5sum soubor.txt > kontrolni_soucet.md5
   ```

3. Kontrola MD5 kontrolního součtu ze souboru:
   ```bash
   md5sum -c kontrolni_soucet.md5
   ```

4. Výpočet kontrolního součtu pro více souborů:
   ```bash
   md5sum soubor1.txt soubor2.txt
   ```

## Tipy
- Při práci s velkými soubory je dobré použít možnost `-b`, aby se zajistilo, že soubor bude správně zpracován jako binární.
- Uložení kontrolního součtu do souboru je užitečné pro pozdější ověření integrity souboru.
- Při kontrole souborů vždy zkontrolujte, zda je soubor s kontrolním součtem aktuální a odpovídá souboru, který chcete ověřit.