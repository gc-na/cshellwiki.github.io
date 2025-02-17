# [Linux] Bash mkswap použití: Vytváří swap prostor

## Přehled
Příkaz `mkswap` slouží k vytvoření swapového prostoru na disku, který se používá k rozšíření paměti systému. Tento prostor umožňuje operačnímu systému ukládat data, když je fyzická paměť (RAM) plná, což pomáhá zlepšit výkon a stabilitu systému.

## Použití
Základní syntaxe příkazu `mkswap` je následující:

```bash
mkswap [možnosti] [argumenty]
```

## Běžné možnosti
- `-L, --label LABEL` : Nastaví štítek pro swapový prostor.
- `-f, --force` : Vynutí vytvoření swapu i na zařízeních, která nejsou obvykle určena pro swap.
- `-p, --pagesize SIZE` : Určuje velikost stránek pro swap.

## Běžné příklady
1. Vytvoření swapového souboru:
   ```bash
   sudo fallocate -l 1G /swapfile
   sudo mkswap /swapfile
   ```

2. Aktivace swapového souboru:
   ```bash
   sudo swapon /swapfile
   ```

3. Vytvoření swapového prostoru na oddílu:
   ```bash
   sudo mkswap /dev/sdX1
   ```

4. Nastavení štítku pro swapový prostor:
   ```bash
   sudo mkswap -L my_swap /dev/sdX1
   ```

## Tipy
- Před použitím `mkswap` se ujistěte, že cílové zařízení nebo soubor neobsahuje žádná důležitá data, protože příkaz je destruktivní.
- Po vytvoření swapového prostoru je dobré přidat záznam do souboru `/etc/fstab`, aby se swap aktivoval automaticky po restartu.
- Sledujte využití swapu pomocí příkazu `swapon --show`, abyste zajistili, že systém má dostatek dostupného swapu.