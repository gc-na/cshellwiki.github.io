# [Linux] Bash test bruk: Sjekk betingelser

## Oversikt
`test`-kommandoen brukes i Bash for å evaluere betingelser og returnere en statuskode basert på resultatet. Den er nyttig for å sjekke om filer eksisterer, om variabler er satt, eller for å sammenligne verdier.

## Bruk
Grunnleggende syntaks for `test`-kommandoen er som følger:

```bash
test [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e fil`: Sjekker om filen eksisterer.
- `-d fil`: Sjekker om filen er en katalog.
- `-f fil`: Sjekker om filen er en vanlig fil.
- `-z streng`: Sjekker om strengen er tom.
- `-n streng`: Sjekker om strengen ikke er tom.
- `a -o b`: Sjekker om enten a eller b er sant (logisk OR).
- `a -a b`: Sjekker om både a og b er sanne (logisk AND).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `test` kan brukes:

### Sjekke om en fil eksisterer
```bash
if test -e fil.txt; then
    echo "Filen eksisterer."
else
    echo "Filen eksisterer ikke."
fi
```

### Sjekke om en variabel er tom
```bash
variabel=""
if test -z "$variabel"; then
    echo "Variabelen er tom."
else
    echo "Variabelen har en verdi."
fi
```

### Sjekke om en katalog eksisterer
```bash
if test -d /path/to/directory; then
    echo "Katalogen eksisterer."
else
    echo "Katalogen eksisterer ikke."
fi
```

### Sammenligne to tall
```bash
tall1=5
tall2=10
if test $tall1 -lt $tall2; then
    echo "$tall1 er mindre enn $tall2."
fi
```

## Tips
- Bruk `[` (eck bracket) som en alternativ syntaks for `test`, for eksempel: `[ -e fil.txt ]`.
- Husk at `test` returnerer en statuskode på 0 for sann og 1 for usann, noe som kan brukes i if-setninger.
- For mer lesbarhet, vurder å bruke `[[ ... ]]` i stedet for `test` for komplekse betingelser, da det gir mer fleksibilitet og bedre håndtering av strenger.