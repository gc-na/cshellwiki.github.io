# [Linux] Bash dmesg použití: Zobrazí zprávy jádra

## Přehled
Příkaz `dmesg` slouží k zobrazení zpráv jádra operačního systému. Tyto zprávy obsahují informace o hardwarových událostech, ovladačích a dalších systémových aktivitách, které se odehrály od posledního spuštění systému. Je užitečný pro diagnostiku problémů a sledování stavu systému.

## Použití
Základní syntaxe příkazu `dmesg` je následující:

```bash
dmesg [možnosti] [argumenty]
```

## Běžné možnosti
- `-C`: Vymaže aktuální vyrovnávací paměť zpráv jádra.
- `-c`: Zobrazí zprávy a poté je vymaže.
- `-n LEVEL`: Nastaví úroveň závažnosti zpráv, které se mají zobrazit.
- `-T`: Zobrazí časové značky ve čitelné podobě.
- `--follow`: Nepřetržitě sleduje nové zprávy jádra.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `dmesg`:

1. **Zobrazení všech zpráv jádra:**
   ```bash
   dmesg
   ```

2. **Zobrazení zpráv s časovými značkami:**
   ```bash
   dmesg -T
   ```

3. **Vymazání zpráv jádra po jejich zobrazení:**
   ```bash
   dmesg -c
   ```

4. **Sledování nových zpráv jádra v reálném čase:**
   ```bash
   dmesg --follow
   ```

5. **Zobrazení zpráv s určitou úrovní závažnosti:**
   ```bash
   dmesg -n 1
   ```

## Tipy
- Používejte `dmesg -T` pro snadnější čtení časových značek, zejména při analýze událostí.
- Pravidelně kontrolujte zprávy jádra po připojení nového hardwaru nebo instalaci ovladačů.
- Můžete kombinovat `dmesg` s dalšími příkazy, jako je `grep`, pro filtrování specifických zpráv. Například:
  ```bash
  dmesg | grep error
  ```