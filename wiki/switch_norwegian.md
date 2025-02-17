# [Linux] Bash switch-bruk: Bytt mellom alternativer

## Oversikt
Bash-kommandoen `switch` brukes til å bytte mellom forskjellige alternativer i skript og programmering. Den lar deg evaluere en verdi og utføre forskjellige handlinger basert på den verdien.

## Bruk
Den grunnleggende syntaksen for `switch`-kommandoen er som følger:

```bash
switch [alternativer] [argumenter]
```

## Vanlige alternativer
- `-e`: Angir at uttrykket skal evalueres som en betingelse.
- `-d`: Setter standardverdi hvis ingen alternativer matcher.
- `-h`: Viser hjelp og tilgjengelige alternativer.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `switch` kan brukes:

### Eksempel 1: Enkel switch-setning
```bash
case $valg in
    1)
        echo "Valg 1 valgt"
        ;;
    2)
        echo "Valg 2 valgt"
        ;;
    *)
        echo "Ugyldig valg"
        ;;
esac
```

### Eksempel 2: Bruke switch med variabler
```bash
status="aktiv"
case $status in
    aktiv)
        echo "Systemet er aktivt"
        ;;
    inaktiv)
        echo "Systemet er inaktivt"
        ;;
    *)
        echo "Ukjent status"
        ;;
esac
```

### Eksempel 3: Kombinere flere alternativer
```bash
farge="rød"
case $farge in
    rød|blå)
        echo "Fargen er primær"
        ;;
    grønn)
        echo "Fargen er sekundær"
        ;;
    *)
        echo "Ukjent farge"
        ;;
esac
```

## Tips
- Sørg for å bruke `;;` for å avslutte hver case-blokk for å unngå uventet oppførsel.
- Bruk `*` som en fangstblokk for å håndtere alle uventede verdier.
- Test skriptet ditt grundig for å sikre at alle mulige alternativer er dekket.