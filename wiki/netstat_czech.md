# [Linux] Bash netstat použití: Zobrazení síťových připojení

## Přehled
Příkaz `netstat` slouží k zobrazení síťových připojení, směrovacích tabulek a statistiky síťových rozhraní. Umožňuje uživatelům sledovat aktivní síťová spojení a diagnostikovat problémy se sítí.

## Použití
Základní syntaxe příkazu `netstat` je následující:

```
netstat [možnosti] [argumenty]
```

## Běžné možnosti
- `-a` : Zobrazí všechna připojení a naslouchající porty.
- `-t` : Zobrazí pouze TCP připojení.
- `-u` : Zobrazí pouze UDP připojení.
- `-n` : Zobrazí adresy a porty v číselném formátu, místo aby je převáděl na názvy.
- `-l` : Zobrazí pouze naslouchající sockety.
- `-p` : Zobrazí procesy, které používají daná připojení.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `netstat`:

1. Zobrazení všech aktivních připojení:
   ```bash
   netstat -a
   ```

2. Zobrazení pouze TCP připojení:
   ```bash
   netstat -t
   ```

3. Zobrazení naslouchajících portů:
   ```bash
   netstat -l
   ```

4. Zobrazení připojení s číselnými adresami:
   ```bash
   netstat -n
   ```

5. Zobrazení připojení s informacemi o procesech:
   ```bash
   netstat -p
   ```

## Tipy
- Používejte kombinaci možností pro podrobnější výstup, například `netstat -tuln` pro zobrazení všech naslouchajících TCP a UDP portů v číselném formátu.
- Pravidelně kontrolujte aktivní připojení pro detekci podezřelých aktivit.
- Příkaz `netstat` může být užitečný při ladění síťových problémů, proto se nebojte experimentovat s různými možnostmi.