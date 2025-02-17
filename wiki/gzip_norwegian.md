# [Linux] Bash gzip Bruk: Komprimere filer

## Oversikt
`gzip` er et kommandolinjeverktøy som brukes til å komprimere filer. Det reduserer filstørrelsen ved å bruke Lempel-Ziv algoritmen, noe som gjør det lettere å lagre og overføre data.

## Bruk
Grunnleggende syntaks for `gzip`-kommandoen er som følger:

```bash
gzip [alternativer] [argumenter]
```

## Vanlige alternativer
- `-d` eller `--decompress`: Dekomprimerer en gzip-komprimert fil.
- `-k` eller `--keep`: Beholder den opprinnelige filen etter komprimering.
- `-v` eller `--verbose`: Viser detaljer om komprimeringsprosessen.
- `-r` eller `--recursive`: Komprimerer filer i alle undermapper.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `gzip`:

1. Komprimere en fil:
   ```bash
   gzip fil.txt
   ```

2. Dekomprimere en gzip-fil:
   ```bash
   gzip -d fil.txt.gz
   ```

3. Beholde den opprinnelige filen etter komprimering:
   ```bash
   gzip -k fil.txt
   ```

4. Komprimere alle `.txt`-filer i en mappe:
   ```bash
   gzip *.txt
   ```

5. Komprimere filer rekursivt i en mappe:
   ```bash
   gzip -r mappe/
   ```

## Tips
- Når du komprimerer store filer, kan det være lurt å bruke `-v` for å se fremdriften.
- Vær oppmerksom på at komprimerte filer får filendelsen `.gz`, så husk å bruke riktig filnavn ved dekomprimering.
- For å spare plass, vurder å bruke `gzip` sammen med `tar` for å komprimere hele kataloger.