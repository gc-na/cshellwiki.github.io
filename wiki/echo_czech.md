# [Linux] Bash echo použití: Zobrazí text na obrazovce

## Přehled
Příkaz `echo` v Bash slouží k zobrazení textu nebo proměnných na standardním výstupu, což je obvykle terminál. Je to užitečný nástroj pro zobrazování zpráv, hodnot proměnných nebo pro testování skriptů.

## Použití
Základní syntaxe příkazu `echo` je následující:

```bash
echo [možnosti] [argumenty]
```

## Běžné možnosti
- `-n`: Nezobrazí nový řádek na konci výstupu.
- `-e`: Aktivuje interpretaci speciálních znaků (např. `\n` pro nový řádek).
- `-E`: Deaktivuje interpretaci speciálních znaků (toto je výchozí chování).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `echo`:

1. Základní zobrazení textu:
   ```bash
   echo "Ahoj, světe!"
   ```

2. Zobrazení proměnné:
   ```bash
   jmeno="Jan"
   echo "Moje jméno je $jmeno."
   ```

3. Zobrazení textu bez nového řádku:
   ```bash
   echo -n "Toto je text bez nového řádku."
   ```

4. Použití speciálních znaků:
   ```bash
   echo -e "První řádek\nDruhý řádek"
   ```

5. Zobrazení cesty k aktuálnímu adresáři:
   ```bash
   echo "Aktuální adresář je $(pwd)"
   ```

## Tipy
- Používejte `-n`, pokud chcete, aby následující výstup byl na stejném řádku.
- Pokud potřebujete zobrazit speciální znaky, nezapomeňte použít možnost `-e`.
- Pro lepší čitelnost výstupu můžete použít úpravy, jako jsou mezery nebo nové řádky, pomocí speciálních znaků.