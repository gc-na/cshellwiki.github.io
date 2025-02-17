# [Linux] Bash rmdir Bruk: Fjerner tomme kataloger

## Oversikt
`rmdir`-kommandoen brukes til å fjerne tomme kataloger i Linux. Den kan ikke brukes til å slette kataloger som inneholder filer eller andre kataloger.

## Bruk
Den grunnleggende syntaksen for `rmdir`-kommandoen er:

```bash
rmdir [alternativer] [argumenter]
```

## Vanlige alternativer
- `--ignore-fail-on-non-empty`: Ignorerer feilmeldinger hvis katalogen ikke er tom.
- `--verbose`: Viser detaljer om hva som skjer når kataloger blir fjernet.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `rmdir`:

1. **Fjerne en tom katalog:**
   ```bash
   rmdir min_katalog
   ```

2. **Fjerne flere tomme kataloger samtidig:**
   ```bash
   rmdir katalog1 katalog2 katalog3
   ```

3. **Bruke alternativet for å ignorere feil ved ikke-tomme kataloger:**
   ```bash
   rmdir --ignore-fail-on-non-empty min_katalog
   ```

4. **Vise detaljer om fjerning av katalog:**
   ```bash
   rmdir --verbose min_katalog
   ```

## Tips
- Sørg for at katalogen er tom før du prøver å fjerne den med `rmdir`.
- Bruk `ls`-kommandoen for å sjekke innholdet i katalogen før du sletter den.
- Vær forsiktig med å bruke `--ignore-fail-on-non-empty`, da det kan føre til at du glemmer å fjerne innholdet i katalogen først.