# [Linux] Bash tmux gebruik: Een terminal multiplexer

## Overzicht
Tmux is een terminal multiplexer die gebruikers in staat stelt om meerdere terminalsessies binnen één enkele venster te beheren. Het stelt je in staat om sessies te splitsen, te detacheren en opnieuw aan te sluiten, wat het ideaal maakt voor het werken op afstand of voor het organiseren van verschillende taken.

## Gebruik
De basis syntaxis van het tmux-commando is als volgt:

```bash
tmux [opties] [argumenten]
```

## Veelvoorkomende opties
- `new`: Start een nieuwe tmux-sessie.
- `attach`: Verbind met een bestaande tmux-sessie.
- `detach`: Ontkoppel de huidige sessie.
- `list-sessions`: Toon een lijst van actieve sessies.
- `kill-session`: Sluit een specifieke sessie.

## Veelvoorkomende voorbeelden

### Een nieuwe sessie starten
Om een nieuwe tmux-sessie te starten, gebruik je het volgende commando:

```bash
tmux new -s mijnsessie
```

### Verbinden met een bestaande sessie
Als je wilt verbinden met een bestaande sessie, gebruik je:

```bash
tmux attach -t mijnsessie
```

### Lijst van actieve sessies bekijken
Om een lijst van actieve sessies te bekijken, voer je dit commando uit:

```bash
tmux list-sessions
```

### Een sessie ontkoppelen
Om de huidige sessie te ontkoppelen, druk je op `Ctrl+b` gevolgd door `d`.

### Een sessie sluiten
Om een specifieke sessie te sluiten, gebruik je:

```bash
tmux kill-session -t mijnsessie
```

## Tips
- Gebruik `Ctrl+b` als prefix-toets voor tmux-commando's.
- Maak gebruik van paneel-splitsing (`Ctrl+b %` voor verticale splitsing en `Ctrl+b "` voor horizontale splitsing) om meerdere terminalvensters binnen één sessie te beheren.
- Sla je tmux-configuratie op in `~/.tmux.conf` om je instellingen aan te passen en te personaliseren.

Met deze basisinformatie en voorbeelden kun je beginnen met het gebruik van tmux om je terminalervaring te verbeteren.