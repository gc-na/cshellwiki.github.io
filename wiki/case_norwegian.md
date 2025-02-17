# [Linux] Bash case-bruk: Behandle betingelser i skript

## Oversikt
`case`-kommandoen i Bash brukes til å evaluere en variabel mot flere mønstre. Dette gjør det enkelt å håndtere forskjellige betingelser i skript, og gir en mer lesbar og strukturert tilnærming enn flere `if`-setninger.

## Bruk
Den grunnleggende syntaksen for `case`-kommandoen er som følger:

```bash
case [variabel] in
    mønster1)
        # kommandoer for mønster1
        ;;
    mønster2)
        # kommandoer for mønster2
        ;;
    *)
        # kommandoer for alle andre tilfeller
        ;;
esac
```

## Vanlige alternativer
`case`-kommandoen har ikke mange alternativer, men her er noen nyttige mønstre:

- `*)`: Fanger opp alle andre tilfeller (wildcard).
- `|`: Brukes for å spesifisere flere mønstre for samme kommando.

## Vanlige eksempler

### Eksempel 1: Enkel bruk av case
```bash
read -p "Skriv inn en farge: " farge
case $farge in
    rød)
        echo "Du valgte rød."
        ;;
    blå)
        echo "Du valgte blå."
        ;;
    grønn)
        echo "Du valgte grønn."
        ;;
    *)
        echo "Ukjent farge."
        ;;
esac
```

### Eksempel 2: Bruke flere mønstre
```bash
read -p "Skriv inn en frukt: " frukt
case $frukt in
    eple|pære)
        echo "Du valgte en steinfrukt."
        ;;
    banan|kiwi)
        echo "Du valgte en tropisk frukt."
        ;;
    *)
        echo "Ukjent frukt."
        ;;
esac
```

### Eksempel 3: Bruke case med filtyper
```bash
fil="dokument.pdf"
case $fil in
    *.pdf)
        echo "Dette er en PDF-fil."
        ;;
    *.txt)
        echo "Dette er en tekstfil."
        ;;
    *.jpg|*.png)
        echo "Dette er et bilde."
        ;;
    *)
        echo "Ukjent filtype."
        ;;
esac
```

## Tips
- Bruk `case` når du har flere betingelser å sjekke; det gjør koden mer lesbar.
- Husk å avslutte hvert mønster med `;;` for å indikere slutten på kommandoene for det mønsteret.
- Vær oppmerksom på at `case` er sensitiv for store og små bokstaver, så vær konsekvent med skrivemåten.