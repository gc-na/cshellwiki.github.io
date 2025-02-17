# [Linux] Bash nohup použití: Spuštění příkazů na pozadí bez přerušení

## Přehled
Příkaz `nohup` (no hang up) slouží k tomu, aby se procesy spouštěly na pozadí a pokračovaly v běhu i po odhlášení uživatele. To je užitečné, když potřebujete spustit dlouhotrvající úlohu a nechcete, aby se zastavila, když se odpojíte od terminálu.

## Použití
Základní syntaxe příkazu `nohup` je následující:

```
nohup [možnosti] [argumenty] &
```

Zde `&` znamená, že proces poběží na pozadí.

## Běžné možnosti
- `-h`: Zobrazí nápovědu k příkazu.
- `-v`: Zobrazí verzi příkazu.
- `-p`: Umožňuje spustit příkaz s určitou prioritou.

## Běžné příklady
1. Spuštění skriptu na pozadí:
   ```bash
   nohup ./myscript.sh &
   ```

2. Spuštění příkazu `ping` na pozadí a přesměrování výstupu do souboru:
   ```bash
   nohup ping google.com > ping_output.txt &
   ```

3. Spuštění Python skriptu na pozadí:
   ```bash
   nohup python3 myscript.py &
   ```

4. Spuštění dlouhého příkazu s přesměrováním chyb:
   ```bash
   nohup long_running_command > output.log 2>&1 &
   ```

## Tipy
- Vždy přesměrovávejte výstup příkazu do souboru, abyste mohli sledovat, co se děje, když je proces spuštěn na pozadí.
- Používejte příkaz `jobs` pro zobrazení běžících úloh na pozadí.
- Pokud potřebujete proces zastavit, můžete použít příkaz `kill` s PID procesu, který zjistíte pomocí příkazu `ps`.