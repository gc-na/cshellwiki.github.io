# [Linux] Bash ping použití: Ověření dostupnosti síťových zařízení

## Přehled
Příkaz `ping` se používá k testování dostupnosti síťových zařízení a měření doby odezvy mezi vaším počítačem a cílovým serverem. Odesílá ICMP echo požadavky a čeká na odpovědi, což umožňuje diagnostikovat problémy v síti.

## Použití
Základní syntaxe příkazu `ping` je následující:

```
ping [možnosti] [cílová_adresa]
```

## Běžné možnosti
- `-c [počet]`: Odeslat pouze zadaný počet echo požadavků.
- `-i [interval]`: Nastavit interval mezi odesíláním požadavků v sekundách.
- `-t [TTL]`: Nastavit hodnotu Time To Live pro pakety.
- `-s [velikost]`: Nastavit velikost odesílaného paketu.

## Běžné příklady
- Odeslání nekonečného počtu echo požadavků na server `example.com`:
  ```bash
  ping example.com
  ```

- Odeslání 5 echo požadavků:
  ```bash
  ping -c 5 example.com
  ```

- Odeslání echo požadavků s intervalem 2 sekundy:
  ```bash
  ping -i 2 example.com
  ```

- Odeslání echo požadavků s velikostí paketu 128 bajtů:
  ```bash
  ping -s 128 example.com
  ```

## Tipy
- Používejte `ping` k rychlé diagnostice problémů s připojením k internetu nebo k síťovým zařízením.
- Pokud máte podezření na ztrátu paketů, sledujte statistiky zobrazené po ukončení příkazu.
- Pro podrobnější analýzu můžete použít příkaz `traceroute`, který ukáže cestu paketů k cílové adrese.