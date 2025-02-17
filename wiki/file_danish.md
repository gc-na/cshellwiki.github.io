# [Linux] Bash filkommando brug: Identificer filtyper

## Oversigt
`file` kommandoen bruges til at bestemme typen af en fil. Den analyserer filens indhold og returnerer en beskrivelse af filens format, hvilket kan være nyttigt til at identificere ukendte filer.

## Brug
Den grundlæggende syntaks for `file` kommandoen er som følger:

```bash
file [muligheder] [argumenter]
```

## Almindelige muligheder
- `-b`: Vis kun filtypen uden filnavnet.
- `-i`: Vis MIME-type i stedet for den almindelige beskrivelse.
- `-f`: Læs filnavne fra en fil i stedet for kommandolinjen.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `file` kommandoen:

1. **Identificer en enkelt filtype:**
   ```bash
   file eksempel.txt
   ```

2. **Brug `-b` for kun at vise filtypen:**
   ```bash
   file -b eksempel.txt
   ```

3. **Vis MIME-type:**
   ```bash
   file -i eksempel.txt
   ```

4. **Identificer flere filer på én gang:**
   ```bash
   file fil1.txt fil2.jpg fil3.pdf
   ```

5. **Læs filnavne fra en fil:**
   ```bash
   file -f filnavne.txt
   ```

## Tips
- Brug `file` kommandoen som en del af dine scripts for automatisk at håndtere filer baseret på deres typer.
- Kombiner `file` med andre kommandoer som `grep` for at filtrere resultaterne.
- Husk at `file` analyserer indholdet af filen, så det kan give mere præcise resultater end blot at kigge på filendelsen.