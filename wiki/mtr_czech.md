# [Linux] Bash mtr Použití: Nástroj pro diagnostiku sítě

## Přehled
Příkaz `mtr` (My Traceroute) kombinuje funkce příkazů `ping` a `traceroute`, což umožňuje uživatelům sledovat cestu paketů přes síť a měřit latenci na jednotlivých skocích. Je to užitečný nástroj pro diagnostiku síťových problémů.

## Použití
Základní syntaxe příkazu `mtr` je následující:

```
mtr [možnosti] [argumenty]
```

## Běžné možnosti
- `-r` : Spustí mtr v režimu reportu, který zobrazí výsledky pouze jednou a poté se ukončí.
- `-c <číslo>` : Určuje počet paketů, které mají být odeslány na každý skok.
- `-i <čas>` : Nastavuje interval mezi odesláním paketů (v sekundách).
- `-p` : Spustí mtr v režimu, který zobrazuje pouze skoky, které odpovídají.
- `-n` : Zobrazí IP adresy místo DNS jmen.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `mtr`:

1. Základní použití pro sledování cesty k cílové adrese:
   ```bash
   mtr example.com
   ```

2. Spuštění mtr v režimu reportu s 10 odeslanými pakety:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Sledování cesty s nastaveným intervalem 1 sekundy mezi pakety:
   ```bash
   mtr -i 1 example.com
   ```

4. Zobrazení pouze IP adres bez DNS jmen:
   ```bash
   mtr -n example.com
   ```

## Tipy
- Používejte `mtr` s administrátorskými právy (např. pomocí `sudo`), pokud potřebujete sledovat cesty na síťových rozhraních, které vyžadují vyšší oprávnění.
- Pro komplexnější analýzu můžete kombinovat různé možnosti, například `-r` s `-c`, abyste získali rychlý report s konkrétním počtem paketů.
- Pravidelně monitorujte síťové cesty, abyste identifikovali možné problémy s latencí nebo ztrátou paketů.