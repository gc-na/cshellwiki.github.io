# [Linux] Bash modprobe použití: Správa modulů jádra

## Přehled
Příkaz `modprobe` slouží k načítání a odstraňování modulů jádra v operačním systému Linux. Umožňuje uživatelům spravovat ovladače zařízení a další funkce jádra bez nutnosti restartování systému.

## Použití
Základní syntaxe příkazu `modprobe` je následující:

```bash
modprobe [možnosti] [argumenty]
```

## Běžné možnosti
- `-r`, `--remove`: Odstraní modul jádra.
- `-n`, `--dry-run`: Zobrazí, co by se stalo, aniž by se skutečně provedla akce.
- `-v`, `--verbose`: Zobrazí podrobnosti o prováděných akcích.
- `--show`: Zobrazí informace o modulu bez jeho načtení.

## Běžné příklady
Načtení modulu jádra:

```bash
modprobe nfs
```

Odstranění modulu jádra:

```bash
modprobe -r nfs
```

Zobrazení, co by se stalo při načítání modulu:

```bash
modprobe -n nfs
```

Načtení modulu s podrobným výstupem:

```bash
modprobe -v nfs
```

## Tipy
- Před použitím `modprobe` se ujistěte, že máte potřebná oprávnění (obvykle je potřeba být root).
- Používejte možnost `--dry-run` pro ověření, co se stane, než provedete skutečné akce.
- Pravidelně kontrolujte, které moduly jsou načteny pomocí příkazu `lsmod`, abyste měli přehled o aktuálním stavu jádra.