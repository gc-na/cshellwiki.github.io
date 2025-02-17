# [Linux] Bash socat použití: Přesměrování a manipulace s datovými toky

## Přehled
`socat` (Socket CAT) je mocný nástroj pro přesměrování a manipulaci s datovými toky mezi různými zdroji. Umožňuje spojení mezi sockety, soubory, terminály a dalšími datovými proudy, což z něj činí užitečný nástroj pro síťovou komunikaci a testování.

## Použití
Základní syntaxe příkazu `socat` je následující:

```bash
socat [možnosti] [argumenty]
```

## Běžné možnosti
- `-v`: Zobrazí podrobnosti o přenosech dat.
- `-u`: Používá neblokující režim.
- `TCP:<host>:<port>`: Vytvoří TCP spojení na zadanou adresu a port.
- `UDP:<host>:<port>`: Vytvoří UDP spojení na zadanou adresu a port.
- `FILE:<cesta>`: Otevře soubor pro čtení nebo zápis.

## Běžné příklady
1. **Základní TCP spojení**:
   ```bash
   socat TCP:localhost:1234 -
   ```
   Tento příkaz vytvoří TCP spojení na localhost na portu 1234 a přesměruje standardní vstup a výstup.

2. **Přesměrování portu**:
   ```bash
   socat TCP-LISTEN:1234,fork EXEC:/bin/cat
   ```
   Tento příkaz naslouchá na portu 1234 a pro každý příchozí spojení spustí příkaz `cat`.

3. **Připojení k UDP serveru**:
   ```bash
   socat -u UDP:localhost:1234 -
   ```
   Tento příkaz odešle data na UDP server běžící na localhost na portu 1234.

4. **Přesměrování souboru do TCP spojení**:
   ```bash
   socat TCP:localhost:1234 FILE:/path/to/file
   ```
   Tento příkaz odešle obsah souboru na TCP server na localhost na portu 1234.

## Tipy
- Při práci s `socat` je dobré používat volbu `-v` pro sledování přenosu dat, což může pomoci při ladění.
- Ujistěte se, že porty, které používáte, nejsou blokovány firewallem nebo jinými bezpečnostními opatřeními.
- Experimentujte s různými typy socketů a datových proudů, abyste plně využili možnosti `socat`.