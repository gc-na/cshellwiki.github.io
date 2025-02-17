# [Linux] Bash uniq použití: Odstranění duplicitních řádků

## Přehled
Příkaz `uniq` slouží k odstranění duplicitních řádků ze souboru nebo výstupu jiného příkazu. Tento nástroj je často používán v kombinaci s příkazem `sort`, aby se zajistilo, že duplicitní řádky jsou vedle sebe a mohou být efektivně odstraněny.

## Použití
Základní syntaxe příkazu `uniq` je následující:

```
uniq [možnosti] [argumenty]
```

## Běžné možnosti
- `-c`: Zobrazí počet výskytů každého unikátního řádku.
- `-d`: Zobrazí pouze řádky, které se opakují.
- `-u`: Zobrazí pouze unikátní řádky, které se neopakují.
- `-i`: Ignoruje rozdíly mezi velkými a malými písmeny.

## Běžné příklady
1. Odstranění duplicitních řádků ze souboru:
   ```bash
   uniq soubor.txt
   ```

2. Zobrazení počtu výskytů každého řádku:
   ```bash
   uniq -c soubor.txt
   ```

3. Zobrazení pouze duplicitních řádků:
   ```bash
   uniq -d soubor.txt
   ```

4. Zobrazení pouze unikátních řádků:
   ```bash
   uniq -u soubor.txt
   ```

5. Použití s příkazem `sort` pro odstranění duplicitních řádků:
   ```bash
   sort soubor.txt | uniq
   ```

## Tipy
- Před použitím `uniq` je dobré data seřadit pomocí `sort`, aby se zajistilo, že duplicitní řádky jsou vedle sebe.
- Používejte volbu `-i`, pokud chcete ignorovat rozdíly mezi velkými a malými písmeny, což může být užitečné při práci s textem.
- Při práci s velkými soubory může být užitečné použít `uniq` v kombinaci s dalšími příkazy pro efektivní zpracování dat.