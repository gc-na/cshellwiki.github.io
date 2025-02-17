# [Linux] Bash hostname použití: Zobrazí nebo nastaví název hostitele

## Přehled
Příkaz `hostname` se používá k zobrazení nebo nastavení názvu hostitele systému. Název hostitele je identifikátor, který se používá k rozlišení počítače v síti.

## Použití
Základní syntaxe příkazu je následující:

```bash
hostname [options] [arguments]
```

## Běžné možnosti
- `-a`, `--alias`: Zobrazí alias hostitele.
- `-d`, `--domain`: Zobrazí doménu hostitele.
- `-f`, `--fqdn`: Zobrazí plně kvalifikovaný název domény (FQDN).
- `-i`, `--ip-address`: Zobrazí IP adresu hostitele.
- `-s`, `--short`: Zobrazí krátký název hostitele.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `hostname`:

1. Zobrazení aktuálního názvu hostitele:
   ```bash
   hostname
   ```

2. Zobrazení plně kvalifikovaného názvu domény:
   ```bash
   hostname -f
   ```

3. Zobrazení IP adresy hostitele:
   ```bash
   hostname -i
   ```

4. Nastavení nového názvu hostitele:
   ```bash
   sudo hostname novy-nazev
   ```

5. Zobrazení aliasu hostitele:
   ```bash
   hostname -a
   ```

## Tipy
- Při nastavování nového názvu hostitele použijte `sudo`, abyste měli potřebná oprávnění.
- Po změně názvu hostitele je dobré restartovat systém, aby se změny projevily.
- Pro trvalé změny názvu hostitele můžete upravit soubor `/etc/hostname`.