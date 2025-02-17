# [Linux] Bash gzip brug: Komprimering af filer

## Oversigt
`gzip` (GNU zip) er et komprimeringsværktøj, der bruges til at reducere størrelsen af filer ved at anvende en algoritme til datakomprimering. Det er især nyttigt til at spare plads på disk og til hurtigere overførsel af filer.

## Brug
Den grundlæggende syntaks for `gzip`-kommandoen er som følger:

```bash
gzip [muligheder] [argumenter]
```

## Almindelige muligheder
- `-d`, `--decompress`: Dekomprimerer en gzip-komprimeret fil.
- `-k`, `--keep`: Beholder den originale fil efter komprimering.
- `-v`, `--verbose`: Viser detaljeret information om komprimeringsprocessen.
- `-r`, `--recursive`: Komprimerer alle filer i en mappe og dens undermapper.
- `-f`, `--force`: Tvinger komprimering, selvom det overskriver eksisterende filer.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `gzip`:

1. **Komprimere en fil:**
   ```bash
   gzip fil.txt
   ```
   Dette vil komprimere `fil.txt` til `fil.txt.gz`.

2. **Dekomprimere en fil:**
   ```bash
   gzip -d fil.txt.gz
   ```
   Dette vil gendanne den komprimerede fil til dens oprindelige tilstand.

3. **Beholde den originale fil:**
   ```bash
   gzip -k fil.txt
   ```
   Dette vil komprimere `fil.txt` til `fil.txt.gz`, men beholde den originale `fil.txt`.

4. **Komprimere alle filer i en mappe:**
   ```bash
   gzip -r /sti/til/mappe/
   ```
   Dette vil komprimere alle filer i den angivne mappe og dens undermapper.

5. **Vis detaljer om komprimering:**
   ```bash
   gzip -v fil.txt
   ```
   Dette vil vise information om komprimeringsprocessen, herunder hvor meget plads der er blevet sparet.

## Tips
- Overvej at bruge `-k`-muligheden, hvis du vil bevare den originale fil, mens du arbejder med den komprimerede version.
- Brug `-v` for at få indsigt i komprimeringsprocessen, især når du arbejder med mange filer.
- Hvis du arbejder med store filer, kan det være nyttigt at komprimere dem i baggrunden ved at tilføje `&` til slutningen af din kommando.