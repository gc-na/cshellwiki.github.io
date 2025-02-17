# [Linux] Bash killall použití: Ukončení procesů podle názvu

## Přehled
Příkaz `killall` slouží k ukončení všech procesů, které mají specifikovaný název. Tento příkaz je užitečný, když chcete rychle zastavit více instancí programu bez nutnosti hledat jejich identifikátory procesů (PID).

## Použití
Základní syntaxe příkazu `killall` je následující:

```bash
killall [možnosti] [argumenty]
```

## Běžné možnosti
- `-u, --user <uživatel>`: Ukončí pouze procesy patřící zadanému uživateli.
- `-q, --quiet`: Potlačí výstup příkazu, pokud nejsou nalezeny žádné procesy.
- `-I, --ignore-case`: Ignoruje velikost písmen při porovnávání názvů procesů.
- `-s, --signal <signál>`: Určuje signál, který má být odeslán procesům (výchozí je SIGTERM).

## Běžné příklady
1. Ukončení všech procesů s názvem `firefox`:
   ```bash
   killall firefox
   ```

2. Ukončení všech procesů s názvem `python`, přičemž se ignoruje velikost písmen:
   ```bash
   killall -I python
   ```

3. Ukončení procesů patřících uživateli `john`:
   ```bash
   killall -u john
   ```

4. Odeslání signálu SIGKILL procesům s názvem `myapp`:
   ```bash
   killall -s SIGKILL myapp
   ```

## Tipy
- Používejte `killall` s opatrností, protože může ukončit více procesů najednou, což může vést k ztrátě neuložené práce.
- Před použitím příkazu je dobré zkontrolovat běžící procesy pomocí `ps` nebo `pgrep`, abyste se ujistili, že ukončujete správné procesy.
- Pokud potřebujete ukončit pouze konkrétní instanci procesu, zvažte použití příkazu `kill` s PID.