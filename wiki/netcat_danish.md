# [Linux] Bash netcat brug: Netværkskommunikation og fejlfinding

## Oversigt
Netcat, ofte kaldet "Swiss Army knife" for netværksværktøjer, er et alsidigt kommandolinjeprogram, der bruges til at oprette forbindelser mellem computere over et netværk. Det kan bruges til at sende og modtage data, oprette TCP/UDP-forbindelser, og til fejlfinding af netværksproblemer.

## Brug
Den grundlæggende syntaks for netcat-kommandoen er:

```bash
netcat [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l`: Lyt på en port for indkommende forbindelser.
- `-p`: Angiv portnummeret, der skal bruges.
- `-u`: Brug UDP i stedet for TCP.
- `-v`: Aktivér detaljeret (verbose) output.
- `-z`: Scanning mode, hvor der ikke sendes data.

## Almindelige eksempler

### Opret en simpel TCP-forbindelse
For at oprette en forbindelse til en server på port 80 kan du bruge følgende kommando:

```bash
netcat example.com 80
```

### Lytte på en port
For at lytte på port 1234 og vente på indkommende forbindelser:

```bash
netcat -l -p 1234
```

### Send en tekstfil til en server
For at sende en fil til en server via netcat:

```bash
netcat example.com 1234 < fil.txt
```

### Modtag en fil fra en server
For at modtage en fil fra en server og gemme den:

```bash
netcat -l -p 1234 > modtaget_fil.txt
```

### Scanning af porte
For at scanne åbne porte på en vært:

```bash
netcat -zv example.com 1-1000
```

## Tips
- Brug `-v` for at få mere information om forbindelserne, hvilket kan være nyttigt til fejlfinding.
- Vær opmærksom på sikkerhed, når du lytter på porte; sørg for, at du kun lytter på sikre netværk.
- Netcat kan også bruges til at oprette en simpel chat-applikation ved at forbinde to terminaler.