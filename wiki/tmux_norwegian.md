# [Linux] Bash tmux bruk: Administrere terminalvinduer

## Oversikt
`tmux` er en terminal multiplexer som lar deg kjøre flere terminaløkter i ett enkelt vindu. Dette er nyttig for å organisere arbeidsflyten din, spesielt når du jobber med flere prosesser eller oppgaver samtidig.

## Bruk
Grunnleggende syntaks for `tmux` er som følger:

```bash
tmux [alternativer] [argumenter]
```

## Vanlige alternativer
- `new`: Opprett en ny tmux-økt.
- `attach`: Koble til en eksisterende tmux-økt.
- `list-sessions`: Vis alle aktive tmux-økter.
- `kill-session`: Avslutt en spesifikk tmux-økt.
- `detach`: Frakoble den nåværende tmux-økten.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `tmux`:

### Opprett en ny tmux-økt
```bash
tmux new -s minØkt
```

### Koble til en eksisterende tmux-økt
```bash
tmux attach -t minØkt
```

### Liste opp alle aktive tmux-økter
```bash
tmux list-sessions
```

### Avslutte en spesifikk tmux-økt
```bash
tmux kill-session -t minØkt
```

### Frakoble fra den nåværende tmux-økten
For å frakoble fra en økt, trykk `Ctrl+b` etterfulgt av `d`.

## Tips
- Bruk `tmux` sammen med `vim` eller andre tekstredigerere for å forbedre produktiviteten din.
- Lag snarveier for vanlige kommandoer ved å bruke tmux-konfigurasjonsfilen (`~/.tmux.conf`).
- Utforsk tmux-panelet for å dele vinduet i flere ruter, noe som gir deg muligheten til å overvåke flere prosesser samtidig.