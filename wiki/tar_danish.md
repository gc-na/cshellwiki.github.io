# [Linux] Bash tar brug: Komprimere og arkivere filer

## Oversigt
`tar` (tape archive) er et kommandolinjeværktøj, der bruges til at samle flere filer og mapper til en enkelt fil, ofte for at komprimere dem og spare plads. Det er især nyttigt til sikkerhedskopiering og distribution af filer.

## Brug
Den grundlæggende syntaks for `tar`-kommandoen er:

```bash
tar [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c`: Opret en ny arkivfil.
- `-x`: Udpak en arkivfil.
- `-f`: Angiv navnet på arkivfilen.
- `-v`: Vis detaljer om de filer, der behandles (verbose).
- `-z`: Komprimer med gzip.
- `-j`: Komprimer med bzip2.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `tar`:

1. **Oprette et arkiv**:
   For at oprette et arkiv af en mappe kaldet `minmappe`:
   ```bash
   tar -cvf minmappe.tar minmappe
   ```

2. **Oprette et komprimeret arkiv**:
   For at oprette et gzip-komprimeret arkiv:
   ```bash
   tar -czvf minmappe.tar.gz minmappe
   ```

3. **Udpak et arkiv**:
   For at udpake et arkiv:
   ```bash
   tar -xvf minmappe.tar
   ```

4. **Udpak et komprimeret arkiv**:
   For at udpake et gzip-komprimeret arkiv:
   ```bash
   tar -xzvf minmappe.tar.gz
   ```

5. **Liste indholdet af et arkiv**:
   For at se indholdet af et arkiv uden at udpakke det:
   ```bash
   tar -tvf minmappe.tar
   ```

## Tips
- Brug `-v`-muligheden for at få feedback om, hvilke filer der bliver arkiveret eller udpakket.
- Overvej at bruge komprimering (`-z` eller `-j`) for at spare plads, især ved store arkiver.
- Sørg for at kontrollere filrettighederne, når du pakker og udpakkede filer, da de kan ændre sig.
- For sikkerhedskopiering, overvej at kombinere `tar` med `cron` for automatiserede opgaver.