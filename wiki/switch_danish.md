# [Linux] Bash switch brug: Skift mellem forskellige tilstande

## Oversigt
`switch`-kommandoen bruges til at skifte mellem forskellige tilstande eller værdier i et Bash-script. Det er en nyttig funktion, når du har brug for at håndtere flere betingelser og udføre forskellige handlinger baseret på disse betingelser.

## Brug
Den grundlæggende syntaks for `switch`-kommandoen er som følger:

```bash
switch [options] [arguments]
```

## Almindelige muligheder
- `-e`: Angiver, at der skal udføres en handling, hvis en betingelse er opfyldt.
- `-d`: Angiver en standardhandling, hvis ingen betingelser er opfyldt.
- `-c`: Bruges til at angive en bestemt tilstand eller værdi, der skal skiftes til.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `switch`-kommandoen kan bruges:

### Eksempel 1: Enkel tilstandsskift
```bash
case $value in
    "1")
        echo "Du valgte 1"
        ;;
    "2")
        echo "Du valgte 2"
        ;;
    *)
        echo "Ugyldigt valg"
        ;;
esac
```

### Eksempel 2: Brug af standardværdi
```bash
case $input in
    "ja")
        echo "Du svarede ja."
        ;;
    "nej")
        echo "Du svarede nej."
        ;;
    *)
        echo "Ugyldigt input, venligst prøv igen."
        ;;
esac
```

### Eksempel 3: Flere betingelser
```bash
case $day in
    "mandag" | "tirsdag" | "onsdag")
        echo "Det er en hverdag."
        ;;
    "lørdag" | "søndag")
        echo "Det er weekend."
        ;;
    *)
        echo "Ugyldig dag."
        ;;
esac
```

## Tips
- Brug `case`-strukturen i stedet for `if`-udsagn, når du har mange betingelser at kontrollere, da det kan gøre koden mere læsbar.
- Sørg for at afslutte hver betingelse med `;;` for at undgå fejl.
- Test altid dine scripts med forskellige input for at sikre, at alle betingelser håndteres korrekt.