# [Linux] Bash hwclock použití: Správa hardwarového hodin

## Přehled
Příkaz `hwclock` slouží k zobrazení a nastavení hardwarových hodin počítače. Tyto hodiny fungují nezávisle na operačním systému a udržují čas i při vypnutí zařízení.

## Použití
Základní syntaxe příkazu je následující:

```bash
hwclock [možnosti] [argumenty]
```

## Běžné možnosti
- `--show`: Zobrazí aktuální čas hardwarových hodin.
- `--set`: Nastaví čas hardwarových hodin.
- `--hctosys`: Nastaví systémový čas na hodnotu hardwarových hodin.
- `--systohc`: Nastaví hardwarové hodiny na aktuální systémový čas.
- `--utc`: Umožňuje nastavit čas v UTC (koordinovaný světový čas).

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `hwclock`:

1. Zobrazení aktuálního času hardwarových hodin:
   ```bash
   hwclock --show
   ```

2. Nastavení hardwarových hodin na aktuální systémový čas:
   ```bash
   hwclock --systohc
   ```

3. Nastavení systémového času na hodnotu hardwarových hodin:
   ```bash
   hwclock --hctosys
   ```

4. Nastavení hardwarových hodin na konkrétní datum a čas (např. 1. ledna 2023, 12:00):
   ```bash
   hwclock --set --date="2023-01-01 12:00:00"
   ```

5. Zobrazení času v UTC:
   ```bash
   hwclock --show --utc
   ```

## Tipy
- Před provedením změn v hardwarových hodinách se ujistěte, že máte správná oprávnění (např. spusťte příkaz jako root).
- Pravidelně synchronizujte hardwarové hodiny se systémovým časem, aby se předešlo nesrovnalostem.
- Používejte volbu `--utc`, pokud pracujete s více operačními systémy, které mohou mít různé časové zóny.