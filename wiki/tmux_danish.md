# [Linux] Bash tmux brug: Terminal multiplexer

## Oversigt
tmux er en terminal multiplexer, der giver brugerne mulighed for at oprette, administrere og navigere mellem flere terminalsessioner inden for et enkelt vindue. Det er især nyttigt for udviklere og systemadministratorer, der ønsker at køre flere opgaver samtidigt uden at åbne flere terminalvinduer.

## Brug
Den grundlæggende syntaks for tmux er:

```
tmux [muligheder] [argumenter]
```

## Almindelige muligheder
- `new`: Opretter en ny tmux-session.
- `attach`: Tilslutter til en eksisterende tmux-session.
- `list-sessions`: Viser en liste over aktive tmux-sessioner.
- `kill-session`: Dræber en specifik tmux-session.
- `detach`: Afbryder forbindelsen til den aktuelle session uden at afslutte den.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger tmux:

1. Opret en ny tmux-session:
   ```bash
   tmux new -s min_session
   ```

2. Tilslut til en eksisterende session:
   ```bash
   tmux attach -t min_session
   ```

3. Liste alle aktive tmux-sessioner:
   ```bash
   tmux list-sessions
   ```

4. Dræb en specifik session:
   ```bash
   tmux kill-session -t min_session
   ```

5. Afbryd fra den aktuelle session:
   ```bash
   Ctrl + b, d
   ```

## Tips
- Brug `Ctrl + b` efterfulgt af en tast for at udføre kommandoer i tmux. For eksempel, `Ctrl + b, c` opretter en ny vindue.
- Navngiv dine sessioner for lettere at kunne identificere dem senere.
- Overvej at tilpasse din tmux-konfiguration ved at redigere `~/.tmux.conf` for at forbedre din arbejdsgang.