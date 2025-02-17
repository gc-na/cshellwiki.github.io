# [Linux] Bash pwd Bruk: Vise gjeldende arbeidskatalog

## Oversikt
`pwd` (print working directory) er en Bash-kommando som viser den nåværende arbeidskatalogen i terminalen. Den gir deg den fullstendige stien til katalogen du befinner deg i, noe som er nyttig for navigering og skripting.

## Bruk
Den grunnleggende syntaksen for `pwd`-kommandoen er:

```bash
pwd [alternativer]
```

## Vanlige alternativer
- `-L`: Viser den logiske banen til den nåværende arbeidskatalogen, som kan inkludere symboliske lenker.
- `-P`: Viser den fysiske banen til den nåværende arbeidskatalogen, som viser den faktiske banen uten symboliske lenker.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `pwd`:

1. Vise den nåværende arbeidskatalogen:
   ```bash
   pwd
   ```

2. Vise den fysiske banen til arbeidskatalogen:
   ```bash
   pwd -P
   ```

3. Vise den logiske banen til arbeidskatalogen:
   ```bash
   pwd -L
   ```

## Tips
- Bruk `pwd` i skript for å dynamisk referere til den nåværende arbeidskatalogen.
- Kombiner `pwd` med andre kommandoer for å lage mer komplekse kommandoer, for eksempel:
  ```bash
  echo "Den nåværende katalogen er: $(pwd)"
  ```
- Husk at `pwd` alltid viser den aktive katalogen, så vær oppmerksom på hvilken katalog du er i før du kjører kommandoen.