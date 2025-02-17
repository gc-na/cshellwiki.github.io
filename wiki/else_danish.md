# [Linux] Bash else brug: Kontrol af betingelser i scripts

## Oversigt
`else`-kommandoen i Bash bruges til at angive en alternativ handling, der skal udføres, hvis en betingelse i en `if`-sætning ikke er opfyldt. Det er en vigtig del af kontrolstrukturen i Bash-scripts, der gør det muligt at styre flowet af programmet.

## Brug
Den grundlæggende syntaks for `else`-kommandoen er som følger:

```bash
if [ betingelse ]; then
    # handling hvis betingelsen er sand
else
    # handling hvis betingelsen er falsk
fi
```

## Almindelige muligheder
`else`-kommandoen har ikke specifikke muligheder, men den bruges sammen med `if` og `elif` for at skabe komplekse betingede strukturer.

## Almindelige eksempler

### Eksempel 1: Enkel if-else
```bash
#!/bin/bash
if [ -f "fil.txt" ]; then
    echo "Filen findes."
else
    echo "Filen findes ikke."
fi
```

### Eksempel 2: Tjek for en brugerinput
```bash
#!/bin/bash
echo "Indtast et tal:"
read tal
if [ $tal -gt 10 ]; then
    echo "Tallet er større end 10."
else
    echo "Tallet er 10 eller mindre."
fi
```

### Eksempel 3: Brug af if-elif-else
```bash
#!/bin/bash
echo "Indtast en karakter:"
read karakter
if [ "$karakter" == "a" ]; then
    echo "Du indtastede a."
elif [ "$karakter" == "b" ]; then
    echo "Du indtastede b."
else
    echo "Du indtastede en anden karakter."
fi
```

## Tips
- Sørg for at bruge `fi` for at afslutte `if`-strukturen korrekt.
- Indsæt altid mellemrum omkring operatorerne i betingelserne for at undgå syntaksfejl.
- Brug `elif` for at tilføje flere betingelser, hvis det er nødvendigt, i stedet for at have flere `else`-blokke.