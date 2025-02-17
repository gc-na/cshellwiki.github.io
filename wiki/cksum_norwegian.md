# [Linux] Bash cksum bruksanvisning: Beregn sjekksum og filstørrelse

## Oversikt
`cksum`-kommandoen brukes til å beregne sjekksummen og størrelsen på filer. Den genererer en CRC (Cyclic Redundancy Check) sjekksum, som kan brukes til å verifisere integriteten til dataene i filen.

## Bruk
Grunnleggende syntaks for `cksum`-kommandoen er som følger:
```bash
cksum [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a, --algorithm=ALGO`: Spesifiser algoritmen som skal brukes for å beregne sjekksummen.
- `--help`: Vis hjelp og tilgjengelige alternativer for `cksum`.
- `--version`: Vis versjonsinformasjon om `cksum`.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `cksum`:

1. Beregn sjekksummen for en fil:
   ```bash
   cksum filnavn.txt
   ```

2. Beregn sjekksummen for flere filer:
   ```bash
   cksum fil1.txt fil2.txt fil3.txt
   ```

3. Bruk `--help` for å vise tilgjengelige alternativer:
   ```bash
   cksum --help
   ```

4. Beregn sjekksummen med en spesifikk algoritme (hvis støttet):
   ```bash
   cksum --algorithm=crc32 filnavn.txt
   ```

## Tips
- Bruk `cksum` i skript for å verifisere filintegritet etter overføring eller lagring.
- Sammenlign sjekksummer for å sjekke om to filer er identiske.
- Husk at `cksum` kan gi forskjellige resultater for filer med forskjellige innhold, selv om de har samme navn.