# [Linux] Bash wc použití: Počítání řádků, slov a znaků

## Přehled
Příkaz `wc` (word count) slouží k počítání řádků, slov a znaků v souborech nebo standardním vstupu. Je užitečný pro rychlou analýzu textových dat.

## Použití
Základní syntaxe příkazu je následující:

```bash
wc [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Počítá pouze řádky.
- `-w`: Počítá pouze slova.
- `-c`: Počítá pouze znaky.
- `-m`: Počítá pouze znaky (včetně multibyte znaků).
- `-L`: Zobrazí délku nejdelšího řádku.

## Běžné příklady
1. Počítání řádků, slov a znaků v souboru:
   ```bash
   wc soubor.txt
   ```

2. Počítání pouze řádků:
   ```bash
   wc -l soubor.txt
   ```

3. Počítání pouze slov:
   ```bash
   wc -w soubor.txt
   ```

4. Počítání pouze znaků:
   ```bash
   wc -c soubor.txt
   ```

5. Počítání délky nejdelšího řádku:
   ```bash
   wc -L soubor.txt
   ```

## Tipy
- Pokud chcete počítat více souborů najednou, můžete je uvést za sebou:
  ```bash
  wc soubor1.txt soubor2.txt
  ```
- Příkaz `wc` můžete kombinovat s dalšími příkazy pomocí roury (`|`). Například pro počítání řádků výstupu příkazu `grep`:
  ```bash
  grep "hledaný_text" soubor.txt | wc -l
  ```
- Pro analýzu velkých souborů je užitečné použít `-l` nebo `-w`, abyste se vyhnuli zbytečnému počítání znaků, což může být časově náročné.