# [Linux] Bash ping6 použití: Ověření dostupnosti IPv6 adres

## Přehled
Příkaz `ping6` slouží k testování dostupnosti IPv6 adres. Umožňuje uživatelům posílat ICMPv6 echo požadavky na cílovou adresu a měřit dobu odezvy, což je užitečné pro diagnostiku síťových problémů.

## Použití
Základní syntaxe příkazu je následující:

```bash
ping6 [možnosti] [argumenty]
```

## Běžné možnosti
- `-c [číslo]`: Určuje počet echo požadavků, které se mají odeslat.
- `-i [sekundy]`: Nastavuje interval mezi jednotlivými požadavky.
- `-w [sekundy]`: Určuje maximální dobu trvání testu.
- `-s [velikost]`: Nastavuje velikost datového paketu.

## Běžné příklady
1. Odeslání základního echo požadavku na IPv6 adresu:
   ```bash
   ping6 2001:db8::1
   ```

2. Odeslání 5 echo požadavků:
   ```bash
   ping6 -c 5 2001:db8::1
   ```

3. Odeslání požadavků s intervalem 2 sekundy:
   ```bash
   ping6 -i 2 2001:db8::1
   ```

4. Odeslání požadavků s nastavenou velikostí paketu na 128 bytů:
   ```bash
   ping6 -s 128 2001:db8::1
   ```

5. Odeslání požadavků po dobu 10 sekund:
   ```bash
   ping6 -w 10 2001:db8::1
   ```

## Tipy
- Používejte `-c` možnost pro omezení počtu požadavků, abyste nezatěžovali síť.
- Zkontrolujte, zda je cílová IPv6 adresa správná, abyste se vyhnuli chybám.
- Při diagnostice problémů se sítí sledujte průměrnou dobu odezvy a ztrátu paketů.