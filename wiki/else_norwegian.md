# [Linux] Bash else bruken: Kontrollflyt i skripting

## Oversikt
`else`-kommandoen i Bash brukes i kontrollflyt for å spesifisere hva som skal skje hvis en betingelse ikke er oppfylt. Den brukes sammen med `if`-setningen for å håndtere alternative handlinger i skript.

## Bruk
Den grunnleggende syntaksen for `else`-kommandoen er som følger:

```bash
if [ betingelse ]; then
    # kommandoer hvis betingelsen er sann
else
    # kommandoer hvis betingelsen er usann
fi
```

## Vanlige alternativer
Det er ingen spesifikke alternativer for `else`, men det er viktig å bruke det sammen med `if` og `fi` for å danne en komplett kontrollstruktur.

## Vanlige eksempler

### Eksempel 1: Enkel if-else
```bash
if [ -f "fil.txt" ]; then
    echo "Fil finnes."
else
    echo "Fil finnes ikke."
fi
```

### Eksempel 2: Sjekke om en variabel er tom
```bash
variabel=""
if [ -z "$variabel" ]; then
    echo "Variabelen er tom."
else
    echo "Variabelen har en verdi."
fi
```

### Eksempel 3: Bruke if-else i et skript
```bash
#!/bin/bash

echo "Skriv inn et tall:"
read tall

if [ "$tall" -gt 10 ]; then
    echo "Tallet er større enn 10."
else
    echo "Tallet er 10 eller mindre."
fi
```

## Tips
- Sørg for å alltid avslutte `if`-setningen med `fi` for å unngå syntaksfeil.
- Bruk klare og beskrivende meldinger i `echo`-kommandoene for bedre lesbarhet.
- Test betingelsene grundig for å sikre at skriptet oppfører seg som forventet under ulike forhold.