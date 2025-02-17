# [Linux] Bash swapon použití: Aktivace swapového prostoru

## Přehled
Příkaz `swapon` se používá k aktivaci swapového prostoru v systému Linux. Swap je oblast na pevném disku, která slouží jako rozšíření paměti RAM, což umožňuje systému efektivněji spravovat paměťové zdroje.

## Použití
Základní syntaxe příkazu je následující:

```bash
swapon [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Aktivuje všechny swapové soubory uvedené v souboru `/etc/fstab`.
- `-s`: Zobrazí informace o aktuálně aktivních swapových oblastech.
- `--show`: Zobrazí podrobnosti o swapových oblastech, které jsou aktivní.

## Běžné příklady
Aktivace swapového souboru:

```bash
sudo swapon /cesta/k/swapfile
```

Aktivace všech swapových oblastí definovaných v `/etc/fstab`:

```bash
sudo swapon -a
```

Zobrazení aktuálních swapových oblastí:

```bash
swapon -s
```

Zobrazení podrobných informací o aktivních swapových oblastech:

```bash
swapon --show
```

## Tipy
- Ujistěte se, že swapový soubor má správná oprávnění, aby byl bezpečný a funkční.
- Pravidelně kontrolujte využití swapu pomocí příkazu `swapon -s` nebo `free -h`, abyste se ujistili, že váš systém má dostatek paměti.
- Při vytváření swapového souboru použijte příkaz `fallocate` nebo `dd`, abyste zajistili, že je správně inicializován.