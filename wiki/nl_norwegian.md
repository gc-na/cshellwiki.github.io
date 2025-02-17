# [Linux] Bash nl Bruk: Nummerer linjer i tekstfiler

## Oversikt
`nl`-kommandoen brukes til å nummerere linjer i tekstfiler. Den kan være nyttig for å gjøre dokumenter mer oversiktlige, spesielt når man arbeider med lange filer eller når man ønsker å referere til spesifikke linjer.

## Bruk
Den grunnleggende syntaksen for `nl`-kommandoen er:

```bash
nl [alternativer] [argumenter]
```

## Vanlige alternativer
- `-b`: Angir hvilken linje som skal nummereres (f.eks. `a` for alle linjer, `t` for bare ikke-tomme linjer).
- `-f`: Angir hvilken linje som skal nummereres på nytt etter en tom linje.
- `-n`: Angir formatet for nummereringen (f.eks. `ln` for linjenummer, `rn` for høyrejustert nummer).
- `-w`: Angir bredden på linjenummeret.
- `-s`: Angir et spesifikt skilletegn som skal brukes mellom linjenummeret og teksten.

## Vanlige eksempler

1. Nummerere alle linjer i en fil:
   ```bash
   nl fil.txt
   ```

2. Nummerere bare ikke-tomme linjer:
   ```bash
   nl -b t fil.txt
   ```

3. Bruke høyrejustert nummerering med en bredde på 5:
   ```bash
   nl -n rn -w 5 fil.txt
   ```

4. Spesifisere et skilletegn mellom linjenummer og tekst:
   ```bash
   nl -s ": " fil.txt
   ```

5. Nummerere linjer på nytt etter hver tom linje:
   ```bash
   nl -f 1 fil.txt
   ```

## Tips
- Bruk `nl` sammen med `cat` for å vise innholdet i en fil med linjenumre i terminalen.
- Kombiner `nl` med andre verktøy som `grep` for å filtrere linjer før nummerering.
- Husk at `nl` ikke endrer den opprinnelige filen; den viser bare nummererte linjer i terminalen. Hvis du vil lagre resultatet, kan du bruke omdirigering:
  ```bash
  nl fil.txt > nummerert_fil.txt
  ```