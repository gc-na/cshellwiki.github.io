# [Linux] Bash psql použití: Interakce s PostgreSQL databází

## Přehled
Příkaz `psql` je interaktivní terminálový nástroj pro práci s databázemi PostgreSQL. Umožňuje uživatelům spouštět SQL dotazy, spravovat databáze a provádět administrativní úkoly.

## Použití
Základní syntaxe příkazu `psql` je následující:

```bash
psql [možnosti] [argumenty]
```

## Běžné možnosti
- `-h` : Určuje hostitele databázového serveru.
- `-U` : Určuje uživatelské jméno pro přihlášení.
- `-d` : Určuje název databáze, ke které se chcete připojit.
- `-p` : Určuje port, na kterém databázový server naslouchá.
- `-c` : Spustí zadaný SQL příkaz a poté ukončí.

## Běžné příklady
1. Připojení k databázi:
   ```bash
   psql -h localhost -U uživatel -d databáze
   ```

2. Spuštění SQL příkazu přímo z příkazového řádku:
   ```bash
   psql -U uživatel -d databáze -c "SELECT * FROM tabulka;"
   ```

3. Import dat ze souboru:
   ```bash
   psql -U uživatel -d databáze -f cesta/k/souboru.sql
   ```

4. Export dat do souboru:
   ```bash
   psql -U uživatel -d databáze -c "COPY tabulka TO 'cesta/k/souboru.csv' DELIMITER ',' CSV HEADER;"
   ```

## Tipy
- Při práci s `psql` je užitečné používat interaktivní režim pro snadnější zadávání a testování SQL dotazů.
- Uložte si často používané příkazy do skriptů, abyste je mohli snadno znovu použít.
- Využívejte možnost `\?` v interaktivním režimu pro zobrazení dostupných příkazů a možností.