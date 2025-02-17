# [Linux] Bash write příkaz: Odesílání zpráv uživatelům

## Přehled
Příkaz `write` slouží k odesílání zpráv přímo jiným uživatelům přihlášeným na stejném systému. Umožňuje komunikaci v reálném čase mezi uživateli, což může být užitečné pro rychlé sdílení informací nebo upozornění.

## Použití
Základní syntaxe příkazu je následující:

```
write [uživatel] [terminál]
```

## Běžné možnosti
- `-n`: Nepoužívat hlavičku při odesílání zprávy.
- `-h`: Zobrazit nápovědu k příkazu.

## Běžné příklady
1. Odeslání zprávy uživateli `jan` na jeho terminál:
   ```bash
   write jan
   Ahoj Jan, jak se máš?
   ```

2. Odeslání zprávy uživateli `petr` na terminál `pts/1`:
   ```bash
   write petr pts/1
   Měj se hezky, Petře!
   ```

3. Odeslání zprávy bez hlavičky:
   ```bash
   write -n jan
   Tohle je zpráva bez hlavičky.
   ```

## Tipy
- Ujistěte se, že uživatel, kterému chcete zprávu poslat, je přihlášen a má otevřený terminál.
- Pokud je terminál uživatele obsazen, zpráva se zobrazí až poté, co uživatel uvolní terminál.
- Používejte `Ctrl + D` pro ukončení zprávy a odeslání.