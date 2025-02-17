# [Linux] Bash watch bruk: Overvåk kommandoer i sanntid

## Oversikt
`watch`-kommandoen brukes til å kjøre en spesifisert kommando gjentatte ganger, og viser resultatet i sanntid. Dette er nyttig for å overvåke endringer i utdataene fra en kommando over tid.

## Bruk
Den grunnleggende syntaksen for `watch`-kommandoen er:

```bash
watch [alternativer] [kommando]
```

## Vanlige Alternativer
- `-n, --interval`: Angir hvor ofte (i sekunder) kommandoen skal kjøres på nytt. Standard er 2 sekunder.
- `-d, --differences`: Marker forskjeller mellom påfølgende utdata.
- `-t, --no-title`: Skjul tittellinjen som viser kommandoen som kjøres.
- `-h, --help`: Vis hjelp og informasjon om bruken av `watch`.

## Vanlige Eksempler
Her er noen praktiske eksempler på hvordan `watch` kan brukes:

1. Overvåke diskbruk:
   ```bash
   watch -n 5 df -h
   ```

2. Se på prosesslisten for endringer:
   ```bash
   watch -d ps aux
   ```

3. Overvåke nettverksforbindelser:
   ```bash
   watch -n 2 netstat -tuln
   ```

4. Se på loggfilen i sanntid:
   ```bash
   watch tail -n 10 /var/log/syslog
   ```

## Tips
- Bruk `-d` for å lett se hva som har endret seg mellom oppdateringer.
- Juster intervallet med `-n` for å tilpasse hvor ofte du vil se oppdateringer, avhengig av hvor raskt dataene endres.
- Kombiner `watch` med andre kommandoer for å overvåke spesifikke systemressurser eller applikasjoner.