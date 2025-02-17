# [Linux] Bash uptime použití: Zobrazení doby běhu systému

## Přehled
Příkaz `uptime` slouží k zobrazení doby, po kterou je systém v chodu, a také poskytuje informace o počtu uživatelů přihlášených do systému a průměrné zatížení systému za poslední 1, 5 a 15 minut.

## Použití
Základní syntaxe příkazu je následující:

```bash
uptime [možnosti]
```

## Běžné možnosti
- `-p` : Zobrazí dobu běhu systému v lidsky čitelné podobě.
- `-s` : Zobrazí čas, kdy byl systém naposledy spuštěn.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `uptime`:

1. Základní příkaz pro zobrazení doby běhu systému:
   ```bash
   uptime
   ```

2. Zobrazení doby běhu systému v lidsky čitelné podobě:
   ```bash
   uptime -p
   ```

3. Zobrazení času posledního spuštění systému:
   ```bash
   uptime -s
   ```

## Tipy
- Používejte příkaz `uptime` pravidelně pro sledování výkonu a stability systému.
- Kombinujte `uptime` s dalšími příkazy, jako je `top` nebo `htop`, pro komplexní analýzu zatížení systému.
- Pokud potřebujete monitorovat systém na dálku, můžete použít `uptime` v rámci skriptů pro automatizaci sledování.