# [Linux] Bash tmux použití: Správa terminálových relací

## Přehled
Tmux je terminálový multiplexer, který umožňuje uživatelům spravovat více terminálových relací v jednom okně. Umožňuje rozdělení obrazovky, přepínání mezi relacemi a udržení běžících procesů i po odhlášení.

## Použití
Základní syntaxe příkazu tmux je následující:

```bash
tmux [možnosti] [argumenty]
```

## Běžné možnosti
- `new`: Vytvoří novou relaci.
- `attach`: Připojí se k existující relaci.
- `list-sessions`: Zobrazí seznam všech aktivních relací.
- `kill-session`: Ukončí specifikovanou relaci.
- `split-window`: Rozdělí aktuální okno na dvě části.

## Běžné příklady
1. **Vytvoření nové relace:**
   ```bash
   tmux new -s moje_relace
   ```

2. **Připojení k existující relaci:**
   ```bash
   tmux attach -t moje_relace
   ```

3. **Zobrazení seznamu relací:**
   ```bash
   tmux list-sessions
   ```

4. **Ukončení relace:**
   ```bash
   tmux kill-session -t moje_relace
   ```

5. **Rozdělení okna na dvě části:**
   ```bash
   tmux split-window
   ```

## Tipy
- Používejte klávesové zkratky pro rychlé ovládání tmuxu, například `Ctrl+b` následované `c` pro vytvoření nového okna.
- Pojmenujte své relace pro snadnější identifikaci.
- Uložte si konfiguraci tmux do souboru `~/.tmux.conf` pro personalizaci a automatizaci nastavení.