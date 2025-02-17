# [Linux] Bash rmdir brug: Slet tomme mapper

## Oversigt
`rmdir`-kommandoen bruges til at fjerne tomme mapper i Linux. Hvis mappen indeholder filer eller undermapper, vil kommandoen ikke kunne slette den.

## Brug
Den grundlæggende syntaks for `rmdir`-kommandoen er som følger:

```bash
rmdir [muligheder] [argumenter]
```

## Almindelige muligheder
- `-p`: Slet også forældremapper, hvis de er tomme.
- `--ignore-fail-on-non-empty`: Ignorer fejl, hvis mappen ikke er tom.
- `--verbose`: Vis en meddelelse for hver slettet mappe.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `rmdir`:

1. Slet en tom mappe:
   ```bash
   rmdir min_tomme_mappe
   ```

2. Slet flere tomme mapper på én gang:
   ```bash
   rmdir mappe1 mappe2 mappe3
   ```

3. Slet en tom mappe og dens tomme forældre:
   ```bash
   rmdir -p forælder_mappe/barn_mappe
   ```

4. Vis meddelelser, når mapper slettes:
   ```bash
   rmdir --verbose min_tomme_mappe
   ```

## Tips
- Sørg for, at mappen er tom, før du bruger `rmdir`, da den ellers vil fejle.
- Brug `-p`-muligheden, hvis du ønsker at rydde op i flere niveauer af tomme mapper på én gang.
- Overvej at bruge `rm -r` med forsigtighed, hvis du vil slette mapper, der ikke er tomme, da det kan fjerne indholdet uden advarsel.