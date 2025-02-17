# [Linux] Bash nslookup použití: Získání informací o DNS

## Overview
Příkaz `nslookup` slouží k dotazování na DNS (Domain Name System) a umožňuje uživatelům získávat informace o doménách, jako jsou IP adresy a další související záznamy. Tento nástroj je užitečný pro diagnostiku a správu síťových problémů.

## Usage
Základní syntaxe příkazu `nslookup` je následující:

```bash
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE` - Určuje typ DNS záznamu, který chcete vyhledat (např. A, AAAA, MX).
- `-timeout=SECONDS` - Nastavuje časový limit pro dotaz na DNS.
- `-retry=NUMBER` - Určuje počet pokusů o opakování dotazu.
- `-debug` - Zobrazí podrobné informace o dotazu a odpovědi.

## Common Examples
1. Získání IP adresy pro doménu:
   ```bash
   nslookup example.com
   ```

2. Vyhledání specifického typu DNS záznamu (např. MX):
   ```bash
   nslookup -type=MX example.com
   ```

3. Dotaz na konkrétní DNS server:
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. Získání podrobných informací o dotazu:
   ```bash
   nslookup -debug example.com
   ```

## Tips
- Používejte `nslookup` pro rychlé ověření, zda je doména aktivní a jaké IP adresy jí odpovídají.
- Pokud máte problémy s připojením k webu, zkuste zjistit, zda je problém na straně DNS pomocí `nslookup`.
- Mějte na paměti, že `nslookup` je zastaralý a pro pokročilejší funkce můžete zvážit použití příkazu `dig`.