# [Linux] Bash case brug: Behandler betingelser

## Oversigt
`case`-kommandoen i Bash bruges til at udføre betingede handlinger baseret på værdien af en variabel. Det er en effektiv måde at håndtere flere betingelser uden at skulle bruge flere `if`-sætninger.

## Brug
Den grundlæggende syntaks for `case`-kommandoen er som følger:

```bash
case [variabel] in
    mønster1)
        # handling for mønster1
        ;;
    mønster2)
        # handling for mønster2
        ;;
    *)
        # standard handling
        ;;
esac
```

## Almindelige muligheder
`case`-kommandoen har ikke mange indbyggede muligheder, men den arbejder med mønstre, som kan være:
- `*` - Matcher enhver værdi.
- `?` - Matcher et enkelt tegn.
- `[abc]` - Matcher et enkelt tegn fra de angivne tegn.

## Almindelige eksempler

### Eksempel 1: Grundlæggende brug
```bash
read -p "Indtast en farve: " farve
case $farve in
    rød)
        echo "Du valgte rød."
        ;;
    blå)
        echo "Du valgte blå."
        ;;
    grøn)
        echo "Du valgte grøn."
        ;;
    *)
        echo "Ugyldig farve."
        ;;
esac
```

### Eksempel 2: Brug af mønstre
```bash
read -p "Indtast et tal: " tal
case $tal in
    [1-9])
        echo "Du indtastede et enkelt ciffer."
        ;;
    1[0-9])
        echo "Du indtastede et to-cifret tal mellem 10 og 19."
        ;;
    *)
        echo "Ugyldigt tal."
        ;;
esac
```

### Eksempel 3: Flere mønstre
```bash
read -p "Indtast en dag: " dag
case $dag in
    mandag|tirsdag|onsdag|torsdag|fredag)
        echo "Det er en hverdag."
        ;;
    lørdag|søndag)
        echo "Det er weekend."
        ;;
    *)
        echo "Ugyldig dag."
        ;;
esac
```

## Tips
- Brug `case`-kommandoen, når du har mange betingelser at kontrollere; det gør koden mere læsbar.
- Husk at afslutte hver handling med `;;` for at indikere slutningen af det specifikke mønster.
- Vær opmærksom på, at `case`-kommandoen er skelnet mellem store og små bogstaver, medmindre du håndterer det specifikt.