# [Linux] Bash dig použití: Získání informací o DNS

## Přehled
Příkaz `dig` (Domain Information Groper) slouží k dotazování na DNS (Domain Name System) a poskytuje uživatelům detailní informace o doménách a jejich záznamech. Je to mocný nástroj pro správu a diagnostiku DNS.

## Použití
Základní syntaxe příkazu `dig` je následující:

```bash
dig [možnosti] [argumenty]
```

## Běžné možnosti
- `@server` - Určuje DNS server, který má být dotazován.
- `-t type` - Určuje typ DNS záznamu (např. A, MX, TXT).
- `+short` - Zobrazí zjednodušený výstup.
- `+trace` - Sleduje cestu dotazu přes DNS servery.

## Běžné příklady
1. Základní dotaz na A záznam domény:
   ```bash
   dig example.com
   ```

2. Dotaz na specifický typ záznamu (např. MX):
   ```bash
   dig -t MX example.com
   ```

3. Dotaz na konkrétní DNS server:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. Zjednodušený výstup:
   ```bash
   dig +short example.com
   ```

5. Sledování cesty dotazu:
   ```bash
   dig +trace example.com
   ```

## Tipy
- Používejte `+short` pro rychlé a přehledné výsledky, pokud nepotřebujete detailní informace.
- Pokud se potýkáte s problémy s DNS, `+trace` vám může pomoci zjistit, kde se dotaz ztrácí.
- Zvažte použití různých DNS serverů (např. Google DNS 8.8.8.8) pro porovnání výsledků.