# [Linux] Bash timedatectl použití: Správa času a data v systému

## Přehled
Příkaz `timedatectl` slouží k správě a zobrazení informací o čase a datu v systému. Umožňuje uživatelům konfigurovat časové zóny, synchronizaci času a další související nastavení.

## Použití
Základní syntaxe příkazu je následující:

```bash
timedatectl [možnosti] [argumenty]
```

## Běžné možnosti
- `status` - Zobrazí aktuální stav času a data.
- `set-time` - Nastaví čas a datum.
- `set-timezone` - Změní časovou zónu.
- `set-ntp` - Povolení nebo zakázání synchronizace času s NTP serverem.
- `list-timezones` - Zobrazí seznam dostupných časových zón.

## Běžné příklady
- Zobrazení aktuálního stavu času a data:

```bash
timedatectl status
```

- Nastavení konkrétního času a data:

```bash
timedatectl set-time '2023-10-01 12:00:00'
```

- Změna časové zóny na "Europe/Prague":

```bash
timedatectl set-timezone Europe/Prague
```

- Povolení synchronizace času s NTP serverem:

```bash
timedatectl set-ntp true
```

- Zobrazení seznamu dostupných časových zón:

```bash
timedatectl list-timezones
```

## Tipy
- Při nastavování času a data se ujistěte, že používáte správný formát.
- Pravidelně kontrolujte stav synchronizace času, zejména na serverech.
- Při změně časové zóny je dobré restartovat aplikace, které závisí na čase, aby se projevily změny.