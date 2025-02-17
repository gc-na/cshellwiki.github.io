# [Linux] Bash shutdown bruk: Stenge ned systemet

## Oversikt
`shutdown`-kommandoen brukes til å stenge ned eller starte systemet på nytt. Den gir brukeren mulighet til å planlegge nedstenging, spesifisere tidsintervaller og sende meldinger til andre brukere før systemet stenges.

## Bruk
Grunnleggende syntaks for `shutdown`-kommandoen er som følger:

```bash
shutdown [alternativer] [tid] [melding]
```

## Vanlige alternativer
- `-h`: Stenger ned systemet.
- `-r`: Starter systemet på nytt.
- `-c`: Avbryter en planlagt nedstenging.
- `+m`: Angir nedstenging etter m minutter.
- `hh:mm`: Angir spesifikk tid for nedstenging i formatet timer:minutter.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `shutdown`-kommandoen:

1. Stenge ned systemet umiddelbart:
   ```bash
   shutdown -h now
   ```

2. Starte systemet på nytt etter 5 minutter:
   ```bash
   shutdown -r +5
   ```

3. Planlegge nedstenging til kl. 22:00:
   ```bash
   shutdown -h 22:00
   ```

4. Avbryte en planlagt nedstenging:
   ```bash
   shutdown -c
   ```

5. Stenge ned systemet med en melding til brukere:
   ```bash
   shutdown -h now "Systemet stenges ned for vedlikehold."
   ```

## Tips
- Sørg for å informere alle brukere om en planlagt nedstenging for å unngå tap av data.
- Bruk `shutdown -c` hvis du trenger å avbryte en nedstenging som allerede er planlagt.
- Vær oppmerksom på at du må ha administrative rettigheter for å bruke `shutdown`-kommandoen.