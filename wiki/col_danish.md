# [Linux] Bash col brug: Rydder op i tekstformater

## Oversigt
`col` er et Bash-kommando, der bruges til at filtrere og rydde tekst, der indeholder formateringskontroltegn. Det er nyttigt til at vise tekst korrekt på terminalen ved at fjerne eller ignorere kontroltegn, der kan forstyrre visningen.

## Brug
Den grundlæggende syntaks for `col` er:

```bash
col [muligheder] [argumenter]
```

## Almindelige muligheder
- `-b`: Ignorerer backspace-tegn.
- `-x`: Behandler indrykning som tabulatorer.
- `-f`: Konverterer formateringskontroltegn til deres visuelle repræsentation.

## Almindelige eksempler

1. **Filtrering af en tekstfil**:
   For at rydde op i en tekstfil og fjerne kontroltegn, kan du bruge følgende kommando:
   ```bash
   col < filnavn.txt
   ```

2. **Brug af -b mulighed**:
   Hvis du vil ignorere backspace-tegn i en fil, kan du køre:
   ```bash
   col -b < filnavn.txt
   ```

3. **Visning af output fra en anden kommando**:
   Du kan også bruge `col` til at filtrere output fra en anden kommando. For eksempel:
   ```bash
   man ls | col -b
   ```

4. **Konvertering af kontroltegn**:
   For at konvertere kontroltegn til deres visuelle repræsentation, kan du bruge:
   ```bash
   col -f < filnavn.txt
   ```

## Tips
- Brug `col` i kombination med `man` for at få en mere læsbar visning af manualer.
- Eksperimenter med forskellige muligheder for at se, hvordan de påvirker output.
- Husk at `col` kun ændrer den måde, teksten vises på, og ikke ændrer den originale fil.