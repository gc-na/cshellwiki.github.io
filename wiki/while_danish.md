# [Linux] Bash while brug: Gentag handlinger baseret på en betingelse

## Oversigt
`while`-kommandoen i Bash bruges til at udføre en blok af kommandoer gentagne gange, så længe en specificeret betingelse er sand. Det er nyttigt til at automatisere opgaver, der kræver gentagelse, indtil en bestemt tilstand er opnået.

## Brug
Den grundlæggende syntaks for `while`-kommandoen er som følger:

```bash
while [betingelse]; do
    # kommandoer
done
```

## Almindelige muligheder
`while`-kommandoen har ikke mange indbyggede muligheder, da den primært fungerer baseret på den betingelse, der gives. Betingelsen kan være en hvilken som helst kommando, der returnerer en exit-status.

## Almindelige eksempler

### Eksempel 1: Tælle fra 1 til 5
```bash
count=1
while [ $count -le 5 ]; do
    echo "Tæller: $count"
    ((count++))
done
```

### Eksempel 2: Læse linjer fra en fil
```bash
while IFS= read -r line; do
    echo "Linje: $line"
done < fil.txt
```

### Eksempel 3: Gentage indtil brugeren indtaster 'exit'
```bash
input=""
while [ "$input" != "exit" ]; do
    read -p "Indtast noget (eller 'exit' for at afslutte): " input
    echo "Du indtastede: $input"
done
```

## Tips
- Sørg for at have en betingelse, der vil blive falsk på et tidspunkt for at undgå uendelige løkker.
- Brug `break`-kommandoen til at afslutte løkken tidligt, hvis det er nødvendigt.
- Overvej at bruge `until`-kommandoen, hvis du ønsker at gentage, indtil en betingelse bliver sand.