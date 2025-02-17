# [Linux] Bash exec použití: Spouštění příkazů v aktuálním shellu

## Přehled
Příkaz `exec` v Bash se používá k nahrazení aktuálního shell procesu novým procesem. To znamená, že když spustíte příkaz pomocí `exec`, aktuální shell se ukončí a je nahrazen tímto příkazem. Tento příkaz je užitečný, když chcete spustit program a nechcete se vrátit zpět do původního shellu.

## Použití
Základní syntaxe příkazu `exec` je následující:

```bash
exec [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Umožňuje specifikovat alternativní jméno pro nový proces.
- `-l`: Spustí nový shell jako login shell.
- `-c`: Spustí příkaz v novém shellu.

## Běžné příklady
1. Nahrazení aktuálního shellu příkazem `bash`:
   ```bash
   exec bash
   ```

2. Spuštění programu `top` a nahrazení aktuálního shellu:
   ```bash
   exec top
   ```

3. Spuštění skriptu s alternativním názvem:
   ```bash
   exec -a novy_nazev ./moj_skript.sh
   ```

4. Spuštění příkazu s login shellem:
   ```bash
   exec -l /bin/sh
   ```

## Tipy
- Používejte `exec` s opatrností, protože nahrazení shellu znamená, že se nevrátíte zpět do původního shellu.
- `exec` je užitečné pro skripty, kde chcete, aby poslední příkaz nahradil skript, čímž se uvolní systémové prostředky.
- Mějte na paměti, že jakýkoliv příkaz spuštěný pomocí `exec` nebude mít možnost se vrátit zpět do shellu, pokud se neprovádí v subshellu.