# [Linux] Bash standard kommando: [udføre kommandoer]

## Oversigt
Bash er en kommandolinjetolk, der bruges til at udføre kommandoer på Unix-lignende operativsystemer. Den giver brugerne mulighed for at interagere med systemet ved at skrive kommandoer, der kan udføre forskellige opgaver som filhåndtering, systemadministration og meget mere.

## Brug
Den grundlæggende syntaks for at udføre en kommando i Bash er:

```bash
kommando [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h`, `--help`: Viser hjælp og information om kommandoen.
- `-v`, `--verbose`: Viser detaljerede oplysninger om, hvad der sker under udførelsen.
- `-q`, `--quiet`: Kører kommandoen uden at vise output (stille tilstand).

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger Bash-kommandoer:

1. **Liste filer i en mappe:**
   ```bash
   ls -l
   ```

2. **Kopiere en fil:**
   ```bash
   cp kilde.txt destination.txt
   ```

3. **Flytte en fil:**
   ```bash
   mv gammel.txt ny.txt
   ```

4. **Slette en fil:**
   ```bash
   rm fil.txt
   ```

5. **Søge efter en fil:**
   ```bash
   find /sti/til/mappe -name "filnavn.txt"
   ```

## Tips
- Brug `tab` for at autoudfylde filnavne og kommandoer, hvilket kan spare tid.
- Tjek altid med `--help` for at få en liste over tilgængelige muligheder for en given kommando.
- Vær forsigtig med `rm`-kommandoen, da den permanent sletter filer uden at sende dem til papirkurven.