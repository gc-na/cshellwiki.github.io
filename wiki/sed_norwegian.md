# [Linux] Bash sed Bruk: Tekstbehandling og redigering

## Oversikt
`sed` (Stream Editor) er et kraftig verktøy for tekstbehandling i Unix-lignende operativsystemer. Det brukes til å utføre grunnleggende teksttransformasjoner på en strøm av tekstdata, som kan være fra filer eller standard input.

## Bruk
Den grunnleggende syntaksen for `sed` er som følger:

```bash
sed [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e`: Angir en kommando som skal utføres.
- `-i`: Endrer filen direkte (in-place).
- `-n`: Undertrykker automatisk utskrift av linjer, og lar deg spesifisere hvilke linjer som skal skrives ut.
- `s/pattern/replacement/`: Erstatter mønsteret med erstatningen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `sed` kan brukes:

### Erstatte tekst i en fil
For å erstatte "hund" med "katt" i en fil kalt `dyr.txt`:

```bash
sed -i 's/hund/katt/g' dyr.txt
```

### Skrive ut spesifikke linjer
For å skrive ut linje 2 til 4 fra en fil:

```bash
sed -n '2,4p' fil.txt
```

### Fjerne tomme linjer
For å fjerne alle tomme linjer fra en fil:

```bash
sed -i '/^$/d' fil.txt
```

### Erstatte tekst i en tekststrøm
For å erstatte "foo" med "bar" i en tekststreng:

```bash
echo "foo baz" | sed 's/foo/bar/'
```

## Tips
- Bruk `-n` sammen med `p` for å kontrollere hvilke linjer som skrives ut, noe som kan være nyttig for feilsøking.
- Husk å ta sikkerhetskopi av filer før du bruker `-i` for å unngå tap av data.
- Du kan kombinere flere `sed`-kommandoer ved å bruke `-e` flere ganger eller ved å bruke semikolon for å separere dem.