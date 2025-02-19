# [Linux] C Shell (csh) tmux gebruik: Beheer van terminalmultiplexers

## Overzicht
De `tmux`-opdracht is een terminalmultiplexer die gebruikers in staat stelt om meerdere terminalsessies binnen één enkele venster te beheren. Dit is bijzonder handig voor het organiseren van verschillende taken en processen zonder meerdere terminalvensters te openen.

## Gebruik
De basis syntaxis van de `tmux`-opdracht is als volgt:

```bash
tmux [opties] [argumenten]
```

## Veelvoorkomende opties
- `new`: Start een nieuwe tmux-sessie.
- `attach`: Verbind met een bestaande tmux-sessie.
- `list-sessions`: Toon een lijst van actieve tmux-sessies.
- `kill-session`: Sluit een specifieke tmux-sessie af.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `tmux`:

1. **Een nieuwe tmux-sessie starten:**
   ```bash
   tmux new -s mijnsessie
   ```

2. **Verbind met een bestaande sessie:**
   ```bash
   tmux attach -t mijnsessie
   ```

3. **Lijst van actieve sessies bekijken:**
   ```bash
   tmux list-sessions
   ```

4. **Een specifieke sessie beëindigen:**
   ```bash
   tmux kill-session -t mijnsessie
   ```

## Tips
- Gebruik `Ctrl+b` gevolgd door `%` om een verticale splitsing van het venster te maken, en `Ctrl+b` gevolgd door `"` voor een horizontale splitsing.
- Maak gebruik van paneel-navigatie met `Ctrl+b` gevolgd door de pijltjestoetsen om snel tussen verschillende vensters te schakelen.
- Sla je sessies op door regelmatig te controleren op actieve sessies met `tmux list-sessions`, zodat je geen werk verliest.