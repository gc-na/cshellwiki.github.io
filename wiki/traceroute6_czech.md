# [Linux] Bash traceroute6 použití: Zjistit cestu IPv6 paketů

## Přehled
Příkaz `traceroute6` slouží k sledování cesty, kterou IPv6 pakety procházejí z vašeho počítače na cílovou adresu. Pomocí tohoto příkazu můžete zjistit, jaké servery a směrovače jsou mezi vámi a cílovým místem, což je užitečné pro diagnostiku síťových problémů.

## Použití
Základní syntaxe příkazu `traceroute6` je následující:

```bash
traceroute6 [možnosti] [argumenty]
```

## Běžné možnosti
- `-m <max_hops>`: Nastaví maximální počet skoků, které se mají sledovat.
- `-p <port>`: Určuje port, který se má použít pro odesílání paketů.
- `-w <timeout>`: Nastavuje časový limit pro čekání na odpověď od každého skoku.
- `-q <n>`: Určuje počet dotazů, které se mají poslat na každý skok.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `traceroute6`:

1. Základní použití pro sledování cesty k cílové adrese:
   ```bash
   traceroute6 google.com
   ```

2. Sledování cesty s maximálním počtem skoků nastaveným na 15:
   ```bash
   traceroute6 -m 15 google.com
   ```

3. Použití specifického portu pro sledování cesty:
   ```bash
   traceroute6 -p 80 google.com
   ```

4. Nastavení časového limitu na 2 sekundy:
   ```bash
   traceroute6 -w 2 google.com
   ```

5. Odeslání tří dotazů na každý skok:
   ```bash
   traceroute6 -q 3 google.com
   ```

## Tipy
- Ujistěte se, že máte oprávnění k odesílání paketů, protože některé systémy mohou vyžadovat administrátorská práva.
- Používejte `traceroute6` v kombinaci s dalšími diagnostickými nástroji, jako je `ping`, pro komplexnější analýzu síťových problémů.
- Pokud narazíte na problémy s časováním, zkuste experimentovat s různými hodnotami pro `-w` a `-m`, abyste získali lepší výsledky.