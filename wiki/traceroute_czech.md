# [Linux] Bash traceroute použití: Zjistit cestu paketů v síti

## Přehled
Příkaz `traceroute` slouží k diagnostice sítě tím, že zobrazuje cestu, kterou pakety procházejí z vašeho počítače na cílovou adresu. Ukazuje jednotlivé skoky (hops) mezi routery a poskytuje informace o latenci každého skoku.

## Použití
Základní syntaxe příkazu `traceroute` je následující:

```bash
traceroute [možnosti] [cílová_adresa]
```

## Běžné možnosti
- `-m <max_hops>`: Nastaví maximální počet skoků, které traceroute provede.
- `-w <timeout>`: Určuje časový limit pro čekání na odpověď od každého skoku.
- `-n`: Zobrazí IP adresy místo DNS názvů.
- `-p <port>`: Specifikuje port, který se má použít pro UDP pakety (výchozí je 33434).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `traceroute`:

1. Základní použití pro sledování cesty k webové stránce:
   ```bash
   traceroute www.example.com
   ```

2. Zobrazení cesty k IP adrese s maximálním počtem skoků 15:
   ```bash
   traceroute -m 15 192.168.1.1
   ```

3. Použití bez DNS názvů:
   ```bash
   traceroute -n www.example.com
   ```

4. Nastavení časového limitu na 2 sekundy:
   ```bash
   traceroute -w 2 www.example.com
   ```

5. Sledování cesty pomocí specifického portu:
   ```bash
   traceroute -p 80 www.example.com
   ```

## Tipy
- Používejte možnost `-n`, pokud chcete rychlejší výsledky, protože se neprovádí DNS dotazy.
- Pokud máte problémy s připojením, zkuste zvýšit časový limit pomocí `-w`.
- Pro analýzu latence mezi jednotlivými skoky sledujte časy zobrazené vedle každého skoku.