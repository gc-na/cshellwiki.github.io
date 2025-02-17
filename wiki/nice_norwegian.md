# [Linux] Bash nice bruk: Juster prosessprioritet

## Oversikt
`nice`-kommandoen brukes til å starte prosesser med en spesifisert prioritet. Den lar brukeren justere hvor mye CPU-tid en prosess får i forhold til andre prosesser som kjører på systemet. Dette kan være nyttig for å sikre at viktige oppgaver får mer ressurser, mens mindre viktige oppgaver får mindre.

## Bruk
Den grunnleggende syntaksen for `nice`-kommandoen er som følger:

```bash
nice [alternativer] [kommando]
```

## Vanlige alternativer
- `-n, --adjustment`: Angir justeringen av prioriteten. Verdien kan være et heltall fra -20 (høyest prioritet) til 19 (lavest prioritet).
- `-h, --help`: Viser hjelpetekst for `nice`.
- `--version`: Viser versjonsinformasjon for `nice`.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `nice` kan brukes:

1. **Starte en prosess med lavere prioritet:**
   ```bash
   nice -n 10 ./min_prosess
   ```
   Dette starter `min_prosess` med en prioritet justert til 10.

2. **Starte en prosess med høyere prioritet:**
   ```bash
   nice -n -5 ./viktig_prosess
   ```
   Dette starter `viktig_prosess` med en prioritet justert til -5.

3. **Sjekke nåværende prioritet for en prosess:**
   ```bash
   ps -o pid,ni,cmd
   ```
   Dette viser prosess-ID, nice-verdi og kommando for alle kjørende prosesser.

## Tips
- Vær forsiktig med å bruke negative prioriteringer, da dette kan påvirke systemets ytelse ved å gi for mye CPU-tid til en enkelt prosess.
- Bruk `nice` i kombinasjon med `nohup` for å kjøre lange prosesser i bakgrunnen uten å bli avbrutt når du logger ut.
- For å endre prioriteten til en allerede kjørende prosess, kan du bruke `renice`-kommandoen.