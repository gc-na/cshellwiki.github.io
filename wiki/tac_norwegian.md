# [Linux] Bash tac Bruk: Vender innholdet i en fil

## Oversikt
`tac` er et Bash-kommando som brukes til å vise innholdet i en fil i omvendt rekkefølge, linje for linje. Det er en nyttig kommando når du ønsker å se de nyeste linjene først.

## Bruk
Den grunnleggende syntaksen for `tac` er som følger:

```bash
tac [alternativer] [argumenter]
```

## Vanlige alternativer
- `-b`, `--before`: Sett inn linjene i omvendt rekkefølge før linjeskift.
- `-r`, `--regex`: Behandle linjene som regulære uttrykk.
- `-s`, `--separator`: Angi en spesifikk separator for linjene.

## Vanlige eksempler

1. Vise innholdet i en fil i omvendt rekkefølge:
   ```bash
   tac filnavn.txt
   ```

2. Vise innholdet i en fil med en spesifikk separator:
   ```bash
   tac -s ',' filnavn.csv
   ```

3. Bruke `tac` sammen med `echo` for å vise flere linjer:
   ```bash
   echo -e "Linje 1\nLinje 2\nLinje 3" | tac
   ```

4. Vise innholdet i en fil og lagre det i en ny fil:
   ```bash
   tac filnavn.txt > omvendt_fil.txt
   ```

## Tips
- Bruk `tac` sammen med `grep` for å filtrere linjer før du viser dem i omvendt rekkefølge.
- Kombiner `tac` med `head` eller `tail` for å vise et spesifikt antall linjer fra bunnen av eller slutten av filen.
- Husk at `tac` kan håndtere store filer, men ytelsen kan variere avhengig av systemressursene.