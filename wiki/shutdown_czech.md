# [Linux] Bash shutdown použití: Ukončení systému

## Přehled
Příkaz `shutdown` slouží k bezpečnému vypnutí nebo restartování systému. Umožňuje uživatelům naplánovat vypnutí nebo restart v určitém čase nebo okamžitě.

## Použití
Základní syntaxe příkazu je následující:

```bash
shutdown [možnosti] [argumenty]
```

## Běžné možnosti
- `-h` : Vypne systém.
- `-r` : Restartuje systém.
- `-t [sekundy]` : Nastaví časový interval před vypnutím nebo restartem.
- `now` : Okamžité vypnutí nebo restart.
- `+[minuty]` : Naplánuje vypnutí nebo restart za zadaný počet minut.

## Běžné příklady
- Okamžité vypnutí systému:
  ```bash
  shutdown -h now
  ```

- Naplánování vypnutí za 10 minut:
  ```bash
  shutdown -h +10
  ```

- Restartování systému okamžitě:
  ```bash
  shutdown -r now
  ```

- Naplánování restartu za 5 minut:
  ```bash
  shutdown -r +5
  ```

- Vypnutí systému v konkrétním čase (např. 22:00):
  ```bash
  shutdown -h 22:00
  ```

## Tipy
- Před použitím příkazu `shutdown` se ujistěte, že máte uloženou veškerou práci, abyste předešli ztrátě dat.
- Používejte příkaz `shutdown -c` pro zrušení naplánovaného vypnutí nebo restartu.
- Můžete také informovat ostatní uživatele o plánovaném vypnutí pomocí zprávy: 
  ```bash
  shutdown -h +10 "Systém bude vypnut za 10 minut."
  ```