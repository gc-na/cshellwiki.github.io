# [Linux] Bash vgs brug: Viser volumengrupper

## Oversigt
`vgs` er et Bash-kommando, der bruges til at vise oplysninger om volumengrupper i Logical Volume Manager (LVM). Det giver en oversigt over de tilgængelige volumengrupper, deres størrelse, brug og status.

## Brug
Den grundlæggende syntaks for `vgs`-kommandoen er:

```bash
vgs [options] [arguments]
```

## Almindelige muligheder
- `-o, --units`: Angiv hvilke enheder der skal bruges til output.
- `-a, --all`: Vis også inaktive volumengrupper.
- `-h, --help`: Vis hjælp og afslut.
- `-v, --verbose`: Vis mere detaljerede oplysninger.

## Almindelige eksempler
1. **Vis alle volumengrupper**:
   ```bash
   vgs
   ```

2. **Vis detaljerede oplysninger om volumengrupper**:
   ```bash
   vgs -v
   ```

3. **Vis inaktive volumengrupper**:
   ```bash
   vgs -a
   ```

4. **Vis volumengrupper med specifikke enheder**:
   ```bash
   vgs -o +size,free
   ```

## Tips
- Brug `vgs` sammen med `lvdisplay` for at få en komplet oversigt over både volumengrupper og logiske volumener.
- Overvej at bruge `-h` for at få hjælp, hvis du er usikker på de tilgængelige muligheder.
- For at få en mere visuel repræsentation af din LVM-struktur, kan du kombinere `vgs` med `lsblk`.