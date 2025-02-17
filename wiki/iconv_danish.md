# [Linux] Bash iconv brug: Konverterer tekstfilers tegnsæt

## Oversigt
`iconv` er et kommandolinjeværktøj, der bruges til at konvertere tekstfiler fra et tegnsæt til et andet. Det er nyttigt, når du arbejder med filer, der bruger forskellige kodninger, og du ønsker at sikre, at teksten vises korrekt.

## Brug
Den grundlæggende syntaks for `iconv` er:

```bash
iconv [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f` : Angiver kildetegnsættet (f.eks. UTF-8).
- `-t` : Angiver målt tegnsæt (f.eks. ISO-8859-1).
- `-o` : Angiver outputfilen, hvor den konverterede tekst skal gemmes.
- `-c` : Ignorerer ugyldige tegn i inputfilen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `iconv`:

1. **Konvertere en fil fra UTF-8 til ISO-8859-1**:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. **Konvertere en fil og skrive output til standard output**:
   ```bash
   iconv -f UTF-8 -t UTF-16 input.txt
   ```

3. **Ignorer ugyldige tegn under konvertering**:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
   ```

4. **Konvertere en fil fra Windows-1252 til UTF-8**:
   ```bash
   iconv -f WINDOWS-1252 -t UTF-8 input.txt -o output.txt
   ```

## Tips
- Sørg for at kende det korrekte tegnsæt for både input- og outputfiler for at undgå datatab.
- Brug `iconv -l` for at få en liste over understøttede tegnsæt.
- Test konverteringen på en lille fil først for at sikre, at resultatet er som forventet.