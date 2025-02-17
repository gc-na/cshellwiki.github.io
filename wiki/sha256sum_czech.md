# [Linux] Bash sha256sum použití: Vypočítání SHA-256 kontrolního součtu

## Přehled
Příkaz `sha256sum` slouží k výpočtu a ověření SHA-256 kontrolního součtu pro soubory. Tento kontrolní součet se často používá k ověření integrity dat, což znamená, že můžete zjistit, zda byl soubor po jeho vytvoření změněn.

## Použití
Základní syntaxe příkazu je následující:

```bash
sha256sum [možnosti] [argumenty]
```

## Běžné možnosti
- `-b`: Zpracovává binární soubory.
- `-c`: Ověřuje kontrolní součty z uvedeného souboru.
- `--quiet`: Potlačuje výstup, pokud je ověření úspěšné.
- `--tag`: Přidává značku k výstupu.

## Běžné příklady
1. **Vypočítání kontrolního součtu pro soubor:**
   ```bash
   sha256sum soubor.txt
   ```

2. **Uložení kontrolního součtu do souboru:**
   ```bash
   sha256sum soubor.txt > soubor.sha256
   ```

3. **Ověření kontrolního součtu z uloženého souboru:**
   ```bash
   sha256sum -c soubor.sha256
   ```

4. **Vypočítání kontrolního součtu pro více souborů:**
   ```bash
   sha256sum soubor1.txt soubor2.txt
   ```

## Tipy
- Při ověřování kontrolních součtů vždy používejte volbu `-c`, abyste zajistili, že soubory odpovídají původním kontrolním součtům.
- Ukládejte kontrolní součty do samostatného souboru, abyste je mohli snadno zkontrolovat později.
- Používejte volbu `--quiet`, pokud chcete minimalizovat výstup a soustředit se pouze na chyby.