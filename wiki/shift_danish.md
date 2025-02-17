# [Linux] Bash shift brug: Flyt positionen af argumenter i en shell-script

## Oversigt
`shift`-kommandoen i Bash bruges til at flytte positionen af argumenter, der er givet til et script eller en funktion. Ved at anvende `shift` kan du fjerne det første argument og flytte de resterende argumenter en position til venstre, hvilket gør det lettere at håndtere argumenter i løkker.

## Brug
Den grundlæggende syntaks for `shift`-kommandoen er:

```bash
shift [n]
```

Her angiver `n` hvor mange positioner argumenterne skal flyttes. Hvis `n` ikke angives, flyttes argumenterne én position.

## Almindelige muligheder
- `n`: Angiver hvor mange positioner argumenterne skal flyttes. Hvis `n` er 1, fjernes det første argument, og de resterende flyttes til venstre.
  
## Almindelige eksempler

### Eksempel 1: Grundlæggende brug
```bash
#!/bin/bash
echo "Før shift: $1 $2 $3"
shift
echo "Efter shift: $1 $2 $3"
```
I dette eksempel vil det første argument blive fjernet, og de resterende argumenter vil blive flyttet til venstre.

### Eksempel 2: Flytte flere positioner
```bash
#!/bin/bash
echo "Før shift: $1 $2 $3 $4"
shift 2
echo "Efter shift: $1 $2 $3 $4"
```
Her vil de to første argumenter blive fjernet, og de resterende vil blive flyttet til venstre.

### Eksempel 3: Brug i en løkke
```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "Behandler argument: $1"
    shift
done
```
I dette eksempel vil scriptet behandle hvert argument én ad gangen, indtil der ikke er flere argumenter tilbage.

## Tips
- Brug `shift` i kombination med `$#` for at kontrollere antallet af argumenter, der er tilbage.
- Vær opmærksom på, at `shift` ændrer positionen af argumenterne, så sørg for at gemme værdier, hvis du har brug for dem senere.
- Det er en god praksis at kontrollere, om der er tilstrækkeligt med argumenter, før du anvender `shift`, for at undgå fejl.