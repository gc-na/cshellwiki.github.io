# [Linux] Bash grep bruk: Søker etter mønstre i tekst

## Oversikt
`grep` er et kraftig verktøy i Bash som brukes til å søke etter spesifikke mønstre i tekstfiler. Det står for "Global Regular Expression Print" og kan håndtere både enkle og komplekse søk ved hjelp av regulære uttrykk.

## Bruk
Den grunnleggende syntaksen for `grep` er som følger:

```bash
grep [alternativer] [mønster] [fil]
```

## Vanlige alternativer
- `-i`: Ignorerer store og små bokstaver i søket.
- `-r`: Søker rekursivt gjennom kataloger.
- `-v`: Viser linjer som ikke matcher mønsteret.
- `-n`: Viser linjenummeret sammen med resultatene.
- `-l`: Viser bare filnavnene som inneholder mønsteret.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `grep` kan brukes:

### Søke etter et enkelt ord i en fil
```bash
grep "ord" fil.txt
```

### Søke etter et ord uten å ta hensyn til store og små bokstaver
```bash
grep -i "ord" fil.txt
```

### Søke rekursivt i en katalog
```bash
grep -r "ord" /sti/til/katalog
```

### Vise linjenumre med resultatene
```bash
grep -n "ord" fil.txt
```

### Vise linjer som ikke inneholder et bestemt ord
```bash
grep -v "ord" fil.txt
```

## Tips
- Bruk `grep` sammen med andre kommandoer ved å bruke pipe (`|`) for å filtrere ut resultater. For eksempel: `dette er en test | grep "test"`.
- Kombiner `grep` med regulære uttrykk for mer avanserte søk.
- Lag aliaser for vanlige `grep`-kommandoer for å spare tid. For eksempel: `alias grepci='grep -i'` for å lage et alias for case-insensitive grep.