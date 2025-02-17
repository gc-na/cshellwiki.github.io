# [Linux] Bash date použití: Získání aktuálního data a času

## Přehled
Příkaz `date` v Bash se používá k zobrazení aktuálního data a času. Můžete jej také použít k formátování data a času podle svých potřeb.

## Použití
Základní syntaxe příkazu `date` je následující:

```bash
date [options] [arguments]
```

## Běžné možnosti
- `+FORMAT`: Umožňuje specifikovat formát výstupu. Například `%Y` pro rok, `%m` pro měsíc atd.
- `-u`: Zobrazí čas v UTC (Coordinated Universal Time).
- `-d STRING`: Zobrazí datum a čas podle zadaného řetězce. Například `-d "next Friday"`.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `date`:

1. Zobrazení aktuálního data a času:
   ```bash
   date
   ```

2. Zobrazení data ve formátu YYYY-MM-DD:
   ```bash
   date +%Y-%m-%d
   ```

3. Zobrazení aktuálního času v 24hodinovém formátu:
   ```bash
   date +%H:%M:%S
   ```

4. Zobrazení data a času v UTC:
   ```bash
   date -u
   ```

5. Zobrazení data příštího pátku:
   ```bash
   date -d "next Friday"
   ```

## Tipy
- Používejte formátovací řetězce pro přizpůsobení výstupu podle svých potřeb.
- Pokud potřebujete čas v jiném časovém pásmu, můžete použít proměnné prostředí `TZ`.
- Uložení výstupu příkazu `date` do proměnné pro další zpracování:
  ```bash
  current_date=$(date +%Y-%m-%d)
  echo $current_date
  ```