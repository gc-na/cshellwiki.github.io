# [Linux] Bash reboot použití: Restartování systému

## Přehled
Příkaz `reboot` slouží k restartování operačního systému. Je to užitečný nástroj pro administrátory, kteří potřebují rychle a efektivně restartovat server nebo počítač.

## Použití
Základní syntaxe příkazu je následující:

```
reboot [možnosti] [argumenty]
```

## Běžné možnosti
- `-f` : Vynucený restart bez provedení běžného vypnutí.
- `-i` : Informuje o důvodu restartu.
- `-p` : Vypnutí systému po restartu (pouze pokud je podporováno).

## Běžné příklady
1. **Jednoduchý restart systému:**
   ```bash
   reboot
   ```

2. **Vynucený restart bez vypnutí:**
   ```bash
   reboot -f
   ```

3. **Restart s informováním o důvodu:**
   ```bash
   reboot -i "Plánovaný restart pro údržbu"
   ```

4. **Restart a vypnutí systému:**
   ```bash
   reboot -p
   ```

## Tipy
- Před restartem se ujistěte, že jsou uloženy všechny důležité práce, aby nedošlo ke ztrátě dat.
- Používejte vynucený restart (`-f`) pouze v případě, že je to nezbytné, protože může způsobit ztrátu dat.
- Zvažte naplánování restartu pomocí `at` nebo `cron`, pokud potřebujete restartovat systém pravidelně.