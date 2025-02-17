# [Linux] Bash sleep použití: Zpoždění provádění skriptů

## Přehled
Příkaz `sleep` v Bash slouží k pozastavení provádění skriptu na určitou dobu. Můžete jej použít k vytvoření zpoždění mezi příkazy, což je užitečné například při automatizaci úloh nebo při čekání na dokončení jiných procesů.

## Použití
Základní syntaxe příkazu `sleep` je následující:

```
sleep [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`, `--help`: Zobrazí nápovědu k příkazu.
- `-v`, `--version`: Zobrazí verzi příkazu.

## Běžné příklady
1. **Zpoždění o 5 sekund:**
   ```bash
   sleep 5
   ```

2. **Zpoždění o 2 minuty:**
   ```bash
   sleep 2m
   ```

3. **Zpoždění o 1 hodinu:**
   ```bash
   sleep 1h
   ```

4. **Zpoždění s kombinací časových jednotek (např. 1 minuta a 30 sekund):**
   ```bash
   sleep 1m30s
   ```

5. **Použití v skriptu pro zpoždění mezi příkazy:**
   ```bash
   echo "Začínám..."
   sleep 3
   echo "Pokračuji po 3 sekundách."
   ```

## Tipy
- Používejte `sleep` pro synchronizaci úloh ve skriptech, abyste zajistili, že se některé příkazy neprovádějí příliš rychle za sebou.
- Pokud potřebujete delší zpoždění, můžete kombinovat různé časové jednotky (např. minuty a sekundy).
- V případě, že potřebujete zpoždění v rámci smyčky, ujistěte se, že zpoždění je dostatečné, aby nedošlo k přetížení systému.