# [Linux] Bash sqlite3 použití: Práce s databázemi SQLite

## Přehled
Příkaz `sqlite3` slouží k interakci s databázemi SQLite. Umožňuje uživatelům vytvářet, upravovat a dotazovat se na databáze pomocí SQL příkazů. Je to mocný nástroj pro správu dat v jednoduchých a přenosných databázích.

## Použití
Základní syntaxe příkazu `sqlite3` je následující:

```bash
sqlite3 [možnosti] [argumenty]
```

## Běžné možnosti
- `-help`: Zobrazí nápovědu k příkazu.
- `-version`: Zobrazí verzi SQLite.
- `-init <soubor>`: Spustí SQL příkazy z uvedeného souboru při spuštění.
- `-batch`: Spustí SQLite v dávkovém režimu, což je užitečné pro skripty.
- `-readonly`: Otevře databázi pouze pro čtení.

## Běžné příklady
1. **Otevření databáze**:
   ```bash
   sqlite3 moje_databaze.db
   ```

2. **Vytvoření nové tabulky**:
   ```bash
   sqlite3 moje_databaze.db "CREATE TABLE uzivatele (id INTEGER PRIMARY KEY, jmeno TEXT, vek INTEGER);"
   ```

3. **Vložení dat do tabulky**:
   ```bash
   sqlite3 moje_databaze.db "INSERT INTO uzivatele (jmeno, vek) VALUES ('Jan', 30);"
   ```

4. **Dotaz na data**:
   ```bash
   sqlite3 moje_databaze.db "SELECT * FROM uzivatele;"
   ```

5. **Export dat do souboru**:
   ```bash
   sqlite3 moje_databaze.db ".output export.txt" ".dump" ".output stdout"
   ```

## Tipy
- Používejte `-init` pro automatické spuštění SQL skriptů při otevírání databáze.
- Vždy zálohujte databázi před prováděním destruktivních operací.
- Pro efektivní práci s většími databázemi zvažte použití dávkového režimu s `-batch`.