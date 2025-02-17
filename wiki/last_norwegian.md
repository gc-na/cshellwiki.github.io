# [Linux] Bash last bruk: Vise siste innlogginger

## Oversikt
`last`-kommandoen brukes til å vise en liste over de siste innloggingene på systemet. Den henter informasjon fra filen `/var/log/wtmp`, som registrerer alle innlogginger og utlogginger.

## Bruk
Grunnleggende syntaks for `last`-kommandoen er som følger:

```bash
last [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser den fulle vertsnavnet til brukeren.
- `-n [antall]`: Angir hvor mange innlogginger som skal vises.
- `-x`: Viser systemoppstart og nedstengninger i tillegg til innloggingene.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `last`-kommandoen:

1. Vise alle siste innlogginger:
   ```bash
   last
   ```

2. Vise de siste 5 innloggingene:
   ```bash
   last -n 5
   ```

3. Vise innlogginger med vertsnavn:
   ```bash
   last -a
   ```

4. Vise innlogginger og systemoppstart:
   ```bash
   last -x
   ```

## Tips
- Bruk `last -n [antall]` for å begrense resultatene til et håndterbart antall.
- Kombiner `last` med `grep` for å filtrere resultater basert på spesifikke brukernavn.
- Vær oppmerksom på at `last` viser informasjon fra `/var/log/wtmp`, så hvis denne filen er tømt, vil du ikke få resultater.