# [Linux] Bash write bruken: Skrive meldinger til andre brukere

## Oversikt
`write`-kommandoen lar deg sende meldinger direkte til en annen bruker som er logget inn på systemet. Dette kan være nyttig for rask kommunikasjon i et flerbrukermiljø.

## Bruk
Den grunnleggende syntaksen for `write`-kommandoen er som følger:

```bash
write [brukernavn] [terminal]
```

## Vanlige alternativer
- `-n`: Brukes for å spesifisere at meldingen skal sendes uten å vise terminalen.
- `-h`: Viser hjelp og tilgjengelige alternativer for `write`-kommandoen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `write`-kommandoen:

1. Sende en melding til en spesifikk bruker:
   ```bash
   write ola
   Hei Ola, hvordan har du det?
   ```

2. Sende en melding til en spesifikk terminal:
   ```bash
   write ola pts/1
   Jeg er klar for møtet nå.
   ```

3. Avbryte en melding (trykk Ctrl+C):
   ```bash
   write ola
   Dette er en testmelding.
   ```

## Tips
- Sørg for at mottakeren er logget inn og har en aktiv terminal for å motta meldingen.
- Bruk `who`-kommandoen for å se hvilke brukere som er logget inn og deres terminaler før du sender meldinger.
- Vær oppmerksom på at meldinger kan være forstyrrende, så bruk `write` med omhu, spesielt i travle miljøer.