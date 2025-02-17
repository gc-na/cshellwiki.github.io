# [Linux] Bash-kommando `grep`: Søk i tekst

## Oversikt
`grep` er en kraftig kommando i Bash som brukes til å søke etter spesifikke mønstre i tekstfiler. Den kan filtrere ut linjer som inneholder et bestemt mønster, noe som gjør den svært nyttig for tekstbehandling og analyse.

## Bruk
Den grunnleggende syntaksen for `grep` er som følger:

```bash
grep [alternativer] mønster [filnavn]
```

## Vanlige alternativer
- `-i`: Ignorerer store og små bokstaver i søket.
- `-v`: Viser linjer som ikke matcher mønsteret.
- `-r`: Søker rekursivt gjennom kataloger.
- `-n`: Viser linjenummeret til hver match.
- `-l`: Viser bare filnavnene som inneholder en match.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `grep` kan brukes:

1. Søke etter et ord i en fil:
   ```bash
   grep "ord" fil.txt
   ```

2. Søke etter et ord uten å ta hensyn til store og små bokstaver:
   ```bash
   grep -i "ord" fil.txt
   ```

3. Vise linjenumrene til hver match:
   ```bash
   grep -n "ord" fil.txt
   ```

4. Søke rekursivt i alle filer i en katalog:
   ```bash
   grep -r "ord" /sti/til/katalog
   ```

5. Vise alle linjer som ikke inneholder et bestemt ord:
   ```bash
   grep -v "ord" fil.txt
   ```

## Tips
- Bruk `grep` sammen med andre kommandoer ved å bruke pipe (`|`) for å filtrere ut resultater. For eksempel:
  ```bash
  dmesg | grep "feil"
  ```
- Lagre ofte brukte søk i en alias for raskere tilgang. For eksempel:
  ```bash
  alias søkord='grep -i "ord" fil.txt'
  ```
- Kombiner `grep` med `find` for å søke i spesifikke filtyper:
  ```bash
  find . -name "*.txt" | xargs grep "ord"
  ```