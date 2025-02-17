# [Linux] Bash comm bruk: Sammenligne sorterte filer

## Oversikt
`comm`-kommandoen brukes til å sammenligne to sorterte filer linje for linje. Den viser forskjeller og likheter mellom filene, noe som gjør den nyttig for å analysere innholdet i tekstfiler.

## Bruk
Grunnleggende syntaks for `comm`-kommandoen er som følger:

```bash
comm [alternativer] [fil1] [fil2]
```

## Vanlige alternativer
- `-1`: Undertrykk linjer som kun finnes i den første filen.
- `-2`: Undertrykk linjer som kun finnes i den andre filen.
- `-3`: Undertrykk linjer som finnes i begge filer.
- `-i`: Ignorer store og små bokstaver ved sammenligning.
- `-u`: Vis kun linjer som er unike for hver fil.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `comm`:

1. Sammenligne to filer og vise alle linjer:
   ```bash
   comm fil1.txt fil2.txt
   ```

2. Vise kun linjer som finnes i den første filen:
   ```bash
   comm -13 fil1.txt fil2.txt
   ```

3. Vise linjer som finnes i begge filer:
   ```bash
   comm -12 fil1.txt fil2.txt
   ```

4. Ignorere store og små bokstaver:
   ```bash
   comm -i fil1.txt fil2.txt
   ```

## Tips
- Sørg for at filene er sortert før du bruker `comm`, da kommandoen forutsetter at innholdet er sortert.
- Du kan bruke `sort`-kommandoen i kombinasjon med `comm` for å sortere filene automatisk:
  ```bash
  comm <(sort fil1.txt) <(sort fil2.txt)
  ```
- Bruk `-u` for å raskt finne unike linjer i hver fil, noe som kan være nyttig for dataanalyse.