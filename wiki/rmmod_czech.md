# [Linux] Bash rmmod: Odstranění modulů jádra

## Přehled
Příkaz `rmmod` slouží k odstranění modulů jádra v operačním systému Linux. Moduly jádra jsou součásti, které rozšiřují funkčnost jádra a umožňují přidávat nové ovladače a funkce bez nutnosti restartování systému.

## Použití
Základní syntaxe příkazu je následující:

```
rmmod [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`: Vynutí odstranění modulu, i když je používán.
- `--verbose`: Zobrazí podrobnosti o procesu odstraňování.
- `--quiet`: Potlačí výstup, pokud je odstranění úspěšné.

## Běžné příklady
1. **Odstranění modulu bez dalších možností:**
   ```bash
   rmmod modul_jadra
   ```

2. **Vynucení odstranění modulu:**
   ```bash
   rmmod -f modul_jadra
   ```

3. **Zobrazení podrobností o procesu:**
   ```bash
   rmmod --verbose modul_jadra
   ```

4. **Odstranění více modulů najednou:**
   ```bash
   rmmod modul1 modul2 modul3
   ```

## Tipy
- Před odstraněním modulu se ujistěte, že není používán jinými procesy, aby se předešlo chybám.
- Používejte volbu `--verbose`, pokud potřebujete sledovat, co se děje během odstraňování modulu.
- Vždy je dobré mít zálohu důležitých dat před prováděním změn v jádře systému.