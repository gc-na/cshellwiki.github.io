# [Linux] Bash split bruk: Deler filer i mindre deler

## Oversikt
`split`-kommandoen brukes til å dele opp store filer i mindre deler. Dette kan være nyttig når du ønsker å håndtere store datamengder eller forberede filer for overføring.

## Bruk
Grunnleggende syntaks for `split`-kommandoen er som følger:

```bash
split [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l NUM`: Del filen etter et spesifisert antall linjer.
- `-b SIZE`: Del filen etter en spesifisert størrelse (f.eks. 1M for 1 megabyte).
- `-d`: Bruk numeriske suffikser i stedet for alfabetiske suffikser for de delte filene.
- `--additional-suffix=SUFFIX`: Legg til et ekstra suffiks til de delte filene.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `split`:

### Eksempel 1: Dele en fil etter linjer
For å dele en fil kalt `storfil.txt` i deler med 100 linjer hver:

```bash
split -l 100 storfil.txt
```

### Eksempel 2: Dele en fil etter størrelse
For å dele en fil kalt `storfil.txt` i deler på 1 megabyte hver:

```bash
split -b 1M storfil.txt
```

### Eksempel 3: Dele med numeriske suffikser
For å dele en fil og bruke numeriske suffikser:

```bash
split -d -l 50 storfil.txt del_
```

### Eksempel 4: Legge til ekstra suffiks
For å dele en fil og legge til et ekstra suffiks:

```bash
split --additional-suffix=.txt -l 10 storfil.txt del_
```

## Tips
- Bruk `-d` for å unngå forvirring med alfabetiske suffikser når du deler mange filer.
- Vær oppmerksom på at de delte filene får standardnavn som `xaa`, `xab`, osv. Du kan spesifisere et prefiks med `split` for å gjøre det lettere å identifisere filene.
- Sjekk størrelsen på de delte filene etter deling for å sikre at de er som forventet.