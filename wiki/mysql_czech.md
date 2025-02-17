# [Linux] Bash mysql použití: Správa databází MySQL

## Přehled
Příkaz `mysql` slouží k interakci s databázemi MySQL. Umožňuje uživatelům provádět dotazy, spravovat databáze a manipulovat s daty přímo z příkazového řádku.

## Použití
Základní syntaxe příkazu `mysql` je následující:

```bash
mysql [možnosti] [argumenty]
```

## Běžné možnosti
- `-u` : Určuje uživatelské jméno pro připojení k databázi.
- `-p` : Vyžaduje heslo pro uživatelské jméno. Heslo bude vyžadováno po spuštění příkazu.
- `-h` : Určuje hostname nebo IP adresu serveru MySQL.
- `-D` : Určuje jméno databáze, se kterou se má pracovat.
- `--execute` : Umožňuje provést SQL dotaz přímo z příkazového řádku.

## Běžné příklady
1. Připojení k MySQL serveru s uživatelským jménem a heslem:

```bash
mysql -u uživatel -p
```

2. Připojení k MySQL serveru na specifickém hostiteli:

```bash
mysql -h 192.168.1.1 -u uživatel -p
```

3. Spuštění SQL dotazu přímo z příkazového řádku:

```bash
mysql -u uživatel -p -D databaze --execute "SELECT * FROM tabulka;"
```

4. Zobrazení seznamu dostupných databází:

```bash
mysql -u uživatel -p -e "SHOW DATABASES;"
```

## Tipy
- Vždy používejte silná hesla pro uživatelské účty v MySQL.
- Pokud často používáte stejný příkaz, zvažte vytvoření skriptu pro automatizaci.
- Pro bezpečnostní účely se vyhněte zadávání hesla přímo v příkazovém řádku; použijte možnost `-p` bez hesla pro vyžádání hesla po spuštění.
- Udržujte pravidelnou zálohu databází, abyste předešli ztrátě dat.