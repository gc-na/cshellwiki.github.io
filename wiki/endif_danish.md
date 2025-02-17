# [Linux] Bash endif brug: Afslut betingede udsagn

## Oversigt
`endif` er en kommando, der bruges i Bash-scripts til at afslutte en betinget blok, der er startet med en `if`-kommando. Det hjælper med at strukturere scripts og sikre, at betingede udsagn er korrekt afsluttet.

## Brug
Den grundlæggende syntaks for `endif` er:

```bash
endif
```

## Almindelige muligheder
`endif` har ikke specifikke muligheder, da det blot er en afsluttende kommando. Det bruges i sammenhæng med `if`-kommandoen.

## Almindelige eksempler

### Eksempel 1: Simpel if-else struktur
```bash
if [ "$VAR" -eq 1 ]; then
    echo "Variablen er 1"
else
    echo "Variablen er ikke 1"
endif
```

### Eksempel 2: Tjekke filens eksistens
```bash
if [ -f "minfil.txt" ]; then
    echo "Fil findes"
else
    echo "Fil findes ikke"
endif
```

### Eksempel 3: Flere betingelser
```bash
if [ "$TAL" -gt 10 ]; then
    echo "Tallet er større end 10"
elif [ "$TAL" -eq 10 ]; then
    echo "Tallet er lig med 10"
else
    echo "Tallet er mindre end 10"
endif
```

## Tips
- Sørg for, at hver `if`-kommando har en tilsvarende `endif` for at undgå syntaksfejl.
- Brug indrykning i dine scripts for at gøre det lettere at læse og forstå betingede strukturer.
- Test dine scripts grundigt for at sikre, at betingelserne fungerer som forventet.