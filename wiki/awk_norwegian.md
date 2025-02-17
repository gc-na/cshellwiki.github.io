# [Linux] Bash awk Bruk: Behandle tekst og data

## Oversikt
`awk` er et kraftig tekstbehandlingsverktøy i Bash som brukes til å analysere og manipulere data i tekstfiler. Det er spesielt nyttig for å hente ut spesifikke felt fra strukturerte data, som CSV-filer eller loggfiler.

## Bruk
Grunnleggende syntaks for `awk` er som følger:

```bash
awk [alternativer] 'mønster { handling }' filnavn
```

## Vanlige alternativer
- `-F`: Angir feltseparator (f.eks. `-F,` for komma).
- `-v`: Setter en variabel før kjøring av skriptet.
- `-f`: Leser `awk`-programmet fra en fil.
- `-e`: Angir et `awk`-program som en kommandolinjeparameter.

## Vanlige eksempler

### Eksempel 1: Skrive ut spesifikke felt
For å skrive ut det første og tredje feltet fra en fil med tab-separerte verdier:

```bash
awk -F'\t' '{print $1, $3}' fil.txt
```

### Eksempel 2: Filtrere linjer
For å filtrere linjer som inneholder ordet "feil":

```bash
awk '/feil/' logg.txt
```

### Eksempel 3: Beregne summen av et felt
For å summere verdiene i det andre feltet:

```bash
awk '{sum += $2} END {print sum}' tall.txt
```

### Eksempel 4: Bruke variabler
For å bruke en variabel til å angi feltseparator:

```bash
awk -v FS="," '{print $1, $2}' fil.csv
```

## Tips
- Bruk `-F` for å spesifisere feltseparatoren når du arbeider med CSV eller andre strukturerte filer.
- Kombiner `awk` med andre kommandoer ved hjelp av pipe (`|`) for mer avanserte databehandlingsoppgaver.
- Husk at `awk` er case-sensitive, så vær oppmerksom på store og små bokstaver når du filtrerer data.