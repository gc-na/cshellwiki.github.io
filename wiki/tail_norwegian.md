# [Linux] Bash tail bruk: Vise de siste linjene i en fil

## Oversikt
`tail`-kommandoen brukes til å vise de siste linjene i en fil. Den er spesielt nyttig for å overvåke loggfiler eller for å se på de nyeste oppføringene i en tekstfil.

## Bruk
Grunnleggende syntaks for `tail`-kommandoen er som følger:

```bash
tail [alternativer] [filnavn]
```

## Vanlige alternativer
- `-n [antall]`: Viser de siste [antall] linjene i filen. Standard er 10 linjer.
- `-f`: Følger filen i sanntid, noe som betyr at nye linjer som legges til filen vil bli vist umiddelbart.
- `-c [antall]`: Viser de siste [antall] byte i filen i stedet for linjer.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `tail`:

1. Vise de siste 10 linjene i en fil:
   ```bash
   tail filnavn.txt
   ```

2. Vise de siste 20 linjene i en fil:
   ```bash
   tail -n 20 filnavn.txt
   ```

3. Følge en loggfil i sanntid:
   ```bash
   tail -f loggfil.log
   ```

4. Vise de siste 50 byte i en fil:
   ```bash
   tail -c 50 filnavn.txt
   ```

## Tips
- Bruk `tail -f` for å overvåke loggfiler mens programmet kjører, slik at du kan se nye oppføringer umiddelbart.
- Kombiner `tail` med `grep` for å filtrere spesifikke linjer fra loggfiler:
  ```bash
  tail -f loggfil.log | grep "feil"
  ```
- For å se de siste linjene i flere filer samtidig, kan du spesifisere flere filnavn:
  ```bash
  tail fil1.txt fil2.txt
  ```