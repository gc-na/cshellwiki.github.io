# [Linux] Bash renice bruken: Endre prioritet for prosesser

## Oversikt
`renice`-kommandoen brukes til å endre prioriteten til en eller flere kjørende prosesser i Linux. Ved å justere prioriteten kan du kontrollere hvor mye CPU-tid en prosess får i forhold til andre prosesser. Høyere prioritet (lavere tall) betyr at prosessen får mer CPU-tid, mens lavere prioritet (høyere tall) betyr at prosessen får mindre.

## Bruk
Grunnleggende syntaks for `renice`-kommandoen er som følger:

```bash
renice [alternativer] [ny prioritet] [prosesser]
```

## Vanlige alternativer
- `-n` : Angi den nye prioriteten.
- `-p` : Spesifiser prosess-ID (PID) for prosessen som skal endres.
- `-g` : Endre prioriteten til alle prosesser i en gruppe.
- `-u` : Endre prioriteten til alle prosesser eid av en spesifikk bruker.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `renice`:

1. Endre prioriteten til en prosess med PID 1234 til 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Endre prioriteten til alle prosesser i en gruppe med gruppe-ID 5678 til -5:
   ```bash
   renice -n -5 -g 5678
   ```

3. Endre prioriteten til alle prosesser eid av brukeren "brukernavn" til 15:
   ```bash
   renice -n 15 -u brukernavn
   ```

4. Sjekk den nåværende prioriteten til en prosess før du endrer den:
   ```bash
   ps -o pid,nice,cmd -p 1234
   ```

## Tips
- Vær forsiktig med å sette en for høy prioritet på prosesser, da det kan føre til at systemet blir tregt eller ustabilt.
- Du må ha tilstrekkelige rettigheter (som root) for å endre prioriteten til prosesser som ikke tilhører deg.
- Bruk `nice`-kommandoen når du starter en prosess for å sette dens prioritet fra starten av, i stedet for å bruke `renice` senere.