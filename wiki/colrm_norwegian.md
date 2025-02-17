# [Linux] Bash colrm Bruk: Fjerne kolonner fra tekst

## Oversikt
`colrm` er et Bash-kommando som brukes til å fjerne spesifikke kolonner fra tekstlinjer. Dette kan være nyttig når du ønsker å formatere utdata eller fjerne unødvendige data fra tekstfiler.

## Bruk
Den grunnleggende syntaksen for `colrm` er som følger:

```bash
colrm [start] [slutt]
```

Her spesifiserer `start` den første kolonnen som skal fjernes, og `slutt` spesifiserer den siste kolonnen som skal fjernes.

## Vanlige alternativer
- `start`: Angir startkolonnen for fjerning (inkludert).
- `slutt`: Angir sluttkolonnen for fjerning (inkludert).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `colrm` kan brukes:

1. Fjerne de første 5 kolonnene fra en tekstfil:

   ```bash
   colrm 1 5 < fil.txt
   ```

2. Fjerne kolonne 3 til 7 fra standard input:

   ```bash
   echo -e "123456789\n987654321" | colrm 3 7
   ```

3. Fjerne de siste 3 kolonnene fra en fil:

   ```bash
   colrm 8 < fil.txt
   ```

## Tips
- Vær oppmerksom på at kolonnene telles fra 1, ikke 0.
- Du kan bruke `colrm` sammen med andre kommandoer ved å bruke pipe (`|`) for å bearbeide data i sanntid.
- Test alltid kommandoen med en kopi av filen for å unngå tap av data.