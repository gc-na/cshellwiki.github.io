# [Linux] Bash true brug: Returnerer altid en successtatus

## Oversigt
`true` er en simpel Bash-kommando, der altid returnerer en successtatus (0). Den bruges ofte i scripts og kommandolinjer som en placeholder eller for at sikre, at en kommando altid lykkes.

## Brug
Den grundlæggende syntaks for `true` er:

```bash
true [options] [arguments]
```

## Almindelige muligheder
`true` har ikke mange muligheder, da dens primære funktion er at returnere en successtatus. Den accepterer dog følgende:

- **Ingen**: `true` kræver ikke nogen argumenter eller muligheder for at fungere.

## Almindelige eksempler

### Eksempel 1: Grundlæggende brug
Kør `true` for at returnere en successtatus.
```bash
true
```

### Eksempel 2: Brug i et script
`true` kan bruges i scripts til at sikre, at en sekvens af kommandoer fortsætter, selvom en tidligere kommando mislykkes.
```bash
#!/bin/bash
echo "Starter script..."
false || true
echo "Scriptet fortsætter."
```

### Eksempel 3: Brug i en while-løkke
`true` kan anvendes til at skabe en uendelig løkke.
```bash
while true; do
    echo "Dette vil køre for evigt, indtil det stoppes."
done
```

## Tips
- Brug `true` i scripts, hvor du har brug for en kommando, der altid lykkes.
- Det kan være nyttigt i kombination med `&&` og `||` operatorer til at styre flowet af kommandoer.
- Da `true` ikke tager nogen argumenter, er det en hurtig og effektiv måde at sikre, at en kommando altid returnerer succes.