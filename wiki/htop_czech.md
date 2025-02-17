# [Linux] Bash htop použití: Monitorování systémových procesů

## Přehled
Příkaz `htop` je interaktivní nástroj pro sledování procesů v systému. Umožňuje uživatelům zobrazit běžící procesy, využití CPU, paměti a další systémové informace v reálném čase. Na rozdíl od tradičního příkazu `top` nabízí `htop` uživatelsky přívětivější rozhraní a více možností pro interakci s procesy.

## Použití
Základní syntaxe příkazu `htop` je následující:

```bash
htop [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`, `--help`: Zobrazí nápovědu k příkazu a dostupným možnostem.
- `-C`, `--no-color`: Spustí `htop` bez barevného rozlišení.
- `-s`, `--sort`: Umožňuje seřadit procesy podle zvoleného kritéria (např. CPU, paměť).
- `-p`, `--pid`: Sleduje pouze specifikované procesy podle jejich PID.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `htop`:

1. **Základní spuštění htop**:
   ```bash
   htop
   ```

2. **Zobrazení nápovědy**:
   ```bash
   htop -h
   ```

3. **Spuštění htop bez barev**:
   ```bash
   htop -C
   ```

4. **Seřazení procesů podle využití CPU**:
   ```bash
   htop -s PERCENT_CPU
   ```

5. **Sledování konkrétního procesu podle PID**:
   ```bash
   htop -p 1234
   ```

## Tipy
- Používejte klávesové zkratky pro rychlé akce, jako je `F9` pro zabití procesu nebo `F3` pro hledání.
- Pravidelně sledujte využití paměti a CPU, abyste předešli přetížení systému.
- Přizpůsobte si zobrazení podle svých potřeb pomocí klávesy `F2` pro nastavení.