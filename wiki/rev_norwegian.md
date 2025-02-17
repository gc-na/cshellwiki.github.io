# [Linux] Bash rev: snu tekst

## Oversikt
`rev` er et Bash-kommando som brukes til å reversere rekkefølgen av tegn i hver linje av en fil eller fra standard input. Dette kan være nyttig for tekstmanipulering eller når du ønsker å se data i en annen rekkefølge.

## Bruk
Den grunnleggende syntaksen for `rev` er som følger:

```
rev [alternativer] [argumenter]
```

## Vanlige alternativer
- `-o, --output=FIL`: Angi en utdatafil for å skrive den reverserte teksten til en spesifisert fil.
- `-h, --help`: Vis hjelp og informasjon om bruken av kommandoen.

## Vanlige eksempler

Reversere innholdet i en fil:
```bash
rev fil.txt
```

Reversere tekst fra standard input:
```bash
echo "Hei Verden" | rev
```

Reversere innholdet i en fil og lagre det i en ny fil:
```bash
rev fil.txt -o reversert_fil.txt
```

Reversere flere linjer fra standard input:
```bash
cat fil.txt | rev
```

## Tips
- Bruk `rev` sammen med andre tekstbehandlingsverktøy som `grep` eller `awk` for mer avansert tekstmanipulering.
- Vær oppmerksom på at `rev` reverserer tegnene i hver linje, ikke hele filen. Hvis du ønsker å reversere rekkefølgen av linjer, kan du bruke `tac`-kommandoen i stedet.