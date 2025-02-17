# [Linux] Bash cd bruk: Naviger mellom kataloger

## Oversikt
`cd` (change directory) er en Bash-kommando som brukes til å navigere mellom kataloger i filsystemet. Ved å bruke `cd` kan brukeren endre den nåværende arbeidskatalogen til en annen katalog.

## Bruk
Den grunnleggende syntaksen for `cd`-kommandoen er:

```bash
cd [alternativer] [argumenter]
```

## Vanlige alternativer
- `-`: Gå tilbake til den forrige katalogen.
- `..`: Gå opp ett nivå i katalogstrukturen.
- `~`: Gå til hjemme-katalogen til brukeren.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `cd`-kommandoen kan brukes:

1. Gå til en spesifikk katalog:
   ```bash
   cd /path/to/directory
   ```

2. Gå opp ett nivå i katalogstrukturen:
   ```bash
   cd ..
   ```

3. Gå til hjemme-katalogen:
   ```bash
   cd ~
   ```

4. Gå tilbake til den forrige katalogen:
   ```bash
   cd -
   ```

5. Gå til en relativ sti:
   ```bash
   cd Documents/Projects
   ```

## Tips
- Bruk `cd -` for raskt å bytte mellom to kataloger.
- Du kan bruke tab-tasten for å autfullføre katalognavn, noe som sparer tid og reduserer feil.
- For å se den nåværende katalogen, kan du bruke `pwd`-kommandoen etter å ha navigert med `cd`.